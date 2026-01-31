# Gestion du numéro de l'appelant

? Cette fonctionnalité permet d'ouvrir automatiquement la fiche client lorsqu'un appel entrant est détecté sur votre ligne de téléphone fixe.

Fonctionnalité compatible uniquement avec Windows et le modem US Robotics.

## Configuration requise

- Ordinateur sous Windows
- Modem US Robotics connecté à votre ligne téléphonique fixe
- Connexion USB entre le modem et l'ordinateur
-  Application « Caisse Enregistreuse » installée depuis le Windows Store

## Étapes de configuration

1.- Connectez le modem US Robotics à votre ligne fixe et à votre ordinateur Windows via USB.
2.- Installez les pilotes du modem si nécessaire.
3.- Configurez le modem pour qu'il utilise le port COM3.
4.- Installez et lancez notre application depuis le Windows Store.
5.- Dans le logiciel, allez dans **Config \> Options générales \> Matériel** et activez l'option **Utilisation du modem US Robotics**.

Une fois correctement configuré, un message « US Robotics modem detected » s'affichera.

## Fonctionnement

? Lorsqu'un appel est reçu, le logiciel lit automatiquement le numéro de l'appelant.

- Si un client correspond à ce numéro, sa fiche client s'affiche automatiquement.
- Si aucun client n'est trouvé, l'application propose de créer une nouvelle fiche client avec le numéro déjà renseigné.

