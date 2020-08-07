 # Problemes rencontrés et solutionnés

## Les pièces jointes sont supprimées à la validation des devis, commandes, factures
* Sous dolibarr v9.0.4 et avec le module forceproject activé, les pièces jointes ajoutées au statut brouillon dans les devis, les commandes et les factures sont perdues lors de la validation de l'object
* Eldy, consulté par mail le 25/09/2019 indique que le bug sera résolu en V10 pas avant
* Une solution est toutefois trouvé en empêchant le module force project de renommer trop tôt la réféfenceé
* pour cela, dans /forceproject/core/triggers/interface_15_modProject_ForceProject.class.php, commentez les lignes $object->ref=$newref;
* respectivement, ligne 170, 239, 357
