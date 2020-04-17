 # Clients, contact, etc...

## Créer un client 

<!-- tabs:start -->

#### ** En mode semi-automatique **

Depuis le menu horizontal haut, aller sur 'Tiers'
* Cliquez sur 'Nouveau tiers'
* En passant par ce cheminement, vous accédez à une interface de recherche automatique.
* Indiquez un indice de recherche, par exemple 'Menuiserie Picard' et cliquez sur rechercher.
* Le logiciel interroge alors une base de données externe des entreprises et vous propose une liste de résultats.
* Cocher le ou les résultats correspondants et cliquez sur créer
* Dolibarr créé alors automatiquement la fiche du tiers à partir des informations disponibles.

#### ** En mode manuel **

Depuis le menu horizontal haut, aller sur 'Tiers'
* Cliquer sur 'Nouveau client' (ou 'nouveau prospect' selon le cas)
* Seuls les champs en gras sont obligatoires
* Remplissez la fiche de façon exhaustive. 
* Rappelez-vous que cette fiche servira ensuite à toutes les étapes et à chaque fois que nous travaillerons avec ce client. C'est donc un gain de temps pour l'ensemble des personnes qui auront à travailler avec ces informations si la fiche est correctement renseignée.
* Valider votre fiche en cliquant sur 'Créer tiers'
* Créer ensuite les contacts associés à ce tiers
* Attention, le numéro de Siret est obligatoire pour ajouter un tiers. Il permet de vérifier qu'il n'y a pas de doublon dans la base…(en mode semi automatique, le siret est récupéré automatiquement)

<!-- tabs:end -->

## Créer un client sans numéro de siret

<!-- tabs:start -->

#### ** C'est un client particulier **

* Lorsque vous devez créer un client pour un particulier
* Vous devez ch oisir tout en haut de la fiche création du client "Créer un tiers + un contact/adresse/fils"
* En faisant cela, dolibarr préselectionne le type "particulier" pour le champ type de tiers
* **Le numéro de siret n'est alors plus obligatoire, même, si le champ reste en gras.**

#### ** C'est un client pro sans numéro de siret **

* Créer un client en mode manuel et sélectionner le type d'entreprise Particulier
* Dans ce cas le numéro de Siret n'est plus obligatoire
* **Attention, cette fonction n'est à utiliser que dans le cas de la création d'entreprise**

<!-- tabs:end -->
