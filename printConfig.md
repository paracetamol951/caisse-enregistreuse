#? Configurer les imprimantes

## M�thode standard (navigateur)

Cliquez sur le bouton \'Imprimer un ticket de caisse\' depuis l\'interface de la caisse. Le ticket visible dans la zone \'Ticket de caisse\' sera imprim� via l\'imprimante configur�e par d�faut dans votre syst�me.

Pensez � configurer les marges et � d�sactiver les ent�tes/pieds de page via \'Fichier \> Mise en page\' de votre navigateur.

? Aucune configuration n'est requise, mais une bo�te de dialogue s'affiche � chaque impression.

## Impression sans bo�te de dialogue

Pour �viter l\'affichage de la bo�te de dialogue d\'impression, utilisez l\'une des imprimantes compatibles int�gr�es dans nos applications Android, iOS ou Windows.

Cette m�thode permet l'impression automatique du ticket � la fin d'une commande.

## Impression depuis Android

Android permet l'impression via le syst�me. Certaines imprimantes Bluetooth ou r�seau sont compatibles.

## Imprimantes int�gr�es et d�tect�es

Si vous utilisez notre applicatino Android, iOs, ou Microsoft, certaines imprimantes sont automatiquement d�tect�es

- Sunmi : d�tect�e automatiquement sous Android (imprimante et �cran secondaire).
- StarMicronics : connexion Bluetooth (Android/iOs/Microsoft) via Options g�n�rales \> Mat�riel.
- KKmoon POS-5802DD : connexion Bluetooth (Android) via Options g�n�rales \> Mat�riel.
- Epson Connect : connexion Bluetooth (Android/iOs) via Options g�n�rales \> Mat�riel.

## Epson Ethernet (ePOS)

L'impression via r�seau local fonctionne sans bo�te de dialogue et sur tous les navigateurs, mais sa configuration est plus complexe.

1.  Connectez l'imprimante au r�seau local.
2.  Attribuez-lui une IP via EpsonNet Config (ex : 192.168.1.168).
3.  Acc�dez � l'interface de configuration : http://\[adresse_ip\].
4.  Activez Epson ePOS Print et d�finissez un \'Device ID\'.
5.  Dans l'app, activez \'Imprimante Epson Ethernet\' et entrez IP + Device ID.

? Il peut �galement �tre n�cessaire d\'accepter un avertissement de s�curit� sur les appareils qui utiliseront l\'imprimante. Pour accepter l\'�ventuel avertissement de s�curit� (cela d�pend du navigateur utilis�), il faut vous rendre dans ce logiciel dans la page de configuration de l\'imprimante, utiliser le bouton \"Ouvrir la page de configuration Epson\", et accepter l\'avertissement de s�curit�, en cochant �ventuellement \"Toujours accepter l\'avertissement de s�curit�\".

? Appuyez 5 secondes sur le bouton arri�re de votre imprimante Epson pour imprimer les infos r�seau

? Identifiants par defaut pour acc�der � la page de configuration de l\'imprimante : epson / epson

## Imprimante KKmoon POS-5802DD

Cette imprimante fonctionne avec l'application Android/iOS uniquement, via Bluetooth.

Pour l'affichage des caract�res accentu�s et du symbole ?, changez le jeu de caract�res via les drivers KKmoon.

1.  T�l�chargez et installez le pilote KKmoon sur votre ordinateur.
2.  Connectez l'imprimante en USB et ouvrez le logiciel de configuration.
3.  Modifiez le \'Default code page\' en PC437(Std.Europe)(1).

[Inscrivez-vous maintenant](/)\
