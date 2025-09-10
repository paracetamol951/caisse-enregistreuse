# Achats de stock et fournisseurs

Ce module vous permet d\'enregistrer vos commandes de stock dans le logiciel.

Vous pouvez saisir les commandes passées à vos fournisseurs, enregistrer leur réception, et intégrer automatiquement les produits au stock.

Cela permet une meilleure gestion de vos prix d\'achat, et donc de votre marge.

Chaque prix d\'achat est mémorisé, et les rapports affichent des marges calculées précisément en fonction de ces prix.

? Vous pouvez également éditer et envoyer les bons de commande ou bons de réception à vos fournisseurs.

## Configuration de la gestion des fournisseurs et des prix d\'achat

1.- Activez la gestion des fournisseurs en page **Config \> Options générales \> Options du catalogue d\'articles**.
2.- Une fois activée, une nouvelle section **Fournisseurs** apparaît dans le menu de configuration.

Vous pourrez y saisir les coordonnées complètes du fournisseur et son délai moyen de livraison.

? Ensuite, affectez chaque produit à un fournisseur :

- Soit globalement pour un rayon (en page de configuration des rayons),
- Soit produit par produit (en page de configuration des articles).

? Chaque produit peut avoir un fournisseur différent.

## Enregistrement d\'une commande fournisseur

Identifiez les articles à réapprovisionner depuis :

- La page de fermeture de caisse
- Ou **Config \> Fournisseurs \> Stocks**

? Cette page vous présente tous les articles triés par stock croissant, ainsi que leur fournisseur associé.

?? En cliquant sur un fournisseur, ouvrez sa fiche et consultez l'onglet **Renouvellement de stock**.

Vous y verrez pour chaque article :

- Stock restant
- Stock commandé non encore reçu
- Quantité vendue le mois précédent
- ?? Seuil d\'alerte de stock bas

?? Saisissez les quantités à commander, les prix d'achat et le délai prévu avant livraison.

## Suivi des commandes fournisseur

Une fois la commande enregistrée, plusieurs actions sont possibles :

- Télécharger ou envoyer le bon de commande (PDF, email, courrier postal)
- Marquer la commande comme envoyée
- Marquer la commande comme reçue pour intégrer les produits au stock

? Consultez l'historique des commandes fournisseur pour suivre les produits en transit.

## Gestion des stocks avec ou sans fournisseur

?? Si vous modifiez manuellement un stock, le prix d'achat par défaut du produit est utilisé.

? Le stock est débité dans l'ordre suivant :

- ?? D'abord les articles non issus d'une commande fournisseur
- ?? Puis les lots issus des commandes fournisseurs, par ordre chronologique de réception

[Documentation logiciel de caisse](/)\
