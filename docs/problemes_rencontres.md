 # Problemes rencontrés et solutionnés

## Les pièces jointes sont supprimées à la validation des devis, commandes, factures
* Sous dolibarr v9.0.4 et avec le module forceproject activé, les pièces jointes ajoutées au statut brouillon dans les devis, les commandes et les factures sont perdues lors de la validation de l'object
* Eldy, consulté par mail le 25/09/2019 indique que le bug sera résolu en V10 pas avant
* Une solution est toutefois trouvé en empêchant le module force project de renommer trop tôt la réféfenceé
* pour cela, dans /forceproject/core/triggers/interface_15_modProject_ForceProject.class.php, commentez les lignes $object->ref=$newref;
* respectivement, ligne 170, 239, 357

## Mails envoyés n'arrivent pas au destinataire, notamment vers mail-tester.com
* Dolibarr nous indique que les mails sont envoyés. LA configuration dolibarr est correcte
* Depuis le webmail l'envoi du mail est correct
* Après de nombreux tests, il s'avère que c'est la signature mail en HTML qui empêche cet envoi.
* L'envoi doit être considéré comme spam et éliminé
* La solution est de conserver des signatures sans HTML
* Dans le cas de certains compte, la signature, y compris en HTML passe et le mail arrive à destination...

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