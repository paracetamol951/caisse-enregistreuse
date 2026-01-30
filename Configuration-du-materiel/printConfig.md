# Configurer les imprimantes

## Méthode standard (navigateur)

Cliquez sur le bouton 'Imprimer un ticket de caisse' depuis l'interface de la caisse. Le ticket visible dans la zone 'Ticket de caisse' sera imprimé via l'imprimante configurée par défaut dans votre système.

Pensez à configurer les marges et à désactiver les entêtes/pieds de page via 'Fichier \> Mise en page' de votre navigateur.

? Aucune configuration n'est requise, mais une boîte de dialogue s'affiche à chaque impression.

## Impression sans boîte de dialogue

Pour éviter l'affichage de la boîte de dialogue d'impression, utilisez l'une des imprimantes compatibles intégrées dans nos applications Android, iOS ou Windows.

Cette méthode permet l'impression automatique du ticket à la fin d'une commande.

## Impression depuis Android

Android permet l'impression via le système. Certaines imprimantes Bluetooth ou réseau sont compatibles.

## Imprimantes intégrées et détectées

Si vous utilisez notre applicatino Android, iOs, ou Microsoft, certaines imprimantes sont automatiquement détectées

- Sunmi : détectée automatiquement sous Android (imprimante et écran secondaire).
- StarMicronics : connexion Bluetooth (Android/iOs/Microsoft) via Options générales \> Matériel.
- KKmoon POS-5802DD : connexion Bluetooth (Android) via Options générales \> Matériel.
- Epson Connect : connexion Bluetooth (Android/iOs) via Options générales \> Matériel. (Epson ePos)

## Epson Ethernet (non recommandé)

L'impression via réseau local fonctionne sans boîte de dialogue et sur tous les navigateurs, mais sa configuration est plus complexe.

1.  Connectez l'imprimante au réseau local.
2.  Attribuez-lui une IP via EpsonNet Config (ex : 192.168.1.168).
3.  Accédez à l'interface de configuration : http://\[adresse_ip\].
4.  Activez Epson ePOS Print et définissez un 'Device ID'.
5.  Dans l'app, activez 'Imprimante Epson Ethernet' et entrez IP + Device ID.

? Non recommandé : avec les applications Android / iOs, préférez toujours la connexion ePos Epson connect, plus simple à mettre en place

? Non disponible sous Android / iOs (uniquement avec navigateur)

? Il peut également être nécessaire d'accepter un avertissement de sécurité sur les appareils qui utiliseront l'imprimante. Pour accepter l'éventuel avertissement de sécurité (cela dépend du navigateur utilisé), il faut vous rendre dans ce logiciel dans la page de configuration de l'imprimante, utiliser le bouton "Ouvrir la page de configuration Epson", et accepter l'avertissement de sécurité, en cochant éventuellement "Toujours accepter l'avertissement de sécurité".

? Appuyez 5 secondes sur le bouton arrière de votre imprimante Epson pour imprimer les infos réseau

? Identifiants par defaut pour accéder à la page de configuration de l'imprimante : epson / epson

## Imprimante KKmoon POS-5802DD

Cette imprimante fonctionne avec l'application Android/iOS uniquement, via Bluetooth.

Pour l'affichage des caractères accentués et du symbole ?, changez le jeu de caractères via les drivers KKmoon.

1.  Téléchargez et installez le pilote KKmoon sur votre ordinateur.
2.  Connectez l'imprimante en USB et ouvrez le logiciel de configuration.
3.  Modifiez le 'Default code page' en PC437(Std.Europe)(1).

