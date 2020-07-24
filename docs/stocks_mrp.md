 # Stocks - MRP

Le MRP permet de gérer les approvisionnements auprès des fournisseurs, notamment auprès des fournisseurs de panneaux
Par exemple :
- en S29 à la fin de la semaine, le stock LDM d'un produit est à 9.
- On fait un inventaire le vendredi de la S29. Les mecs de l'atelier comptent 2 panneaux de moins.
- On applique une correction  en suppression de 2 panneaux en S29.
- On doit donc avoir après cette correction et en fin de semaine 29 un stock LDM de 7 panneaux.
- en S30, en début de semaine, le stock est donc de 7 panneaux.
- On retire dans cette semaine, une consommation de 10 panneaux. Et on a un mouvement de Stock Chambéry à LDM de +13 panneaux
- Le stock fin de semaine de S30 est donc de 7-10+13=10
- On fait un inventaire en fin de semaine. Le stock est juste, on fait pas de correction
- en S31, le stock début de semaine est donc de 10

## Fabrication des panneaux ABET
* On enregistre une commande fournisseur auprès d'ABET
* Lorsque la commande fournisseur est réceptionnée, on ventile la réception des produits sur l'entrepot correspondant
* Dans le cas d'ABET, on ventilera donc les produits réceptionnés sur le stock BRA


> [!TIP]
> Pour ABET, on considère que nous disposons de 3 entrepots : Bra, Chambery et LDM

## Transfert de stock en masse ABET
* Une fois les produits stockés à BRA, on fait déplacer des produits à Chambéry et de Chambéry à LDM
* Cela va se gérer dans dolibarr via le transfert de stocks en masse
* Le transfert de stock en masse est accessible, selon les droits depuis : produits/services > Entrepôts > Transfert stock en masse
* Sur cet écran, ajouter les articles désirés, en précisant l'entrepôt source et l'entrepôt de destination et la quantité
* Une fois tous les produits du transfert sélectionné, indiquer un libéllé au mouvement, par exemple, en indiquant le BL correspondant
* Enregsitrer le transfert

> [!TIP]
> Dans le cas d'ABET, on fera donc un transfert en masse de Bra vers Chambéry puis de Chambéry vers LDM

## Module MRP
* Le module MRP se base sur une catégorie de produits.
* Il y aura autant de tables MRP que de catégories dans la catégorie parente "Appros gérés > produits bruts"
* Cette catégorie de référence est elle même définie au niveau de la configurartion du module
* Chaque catégorie de MRP, comme "panneaux print" ou "panneaux polyrey" a un attribut supplémentaire qui permet de définir le délais d'approvisionnement du fournisseur 

## MRP ABET
* Le MRP Abet, accessible depuis produits / services > Tables MRP > Tables MRP Abet / Print est spécifique à ce fournisseur
* Le MRP ABET calcule le nombre de panneaux à commander auprès de ce fournisseur à partir des informations en stocks à Bra, Chambéry et LDM.
* Il afffiche en bas du tableau les quantité à passer en commande.
* Le fait de cliquer sur une quantité à commander, permet de préparer une commande fournisseur.

> [!TIP]
> A partir de la commande fournisseur générée par la table MRP, on fait la réception des produits fabriqué cf §Fabrication des panneaux ABET