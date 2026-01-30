# Synchronisation Prestashop

Connectez votre boutique Prestashop à votre caisse pour synchroniser automatiquement vos articles et enregistrer les ventes en ligne.

## Importer les articles depuis Prestashop

La synchronisation permet d'importer ou de mettre à jour automatiquement la liste des articles de votre caisse à partir des données saisies dans Prestashop.

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

## TVA et frais de livraison

En Europe, les frais de livraison doivent généralement être soumis à la TVA, au même taux que les produits livrés.

- Créez un article nommé par exemple *Frais de livraison* et appliquez-lui le taux de TVA adéquat.
- En cas de commande mixte (produits à taux de TVA différents), vous pouvez appliquer le taux le plus bas, sauf s'il est de 0%.

La synchronisation Prestashop vous fait gagner du temps tout en assurant la cohérence entre votre boutique en ligne et votre point de vente physique.

