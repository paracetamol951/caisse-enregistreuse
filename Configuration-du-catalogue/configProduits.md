# Configurer les articles

? Pour effectuer cette opération, vous devez disposer des droits administrateur.

?? Accédez à la page **Config** pour gérer vos articles.

## Ajouter un nouvel article

Cliquez sur le bouton « Ajouter » situé en haut du tableau.

Remplissez les champs proposés dans la fenêtre qui s\'affiche.

## Modifier un article existant

- Double-cliquez sur le champ que vous souhaitez modifier.
- Appuyez sur Entrée pour valider la saisie.
- Les modifications sont enregistrées automatiquement à chaque modification de champ.
- Pour modifier l'image de l'article, cliquez sur l'image actuelle et remplissez le formulaire affiché.

## Signification des champs

- **Nom** : Nom de l'article tel qu'il apparaîtra sur le ticket de caisse et sur le clavier.
- **Taux de TVA** : Taux appliqué à cet article. Par défaut, celui du rayon est utilisé si « Rayon » est sélectionné.
- **Réduction** : Réduction appliquée à cet article. Par défaut, celle du rayon est utilisée si « Rayon » est sélectionné.
- **Prix** : Prix de vente de l'article (TTC ou HT selon la configuration dans *Configuration \> Boutique*).
- **Rayon** : Rayon dans lequel classer cet article.
- **Image** : Image affichée sur le clavier de caisse (JPG ou PNG, moins de 2 Mo).
- **Position** : Position du bouton dans le clavier. Vous pouvez également déplacer les articles par glisser-déposer.

D'autres champs peuvent apparaître selon votre configuration (code-barres, DLC, seuil de stock, etc.).

## Gestion du prix d'achat

Après activation de la fonctionnalité dans les options générales, vous pourrez saisir le prix d'achat unitaire de chaque article.

Ces informations sont utilisées dans les rapports PDF pour calculer précisément vos marges.

## Articles invisibles sur le ticket de caisse

Certains articles peuvent être configurés pour ne pas apparaître sur le ticket de caisse client.

- Leur prix doit être de 0.
- Leur nom doit commencer par `/*/*`

Ces articles sont utiles par exemple pour la gestion des ingrédients ou de composants invisibles.

Ils resteront visibles dans l'interface du vendeur et dans les rapports.

## Facteur de saisie

Afin d\'économiser des actions dans le processus de vente, il est possible d\'indiquer un facteur de saisie pour les quantités d\'articles.\
Ceci vous permet de saisir les quantités multipliées par 10, 100, 1000, etc afin de ne pas avoir à saisir la virgule.

- Activez les facteurs de saisie en page Configuration, Options générales, paragraphe \"Options du catalogue d\'articles\"
- En page de configuration des articles, renseignez le facteur de saisie (1 par défaut)

Avec un facteur de saisie de 100, saisissez 150 pour une quantité de 1.5

Le facteur de saisie doit être une puissance de 10

[Documentation logiciel de caisse](/)\
[![Licence Creative Commons](images/34101c8bb1c1253f61bed847b98016c2c0f519af.png)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener mt-4"} Ce document est mis à disposition selon les termes de la [licence Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener"} .
