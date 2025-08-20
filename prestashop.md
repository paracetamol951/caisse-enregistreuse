# Synchronisation Prestashop

Connectez votre boutique Prestashop � votre caisse pour synchroniser automatiquement vos articles et enregistrer les ventes en ligne.

## Importer les articles depuis Prestashop

La synchronisation permet d\'importer ou de mettre � jour automatiquement la liste des articles de votre caisse � partir des donn�es saisies dans Prestashop.

## Configuration c�t� Prestashop

1.  Connectez-vous � votre interface d'administration Prestashop.
2.  Acc�dez � **Param�tres avanc�s** \> **Webservices**.
3.  Cliquez sur **Ajouter une cl� webservice**.
4.  G�n�rez une cl�, copiez-la, puis cochez les droits **GET** pour les ressources n�cessaires (minimum : categories, images, languages, products, tax_rule_groups).
5.  Enregistrez les modifications.

## Configuration c�t� caisse

1.  Rendez-vous dans **Config \> Options g�n�rales \> Commandes**.
2.  Saisissez votre **nom de domaine Prestashop** (ex. `xxxxx.pswebshop.com`) et votre **cl� API**.
3.  Cliquez sur **Enregistrer** pour m�moriser la configuration.
4.  Dans la page de configuration des articles, cliquez sur le bouton **Synchroniser** pour lancer l'import ou la mise � jour.

## Module Prestashop (enregistrement automatique des ventes)

Un module Prestashop est �galement disponible pour enregistrer automatiquement les ventes r�alis�es sur votre boutique en ligne dans la caisse.

1.  [T�l�chargez le **module Prestashop caisse enregistreuse**.](/Caisse-Enregistreuse/Prestashop/Module/ns_caisseEnregistreusepro.zip){target="_blank"}
2.  Dans votre backoffice Prestashop, ouvrez **Module Manager**.
3.  Cliquez sur **Installer un module**, puis s�lectionnez le fichier du module t�l�charg�.
4.  Une fois install�, cliquez sur **Configurer**.
5.  Dans le logiciel de caisse, copiez les informations **Cl� API** et **Identifiant de boutique**, puis collez-les dans la configuration du module.

## TVA et frais de livraison

En Europe, les frais de livraison doivent g�n�ralement �tre soumis � la TVA, au m�me taux que les produits livr�s.

- Cr�ez un article nomm� par exemple *Frais de livraison* et appliquez-lui le taux de TVA ad�quat.
- En cas de commande mixte (produits � taux de TVA diff�rents), vous pouvez appliquer le taux le plus bas, sauf s'il est de 0%.

La synchronisation Prestashop vous fait gagner du temps tout en assurant la coh�rence entre votre boutique en ligne et votre point de vente physique.

## Aide � la configuration du module Prestashop

Cette page vous guide pour connecter et param�trer le module Prestashop avec votre caisse enregistreuse.

### 1. Connexion au compte caisse

Apr�s l'installation du module sur Prestashop, la premi�re �tape consiste � renseigner votre **cl� API** et votre **ID boutique**.

Ces informations sont disponibles dans le logiciel de caisse, � la page **Webservice**.

[Cl� API]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Captureapi.PNG" original-image-title=""} [ID boutique]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Captureidcaisse.PNG" original-image-title=""}

### 2. Configuration des d�clinaisons

Cr�ez d'abord vos d�clinaisons dans **Prestashop** et dans votre **caisse enregistreuse**.

?? Attention : maximum 5 d�clinaisons par produit. Au-del�, les commandes ne seront pas transmises � la caisse.

#### Exemple de d�clinaisons c�t� site Prestashop

[D�clinaisons Prestashop]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturedecli.PNG" original-image-title=""}

#### R�cup�rer les IDs de d�clinaisons c�t� caisse

[ID d�clinaisons caisse]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturedeclicaisse.PNG" original-image-title=""}

#### Associer chaque d�clinaison Prestashop avec l\'ID correspondant dans la caisse

[Correspondance d�clinaisons]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturediclimod.PNG" original-image-title=""}

R�p�tez cette �tape pour chaque d�clinaison disponible.

### 3. Options avanc�es

Dans l'onglet **Options** du module Prestashop, vous pouvez synchroniser l'heure serveur de votre site avec celle de la caisse (utile si vous utilisez un calendrier de livraison).

[Heure serveur]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Captureheure.PNG" original-image-title=""}

Vous pouvez �galement d�finir sous quel **utilisateur de la caisse** les commandes seront enregistr�es.

[Utilisateur de la caisse]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturecomm.PNG" original-image-title=""}

L'ID utilisateur est visible dans l'onglet **Webservice** du logiciel de caisse.

[ID utilisateur]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Captureiduser.PNG" original-image-title=""}

### 4. Transporteurs

Associez les transporteurs de votre boutique Prestashop aux m�thodes de livraison configur�es dans la caisse.

[Transporteurs]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturelivraison.PNG" original-image-title=""}

### 5. M�thodes de paiement

Associez les moyens de paiement de Prestashop avec ceux configur�s dans le logiciel de caisse.

[Moyens de paiement]{.image .placeholder original-image-src="/Caisse-Enregistreuse/Prestashop/Capturepaiement.PNG" original-image-title=""}

[Inscrivez-vous maintenant](/)\
