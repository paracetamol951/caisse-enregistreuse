# Gestion des rayons

Ajoutez, modifiez, ou supprimez des rayons

## Ajouter un Rayon

### POST https://kash.click/workers/addDept.php

Ajouter un nouveau rayon à votre catalogue

### Paramètres POST

| Nom                  | Obligatoire | Description                        |
|----------------------|-------------|------------------------------------|
| `shopID`             | Oui         | Identifiant de votre établissement |
| `key`                | Oui         | Votre clé pour l'API               |
| `data[title]`        | Oui         | Intitulé (requis)                  |
| `data[shortTitle]`   | Non         | Nom de la boutique                 |
| `data[stock]`        | Non         | Quantité en stock                  |
| `data[vatID]`        | Non         | ID du taux de TVA                  |
| `data[eatinvatID]`   | Non         | ID du taux de TVA sur place        |
| `data[discountID]`   | Non         | ID de la réduction                 |
| `data[price]`        | Non         | Prix de vente                      |
| `data[keyboardHide]` | Non         | Masquer de l'interface de vente    |
| `data[shopHide]`     | Non         | Masquer de la boutique             |
| `data[position]`     | Non         | Position (sur l'interface)         |
| `data[deptGroupID]`  | Non         | ID du Groupe de rayon              |
| `data[unitID]`       | Non         | ID unité                           |
| `data[needPrepa]`    | Non         | Lieu de préparation du rayon       |
| `data[variationID0]` | Non         | ID déclinaison 0                   |
| `data[variationID1]` | Non         | ID déclinaison 1                   |
| `data[variationID2]` | Non         | ID déclinaison 2                   |
| `data[variationID3]` | Non         | ID déclinaison 3                   |
| `data[variationID4]` | Non         | ID déclinaison 4                   |
| `data[activityCode]` | Non         | Code comptable d'activité          |

## Editer un Rayon

### POST https://kash.click/workers/editDept.php

Modifier un rayon de votre catalogue

### Paramètres POST

| Nom                  | Obligatoire | Description                        |
|----------------------|-------------|------------------------------------|
| `shopID`             | Oui         | Identifiant de votre établissement |
| `key`                | Oui         | Votre clé pour l'API               |
| `id`                 | Oui         | Identifiant du Rayon               |
| `data[title]`        | Non         | Intitulé (requis)                  |
| `data[shortTitle]`   | Non         | Nom de la boutique                 |
| `data[stock]`        | Non         | Quantité en stock                  |
| `data[vatID]`        | Non         | ID du taux de TVA                  |
| `data[eatinvatID]`   | Non         | ID du taux de TVA sur place        |
| `data[discountID]`   | Non         | ID de la réduction                 |
| `data[price]`        | Non         | Prix de vente                      |
| `data[keyboardHide]` | Non         | Masquer de l'interface de vente    |
| `data[shopHide]`     | Non         | Masquer de la boutique             |
| `data[position]`     | Non         | Position (sur l'interface)         |
| `data[deptGroupID]`  | Non         | ID du Groupe de rayon              |
| `data[unitID]`       | Non         | ID unité                           |
| `data[needPrepa]`    | Non         | Lieu de préparation du rayon       |
| `data[variationID0]` | Non         | ID déclinaison 0                   |
| `data[variationID1]` | Non         | ID déclinaison 1                   |
| `data[variationID2]` | Non         | ID déclinaison 2                   |
| `data[variationID3]` | Non         | ID déclinaison 3                   |
| `data[variationID4]` | Non         | ID déclinaison 4                   |
| `data[activityCode]` | Non         | Code comptable d'activité          |

## Supprimer un Rayon

### POST https://kash.click/workers/delDept.php

Supprimer un rayon de votre catalogue

### Paramètres POST

| Nom      | Obligatoire | Description                        |
|----------|-------------|------------------------------------|
| `shopID` | Oui         | Identifiant de votre établissement |
| `key`    | Oui         | Votre clé pour l'API               |
| `id`     | Oui         | Identifiant du Rayon               |

#### Exemple JavaScript

    async function editDept(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        id: 123,
        'data[title]': 'New title'
      });

      const res = await fetch("https://kash.click/workers/editDept.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

