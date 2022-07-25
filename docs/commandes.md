# Commandes et tranches
 
## Créer une commande client
* Lorsqu'un devis est validé et que vous l'avez cloturé au statut signé (cf. cloturer un devis(https://iouston.github.io/ldm_documentation/#/devis?id=cl%c3%b4turer-un-devis)
* Si vous avez les droits suffisants
* Cliquer sur le bouton "Créer commande"
* Saisissez les éléments concernant la commande et créer le brouillon

## Afficher des textes automatiques dans la note de commande
* En fonction de certains paramètres de la commande, le fichier pdf généré affichera certaines informartions ou non
* Par exemple, si vous indiquez pour 'type de commande' que la commande est en fourniture et pose ou en pose, une note relative à la pose sera automatiquement ajoutée.
* Si le type d'expédition est en enlèvement par le client, des précisions seront fournies au client
* Selon les conditions de réglement définies, les moyens de paiement s'affichent ou non
* Ces textes prédéfinies

## Ajouter un avenant dans une commande (marché)
* Dans le cadre de marché, il est nécessaire d'ajouter des avenants dans une commande
* Imaginons que nous avons une commande initiale et un avenant sous forme de devis
* Dans la commande initiale, décaler d'un niveau toutes les localisations (la prochaine version du module aura un bouton qui permettra de faire cela en un clic)
* Créer une localisation globale de niveau 1, qui englobe toute la commande et qu'on intitule 'Commande initiale'
* Aller dans votre devis d'avenant, et faites la même chose, c'est à dire, décaler toutes les localisations d'un niveau et englober le tout dans une localisation de niveau 1 que vous appellez 'Avenant XXYY'
* Le module sous total permet de copier tout un bloc vers un autre élément. Il est ainsi possible de copier un bloc d'un devis vers un devis, un bloc de commande vers une commande, etc...
* Transformer votre devis d'avenant en commande brouillon. 
* Désormais, vous pouvez donc copier votre bloc 'avenant XXYY' vers votre commande commande initiale
* Une fois cela fait, supprimer la commande provisoire de l'avenant
* Enfin, rendez-vous sur le devis d'avenant et lier le depuis la boite 'objet lié' avec la commande initiale afin de conserver la tracabilité
* C'est fin ! 


## Créer des tranches de commandes
* Depuis une commande, rendez-vous sur l'onglet 'Tranche'
* Là, dans la zone 'A trancher' se trouvent les produits et les services encore non affectés à une ou plusieurs tranches
* Sélectionner à droite, via les cases à cocher les items que vous souhaitez, et cliquer sur "Ajouter les produits sélectionnées à une nouvelle tranche".
* Astuce : vous pouvez également cliquer/déplacer des éléments d'une tranche à une autre

## Gérer les tranches de commandes
* Lorsque les tranches sont créées, elles apparaissent en dessous de la zone 'A trancher'
* Vous pouvez éditer rapidement différentes informations de la tranche comme : le numéro d'ordre de la tranche, la semaine prévisionnelle de fab, la charge de fabrication, le statut
* En dépliant la tranche, vous pouvez accéder encore à d'autres informations, en édition et ou en lecture selon vos droits.
* Un changement de statut de la tranche entraine un changement de couleur de fond de façon à vous donner des repères visuels.
* Selon le statut de la tranche vous disposez d'un certain nombre de boutons d'action (situés tout en bas de la zone de la tranche) et qui vous permettent de modifier le statut de la tranche.

> [!WARNING]
> ATTENTION, vous pouvez passer d'un statut de tranche à un autre, sans qu'il y ait de vérification particulière. Soyez-donc pdrudent !

## Répartir plusieurs mêmes produits dans des tranches de commandes
* Lorsque la quantité d'un produit est supérieure à 1, il est possible de répartir les quantités de ce produit 
* Pour cela, ajouter le produit dans une tranche
* Cliquer sur quantité et modifier la quantité. Par exemple, j'ai 10 cabines, et je sélectionne 4 dans le champ de quantité.
* Un produit cabine avec une quantité de 6 sera remise dans la zone 'A trancher'

## 	Modifier l'ordre des tranches de commande

## Modifier le temps de fabrication d'une tranche de commande
* Le temps de fabrication est calculé depuis le champ 'temps de fabrication' de chaque produit
* Il est possible (selon vos droits utilisateurs) de forcer la valeur du temps de fabrication
* Depuis la tranche concernée, cliquer sur le bouton de modification et indiquer la nouvelle valeur. Le temps de fabrication est modifié
* Un bouton (cycle) est également disponible pour demander la réactualisation du calcul du temps de fabrication, suite par exemple à l'ajout ou aux retraits de produits de la tranche. Attention, ce recalcul perd la valeur forcée que vous auriez indiqué précédemment.

## Faire un ajout/ une modification dans une commande qui a déjà des tranches
* Si la commande sur laquelle vous souhaitez intervenir est déjà en tranches
* Vous ne pouvez pas ajouter de produit / service directement au niveau des tranches
* Vous devez modifier la commande, et ajouter les éléments nécessaires
* Vous aurez alors ces éléments dans la partie "A trancher".
* Cette logique de fonctionnement permet d'être sûr que les produits seront bien facturés

## Demander une validation de la commande au client

## Gérer les consommations prévisionnelles d'une commande

## Importer les consommations en masse

## Gérer les commandes hors standard

## Modifier les couleurs et les valeurs de charge de fabrication des tranches
* Les tranches de commandes ont une charge de fabrication qui correspond à une couleur
* Les valeurs et les couleurs affectées se personnalisent depuis accueil > configuration > dictionnaires > Histogramme du planning
