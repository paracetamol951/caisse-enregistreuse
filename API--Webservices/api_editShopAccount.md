# Modification options de compte boutique

Modifiez la configuration de votre compte boutique.

## Modifier les options de compte boutique

### POST https://kash.click/workers/editShop.php

Options du compte boutique

### Paramètres POST

| Nom | Obligatoire | Description |
|----|----|----|
| `shopID` | Oui | Identifiant de votre établissement |
| `key` | Oui | Votre clé pour l'API |
| `data[shopName]` | Non | Nom de la boutique |
| `data[companyRegistrationNum]` | Non | Numéro de société (RCS) |
| `data[taxRegistrationNum]` | Non | Numéro de TVA |
| `data[adressline1]` | Non | Adresse ligne 1 |
| `data[postCode]` | Non | Code postal |
| `data[city]` | Non | Ville |
| `data[country]` | Non | Pays |
| `data[lat]` | Non | lat |
| `data[lng]` | Non | lng |
| `data[phone]` | Non | Telephone |
| `data[urlwebsite]` | Non | URL de votre site web (externe) |
| `data[defaultAccountingChapter]` | Non | Chapitre comptable par défaut |
| `data[pdffooter]` | Non | Texte de footer des factures PDF |
| `data[receiptHeader]` | Non | Entête des tickets |
| `data[receiptFooter]` | Non | Pied de page des tickets |
| `data[defaultVatID]` | Non | Identifiant du taux de TVA par défaut |
| `data[currency]` | Non | Devise |
| `data[language]` | Non | Langue |
| `data[pricesAreProvidedTaxIncluded]` | Non | 0 = Les prix sont saisis TTC ; 1 = Les prix sont saisis HT |
| `data[paypalAddress]` | Non | Votre adresse email Paypal (pour collecter des paiements) |
| `data[deliv_tablePlan]` | Non | Gestion des tables |
| `data[deliv_takeAway]` | Non | Vente à emporter |
| `data[deliv_drivethru]` | Non | Service au volant |
| `data[deliv_deliver]` | Non | Gestion des livraisons |
| `data[deliv_bar]` | Non | Vente au comptoir |
| `data[deliv_relayDeposit]` | Non | Livraison en point retrait |
| `data[deliv_default]` | Non | Méthode de livraison par défaut |
| `data[receipt_showVat]` | Non | Afficher la TVA sur les tickets |
| `data[receipt_showShopName]` | Non | Afficher le nom de la boutique sur les tickets |
| `data[receipt_showCashbox]` | Non | Afficher le nom de la caisse sur les tickets |
| `data[receipt_showSeller]` | Non | Afficher le nom du vendeur sur les tickets |
| `data[receipt_showClient]` | Non | Afficher le nom du client sur les tickets |
| `data[receipt_showAddress]` | Non | Afficher les coordonnées de la boutique sur les tickets |
| `data[receipt_showCompanyRegistrationNum]` | Non | Afficher le numéro de société de la boutique sur les tickets |
| `data[receipt_showClientSurname]` | Non | Afficher le prénom du client sur les tickets |
| `data[receipt_showClientAddress]` | Non | Afficher l'adresse du client sur les tickets |
| `data[receipt_showClientPhone]` | Non | Afficher le numéro de téléphone du client sur les tickets |
| `data[receipt_showGlobalVat]` | Non | Afficher la TVA générale sur les tickets |
| `data[receipt_showComment]` | Non | Afficher le commentaire sur les tickets |
| `data[receipt_showPricesBeforeTaxes]` | Non | Afficher les prix HT sur les tickets |
| `data[orderRequires_deliveryChoice]` | Non | Le choix de la méthode de livraison est obligatoire pour chaque commande |
| `data[orderRequires_name]` | Non | Le nom du client est obligatoire pour chaque commande |
| `data[orderRequires_surname]` | Non | Le prénom du client est obligatoire pour chaque commande |
| `data[orderRequires_address]` | Non | Adresse du client est obligatoire pour chaque commande |
| `data[orderRequires_email]` | Non | Email client est obligatoire pour chaque commande |
| `data[orderRequires_phone]` | Non | Téléphone client est obligatoire pour chaque commande |
| `data[orderRequires_date]` | Non | Le choix de la date est obligatoire pour chaque commande |
| `data[orderRequires_CompanyRegistrationNum]` | Non | Le numéro de société du client est obligatoire pour chaque commande |
| `data[orderRequires_comment]` | Non | Commentaire obligatoire pour chaque commande |
| `data[enable_stock]` | Non | Activer la gestion des stocks |
| `data[enable_barcodes]` | Non | Activer la gestion des codes barres |
| `data[enable_departments]` | Non | Activer la gestion des rayons |
| `data[enable_departmentsGroups]` | Non | Activer la gestion des groupes de rayons |
| `data[enable_credits]` | Non | Activer la gestion des avoirs |
| `data[enable_webservices]` | Non | Activer les webservices |
| `data[enable_descriptionsForItems]` | Non | Activer les descriptions pour les articles |
| `data[enable_variations]` | Non | Activer la gestion des déclinaisons |
| `data[enable_delivShop]` | Non | Activer les livraisons avec Deliv.shop |
| `data[enable_relayDeposit]` | Non | Activer la gestion des points de retrait |
| `data[enable_descriptionForVariations]` | Non | Activer les descriptions pour les articles |
| `data[enable_dateOfConsumption]` | Non | Activer la gestion des Dates limites de consommation |
| `data[enable_coupons]` | Non | Activer la gestion des coupons |
| `data[enable_weightForItems]` | Non | Activer la gestion des poids d'articles |
| `data[enable_whiteLabel]` | Non | Activer la marque blanche (attention : ne peut pas être désactivé) |
| `data[whiteLabelAdminUserID]` | Non | ID de l'utilisateur administrateur marque blanche |
| `data[isWebShopEnabled]` | Non | Activer la webshop |
| `data[webShopURL]` | Non | URL de la webshop |
| `data[webShopLang]` | Non | Langue de la webshop |
| `data[webShopCol1]` | Non | Couleur de fond 1 |
| `data[webShopCol2]` | Non | Couleur de fond 2 |
| `data[webShopCol3]` | Non | Couleur de fond 3 |
| `data[webShopColT1]` | Non | Couleur de texte 1 |
| `data[webShopColT2]` | Non | Couleur de texte 2 |
| `data[webShopColT3]` | Non | Couleur de texte 3 |
| `data[prestaShopApiKey]` | Non | Clé API Prestashop |
| `data[prestaShopURL]` | Non | URL de votre Prestashop |
| `data[enableYavin]` | Non | Activer la collecte de paiements Yavin |
| `data[yavinSecret]` | Non | Code secret |
| `data[yavinSerial]` | Non | yavinSerial |
| `data[enableVivaWallet]` | Non | Activer la collecte des paiements avec Viva.com |
| `data[vivaWalletMerchant]` | Non | Identifiant de marchant Viva.com |
| `data[vivaAccoundID]` | Non | Identifiant de compte Viva.com |
| `data[whiteLabelManagerSet]` | Non | Si data\[whiteLabelManagerSet\]='fromSecret' alors il est possible de fournir également le paramètre \$data\["whiteLabelManagerSecret"\] pour affecter un manager existant au compte ; Si data\[whiteLabelManagerSet\]='new', alors il est également possible de fournir les paramètres \$data\["whiteLabelData"\]\["nom"\],\$data\["whiteLabelData"\]\["rcs"\],\$data\["whiteLabelData"\]\["vat"\],\$data\["whiteLabelData"\]\["addresseLigne1"\],\$data\["whiteLabelData"\]\["addresseLigne2"\],\$data\["whiteLabelData"\]\["codePostal"\],\$data\["whiteLabelData"\]\["ville"\],\$data\["whiteLabelData"\]\["pays"\],\$data\["whiteLabelData"\]\["telephone"\],\$data\["whiteLabelData"\]\["email"\] |

