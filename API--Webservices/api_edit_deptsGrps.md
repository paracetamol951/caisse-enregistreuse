# Gestion des groupes de rayons

Ajoutez, modifiez, ou supprimez des groupes de rayons

## Ajouter un Groupe de rayons

### POST https://kash.click/workers/addGrpDept.php

Ajouter un nouveau groupe de rayon à votre catalogue

### Paramètres POST

| Nom | Obligatoire | Description |
|----|----|----|
| `shopID` | Oui | Identifiant de votre établissement |
| `key` | Oui | Votre clé pour l'API |
| `data[title]` | Oui | Intitulé (requis) |
| `data[position]` | Non | Position (sur l'interface) |
| `data[accountingChapter]` | Non | Chapitre comptable |
| `data[accountingChapterComplement]` | Non | Complément de chapitre comptable |

## Editer un Groupe de rayons

### POST https://kash.click/workers/editGrpDept.php

Modifier un groupe de rayon de votre catalogue

### Paramètres POST

| Nom | Obligatoire | Description |
|----|----|----|
| `shopID` | Oui | Identifiant de votre établissement |
| `key` | Oui | Votre clé pour l'API |
| `id` | Oui | Identifiant du Groupes de rayons |
| `data[title]` | Non | Intitulé (requis) |
| `data[position]` | Non | Position (sur l'interface) |
| `data[accountingChapter]` | Non | Chapitre comptable |
| `data[accountingChapterComplement]` | Non | Complément de chapitre comptable |

## Supprimer un Groupe de rayons

### POST https://kash.click/workers/delGrpDept.php

Supprimer un groupe de rayon de votre catalogue

### Paramètres POST

| Nom      | Obligatoire | Description                        |
|----------|-------------|------------------------------------|
| `shopID` | Oui         | Identifiant de votre établissement |
| `key`    | Oui         | Votre clé pour l'API               |
| `id`     | Oui         | Identifiant du Groupes de rayons   |

#### Exemple JavaScript

    async function editGrpDept(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        id: 123,
        'data[title]': 'New title'
      });

      const res = await fetch("https://kash.click/workers/editGrpDept.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

