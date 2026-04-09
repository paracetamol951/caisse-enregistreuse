# Gestion des taux de TVA

Ajoutez, modifiez, ou supprimez des taux de TVA

## Ajouter un taux de TVA

### POST https://kash.click/workers/addVat.php

Ajouter une nouvelle TVA à votre configuration

### Paramètres POST

| Nom                       | Obligatoire | Description                        |
|---------------------------|-------------|------------------------------------|
| `shopID`                  | Oui         | Identifiant de votre établissement |
| `key`                     | Oui         | Votre clé pour l'API               |
| `data[title]`             | Oui         | Intitulé (requis)                  |
| `data[accountingChapter]` | Non         | Chapitre comptable                 |
| `data[rate]`              | Oui         | Taux (requis)                      |
| `data[legal]`             | Non         | Mention légale                     |

## Modifier un taux de TVA

### POST https://kash.click/workers/editVat.php

Modifier une TVA existante

### Paramètres POST

| Nom                       | Obligatoire | Description                        |
|---------------------------|-------------|------------------------------------|
| `shopID`                  | Oui         | Identifiant de votre établissement |
| `key`                     | Oui         | Votre clé pour l'API               |
| `id`                      | Oui         | Identifiant du VAT rate            |
| `data[title]`             | Non         | Intitulé (requis)                  |
| `data[accountingChapter]` | Non         | Chapitre comptable                 |
| `data[rate]`              | Non         | Taux (requis)                      |
| `data[legal]`             | Non         | Mention légale                     |

## Effacer un taux de TVA

### POST https://kash.click/workers/delVat.php

Supprimer une TVA existante

### Paramètres POST

| Nom      | Obligatoire | Description                        |
|----------|-------------|------------------------------------|
| `shopID` | Oui         | Identifiant de votre établissement |
| `key`    | Oui         | Votre clé pour l'API               |
| `id`     | Oui         | Identifiant du VAT rate            |

#### Exemple JavaScript

    async function editVAT(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        id: 123,
        'data[title]': '20% VAT',
        'data[rate]': 20
      });

      const res = await fetch("https://kash.click/workers/editVat.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

