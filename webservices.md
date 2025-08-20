# Webservices

Les webservices permettent d'enregistrer automatiquement des ventes dans le logiciel depuis un outil ou site externe.

## Conditions d'acc�s

Pour utiliser les webservices, vous devez disposer d'une licence �tendue.

Une fois activ�e, un onglet \'Webservices\' appara�t dans la page de configuration.

## Enregistrer une commande via une URL

Depuis la page Webservices, vous pouvez construire une URL d'appel contenant tous les param�tres n�cessaires.

    https://caisse.enregistreuse.fr/workers/webapp.php?idboutique=ID_SHOP&key=KEYPARAM&payment=ID_PAYMENTMETHOD&deliveryMethod=ID_DELIVERYMETHOD&idUser=ID_USER
    &client[nom]=TestClientName&client[prenom]=TestClientSurname&client[email]=contact@testclient.fr&client[pays]=FR
    &itemsList[]=-ID_DEPT_1_TestDept
    &itemsList[]=ID_ITEM1_1_TestItem&itemsList[]=ID_ITEM2_2_AnotherTestItem
    &dateValeur=TIMESTAMP_DATE

Les param�tres principaux sont :

- ID_SHOP et KEYPARAM : identifiants du compte boutique
- ID_PAYMENTMETHOD : identifiant de la m�thode de paiement
- ID_DELIVERYMETHOD : identifiant de la m�thode de livraison
- ID_USER : identifiant de l\'utilisateur
- Client : soit un ID client, soit les informations d'un nouveau client
- itemsList : liste des articles � ajouter � la commande
- dateValeur : (optionnel) date en timestamp unix

## Exemples de code fournis

Une fois vos param�tres d�finis, la page Webservices vous propose des exemples pr�ts � l'emploi, en :

- Java
- PHP
- Node.js
- jQuery
- cURL (ligne de commande)

[Inscrivez-vous maintenant](/)\
