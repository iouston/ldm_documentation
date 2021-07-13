# Comptabilité

## Compta dans dolibarr
* Dolibarr permet de faciliter le travail de comptabilité,de générer et d'éditer son grand livre et d'exporter les écritures dans des logiciels comptables
* Vérifier que la liaison entre les lignes de factures client existantes et le compte comptable est faite. Compléter les liaisons manquantes. Pour cela, vous pouvez utiliser l'entrée de menu Compta/Tréso-Comptabilité-Liaison factures client.
* Vérifier que la liaison entre les lignes de factures fournisseurs existantes et le compte comptable est faite. Compléter les liaisons manquantes. Pour cela, vous pouvez utiliser l'entrée de menu Compta/Tréso-Comptabilité-Liaison factures fournisseur.
* Vérifiez que la liaison entre le type de notes de frais et le compte comptable est faite. Compléter les liaisons manquantes. Vous pouvez définir les comptes comptables à utiliser pour chaque type de ligne de note de frais sur la page Compta/Tréso-Comptabilité-Liaison notes de frais.
*Ecrire les transactions dans le Grand Livre. Pour cela, aller sur chaque Journal, et cliquer sur le bouton "Enregistrer les opérations dans le Grand Livre".
*Ajouter ou modifier les opérations existantes et générer des rapports et des exportations.

## Comptabilité de V9 à V13
* Un module numérotation permet la numérotation des codes comptables clients/fournisseurs sur les lettres à partir de la V13. Ce module ne créé pas de doublon dans le cas de tiers au nom proche; Il travaille sur 7 caractères + 1 lettre. Il reste toujours possibile d'éditer manuellement le code comptable du tiers depuis sa fiche

## Laison avec le logiciel de l'expert comptable
* L'expert comptable de LDM utilise ACD Compta. La V9 ne dispose pas d'export pour ACD compta. C'est dispo sur la V13
* Les codes comptables ont une longueur de 8 caractères
* Les codes auxiliaires des clients des fournisseurs commencent par C ou F suivis de lettres (le nom du tiers) sur 7 caractères

## Gestion des A nouveaux
* Dolibarr ne fait pas pour le moment (sur une V13) la gestion des A nouveaux.
* Chaque année, à partir de la balance du 31/12/N, avec les comptes auxiliaires détaillés, on réimporte les balances sur les comptes 6 et 7 .
* On peut partir sur cela du fichier FEC à demander à l'expert comptable et on fiat un import depuis dolibarr en csv

## Comment intégrer une subvention ou un paiement sans facture dans la comptabilité ?
* Pour cela il faut enregsitrer un paiement divers.
* Depuis banque > écritures > ajouter écriture
* Ou bien depuis facture > dépenses spéciale > opérations diverses (paiement divers >V13)

## A quoi servent les groupes personnalisés ?
* Les groupes personnalisés permettent d'agréger plusieurs comptes de façon à analyser l'activité
* Par exemple le groupe 'strat' va permettre de remonter les informations des produits en strat, que ce soient des cabines ou des casiers. Ils permettent donc d'avoir des codes comptables détaillés mais une vision globale sur une typologie de produits
* Il est prévu dans la V14 ou plus de pouvoir lier 1 même code comptable dans plusieurs groupes personnalisés ce qui n'est pas encore le cas pour le moment.

## Lettrage dans dolibarr
* Pour le moment, dolibarr ne sait pas faire le lettrage comptable
* Il faut donc demander au comptable de s'en charger à partir du fichier d'export qu'on lui fourni
* les logiciels de production des comptables ont une fonction de lettrage automatique
* Cette fonction sera sans doute disponible pour la version 16 de dolibarr (2022 ?)


