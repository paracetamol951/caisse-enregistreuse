# Synchronisation WooCommerce

Cette fonctionnalité vous permet de synchroniser automatiquement vos produits et vos clients entre WooCommerce et le logiciel de caisse.

## 1. Générer une clé d'API WooCommerce

Dans votre interface d'administration WordPress, allez dans le menu **WooCommerce \> Settings \> Advanced \> REST API**.

Ajoutez une nouvelle clé, affectez-lui un nom, attribuez les droits de **lecture** uniquement, puis générez la clé.

Une fois générée, conservez bien les deux éléments suivants :

- **Clé utilisateur (Consumer Key)**
- **Code secret utilisateur (Consumer Secret)**

## 2. Configurer la connexion côté caisse

Dans le logiciel de caisse, accédez à **Config \> Options générales \> Commandes**, puis localisez l'encart **WooCommerce**.

Saisissez dans ce formulaire :

- **L'adresse de votre site WooCommerce**, en incluant le préfixe `https://`.
- La **clé utilisateur** et le **code secret** générés à l'étape précédente.

?? Les connexions non sécurisées (http) ne sont pas acceptées.

## 3. Synchronisation des articles et des clients

Une fois la configuration effectuée, des boutons **Synchronisation WooCommerce** apparaîtront dans :

- La page de configuration des **articles**
- La page de configuration des **clients**

Ces boutons vous permettront de synchroniser manuellement votre catalogue produits et vos fiches clients entre WooCommerce et votre caisse.

[Documentation logiciel de caisse](/)\
[![Licence Creative Commons](images/34101c8bb1c1253f61bed847b98016c2c0f519af.png)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener mt-4"} Ce document est mis à disposition selon les termes de la [licence Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener"} .
