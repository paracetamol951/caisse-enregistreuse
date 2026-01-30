# Webhook (notifications HTTP)

## Recevoir des notifications via webhook

Un webhook peut être défini en page Configuration \> Options générales, dans le paragraphe \'Options interface\'.

L'URL du webhook sera appelée automatiquement à chaque commande validée ou terminée.

Paramètres transmis :

- type : validated ou terminated
- orderID : numéro de commande comptable
- orderInternalID : identifiant interne de la commande
- price : montant total
- clientID : identifiant du client
- client : données du client
- cashBoxID : identifiant de la caisse
- deliveryMethod : méthode de livraison
- PDFinvoice : lien vers la facture PDF
- items : liste des articles au format JSON
- VATs : liste des taux et montants de TVA
- VAT : montant total de TVA
- isRefund : true/false si remboursement

? Le webhook est appelé deux fois par commande : une fois à la validation, une autre à la terminaison.

[Documentation logiciel de caisse](/)\
[![Licence Creative Commons](images/34101c8bb1c1253f61bed847b98016c2c0f519af.png)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener mt-4"} Ce document est mis à disposition selon les termes de la [licence Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener"} .
