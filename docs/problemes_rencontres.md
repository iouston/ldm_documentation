 # Problemes rencontrés et solutionnés

 ## Erreur à la création d'une commande depuis un devis
 * Lorsque je créé une commande depuis un devis, j'ai un message d'erreur qui me précise :
 > Erreur lors de l'ajout
> CODE_NOT_VALID_FOR_THIS_ELEMENT
> CODE_NOT_VALID_FOR_THIS_ELEMENT
* La création de la commande échoue
* Dans ce cas là, la solution consiste à cloner le devis pour le même client.
* Valider ce devis et signer le
* Passer ce devis en commande, normalement, ça va fonctionner
* Depuis les objets liés tout en bas de la commande, ajouter un élément en cliquant sur 'lier à...' et faire un lien avec le devis initial qui posait problème.
* Une fois ce lien établi, supprimer le devis qui a été cloné et de cette façon tout est bon. Bien joué !


## Les pièces jointes sont supprimées à la validation des devis, commandes, factures
* Sous dolibarr v9.0.4 et avec le module forceproject activé, les pièces jointes ajoutées au statut brouillon dans les devis, les commandes et les factures sont perdues lors de la validation de l'object
* Eldy, consulté par mail le 25/09/2019 indique que le bug sera résolu en V10 pas avant
* Une solution est toutefois trouvé en empêchant le module force project de renommer trop tôt la réféfence
* pour cela, dans /forceproject/core/triggers/interface_15_modProject_ForceProject.class.php, commentez les lignes $object->ref=$newref;
* respectivement, ligne 170, 239, 357

## Mails envoyés n'arrivent pas au destinataire, notamment vers mail-tester.com
* Dolibarr nous indique que les mails sont envoyés. La configuration dolibarr est correcte
* Depuis le webmail l'envoi du mail est correct
* Après de nombreux tests, il s'avère que c'est la signature mail en HTML qui empêche cet envoi.
* L'envoi doit être considéré comme spam et éliminé
* La solution est de conserver des signatures sans HTML
* Dans le cas de certains compte, la signature, y compris en HTML passe et le mail arrive à destination...

## Mails envoyés n'arrivent pas sur les adresses wanadoo
* Pour une raison inconnue, les adreses mails en @wanadoo.fr ne reçoivent pas toujours nos mails
* Voici le message et la procédure à envoyer à ces personnes
Bonjour,

__Je suis l'informaticien chez LDM Équipement.
Élodie me fait savoir que vous ne recevez aucun des mails que LDM vous envoie.
Nous avons déjà eu le cas par le passé avec des adresses se terminant par @wanadoo.fr alors même que notre serveur d'envoi est parfaitement configuré.
Élodie me dit que vous avez vérifié dans les spams et qu'il n'y a rien. Il faut savoir que chez les adresses orange/wanadoo, la majorité des spams sont retenus et visibles uniquement depuis le webmail.
Aussi, je vous invite à suivre chaque étape de cette procédure : https://assistancepro.orange.fr/mail/depuis_un_ordinateur/parametrer_et_configurer_votre_boite_mail/messagerie_mail_pro__creer_votre_liste_verte-298206
Au point n°6 "Ajouter un destinataire" de cette procédure, indiquer non pas une adresse mais un domaine, c'est à dire "@ldmequipement.fr" et "@vestiaireplus.fr" (qui est la petite soeur de LDM)
Ensuite, vous devriez recevoir nos mails sans aucun problème et à tous les coups.
Je reste à votre disposition pour tout complément d'information
Bien cordialement,__

## Upbutton dans le header
Le module upbutton ajoute dans le header des pages de dolibarr un menu déroulant assez pénible qui se déplie au survol.
Il est neutralisé en passant en commentaire 
> var $upbuttons_container = $('div.tabsAction').first();
> window.setTimeout(getButtonInBanner, 300); //delai for js button
dans upbuttons/js/upbuttons.js.php

## CSS Personnalisé depuis module personnalisateur de thème
*Code CSS ajouté directement dans l'onglet avancé du module personnalisateur de thème
<pre>input, input.flat, textarea, textarea.flat{background:#cbe4f2;}
div.login_block{max-width:240px;}
#blockvmenusearch .select2-container{margin-bottom:100px;}
#search_overlay #blockvmenusearch #select2-currentuserid-container{font-size:18px;padding-top:0px;}
.login_block{max-width:400px!important;right:10px!important;top:10px!important;}
input[type=checkbox] { -webkit-appearance: none; -moz-appearance: none; -ms-appearance: none; }
input[type=checkbox] { border-radius: 4px; height: 15px; width: 15px; background: #fff; border: 1px solid #ccc; }
input[type="checkbox"]:checked {border:1px solid green; background: #99cc99; margin:0px; position: relative; }
input[type="checkbox"]:checked:before { content: 'x'; display: block; color: black; font-size: 18px; position: absolute;top:-3px;left:2px; }</pre>

## Montant différent entre total liste dolibarr et pivot report
* Vérifier que le pivot report prend bien en considération le champ entity dans sa requete. Sinon c'est qu'il fait une requete globale

## Préparer un import de données dans la base de données 
* Les prix doivent être à 8 décimales
* Les points de séparation 2.50 deviennent 2,50 en csv mais il faut 2.50000000 dans la base de données
* Pensez à utiliser substitue pour modifier les virgules en points comme séparateur...

## Menu déroulant dropdown menu
* Lorsqu'on active le menu déroulant dropdown menu dans une entité, le menu des autres entités ne marche plus
* Solution → désactiver le fichier init_sql.sql et désactiver / réactiver le module dans chaque entité

## Update bdd pour remplacer une valeur par une autre dans la même table
* La requête suivante permet de remplacer une valeur par une autre dans la même table
* UPDATE llx_product AS A INNER JOIN llx_product AS P ON A.rowid = P.rowid SET A.pmp = P.cost_price WHERE A.entity=2 

## Lancement d'une tâche cron via travaux planifiés de dolibarr
* Commande à inscrire dans le cron du cpanel : /usr/local/bin/php /home/gestion/scripts/cron/cron_run_jobs.php 53ac6fc1b54ee3ceb15c0a9b846fdad9de20a606 iouston > /home/gestion/public_html/dolibarr_ldm/documents/cron_run_jobs.php.log 2>&1
* dans /home/gestion/scripts/cron/cron_run_jobs.php, modifier le chemin d'incluion de master.inc.php par ce chemin : require_once "/home/gestion/public_html/dolibarr_ldm/master.inc.php";