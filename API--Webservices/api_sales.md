# Télécharger vos ventes

Téléchargez la liste de vos commandes enregistrées

### GET /workers/getOrders.php

**URL de base :** `https://caisse.enregistreuse.fr/workers/getOrders.php`

#### Paramètres

  Nom                      Type                    Obligatoire   Description
  ------------------------ ----------------------- ------------- -------------------------------------------------------------------------
  `idboutique`             string                  Oui           Identifiant de compte boutique (SHOPID)
  `key`                    string                  Oui           Votre token (APIKEY)
  `validatedOrders`        bool                    Non           Commandes / Devis
  `from_date_ISO8601`      string (ISO8601 date)   Non           Period start
  `to_date_ISO8601`        string (ISO8601 date)   Non           Period end
  `filterDeliveryMethod`   int \[0\...6\]          Non           If provided, only orders of the specified delivery method will be shown

#### Exemples JavaScript

    function buildUrl(path, params){
      const qs = new URLSearchParams(params);
      return `${path}?${qs.toString()}`;
    }

    const SHOPID = "[SHOPID]";
    const APIKEY = "[APIKEY]";

    // 1) Export des commandes
    const urlCsv = buildUrl("https://caisse.enregistreuse.fr/workers/getSales.php", {
      idboutique: SHOPID,
      key: APIKEY,
      from_date_ISO8601: '2025-10-26T00:00:00Z', 
      to_date_ISO8601: '2025-10-26T23:59:59Z'
    });
    fetch(urlCsv).then(r=>r.text()).then(csv=>console.log(csv));

