# Gestion des chapitres comptables

Cette fonctionnalité permet de structurer vos exports comptables au format CSV ou FEC, compatibles avec la plupart des logiciels de comptabilité.

## Activation de la fonctionnalité

La gestion des chapitres comptables doit être activée dans **Configuration \> Options générales**.

## Champs à renseigner

### Données de vente

Le chapitre comptable des données de ventes est la concaténation do code activité de groupe de rayon avec le code activité de l'article

- Articles, si absent, le **Code activité du rayon** est utilisé
- **Rayons** : code d'activité par défaut appliqué aux articles
- **Groupes de rayons** : code de chapitre comptable à combiner avec le code d'activité de l'article, si absent, le **Code activité général** est utilisé
- **Code activité général** : en page d'options générales, c'est le paramètre par défaut pour les ventes

### Taux de TVA

- **TVA** : code comptable associé à chaque taux de TVA
- **4457** : le préfixe 4457 sera ajouté automatiquement pour former le chapitre comptable

### Méthodes de paiement

- **Méthodes de paiement** : code comptable par mode de règlement (ex : 582 pour les chèques), 511 par défaut

### Caisses

- **Caisses** : code journal utilisé pour l'export comptable

### Clients

- **Clients** : code comptable, si absent, l'identifiant interne sera utilisé si le groupe du client n'a pas de code comptable
- **Groupe de client** : code comptable qui viendra préfixer le chapitre comptable du client
- **411** : ce code comptable viendra préfixer le chapitre comptable du client, en plus du code comptable du groupe de clients

? Si les groupes de rayons ne sont pas activés, le chapitre comptable par défaut de la boutique sera utilisé.

## Export comptable CSV

Une fois configurée, un nouveau rapport **Export comptable CSV** est disponible depuis la page **Rapports**.

Ce rapport comprend une ligne par article vendu, avec les colonnes requises :

- Code journal
- Date de facture
- N° facture
- Code comptable
- Client
- Intitulé
- Débit
- Crédit
- Quantité

## Exemple d'export CSV

    70;12/12/2020;202012054;702;DUPONT;OEUFS;0.00;11.37;12
    70;12/12/2020;202012054;445712;DUPONT;TVA5.5%;0.00;0.63;0.0
    70;12/12/2020;202012054;53;DUPONT;ESPECE;5.00;0.00;0.00
    70;12/12/2020;202012054;583;DUPONT;TICKETRESTO;5.00;0.00;0.00
    70;12/12/2020;202012054;584;DUPONT;CARTEBLEU;2.00;0.00;0.00

## Ajout dans les rapports PDF et HTML

En activant l'option correspondante dans les paramètres des rapports, un tableau récapitulatif par chapitre comptable est également inclus dans les rapports PDF et HTML.

