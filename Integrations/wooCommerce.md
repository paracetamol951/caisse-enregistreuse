# Synchronisation WooCommerce

Cette fonctionnalit� vous permet de synchroniser automatiquement vos produits et vos clients entre WooCommerce et le logiciel de caisse.

## 1. G�n�rer une cl� d'API WooCommerce

Dans votre interface d'administration WordPress, allez dans le menu **WooCommerce \> Settings \> Advanced \> REST API**.

Ajoutez une nouvelle cl�, affectez-lui un nom, attribuez les droits de **lecture** uniquement, puis g�n�rez la cl�.

Une fois g�n�r�e, conservez bien les deux �l�ments suivants :

- **Cl� utilisateur (Consumer Key)**
- **Code secret utilisateur (Consumer Secret)**

## 2. Configurer la connexion c�t� caisse

Dans le logiciel de caisse, acc�dez � **Config \> Options g�n�rales \> Commandes**, puis localisez l'encart **WooCommerce**.

Saisissez dans ce formulaire :

- **L'adresse de votre site WooCommerce**, en incluant le pr�fixe `https://`.
- La **cl� utilisateur** et le **code secret** g�n�r�s � l'�tape pr�c�dente.

?? Les connexions non s�curis�es (http) ne sont pas accept�es.

## 3. Synchronisation des articles et des clients

Une fois la configuration effectu�e, des boutons **Synchronisation WooCommerce** appara�tront dans :

- La page de configuration des **articles**
- La page de configuration des **clients**

Ces boutons vous permettront de synchroniser manuellement votre catalogue produits et vos fiches clients entre WooCommerce et votre caisse.

[Documentation logiciel de caisse](/)\
