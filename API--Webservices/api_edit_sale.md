# Modifier une vente enregistrée dans le logiciel

Vous pouvez modifier une commande tant qu'elle n'est pas validée.

Une fois validée, il est uniquement possible d'enregistrer le ou les paiements de la commande via le champ "payment".

## POST /workers/editOrder.php

Envoyez une commande complète : articles, client, mode de paiement, livraison, etc.

### Paramètres POST

| Nom | Type | Obligatoire | Description |
|----|----|----|----|
| `shopID` | string | Oui | Votre identifiant de boutique (SHOPID) |
| `key` | string | Oui | Votre Token (APIKEY) |
| `orderID` | int | Oui | L'identifiant de la commande à modifier |
| `idUser` | int | Non | Identifiant d'utilisateur. Si non précisé, le logiciel crée un compte utilisateur avec le login "webservice" s'il n'existe pas déjà, et l'utilise. |
| `payment` | int | Oui | -2 = Non payée, non validée ; -1 = Non payée, validée ; un identifiant de mode de paiement pour indiquer un paiement (peut être un identifiant d'un mode de remboursement) |
| `paymentAmount` | int | Non | Le montant payé, si "payment" indique un mode de paiement (si absent, le paiement est considéré comptant) |
| `idClient` | int | Non | Identifiant du client existant pour l'affecter à la commande |
| `client` | array | Non | Compte client à créer pour l'affecter à la commande\* |
| `idtable` | int | Non | Identifiant de la table pour l'affecter à la commande |
| `idcaisse` | int | Non | Identifiant de la caisse pour l'affecter à la commande |
| `numcouverts` | int | Non | Nombre de couverts servis à la table |
| `publicComment` | string | Non | Commentaire adossé à la commande (public) |
| `privateComment` | string | Non | Commentaire adossé à la commande (privé) |
| `pagerNum` | int | Non | Numéro de bippeur |
| `deliveryMethod` | int | Non | Méthode de livraison\* |
| `itemsList` | array | Oui | Numéro de bippeur |

### Informations complémentaires

#### Créer un nouveau client dans la même requête

Si le client n'existe pas, vous pouvez le créer avec les champs suivants (à envoyer directement en POST) :

    client[nom]=[nom]
    client[prenom]=[Prénom]
    client[email]=[Email]
    client[telephone]=[nom]
    client[adresseligne1]=[Adresse ligne 1]
    client[adresseligne2]=[Adresse ligne 2]
    client[commentaireadresse]=[nom]
    client[codepostal]=[Code postal]
    client[ville]=[Ville]
    client[pays]=FR
    client[numtva]=[Numéro TVA]
    client[rcs]=[Numéro RC]
    client[codeBarre]=[Code barre]
    client[telephone2]=[Téléphone secondaire]
    client[lat]=[latitude]
    client[lng]=[longitude]

#### Méthode de livraison

Le champ deliveryMethod peut avoir des valeurs allant de 0 à 6 :

| Valeur | Signification     |
|--------|-------------------|
| 0      | À emporter        |
| 1      | À livrer          |
| 2      | Sur place         |
| 3      | Service au volant |
| 4      | Vente au comptoir |
| 5      | Point relai       |
| 6      | À expédier        |

#### itemsList\[\] ? Structure

Le champ itemsList est un tableau de chaines de caractères, chaque élément pouvant être de l'un des types suivants:

- `[idArticle]` ? ajoute un article (quantité 1)
- `[idArticle]_[quantite]` ? préciser la quantité
- `[idArticle]_[quantite]_[titre personnalisé]_[prix personnalisé]` ? forcer le titre et le prix
- `[idArticle]_[quantite]_[titre]_[prix]_[idDéclinaison1]_[idDéclinaison2]_[idDéclinaison3]_[idDéclinaison4]_[idDéclinaison5]` ? ajouter jusqu'à 5 déclinaisons
- *Vente libre en rayon* : `-[idRayon]_[prix]_[titre]` ? crée une ligne libre rattachée au rayon
- *Vente libre* : `Free_[prix]_[titre]` ? crée une ligne libre

Rappel : si idUser est omis, le logiciel utilise/crée automatiquement un utilisateur ?webservice?.

### Exemples JavaScript

#### Ajouter des articles à une commande existante non validée

    async function recordSaleWithExistingClient(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        orderID: 123456,
        payment: -1
      });
      body.append("itemsList[]", "Free_12.99_Item");
      body.append("itemsList[]", "Free_9.99_Other item");

      const res = await fetch("https://kash.click/workers/editOrder.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

#### Associer un client à une commande existante non validée

    async function recordSaleWithExistingClient(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        payment: -2,
        orderID: 123456,
        idClient: 123
      });

      const res = await fetch("https://kash.click/workers/editOrder.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

#### Enregistrer un paiement pour une commande

    async function recordSaleWithNewClient(){
      const body = new URLSearchParams({
        shopID: SHOPID,
        key: APIKEY,
        orderID: 123456,
        payment: 123456
      });

      const res = await fetch("https://kash.click/workers/editOrder.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

### Réponse JSON attendue

#### Commande validée, non payée

    {
      "success": true,
      "orderID":17724460,
      "paymentLink":"A link the client can use to pay the order",
      "invoice":"URL of the PDF invoice"
    }

#### Commande non validée, non payée

    {
      "success": true,
      "orderID":17724461,
      "paymentLink":"A link the client can use to pay the order",
      "quote":"URL of the PDF qduote"
    }

#### Commande validée, payée

    {
      "success": true,
      "orderID":17724461,
      "invoice":"URL of the PDF qduote"
    }

#### Echec

    {
      "success": false,
      "result": "Error message"
    }

