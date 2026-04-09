# Gestion des choix de déclinaisons

Ajoutez, modifiez, ou supprimez des choix de déclinaisons

## Ajouter un choix de déclinaison

### POST https://kash.click/workers/addVariationItem.php

Ajouter un nouvel item à une déclinaison de votre catalogue

### Paramètres POST

| Nom                 | Obligatoire | Description                        |
|---------------------|-------------|------------------------------------|
| `shopID`            | Oui         | Identifiant de votre établissement |
| `key`               | Oui         | Votre clé pour l'API               |
| `data[idVariation]` | Non         | ID déclinaison                     |
| `data[title]`       | Oui         | Nom de la boutique                 |
| `data[position]`    | Non         | Position (sur l'interface)         |
| `data[deltaPrice]`  | Non         | Modificateur de prix               |
| `data[description]` | Non         | Description                        |
| `data[ending]`      | Non         | Element final                      |
| `data[unavailable]` | Non         | Element désactivé                  |

## Modifier un choix de déclinaison

### POST https://kash.click/workers/editVariationItem.php

Modifier un item de déclinaison de votre catalogue

### Paramètres POST

| Nom                 | Obligatoire | Description                        |
|---------------------|-------------|------------------------------------|
| `shopID`            | Oui         | Identifiant de votre établissement |
| `key`               | Oui         | Votre clé pour l'API               |
| `id`                | Oui         | Identifiant du Déclinaisons item   |
| `data[idVariation]` | Non         | ID déclinaison                     |
| `data[title]`       | Non         | Nom de la boutique                 |
| `data[position]`    | Non         | Position (sur l'interface)         |
| `data[deltaPrice]`  | Non         | Modificateur de prix               |
| `data[description]` | Non         | Description                        |
| `data[ending]`      | Non         | Element final                      |
| `data[unavailable]` | Non         | Element désactivé                  |

## Effacer un choix de déclinaison

### POST https://kash.click/workers/delVariationItem.php

Supprimer une déclinaison de votre catalogue

### Paramètres POST

| Nom      | Obligatoire | Description                        |
|----------|-------------|------------------------------------|
| `shopID` | Oui         | Identifiant de votre établissement |
| `key`    | Oui         | Votre clé pour l'API               |
| `id`     | Oui         | Identifiant du Déclinaisons item   |

#### Exemple JavaScript

    async function editVariation(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        id: 123,
        'data[title]': 'Variation choice name'
      });

      const res = await fetch("https://kash.click/workers/editVariationItem.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

