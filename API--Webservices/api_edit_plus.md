# Gestion des articles

Ajoutez, modifiez, ou supprimez des articles

## Ajouter un Article

### POST https://kash.click/workers/addPlu.php

Ajouter un nouvel article à votre catalogue

### Paramètres POST

| Nom                     | Obligatoire | Description                        |
|-------------------------|-------------|------------------------------------|
| `shopID`                | Oui         | Identifiant de votre établissement |
| `key`                   | Oui         | Votre clé pour l'API               |
| `data[title]`           | Oui         | Intitulé (requis)                  |
| `data[shortTitle]`      | Non         | Nom de la boutique                 |
| `data[description]`     | Non         | Description                        |
| `data[buyingPrice]`     | Non         | Prix d'achat                       |
| `data[price]`           | Non         | Prix de vente                      |
| `data[calories]`        | Non         | Calories                           |
| `data[weight]`          | Non         | Poids                              |
| `data[unitID]`          | Non         | ID unité                           |
| `data[variationID0]`    | Non         | ID déclinaison 0                   |
| `data[variationID1]`    | Non         | ID déclinaison 1                   |
| `data[variationID2]`    | Non         | ID déclinaison 2                   |
| `data[variationID3]`    | Non         | ID déclinaison 3                   |
| `data[variationID4]`    | Non         | ID déclinaison 4                   |
| `data[deptID]`          | Non         | ID du rayon                        |
| `data[supplierID]`      | Non         | ID du fournisseur                  |
| `data[vatID]`           | Non         | ID du taux de TVA                  |
| `data[eatinvatID]`      | Non         | ID du taux de TVA sur place        |
| `data[discountID]`      | Non         | ID de la réduction                 |
| `data[barcode]`         | Non         | Code barre                         |
| `data[stock]`           | Non         | Quantité en stock                  |
| `data[stockAlert]`      | Non         | Alerte quantité                    |
| `data[consumptionDate]` | Non         | Date limite de consommation        |
| `data[shopHide]`        | Non         | Masquer de la boutique             |
| `data[keyboardHide]`    | Non         | Masquer de l'interface de vente    |
| `data[needPrepa]`       | Non         | Lieu de préparation                |
| `data[prepaLength]`     | Non         | Durée de préparation (secondes)    |
| `data[position]`        | Non         | Position (sur l'interface)         |
| `data[activityCode]`    | Non         | Code comptable d'activité          |
| `data[internalID]`      | Non         | Identifiant libre                  |

## Editer un Article

### POST https://kash.click/workers/editPlu.php

Modifier un article de votre catalogue

### Paramètres POST

| Nom                     | Obligatoire | Description                        |
|-------------------------|-------------|------------------------------------|
| `shopID`                | Oui         | Identifiant de votre établissement |
| `key`                   | Oui         | Votre clé pour l'API               |
| `id`                    | Oui         | Identifiant de l'Article           |
| `data[title]`           | Non         | Intitulé (requis)                  |
| `data[shortTitle]`      | Non         | Nom de la boutique                 |
| `data[description]`     | Non         | Description                        |
| `data[buyingPrice]`     | Non         | Prix d'achat                       |
| `data[price]`           | Non         | Prix de vente                      |
| `data[calories]`        | Non         | Calories                           |
| `data[weight]`          | Non         | Poids                              |
| `data[unitID]`          | Non         | ID unité                           |
| `data[variationID0]`    | Non         | ID déclinaison 0                   |
| `data[variationID1]`    | Non         | ID déclinaison 1                   |
| `data[variationID2]`    | Non         | ID déclinaison 2                   |
| `data[variationID3]`    | Non         | ID déclinaison 3                   |
| `data[variationID4]`    | Non         | ID déclinaison 4                   |
| `data[deptID]`          | Non         | ID du rayon                        |
| `data[supplierID]`      | Non         | ID du fournisseur                  |
| `data[vatID]`           | Non         | ID du taux de TVA                  |
| `data[eatinvatID]`      | Non         | ID du taux de TVA sur place        |
| `data[discountID]`      | Non         | ID de la réduction                 |
| `data[barcode]`         | Non         | Code barre                         |
| `data[stock]`           | Non         | Quantité en stock                  |
| `data[stockAlert]`      | Non         | Alerte quantité                    |
| `data[consumptionDate]` | Non         | Date limite de consommation        |
| `data[shopHide]`        | Non         | Masquer de la boutique             |
| `data[keyboardHide]`    | Non         | Masquer de l'interface de vente    |
| `data[needPrepa]`       | Non         | Lieu de préparation                |
| `data[prepaLength]`     | Non         | Durée de préparation (secondes)    |
| `data[position]`        | Non         | Position (sur l'interface)         |
| `data[activityCode]`    | Non         | Code comptable d'activité          |
| `data[internalID]`      | Non         | Identifiant libre                  |

## Supprimer un Article

### POST https://kash.click/workers/delPlu.php

Supprimer un article de votre catalogue

### Paramètres POST

| Nom      | Obligatoire | Description                        |
|----------|-------------|------------------------------------|
| `shopID` | Oui         | Identifiant de votre établissement |
| `key`    | Oui         | Votre clé pour l'API               |
| `id`     | Oui         | Identifiant de l'Article           |

#### Exemple JavaScript

    async function editPlu(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        id: 123,
        'data[title]': 'New title',
        'data[price]': 2.2
      });

      const res = await fetch("https://kash.click/workers/editPlu.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

