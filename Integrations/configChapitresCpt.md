# Gestion des chapitres comptables

Cette fonctionnalit� permet de structurer vos exports comptables au format CSV ou FEC, compatibles avec la plupart des logiciels de comptabilit�.

## Activation de la fonctionnalit�

La gestion des chapitres comptables doit �tre activ�e dans **Configuration \> Options g�n�rales**.

## Champs � renseigner

- **Articles** : code d'activit� comptable (ex : 703 pour la production, 707 pour la revente, 0 si h�rit� du rayon)
- **Rayons** : code d'activit� par d�faut appliqu� aux articles
- **Groupes de rayons** : code de chapitre comptable � combiner avec le code d'activit� de l'article
- **TVA** : code comptable associ� � chaque taux de TVA
- **M�thodes de paiement** : code comptable par mode de r�glement (ex : 582 pour les ch�ques)
- **Caisses** : code journal utilis� pour l'export comptable

???? Si les groupes de rayons ne sont pas activ�s, le chapitre comptable par d�faut de la boutique sera utilis�.

## Export comptable CSV

Une fois configur�e, un nouveau rapport **Export comptable CSV** est disponible depuis la page **Rapports**.

Ce rapport comprend une ligne par article vendu, avec les colonnes requises :

- Code journal
- Date de facture
- N� facture
- Code comptable
- Client
- Intitul�
- D�bit
- Cr�dit
- Quantit�

## Exemple d'export CSV

    70;12/12/2020;202012054;702;DUPONT;OEUFS;0.00;11.37;12
    70;12/12/2020;202012054;445712;DUPONT;TVA5.5%;0.00;0.63;0.0
    70;12/12/2020;202012054;53;DUPONT;ESPECE;5.00;0.00;0.00
    70;12/12/2020;202012054;583;DUPONT;TICKETRESTO;5.00;0.00;0.00
    70;12/12/2020;202012054;584;DUPONT;CARTEBLEU;2.00;0.00;0.00

## Ajout dans les rapports PDF et HTML

En activant l'option correspondante dans les param�tres des rapports, un tableau r�capitulatif par chapitre comptable est �galement inclus dans les rapports PDF et HTML.

[Inscrivez-vous maintenant](/)\
