# Liste des comptes

Il est possible de lister les comptes liés à une adresse email de manière programmatique, en fournissant un email, et éventuellement le nom du compte

Cet endpoint vous permet d'obtenir l'identifiant de votre compte, afin de demander un mot de passe à usage unique (OTP) qui vous permettra d'obtenir votre clé API.

## 1) Liste des comptes

### 1.1 POST /workers/listShops.php

#### Paramètres POST

| Nom            | Obligatoire | Description                                 |
|----------------|-------------|---------------------------------------------|
| `email`        | Oui         | Adresse email du compte                     |
| `accountTitle` | Non         | Intitulé du compte (nom de l'établissement) |

#### Réponse JSON attendue (succès)

    [{
      "accountTitle": "My Shop",
      "getOPTForAccount": "https://kash.click/workers/getOTPForAccount.php?accountID=123&code=a25d5e4",
      "accountID": "[identifiant de compte 1]"
    },
    {
      "accountTitle": "My other Shop",
      "getOPTForAccount": "https://kash.click/workers/getOTPForAccount.php?accountID=456&code=e5c6548",
      "accountID": "[identifiant de compte 2]"
    }]

#### Exemple JavaScript (fetch)

    const email = "mon.email@example.com";

    fetch("https://kash.click/workers/listShops.php", {
      method: "POST",
      headers: { "Content-Type": "application/x-www-form-urlencoded" },
      body: new URLSearchParams({ email })
    })
      .then(r => r.json())
      .then(data => {
        if (data) {
          console.log("Accounts:", data);
        } else {
          console.error("Auth error", data);
        }
      });

