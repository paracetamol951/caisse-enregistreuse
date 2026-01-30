## Inalterabilite des données

La page Inaltérabilité permet à l'utilisateur de vérifier l'intégrité des données qu'on lui a confiées.  
Dans cette page il sera possible de vérifier si les données qui ont été transmises sont bien conformes et inaltérées en utilisant la présence d'une chaîne cryptographique dont la valeur est indiquée pour chaque commande dans les rapports que le logiciel génère.  
  

### Sceau cryptographique

Dans cette page un premier onglet intitulé ?Sceau cryptographique? permet de vérifier un sceau cryptographique particulier. Ceci permet de s'assurer que le mécanisme de sceau correspond bien à la documentation.  
  

### Chaine cryptographique

Un second onglet intitulé chaîne cryptographique permet de vérifier la chaîne des sceaux cryptographiques depuis la première commande jusqu'à la dernière enregistrée.  
La dernière colonne du tableau affiché indique si le sceau cryptographique enregistré en base de données correspond bien à la vérification faite à l'aide du calcul dynamique du sceau (en se basant sur le sceau de la commande précédente, lui-même vérifié).  
Si un seul prix, méthode de livraison, date de valeur, ou une seule donnée de vente d'une seule commande est modifiée après l'apposition du sceau cryptographique, c'est toute la chaîne qui s'en trouve invalidée. Ceci permet ainsi de garantir l'intangibilité des données issues de ce logiciel de caisse.

