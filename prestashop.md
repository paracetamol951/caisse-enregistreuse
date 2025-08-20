# Synchronisation Prestashop

Connectez votre boutique Prestashop à votre caisse pour synchroniser automatiquement vos articles et enregistrer les ventes en ligne.

## Importer les articles depuis Prestashop

La synchronisation permet d\'importer ou de mettre à jour automatiquement la liste des articles de votre caisse à partir des données saisies dans Prestashop.

## Configuration côté Prestashop

1.  Connectez-vous à votre interface d'administration Prestashop.
2.  Accédez à **Paramètres avancés** \> **Webservices**.
3.  Cliquez sur **Ajouter une clé webservice**.
4.  Générez une clé, copiez-la, puis cochez les droits **GET** pour les ressources nécessaires (minimum : categories, images, languages, products, tax_rule_groups).
5.  Enregistrez les modifications.

## Configuration côté caisse

1.  Rendez-vous dans **Config \> Options générales \> Commandes**.
2.  Saisissez votre **nom de domaine Prestashop** (ex. `xxxxx.pswebshop.com`) et votre **clé API**.
3.  Cliquez sur **Enregistrer** pour mémoriser la configuration.
4.  Dans la page de configuration des articles, cliquez sur le bouton **Synchroniser** pour lancer l'import ou la mise à jour.

## Module Prestashop (enregistrement automatique des ventes)

Un module Prestashop est également disponible pour enregistrer automatiquement les ventes réalisées sur votre boutique en ligne dans la caisse.

1.  [Téléchargez le **module Prestashop caisse enregistreuse**.](/Caisse-Enregistreuse/Prestashop/Module/ns_caisseEnregistreusepro.zip){target="_blank"}
2.  Dans votre backoffice Prestashop, ouvrez **Module Manager**.
3.  Cliquez sur **Installer un module**, puis sélectionnez le fichier du module téléchargé.
4.  Une fois installé, cliquez sur **Configurer**.
5.  Dans le logiciel de caisse, copiez les informations **Clé API** et **Identifiant de boutique**, puis collez-les dans la configuration du module.

## TVA et frais de livraison

En Europe, les frais de livraison doivent généralement être soumis à la TVA, au même taux que les produits livrés.

- Créez un article nommé par exemple *Frais de livraison* et appliquez-lui le taux de TVA adéquat.
- En cas de commande mixte (produits à taux de TVA différents), vous pouvez appliquer le taux le plus bas, sauf s'il est de 0%.

La synchronisation Prestashop vous fait gagner du temps tout en assurant la cohérence entre votre boutique en ligne et votre point de vente physique.

## Aide à la configuration du module Prestashop

Cette page vous guide pour connecter et paramétrer le module Prestashop avec votre caisse enregistreuse.

### 1. Connexion au compte caisse

Après l'installation du module sur Prestashop, la première étape consiste à renseigner votre **clé API** et votre **ID boutique**.

Ces informations sont disponibles dans le logiciel de caisse, à la page **Webservice**.

[Clé API]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Captureapi.PNG" original-image-title=""} [ID boutique]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Captureidcaisse.PNG" original-image-title=""}

### 2. Configuration des déclinaisons

Créez d'abord vos déclinaisons dans **Prestashop** et dans votre **caisse enregistreuse**.

?? Attention : maximum 5 déclinaisons par produit. Au-delà, les commandes ne seront pas transmises à la caisse.

#### Exemple de déclinaisons côté site Prestashop

[Déclinaisons Prestashop]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturedecli.PNG" original-image-title=""}

#### Récupérer les IDs de déclinaisons côté caisse

[ID déclinaisons caisse]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturedeclicaisse.PNG" original-image-title=""}

#### Associer chaque déclinaison Prestashop avec l\'ID correspondant dans la caisse

[Correspondance déclinaisons]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturediclimod.PNG" original-image-title=""}

Répétez cette étape pour chaque déclinaison disponible.

### 3. Options avancées

Dans l'onglet **Options** du module Prestashop, vous pouvez synchroniser l'heure serveur de votre site avec celle de la caisse (utile si vous utilisez un calendrier de livraison).

[Heure serveur]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Captureheure.PNG" original-image-title=""}

Vous pouvez également définir sous quel **utilisateur de la caisse** les commandes seront enregistrées.

[Utilisateur de la caisse]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturecomm.PNG" original-image-title=""}

L'ID utilisateur est visible dans l'onglet **Webservice** du logiciel de caisse.

[ID utilisateur]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Captureiduser.PNG" original-image-title=""}

### 4. Transporteurs

Associez les transporteurs de votre boutique Prestashop aux méthodes de livraison configurées dans la caisse.

[Transporteurs]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturelivraison.PNG" original-image-title=""}

### 5. Méthodes de paiement

Associez les moyens de paiement de Prestashop avec ceux configurés dans le logiciel de caisse.

[Moyens de paiement]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturepaiement.PNG" original-image-title=""}

[Inscrivez-vous maintenant](/)\
