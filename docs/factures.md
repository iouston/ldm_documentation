 # Factures & Comtpabilité

 # Facturation

## Créer une facture
* Dolibarr vous permet d'établir des factures aux clients que vous avez préalablement saisis 
* Vous pouvez créer une facture directement à partir d'une fiche client, depuis une proposition commerciale classée acceptée, ou à partir d'une commande clôturée à l'état "accepté

## Types de factures

<!-- tabs:start -->

#### ** factures de "doit" **

Il s'agit d'une facture standard. Il n'y a aucun prérequis

#### ** factures de remplacement  **

Une facture de remplacement permet de refaire une facture sur laquelle il y aurait des erreurs et sur laquelle rien n'aurait été fait (aucun paiement saisi). On ne peut créer qu'une seule facture de remplacement pour une facture de "doit" donnée. Quand on créé une facture de remplacement R, on choisit la facture de doit F qui doit être remplacée. Il n'est alors plus possible de faire d'actions sur la facture F, bien que cette dernière ne change pas de statut après que la facture de remplacement R ait été créée au statut brouillon. Si la facture de remplacement R est supprimée, la facture F reprends son état initial et le cycle de vie de la facture F peut reprendre. Si la facture de remplacement R est validée, la facture F passe alors au statut abandonnée automatiquement. Le cycle de vie continue sur la facture R.

#### ** Factures d'avoir **

On crée une facture d'avoir sur une facture de "doit". On peut créer plusieurs factures d'avoir sur une facture donnée. La facture d'avoir est transformée en réduction qui sert à réduire le paiement de n'importe quelle autre facture en attente de paiement
L'avoir va servir à annuler une facture.

-------------
**Exemple, double facturation**
* Nous avons facturé par erreur 2 fois le client pour la même prestation
* Le client nous a payé la facture 1
* On ne peut pas supprimer la facture 2 qui n'a pas lieu d'être
* Pour régulariser, on va alors créer une facture d'avoir en partant de la facture 2
* Sur cet avoir, il faut cliquer sur le bouton 'Marquer comme crédit disponible'
* L'avoir devient alors un crédit affecté au client et qui peut permettre de régler une autre facture
* On retourne sur la facture 2
* On utilise la remise disponible du client.
* L'avoir est alors utilisé pour régler la facture 2 qui se retrouve avec un montant à 0
* Il faut cliquer sur le bouton 'classer payée' de la facture 2 pour terminer
* Au final, l'avoir est bien venu "annuler" la facture n°2 et tout est bien qui fini bien
-------------

#### ** Factures d'acomptes **

Vous pouvez créer autant de facture d'acompte que désiré. Une facture d'acompte sera ensuite convertie en réduction (déjà payé) pour une autre facture (la facture définitive) sur laquelle porte l'acompte.

<!-- tabs:end -->

## Créer une facture avec Lettre de Change Relevé (LCR)
* Editer une facture classique (modèle homard)
* Choisissez le moyen de paiement LCR
* Générer votre pdf
* La facture ajoute une page située après les CGV qui contient la LCR et le coupon à renvoyer

## Créer une facture proforma
* Dans certain cas, notamment si le client est en BC1 au niveau des conditions d'expédition, il y a lieu d'encaisser un règlement avant expédition de la marchandise
* Dans ce cas, il faut éditer une facture proforma au client afin de lui fournir les informations nécessaires au paiement sans qu'il s'agisse d'une facture définitive (dite facture de doit)
* La proforma est une facture qui correspondra à la facture finale sans pour autant être la facture finale. Il est donc nécessaire que le process soit suffisamment avancé pour connaitre le montant total de la commande, sans pour autant être une facture
* Pour éditer la facture proforma, allez dans la commande client
* Choisissez le modèle de facture proforma dans les formats de documents
* Générer un fichier pdf

## Encaisser le règlement
* Une fois la facture éditée, dolibarr permet de réaliser et suivre l'encaissement
* Les paiements ne peuvent s'effectuer que sur des factures validées.
* Si un avoir est disponible, il pourra être imputé sur une facture d'un montant total inférieur à celui de l'avoir.
* Après la saisie du paiement, il est possible de régénérer le PDF de la facture pour y faire apparaître le règlement effectué et le solde à payer.

## Clore une facture
* Une facture validée peut être définitivement classée à l'état :
	- Payé (Si la somme des paiements est supérieure ou égale au montant réclamé).
	- Payé partiellement (Si la somme des paiements est supérieure à 0 mais strictement inférieure au montant réclamé).
	- Abandonné (Si aucun paiement n'a eu lieu).

> [!WARNINGS]
> Attention, ce n'est pas parce qu'une facture est close que les éléments liés (devis, commande) sont signalés en "Facturé". Cette approche permet notamment d'exercer un contrôle manuel et humain des différents éléments

## Facture de situation

* La création de factures de situation nécessite d’utiliser une méthodologie particulière pour l’édition desdites factures
* Pour éditer la première facture de situation
* A partir d’un devis ou d’une commande client acceptée, cliquer sur « Créer une facture ou un avoir »
* Choisissez alors « Première facture de situation » et cochez la case correspondante si une retenue de garantie est appliquée
* Indiquez une progression globale, commune à toutes les lignes, ou en éditant les lignes concernées, la situation de chaque élément
* Valider la facture et réalisez son suivi comme pour n’importe quelle autre facture
* Pour éditer la seconde facture de situation et/ ou les suivantes
* Positionnez-vous sur la dernière facture de situation (la première dans notre cas)
* Cliquez sur le bouton « Créer prochaine situation »
* Le curseur se positionne sur « Facture suivant situation » en indiquant le numéro de la dernière facture de situation
* Indiquez le taux de progression de la facture comme précédemment. Attention toutefois, le taux de progression correspond au taux global du projet. Si vous avez facturé une progression de 20% lors de la première situation et que cette facture correspond à 30% supplémentaire de progression, le taux de progression à inscrire à l’échelle de tout le travail à réaliser est bien de 50%
* Éditez une progression globale ou une progression par ligne comme précédemment
* Validez votre facture comme n’importe quelle autre facture
* Vous pouvez ajouter autant de facture de situation que bon vous semble jusqu’à arriver à une progression de 100% sur l’ensemble de chaque élément.
* **A noter que :
	- Vous ne pouvez pas éditer la facture de situation suivante si une facture précédente est toujours en brouillon
	- Même si vous indiquez la progression globale du travail dans dolibarr, c’est le montant correspondant au travail effectivement réalisé pour cette situation qui sera facturé sur le document pdf**

## Attribuer une remise fixe, un avoir a un client
* Depuis l'onglet client de la fiche du Tiers, cliquer sur "remise fixe"
* Ajouter un ou plusieurs avoir et le montant en précisant le motif de cette attribution
* Valider en cliquant sur 'créer remise fixe'
* Tous les utilisateurs de dolibarr auront alors l'information que ce client dispose d'une remise fixe

## Déduire une remise fixe, un avoir sur une facture client
* Au moment de la facturation, le ou les avoir disponibles pour le client apparaissent dans une liste déroulante.
* Il est possible de sélectionner une ou plusieurs remise et de les ajouter à la facture.
* Les remises ajoutées passent alors en déduction sur la facture et le montant de remise accordée au client a été mis à jour dans la fiche du client.

## Déduire un ou plusieurs acomptes d'une facture de solde
* Si le client a réglé une facture d'acompte, il faut transformer cet acompte en "réduction future" depuis le bouton correspondant sur la facture
* L'accompte est donc devenu une remise
* Au moment de la facture de solde, il suffira, de venir ajouter les remises issues des acomptes, qui apparaissent sous forme de menu déroulant en haut de l'écran du client

## Réaliser le contrôle de facturation
* Sur chaque facture, un champ "controle de facturation" est présent. 
* Il permet d'indiquer si le contrôle de facturation a été réalisé.
* A la création de la facture, passez ce champ sur le choix "Non controlée"
* Ce champ est disponible dans les listes de facture pour visualiser rapidement les factures à contrôler
* Une fois le contrôle réalisé sur la facture, passer ce champ sur la position "contrôllée" 

## Toujours envoyer une facture client par courrier
* Certains clients souhaitent recevoir systématiquement une facture par courrier
* Il est possible depuis la fiche du tiers de paramétrer le champ 'facture client' sur Oui
* Dans ce cas, lors de l'envoi de la facture par email, un message d'alerte sera affiché
* Un bouton 'classer envoyée par courrier' sera également disponible et permettra de consigner l'information dans dolibarr

## Vérifier l'encours du client
Voir [§client](clients)

## Vérifier l'état des différents encours
Voir [§client](clients)

# Comptabilité

## Compta dans dolibarr
* Dolibarr permet de faciliter le travail de comptabilité,de générer et d'éditer son grand livre et d'exporter les écritures dans des logiciels comptables
* Vérifier que la liaison entre les lignes de factures client existantes et le compte comptable est faite. Compléter les liaisons manquantes. Pour cela, vous pouvez utiliser l'entrée de menu Compta/Tréso-Comptabilité-Liaison factures client.
* Vérifier que la liaison entre les lignes de factures fournisseurs existantes et le compte comptable est faite. Compléter les liaisons manquantes. Pour cela, vous pouvez utiliser l'entrée de menu Compta/Tréso-Comptabilité-Liaison factures fournisseur.
* Vérifiez que la liaison entre le type de notes de frais et le compte comptable est faite. Compléter les liaisons manquantes. Vous pouvez définir les comptes comptables à utiliser pour chaque type de ligne de note de frais sur la page Compta/Tréso-Comptabilité-Liaison notes de frais.
*Ecrire les transactions dans le Grand Livre. Pour cela, aller sur chaque Journal, et cliquer sur le bouton "Enregistrer les opérations dans le Grand Livre".
*Ajouter ou modifier les opérations existantes et générer des rapports et des exportations.

