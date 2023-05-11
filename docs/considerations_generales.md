 # Considérations générales

## Informations générales

* Dans deoriom, **seuls les champs en gras sont obligatoires** à remplir
* Les liens textes renvoient vers l'élément concerné
* Un clic sur une icone (par exemple, sur une icone pdf), affiche le fichier concerné.
* Dolibarr est accessible à partir de n'importe quelle connexion internet et smartphone
* Votre mot de passe est personnel, ne communiquez pas votre accès à d'autres personnes.
* Il est possible si besoin de vous donner plusieurs accès à dolibarr (pour vos collaborateurs par exemple).

## Procédure générale à l'ajout d'un dossier, d'une affaire
* Lorsqu’une nouvelle demande de prix arrive, la procédure suivante doit s’appliquer :
* Rechercher via le module de recherche en haut à gauche si le client existe dans la base
* Si le client n’existe pas : Créer une fiche client et les contacts associés
* Si le client existe, vérifier la fiche (adresse, code postal, tel, mail, etc…) et vérifier que le contact de l’affaire existe, sinon, le créer
* Créer un projet. Le projet est la pochette virtuelle dans laquelle nous allons glisser tous les éléments relatifs à cette affaire. Chaque projet correspond à une affaire à traiter avec ce client.
* Créer un devis (ou plus selon le cas)
* Créer une commande client (ou plus si besoin)
* Fabriquer et créer une commande fournisseur
* Créer une facture (ou plus si besoin)
* Encaisser le règlement

## Trucs et astuces
* En cliquant sur un lien en cliquant avec la molette de la souris (clic molette), le navigateur ouvre le lien dans un nouvel onglet. C'est vraiement pratique pour garder par exemple une liste d'un côté et avoir le détail d'une information à côté.
* Sur de grandes listes où vous avez une barre de défilement horizontal, vous pouvez maintenir la touche schift (majuscule) et utiliser votre molette de souris. La combinaison des deux, fait défiler la page à l'horizontal. Pour les utilisateurs de mac, remplacer la touche maj par la touche cmd.

## Utilisation des filtres dans dolibarr
* Sur des listes affichées par dolibarr vous pouvez utiliser plusieurs filtres. L'utilisation de plusieurs filtres est compris par le logiciel comme ET.
**Par exemple**, si sur la liste des tiers je mets un filtre '54000' dans code postal et 'Damien Hailant' dans commercial, le logiciel ne me sortira que la liste des tiers du 54000 ET dont Damien est le commercial

## Filtre commence par / fini par
* Je peux utiliser le caractère de remplacement ^ pour indiquer que je cherche ce qui commence par ou ce qui termine par
* Si depuis la liste des tiers j'indique ^54 dans le filtre du code postal, le logiciel va m'afficher tous les tiers qui ont un code postal qui commence par 54.
* A l'inverse, si j'indique 54^, le logiciel va me retourner tout ce qui termine par 54
* Si j'indique ^5400^ il me retournera exactement ce qui correspond à 5400

