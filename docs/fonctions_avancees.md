# Fonctions avancées
 
## Personnaliser les mails préenregistrés pour l'envoi de devis, des commandes et de factures
* Si vos droits utilisateurs vous le permettent
* Aller dans accueil > configuration > Emails > Modèles des courriels
* Editer un modèle déjà existant ou ajouter un nouveau modèle.
* Des variables de substituions sont disponibles en cliquant sur l'icone "?" située à côté du sujet du mail

## Exporter des listes vers Excel
* Si vous en avez la permission
* Une icone verte "csv" s'affiche à droite du titre de chaque liste dans dolibarr
* Une fois votre liste filtrée, il vous suffit de cliqur sur cette icone pour réaliser un export au format csv
* Ce fichier au format csv s'ouvre simplement sous excel et vous permet de travailler les informations correspondantes

## Lier des produits associés à un produit (fonction désactivée pour le moment)
* Si vos droits utilisateurs vous le permettent, vous pouvez ajouter des produits associés à un produit du catalogue.
* Pour cela, rendez-vous sur la fiche d'un produit.
* De là, aller dans l'onglet "Produits associés"
* Rechercher un produit du catalogue et indiquer une quantité et si le produit est requis.
* Vous pouvez ajouter autant de produits associés que nécessaire
![lier produit](_media/lier_produits.jpg)

## Obtenir le prix moyen d'un produit par devis
* Afin d'analyser nos pratiques commerciales et de donner des indicateurs aux agents en charge des devis, il est possible de tracer le prix moyen d'un ou plusieurs produits par devis.
* Par exemple, sur l'écran d'édition des devis la table "Prix moyen par catégorie" vous indique le prix moyen des produits concernés.
* Par défaut, seul le prix moyen des cabines est tracé.
* Il est cependant possible de tracer n'importe quel produit ou groupe de produit.
* Pour cela, il suffit de vous rendre dans une catégorie de produit et de cocher la case : décomptez sur l'écran des devis
* A partir de ce moment, l'intitulé de la catégorie concerné apparait dans la table "Prix moyen par catégorie" et tous les produits qui sont présents dans cette catégorie sont décomptés si ils sont ajoutés au devis en cours.
* Pour pouvoir ajouter des produits dans une ou plusieurs catégorie, vous devez avoir les droits correspondants.
![commercial_ajouter_dpt](_media/categorie_prix_moyen.jpg)
![commercial_ajouter_dpt](_media/prix_moyen_produit.jpg)

## Formater les numéros de téléphone en base
* Fonction réservée aux administrateurs
* Cette fonction permet de formater les numéros de téléphone ne bas en nettoyant les espaces, les caractères spéciaux et autres tirets, de façon à ce que tous les numéros soient semmblables
* Pour cela, aller dans accueil/configuration/Formatage des numéros de téléphone

## Archiver des devis
* Fonction réservée aux administrateurs
* L'archivage des devis permet de supprimer toutes les pièces jointes des devis pendant un laps de temps donné
* Cela permet de soulager le serveur au niveau du stockage
* Les devis ne sont cependant pas supprimés de la base de données. il sera donc possible de régénrer un fichier pdf du devis. Par contre les pièces jointes : plans, messages et autres sont supprimés.






