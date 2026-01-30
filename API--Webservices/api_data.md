# Télécharger vos données

## Télécharger la liste des articles, rayons, clients, etc

Tous les endpoints suivants acceptent &format=json, &format=csv ou &format=html.

### Endpoints disponibles

| Ressource               | Endpoint                           |
|-------------------------|------------------------------------|
| Articles                | `/workers/getPlus.php`             |
| Rayons                  | `/workers/getDepartments.php`      |
| Groupes de rayons       | `/workers/getDepartmentGroups.php` |
| Clients                 | `/workers/getClients.php`          |
| Déclinaisons d'articles | `/workers/getDeclinaisons.php`     |
| Méthodes de livraison   | `/workers/getLivraisons.php`       |
| Méthodes de paiement    | `/workers/getPaymentModes.php`     |
| Caisses                 | `/workers/getCashbox.php`          |
| Zones de livraison      | `/workers/getDeliveryZones.php`    |
| Points relais           | `/workers/getRelayDeposit.php`     |
| Réductions              | `/workers/getDiscounts.php`        |
| Utilisateurs            | `/workers/getUsers.php`            |
| Tables                  | `/workers/getTables.php`           |
| Commandes en cours      | `/workers/getPending.php`          |

#### Patron d?URL

    https://caisse.enregistreuse.fr/workers/[endpoint].php?idboutique=[SHOPID]&key=[APIKEY]&format=[csv|json|html]

#### Exemples JavaScript

    function buildUrl(path, params){
      const qs = new URLSearchParams(params);
      return `${path}?${qs.toString()}`;
    }

    async function fetchResource(endpoint, format = "json"){
      const url = buildUrl(`https://caisse.enregistreuse.fr/workers/${endpoint}.php`, {
        idboutique: SHOPID,
        key: APIKEY,
        format
      });
      const res = await fetch(url);
      return format === "json" ? res.json() : res.text();
    }

    // 1) Items in JSON
    fetchResource("getPlus", "json").then(data => console.log("Articles:", data));

    // 2) Clients in CSV
    fetchResource("getClients", "csv").then(csv => console.log("Clients (CSV):\n", csv));

    // 3) Depts in HTML (injection)
    fetchResource("getDepartments", "html").then(html => {
      document.getElementById("rayons").innerHTML = html;
    });

