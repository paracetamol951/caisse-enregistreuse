# Lecture des codes-barres

? Afin d\'utiliser la fonctionnalit� de lecture des codes-barres, vous devez disposer d'un appareil �quip� d'une cam�ra ou d'un lecteur de codes-barres (USB, Bluetooth).

- Cam�ra d'appareil (smartphone, tablette, etc.)
- Lecteur de codes-barres compatible (USB, Bluetooth, clavier PS/2)

##? Activer la fonctionnalit�

?? Naviguez dans **CONFIG \> OPTIONS G�N�RALES**, puis cochez l'option � Codes barres � dans le paragraphe **Mat�riel**.

## Utilisation sous Android

Installez simplement l'application Caisse Enregistreuse sur votre appareil Android.

- Touche Volume + : ouvre l'�cran de scan
- Touche Volume -- : ferme l'�cran de scan

Le scan se fait via la cam�ra. Veillez � ce que l'�clairage soit suffisant et que le code soit bien centr�.

## Utilisation d'un lecteur laser (USB/Bluetooth)

? Les lecteurs de codes-barres fonctionnent comme un clavier : ils saisissent le code suivi d'une touche Entr�e.

? Vous pouvez tester le bon fonctionnement dans un logiciel de traitement de texte.

La pr�sence de caract�res accentu�s indique un probl�me de configuration du jeu de caract�res.

? Solutions en cas de mauvais encodage :

- Scanner les codes sp�ciaux fournis par le fabricant pour configurer la langue/clavier
- Changer la langue de saisie du syst�me (par exemple, passer en clavier anglais)

## Mode lecture de code-barres dans le logiciel

? Appuyez sur le bouton � Lecture code-barres � ou sur la barre espace du clavier pour indiquer que la saisie suivante est un code-barres.

Cela permet au logiciel d'interpr�ter correctement les donn�es scann�es, sans d�clencher les raccourcis clavier.

## Types de codes-barres reconnus

En plus des articles, le syst�me permet de scanner des codes-barres pour : clients, utilisateurs, rayons, r�ductions\...

  Pr�fixe   Type           Description
  --------- -------------- ----------------------------------------------------
  \$0       Articles       Ajoute l'article � la commande (peut �tre omis)
  \$1       Rayons         Change le filtre de rayon sur l'interface de vente
  \$2       Utilisateurs   Identifie rapidement un utilisateur sur la caisse
  \$3       Clients        Associe un client � la commande en cours
  \$4       R�ductions     Applique une r�duction sp�cifique � la commande

Les codes-barres imprim�s depuis le logiciel utilisent automatiquement ces pr�fixes.

\
\
[Configuration des articles](/codesBarresConfig.md)

[Documentation logiciel de caisse](/)\
