# Export des commandes à destination d'un tableur ou d'un logiciel comptable

Vous pouvez exporter les données de ventes pour les analyser dans un tableur, ou les transmettre à votre expert-comptable au format compatible avec les obligations fiscales.

Ces exports sont aussi disponibles dans la page Rapports, et les mêmes possibilités de filtre ou de sélection de date sont disponibles.

? Il est de la responsabilité de l\'établissement de télécharger les fichiers d\'archives avec une périodicité annuelle, et de conserver ces fichiers pour une durée légale de 6 ans en plus de l\'année fiscale en cours

? Voir également: [Rapports de vente](/graphiques.md)

## Export de l\'archive fiscale

Ce document est le document le plus important à télécharger, au moins chaque année.\
Le format de fichier qui correspond à la génération d\'archives fiscales et le format intitulé \'Archive fiscale\'.\
Ceci vous permettra d\'obtenir un fichier au format ZIP contenant différents fichiers au format CSV.\
Les données de chaque fichier CSV sont signées à l\'aide d\'une chaine de signature HMAC-SHA256.\
Les fichiers CSV exportés sont : paiements, commandes, articles, fermetures, tracabilite

? Document attendu par l\'administration fiscale

## Export vers un tableur

Ces rapports listent les commandes payées sur la période sélectionnée, et peuvent être ouverts avec un tableur.

- **Excel** -- Format .xlsx compatible avec Microsoft Excel
- **CSV** -- Format universel pour tous les autres tableurs

? Les exports tableurs permettent un traitement ou une analyse plus poussée de vos données de vente (tri, filtres, statistiques personnalisées, etc.).

## Export vers un logiciel comptable

Trois formats sont proposés afin de répondre aux besoins des différents outils comptables utilisés par votre cabinet ou votre entreprise.

- **SAF-T** -- Standard Audit File for Tax : format international basé sur XML pour la transmission des écritures comptables.
- **FEC** -- Fichier d'Écritures Comptables : format officiel reconnu par l'administration fiscale française.
- **CSV comptable** -- Fichier au format CSV, avec une ligne par écriture comptable, structuré selon votre configuration de chapitres comptables.

### Export SAF-T

Les fichiers SAF-T sont des rapports comptables complets, conformes aux obligations fiscales de plusieurs pays européens. Ils sont destinés à votre comptable ou aux services fiscaux.

Ils sont signés numériquement pour garantir leur intégrité et leur authenticité. Vous pouvez consulter ces fichiers avec des outils tels que SAF-T Analyzer.

? Pour vérifier l'authenticité des fichiers SAF-T générés, utilisez notre clé publique de vérification cryptographique.

### Export FEC

Les fichiers FEC (Fichier d\'Écritures Comptables) sont conformes aux normes imposées par la législation française.

Ils sont utilisés par la majorité des cabinets comptables et des logiciels comptables en France.

? Vous pouvez générer vos fichiers FEC pour une période donnée, afin de les transmettre à votre comptable ou lors d'un contrôle fiscal.

[Documentation logiciel de caisse](/)\
[![Licence Creative Commons](images/34101c8bb1c1253f61bed847b98016c2c0f519af.png)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener mt-4"} Ce document est mis à disposition selon les termes de la [licence Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener"} .
