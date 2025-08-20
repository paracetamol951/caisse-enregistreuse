# Webhook (notifications HTTP)

## Recevoir des notifications via webhook

Un webhook peut �tre d�fini en page Configuration \> Options g�n�rales, dans le paragraphe \'Options interface\'.

L'URL du webhook sera appel�e automatiquement � chaque commande valid�e ou termin�e.

Param�tres transmis :

- type : validated ou terminated
- orderID : num�ro de commande comptable
- orderInternalID : identifiant interne de la commande
- price : montant total
- clientID : identifiant du client
- client : donn�es du client
- cashBoxID : identifiant de la caisse
- deliveryMethod : m�thode de livraison
- PDFinvoice : lien vers la facture PDF
- items : liste des articles au format JSON
- VATs : liste des taux et montants de TVA
- VAT : montant total de TVA
- isRefund : true/false si remboursement

? Le webhook est appel� deux fois par commande : une fois � la validation, une autre � la terminaison.

[Inscrivez-vous maintenant](/)\
