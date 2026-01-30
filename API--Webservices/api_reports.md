# Télécharger vos rapports

Téléchargez vos rapports quotidiens au format HTML, PDF, XLS, CSV...

### GET /workers/getSales.php

**URL de base :** `https://caisse.enregistreuse.fr/workers/getSales.php`

#### Paramètres

| Nom | Type | Obligatoire | Description |
|----|----|----|----|
| `idboutique` | string | Oui | Identifiant de compte boutique (SHOPID) |
| `key` | string | Oui | Votre token (APIKEY) |
| `d` | int | Non | Jour (si non précisé, la veille est utilisée) |
| `m` | int | Non | Mois |
| `y` | int | Non | Année |
| `formatExport` | string | Oui | Std (rapport HTML), PDF, XLS, CSV, frafec (FEC), saft |

#### Exemples JavaScript

    // Aide pour construire une URL GET
    function buildUrl(path, params){
      const qs = new URLSearchParams(params);
      return `${path}?${qs.toString()}`;
    }

    const SHOPID = "[SHOPID]";
    const APIKEY = "[APIKEY]";

    // 1) Export CSV pour date précise
    const urlCsv = buildUrl("https://caisse.enregistreuse.fr/workers/getSales.php", {
      idboutique: SHOPID,
      key: APIKEY,
      d: 16, m: 10, y: 2025,
      formatExport: "CSV"
    });
    fetch(urlCsv).then(r=>r.text()).then(csv=>console.log(csv));

    // 2) Rapport HTML (Std) pour la veille (sans date)
    const urlStd = buildUrl("https://caisse.enregistreuse.fr/workers/getSales.php", {
      idboutique: SHOPID,
      key: APIKEY,
      formatExport: "Std"
    });
    fetch(urlStd).then(r=>r.text()).then(html=>{
      document.getElementById("rapport").innerHTML = html;
    });

    // 3) Rapport PDF (Blob)
    const urlPdf = buildUrl("https://caisse.enregistreuse.fr/workers/getSales.php", {
      idboutique: SHOPID,
      key: APIKEY,
      d: 16, m: 10, y: 2025,
      formatExport: "PDF"
    });
    fetch(urlPdf).then(r=>r.blob()).then(pdf=>{
      const a = document.createElement("a");
      a.href = URL.createObjectURL(pdf);
      a.download = "rapport-ventes.pdf";
      a.click();
    });

