# Connectez Claude avec caisse.enregistreuse.fr

Ce module vous permet de connecter Claude à votre logiciel de caisse, et de donner accès à Claude à vos données de ventes, ainsi que toutes les autres données, et la capacité d'enregistrer des ventes dans le logiciel

Ce module est actuellement en version beta. Compatible uniquement sur PC ou Mac.

## Prérequis

Node.js : <a href="https://nodejs.org/fr/download" rel="nofollow">Téléchargez et installez Node.js</a>

Claude Desktop : <a href="https://www.claude.com/download" rel="nofollow">Téléchargez et installez Claude Desktop</a>

## Installation

### Installation minimale

Editez votre fichier de configuration claude_desktop_config.json

Sous Windows

    %APPDATA%\Claude\claude_desktop_config.json

Sous Mac OS

    ~/Library/Application Support/Claude/claude_desktop_config.json

Renseignez le fichier de configuration suivant après avoir injecté votre codes d'accès webapp

    {
      "mcpServers": {
        "caisse": {
          "command": "npx",
          "args": [
            "caisse-enregistreuse-mcp-server",
            "--shopid=[replaceWithYourSHOPID]",
            "--apikey=[replaceWithYourAPIKEY]"
          ]
        }
      }
    }

### Installation pas à pas

- Créez un dossier d'installation
- Ouvrez un terminal dans ce dossier, avc les privilèges administrateur
- Installez le module caisse.enregistreuse_mcp

<!-- -->

    npx caisse-enregistreuse-mcp-server --shopid=12345 --apikey=abcdef123456

Peut également être executé pas à pas

    git clone https://github.com/paracetamol951/caisse-enregistreuse-mcp-server.git
    cd caisse-enregistreuse-mcp-server
    npm install
    npm run build
    // tester le lancement (optionnel)
    npm run start:stdio

Lorsque l'installation est terminée, le fichier claude_desktop_config.json devra contenir cette configuration

    {
      "mcpServers": {
        "caisse": {
          "command": "node",
          "args": [
            "[installFolder]\\caisse-enregistreuse-mcp-server\\build\\stdio.js"
          ],
          "cwd": "[installFolder]\\caisse-enregistreuse-mcp-server",
          "env": {
            "APIKEY": "[replaceWithYourAPIKEY]",
            "SHOPID": "[replaceWithYourSHOPID]"
          }
        }
      }
    }

[Serveur MCP](/mcp.md)

