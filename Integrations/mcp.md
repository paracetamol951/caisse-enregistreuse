# Serveur MCP

Le serveur MCP est un point d\'accès programmatique au logiciel, qui communique au système appelant les différents outils disponibles et la manière de les appeler.

Il permet une connectivité avec différents modèles d\'intelligence artificielle (ChatGPT, Claude, \...) et différents outils d\'automatisation (n8n, \...)

Le serveur MCP est disponible à l\'adresse <https://mcp.kash.click/mcp>

::: iframe
# Une erreur s\'est produite. {#une-erreur-sest-produite. .message}

Impossible d\'exécuter JavaScript.
:::

## Fonctionnalités clés {#fonctionnalités-clés .mt-4}

- Ventes : enregistrer des ventes dans le logiciel
- Accéder à votre liste complète de ventes
- Accès aux données : liste des produits, départements, groupes de départements, clients, livraisons, paiements, utilisateurs, etc.

Ce module est open source, et le code source est disponible sur GitHub :\
[GitHub MCP repository](https://github.com/paracetamol951/caisse-enregistreuse-mcp-server#){rel="nofollow"}

## Exemples de requêtes {#exemples-de-requêtes .mt-4}

- "Affiche moi les ventes d\'aujourd\'hui"
- "Enregistre moi une vente de 2 cafés en tabe 84"
- "Comment vont les affaires cette année ?"
- "Pouvez-vous analyser mon historique des ventes de cette année et me faire des recommandations ?"
- "Générez un rapport de caisse pour la semaine."
- "Combien de commandes doivent être livrées ce soir ?"

## Fonctionnalités du connecteur {#datasets}

Le connecteur permet un accès à certaines ressources par le biais de Endpoints

### Endpoints disponibles

  Ressource                  Capacité
  -------------------------- -----------------------------------------
  Vente                      `Enregistre une vente`
  Commandes                  `Consulter vos commandes enregistrées`
  Articles                   `Consulter vos articles`
  Rayons                     `Consulter vos rayons`
  Groupes de rayons          `Consulter vos groupes de rayons`
  Clients                    `Consulter vos rayons`
  Déclinaisons d\'articles   `Consulter vos déclinaisons d'articles`
  Méthodes de livraison      `Consulter vos méthodes de livraison`
  Méthodes de paiement       `Consulter vos méthodes de paiement`
  Caisses                    `Consulter vos caisses`
  Zones de livraison         `Consulter vos zones de livraison`
  Points relais              `Consulter vos points relais`
  Réductions                 `Consulter vos réductions`
  Utilisateurs               `Consulter vos utilisateurs`
  Tables                     `Consulter vos tables`
  Commandes en cours         `Consulter vos commandes en cours`

[Documentation logiciel de caisse](/)\
[![Licence Creative Commons](images/34101c8bb1c1253f61bed847b98016c2c0f519af.png)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener mt-4"} Ce document est mis à disposition selon les termes de la [licence Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener"} .
