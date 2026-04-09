# Gestion des clients

Ajoutez, modifiez, ou supprimez des clients

## Ajouter un compte client

### POST https://kash.click/workers/addClient.php

Ajouter un nouveau client à votre fichier client

### Paramètres POST

| Nom                        | Obligatoire | Description                        |
|----------------------------|-------------|------------------------------------|
| `shopID`                   | Oui         | Identifiant de votre établissement |
| `key`                      | Oui         | Votre clé pour l'API               |
| `data[title]`              | Non         | Civilité                           |
| `data[surname]`            | Non         | Prénom                             |
| `data[name]`               | Non         | Nom de famille                     |
| `data[position]`           | Non         | Position (sur l'interface)         |
| `data[email]`              | Non         | Email                              |
| `data[phone]`              | Non         | Telephone                          |
| `data[addressline1]`       | Non         | Adresse ligne 1                    |
| `data[addressline2]`       | Non         | Adresse ligne 2                    |
| `data[adressComment]`      | Non         | Commentaire adresse                |
| `data[postcode]`           | Non         | Code postal                        |
| `data[city]`               | Non         | Ville                              |
| `data[country]`            | Non         | Pays                               |
| `data[identificationID]`   | Non         | Numéro de pièce d'identité         |
| `data[lat]`                | Non         | lat                                |
| `data[lng]`                | Non         | lng                                |
| `data[commentPrivate]`     | Non         | Note privée                        |
| `data[commentPublic]`      | Non         | Note publique                      |
| `data[registrationNumber]` | Non         | SIRET                              |
| `data[VATnum]`             | Non         | Numéro de TVA                      |
| `data[barcode]`            | Non         | Code barre                         |
| `data[blacklist]`          | Non         | Liste noire                        |
| `data[clientGroupID]`      | Non         | SIRET (14 caractères)              |
| `data[phone2]`             | Non         | Téléphone 2                        |
| `data[birthDate]`          | Non         | Date de naissance (timestamp)      |
| `data[activityCode]`       | Non         | Code comptable                     |

## Editer un compte client

### POST https://kash.click/workers/editClient.php

Modifier un client de votre fichier client

### Paramètres POST

| Nom                        | Obligatoire | Description                        |
|----------------------------|-------------|------------------------------------|
| `shopID`                   | Oui         | Identifiant de votre établissement |
| `key`                      | Oui         | Votre clé pour l'API               |
| `id`                       | Oui         | Identifiant du client              |
| `data[title]`              | Non         | Civilité                           |
| `data[surname]`            | Non         | Prénom                             |
| `data[name]`               | Non         | Nom de famille                     |
| `data[position]`           | Non         | Position (sur l'interface)         |
| `data[email]`              | Non         | Email                              |
| `data[phone]`              | Non         | Telephone                          |
| `data[addressline1]`       | Non         | Adresse ligne 1                    |
| `data[addressline2]`       | Non         | Adresse ligne 2                    |
| `data[adressComment]`      | Non         | Commentaire adresse                |
| `data[postcode]`           | Non         | Code postal                        |
| `data[city]`               | Non         | Ville                              |
| `data[country]`            | Non         | Pays                               |
| `data[identificationID]`   | Non         | Numéro de pièce d'identité         |
| `data[lat]`                | Non         | lat                                |
| `data[lng]`                | Non         | lng                                |
| `data[commentPrivate]`     | Non         | Note privée                        |
| `data[commentPublic]`      | Non         | Note publique                      |
| `data[registrationNumber]` | Non         | SIRET                              |
| `data[VATnum]`             | Non         | Numéro de TVA                      |
| `data[barcode]`            | Non         | Code barre                         |
| `data[blacklist]`          | Non         | Liste noire                        |
| `data[clientGroupID]`      | Non         | SIRET (14 caractères)              |
| `data[phone2]`             | Non         | Téléphone 2                        |
| `data[birthDate]`          | Non         | Date de naissance (timestamp)      |
| `data[activityCode]`       | Non         | Code comptable                     |

## Supprimer un compte client

### POST https://kash.click/workers/delClient.php

Supprimer un client de votre fichier client

### Paramètres POST

| Nom      | Obligatoire | Description                        |
|----------|-------------|------------------------------------|
| `shopID` | Oui         | Identifiant de votre établissement |
| `key`    | Oui         | Votre clé pour l'API               |
| `id`     | Oui         | Identifiant du client              |

#### Exemple JavaScript

    async function editClient(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        id: 123,
        'data[name]': 'Dupond'
      });

      const res = await fetch("https://kash.click/workers/editClient.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

