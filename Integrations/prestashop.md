# Synchronisation Prestashop {#synchronisation-prestashop .mb-10 .mt-20}

Connectez votre boutique Prestashop à votre caisse pour synchroniser automatiquement vos articles et enregistrer les ventes en ligne.

## Importer les articles depuis Prestashop {#importer-les-articles-depuis-prestashop .mb-10 .mt-20}

La synchronisation permet d\'importer ou de mettre à jour automatiquement la liste des articles de votre caisse à partir des données saisies dans Prestashop.

## Configuration côté Prestashop {#configuration-côté-prestashop .mb-10 .mt-20}

1.  Connectez-vous à votre interface d'administration Prestashop.
2.  Accédez à **Paramètres avancés** \> **Webservices**.
3.  Cliquez sur **Ajouter une clé webservice**.
4.  Générez une clé, copiez-la, puis cochez les droits **GET** pour les ressources nécessaires (minimum : categories, images, languages, products, tax_rule_groups).
5.  Enregistrez les modifications.

## Configuration côté caisse {#configuration-côté-caisse .mb-10 .mt-20}

1.  Rendez-vous dans **Config \> Options générales \> Commandes**.
2.  Saisissez votre **nom de domaine Prestashop** (ex. `xxxxx.pswebshop.com`) et votre **clé API**.
3.  Cliquez sur **Enregistrer** pour mémoriser la configuration.
4.  Dans la page de configuration des articles, cliquez sur le bouton **Synchroniser** pour lancer l'import ou la mise à jour.

## TVA et frais de livraison {#tva-et-frais-de-livraison .mb-10 .mt-20}

En Europe, les frais de livraison doivent généralement être soumis à la TVA, au même taux que les produits livrés.

- Créez un article nommé par exemple *Frais de livraison* et appliquez-lui le taux de TVA adéquat.
- En cas de commande mixte (produits à taux de TVA différents), vous pouvez appliquer le taux le plus bas, sauf s'il est de 0%.

La synchronisation Prestashop vous fait gagner du temps tout en assurant la cohérence entre votre boutique en ligne et votre point de vente physique.

[Documentation logiciel de caisse](/)\
[![Licence Creative Commons](images/34101c8bb1c1253f61bed847b98016c2c0f519af.png)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener mt-4"} Ce document est mis à disposition selon les termes de la [licence Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener"} .
