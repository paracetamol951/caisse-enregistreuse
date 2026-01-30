## 

# Yavin : Configurer les paiements CB avec un TPE bancaire

Les terminaux Yavin permettent d\'accepter les paiements par carte bancaire : CB, Visa, Mastercard, American Express, avec ou sans contact.\
Vous pouvez utiliser le contrat monétique Yavin ou celui de votre banque.

Notre logiciel est compatible avec deux méthodes d'intégration Yavin : via Yavin Cloud (1 tablette + 1 terminal) ou directement sur le terminal Yavin.

## Intégration avec Yavin Cloud

Cette méthode permet de piloter votre terminal Yavin à distance via Wi-Fi. Le logiciel transmet automatiquement le montant à encaisser au terminal.

Un bouton dédié dans l'interface de caisse permet d'initier un paiement ou une annulation.

Important : cette méthode ne permet pas l\'impression des tickets directement sur le terminal Yavin.

Pour configurer l'intégration :

- Rendez-vous dans votre interface administrateur Yavin : <https://my.yavin.com>
- Récupérez votre clé secrète et l\'identifiant de votre terminal (Menu Réglages \> À propos \> Numéro de série)
- Saisissez ces informations en page **Config \> Options générales \> Méthodes de Paiements**
- Dans l'interface Yavin, configurez le Webhook :\
  `https://caisse.enregistreuse.fr/workers/NIPYavin.php`

## Intégration directe sur le terminal Yavin

Vous pouvez également installer notre application directement sur votre terminal Yavin depuis le store intégré.

Cette méthode ne nécessite aucune configuration supplémentaire.

Pour obtenir votre terminal, rendez-vous sur : [www.yavin.com](https://yavin.com/?utm_source=caisseenregistreuse)

[Documentation logiciel de caisse](/Yavin/)\
[![Licence Creative Commons](images/34101c8bb1c1253f61bed847b98016c2c0f519af.png)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener mt-4"} Ce document est mis à disposition selon les termes de la [licence Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener"} .
