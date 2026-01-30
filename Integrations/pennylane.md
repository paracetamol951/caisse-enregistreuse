# Intégration de PennyLane dans Kash.Click

## 1. Présentation générale {#présentation-générale .mt-20}

Cette documentation décrit de manière détaillée l'intégration entre le logiciel de caisse Kash.Click et le logiciel de comptabilité PennyLane. Cette intégration permet la transmission automatique des données comptables issues des ventes réalisées dans Kash.Click vers PennyLane, en s'appuyant sur les mécanismes standards de synchronisation et sur le protocole OAuth.

## 2. Prérequis {#prérequis .mt-20}

- Disposer d'un compte Kash.Click actif
- [Disposer d'un compte PennyLane actif](https://pennylane.com?downloadInvoice=1){rel="nofollow"}
- Avoir accès aux paramètres de configuration dans Kash.Click

## 3. Connexion du compte PennyLane {#connexion-du-compte-pennylane .mt-20}

La connexion entre Kash.Click et PennyLane s'effectue depuis l'interface de Kash.Click.

1.  Se rendre dans le menu Configuration
2.  Ouvrir la section Options générales
3.  Accéder au paragraphe Web Services / Intégrations
4.  Cliquer sur le bouton « Se connecter à PennyLane »

Ce bouton utilise le protocole OAuth mis à disposition par PennyLane. L'utilisateur est redirigé vers une page sécurisée hébergée par PennyLane afin d'autoriser ou refuser l'accès de Kash.Click à son compte de comptabilité.

## 4. Autorisation et import des données historiques {#autorisation-et-import-des-données-historiques .mt-20}

Une fois l'autorisation accordée, l'utilisateur est automatiquement redirigé vers Kash.Click. Le logiciel propose alors l'envoi automatique de l'historique des commandes et des paiements vers PennyLane.

Par défaut, la date de début correspond au début de l'exercice comptable. Par exemple, si l'exercice se termine le 31 décembre, toutes les données du 1er janvier jusqu'à la date courante seront transmises. Cette opération peut prendre plusieurs dizaines de minutes selon le volume de données.

## 5. Événements générant des écritures comptables {#événements-générant-des-écritures-comptables .mt-20}

Après la connexion initiale et l'éventuel transfert de l'historique, Kash.Click enregistre automatiquement les données comptables dans PennyLane selon trois types d'événements.

### 5.1 Enregistrement d'une commande {#enregistrement-dune-commande .mt-20}

Lors de l'enregistrement d'une commande, Kash.Click génère plusieurs écritures comptables :

- Un ou plusieurs mouvements sur les comptes des ventes (type 706 / 707 / 711 selon la configuration, ventilé par taux de TVA)
- Un ou plusieurs mouvements sur les comptes de TVA, avec un compte distinct par taux de TVA
- Un mouvement sur le compte du client

Les ventes et les comptes de TVA sont systématiquement ventilés par taux (exemple : 20 %, 5,5 %, etc.).

Avant l'enregistrement, Kash.Click vérifie l'existence du client dans PennyLane :

- Si le client existe déjà, son compte comptable est réutilisé
- Si le client n'existe pas, Kash.Click transmet automatiquement les informations client à PennyLane, qui crée le compte correspondant et retourne le numéro de compte associé

? Si la gestion des chapitres comptables est active, le logiciel utilisera vos chapitres comptables configurés pour les exports Pennylane.

### 5.2 Paiement d'une commande

Le paiement d'une commande déclenche une nouvelle série d'écritures comptables :

- Débit du compte client
- Crédit du compte comptable correspondant au mode de paiement utilisé (espèces, carte bancaire, virement, etc.)

### 5.3 Fermeture de caisse

Lors de la fermeture de caisse, Kash.Click génère des écritures globales :

- Débit du compte général des ventes (non ventilé par TVA)
- Crédit du compte général des recettes

Les éventuelles différences ou erreurs de caisse sont automatiquement enregistrées dans les comptes comptables dédiés aux erreurs de caisse et débitent les chapitres des modes de paiements correspondants.

## 6. Synchronisation des données {#synchronisation-des-données .mt-20}

L'intégration comprend également une synchronisation régulière de certaines données de référence entre Kash.Click et PennyLane.

- Modes de paiement
- Taux de TVA
- Journaux comptables

Chaque caisse configurée dans Kash.Click est associée à un journal comptable distinct dans PennyLane. Cela permet de gérer un commerce utilisant une ou plusieurs caisses, tout en conservant une séparation claire des écritures comptables par caisse.

## 7. Résumé {#résumé .mt-20}

L'intégration PennyLane de Kash.Click assure une transmission fiable, automatisée et structurée des données comptables. Elle garantit une cohérence entre les ventes, les paiements, la TVA, les clients et les fermetures de caisse, tout en respectant les principes comptables attendus par PennyLane.

[Documentation logiciel de caisse](/)\
[![Licence Creative Commons](images/34101c8bb1c1253f61bed847b98016c2c0f519af.png)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener mt-4"} Ce document est mis à disposition selon les termes de la [licence Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener"} .
