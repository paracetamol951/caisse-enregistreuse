# Gestion des déclinaisons

Ajoutez, modifiez, ou supprimez des déclinaisons

## Ajouter une déclinaison

### POST https://kash.click/workers/addVariation.php

Ajouter une nouvelle déclinaison à votre catalogue

### Paramètres POST

| Nom           | Obligatoire | Description                        |
|---------------|-------------|------------------------------------|
| `shopID`      | Oui         | Identifiant de votre établissement |
| `key`         | Oui         | Votre clé pour l'API               |
| `data[title]` | Oui         | Nom de la boutique                 |

## Modifier une déclinaison

### POST https://kash.click/workers/editVariation.php

Modifier une déclinaison de votre catalogue

### Paramètres POST

| Nom           | Obligatoire | Description                        |
|---------------|-------------|------------------------------------|
| `shopID`      | Oui         | Identifiant de votre établissement |
| `key`         | Oui         | Votre clé pour l'API               |
| `id`          | Oui         | Identifiant du Déclinaisons        |
| `data[title]` | Non         | Nom de la boutique                 |

## Effacer une déclinaison

### POST https://kash.click/workers/delVariation.php

Supprimer une déclinaison de votre catalogue

### Paramètres POST

| Nom      | Obligatoire | Description                        |
|----------|-------------|------------------------------------|
| `shopID` | Oui         | Identifiant de votre établissement |
| `key`    | Oui         | Votre clé pour l'API               |
| `id`     | Oui         | Identifiant du Déclinaisons        |

#### Exemple JavaScript

    async function editVariation(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        id: 123,
        'data[title]': 'Variation name'
      });

      const res = await fetch("https://kash.click/workers/editVariation.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

