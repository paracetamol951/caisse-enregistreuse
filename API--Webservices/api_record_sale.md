# Enregistrer des ventes dans le logiciel

Envoyez une commande complète : articles, client, mode de paiement, livraison, etc.

## POST /workers/webapp.php

Envoyez une commande complète : articles, client, mode de paiement, livraison, etc.

### Paramètres POST

  Nom                Type     Obligatoire   Description
  ------------------ -------- ------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  `idboutique`       string   Oui           Votre identifiant de boutique (SHOPID)
  `key`              string   Oui           Votre Token (APIKEY)
  `idUser`           int      Non           Identifiant d'utilisateur. Si non précisé, le logiciel crée un compte utilisateur avec le login \"webservice\" s'il n'existe pas déjà, et l'utilise.
  `payment`          int      Oui           -2 = Non payée, non validée ; -1 = Non payée, validée ; un identifiant de mode de paiement pour indiquer un paiement (peut être un identifiant d'un mode de remboursement)
  `idClient`         int      Non           Identifiant du client existant pour l'affecter à la commande
  `idtable`          int      Non           Identifiant de la table pour l'affecter à la commande
  `idcaisse`         int      Non           Identifiant de la caisse pour l'affecter à la commande
  `numcouverts`      int      Non           Nombre de couverts servis à la table
  `publicComment`    string   Non           Commentaire adossé à la commande (public)
  `privateComment`   string   Non           Commentaire adossé à la commande (privé)
  `pagerNum`         int      Non           Numéro de bippeur

### Créer un nouveau client dans la même requête

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

#### deliveryMethod

  Valeur   Signification
  -------- -------------------
  0        À emporter
  1        À livrer
  2        Sur place
  3        Service au volant
  4        Vente au comptoir
  5        Point relai
  6        À expédier

#### itemsList\[\] --- Structure

- `[idArticle]` --- ajoute un article (quantité 1)
- `[idArticle]_[quantite]` --- préciser la quantité
- `[idArticle]_[quantite]_[titre personnalisé]_[prix personnalisé]` --- forcer le titre et le prix
- `[idArticle]_[quantite]_[titre]_[prix]_[idDéclinaison1]_[idDéclinaison2]_[idDéclinaison3]_[idDéclinaison4]_[idDéclinaison5]` --- ajouter jusqu'à 5 déclinaisons
- *Vente libre en rayon* : `-[idRayon]_[prix]_[titre]` --- crée une ligne libre rattachée au rayon
- *Vente libre* : `Free_[prix]_[titre]` --- crée une ligne libre

#### Exemple JavaScript --- client existant

    async function recordSaleWithExistingClient(){
      const body = new URLSearchParams({
        idboutique: SHOPID,
        key: APIKEY,
        idUser: 1,
        payment: -1,
        deliveryMethod: 0,
        idClient: 123
      });
      body.append("itemsList[]", "12_2_Pizza 4 fromages_14.50_3_8");
      body.append("itemsList[]", "-5_9.99_Vente libre");

      const res = await fetch("https://caisse.enregistreuse.fr/workers/webapp.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

### Exemple JavaScript --- nouveau client + vente

    async function recordSaleWithNewClient(){
      const body = new URLSearchParams({
        idboutique: SHOPID,
        key: APIKEY,
        payment: 2,
        deliveryMethod: 1
      });
      body.append("client[nom]", "Durand");
      body.append("client[prenom]", "Zoé");
      body.append("client[email]", "zoe.durand@example.com");
      body.append("client[telephone]", "+33 6 12 34 56 78");
      body.append("client[adresseligne1]", "10 rue des Écoles");
      body.append("client[adresseligne2]", "Bât. B");
      body.append("client[commentaireadresse]", "Sonner 2 fois");
      body.append("client[codepostal]", "75005");
      body.append("client[ville]", "Paris");
      body.append("client[pays]", "FR");
      body.append("client[numtva]", "FRXX999999999");
      body.append("client[rcs]", "RCS Paris 123 456 789");
      body.append("client[codeBarre]", "CUST-0001");
      body.append("client[telephone2]", "+33 1 23 45 67 89");
      body.append("client[lat]", "48.848");
      body.append("client[lng]", "2.347");
      body.append("itemsList[]", "42_1_Menu midi_12.90");
      body.append("itemsList[]", "15_3_Canette Cola_2.50");

      const res = await fetch("https://caisse.enregistreuse.fr/workers/webapp.php", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body
      });
      let payload; try{ payload = await res.json(); }catch{ payload = await res.text(); }
      console.log(payload);
    }

Rappel : si idUser est omis, le logiciel utilise/crée automatiquement un utilisateur "webservice".

