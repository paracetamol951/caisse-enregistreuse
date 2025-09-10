# Lecture des codes-barres

? Afin d\'utiliser la fonctionnalité de lecture des codes-barres, vous devez disposer d'un appareil équipé d'une caméra ou d'un lecteur de codes-barres (USB, Bluetooth).

- Caméra d'appareil (smartphone, tablette, etc.)
- Lecteur de codes-barres compatible (USB, Bluetooth, clavier PS/2)

##? Activer la fonctionnalité

?? Naviguez dans **CONFIG \> OPTIONS GÉNÉRALES**, puis cochez l'option « Codes barres » dans le paragraphe **Matériel**.

## Utilisation sous Android

Installez simplement l'application Caisse Enregistreuse sur votre appareil Android.

- Touche Volume + : ouvre l'écran de scan
- Touche Volume -- : ferme l'écran de scan

Le scan se fait via la caméra. Veillez à ce que l'éclairage soit suffisant et que le code soit bien centré.

## Utilisation d'un lecteur laser (USB/Bluetooth)

? Les lecteurs de codes-barres fonctionnent comme un clavier : ils saisissent le code suivi d'une touche Entrée.

? Vous pouvez tester le bon fonctionnement dans un logiciel de traitement de texte.

La présence de caractères accentués indique un problème de configuration du jeu de caractères.

? Solutions en cas de mauvais encodage :

- Scanner les codes spéciaux fournis par le fabricant pour configurer la langue/clavier
- Changer la langue de saisie du système (par exemple, passer en clavier anglais)

## Mode lecture de code-barres dans le logiciel

? Appuyez sur le bouton « Lecture code-barres » ou sur la barre espace du clavier pour indiquer que la saisie suivante est un code-barres.

Cela permet au logiciel d'interpréter correctement les données scannées, sans déclencher les raccourcis clavier.

## Types de codes-barres reconnus

En plus des articles, le système permet de scanner des codes-barres pour : clients, utilisateurs, rayons, réductions\...

  Préfixe   Type           Description
  --------- -------------- ----------------------------------------------------
  \$0       Articles       Ajoute l'article à la commande (peut être omis)
  \$1       Rayons         Change le filtre de rayon sur l'interface de vente
  \$2       Utilisateurs   Identifie rapidement un utilisateur sur la caisse
  \$3       Clients        Associe un client à la commande en cours
  \$4       Réductions     Applique une réduction spécifique à la commande

Les codes-barres imprimés depuis le logiciel utilisent automatiquement ces préfixes.

\
\
[Configuration des articles](/codesBarresConfig.md)

[Documentation logiciel de caisse](/)\
