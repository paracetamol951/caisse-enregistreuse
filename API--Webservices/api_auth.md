# Authentification

L\'accès à l\'API nécessite de fournir votre APIKEY et SHOPID.

Résumé rapide : Obtenez un token (APIKEY) + l'identifiant de boutique (SHOPID), puis utilisez-les pour télécharger vos données ou enregistrer des ventes.

## 1) Obtenir un auth token {#auth}

Deux méthodes :

1.  **Depuis l'interface** : Configuration ? Webservices (le token de votre compte y est affiché).
2.  **Par requête POST** : `https://caisse.enregistreuse.fr/workers/getAuthToken.php`

### 1.1 POST /workers/getAuthToken.php

#### Paramètres POST

- `login` --- le login de votre compte existant
- `password` --- le mot de passe de votre compte existant

#### Réponse JSON attendue (succès)

    {
      "result": "OK",
      "APIKEY": "[votre Token]",
      "SHOPID": "[identifiant de compte boutique]"
    }

#### Exemple JavaScript (fetch)

    const login = "mon.email@example.com";
    const password = "myPassword";

    fetch("https://caisse.enregistreuse.fr/workers/getAuthToken.php", {
      method: "POST",
      headers: { "Content-Type": "application/x-www-form-urlencoded" },
      body: new URLSearchParams({ login, password })
    })
      .then(r => r.json())
      .then(data => {
        if (data.result === "OK") {
          console.log("Token:", data.APIKEY);
          console.log("Shop:", data.SHOPID);
        } else {
          console.error("Auth error", data);
        }
      });

## 2) Avec la clé API, vous pouvez... {#with-key}

- Télécharger vos données de ventes
- Télécharger articles, clients, rayons, etc.
- Enregistrer des ventes

[Documentation logiciel de caisse](/)\
[![Licence Creative Commons](images/34101c8bb1c1253f61bed847b98016c2c0f519af.png)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener mt-4"} Ce document est mis à disposition selon les termes de la [licence Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/){rel="license noopener"} .
