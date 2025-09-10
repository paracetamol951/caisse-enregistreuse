## Inalterabilite des donn�es

La page Inalt�rabilit� permet � l\'utilisateur de v�rifier l\'int�grit� des donn�es qu\'on lui a confi�es.\
Dans cette page il sera possible de v�rifier si les donn�es qui ont �t� transmises sont bien conformes et inalt�r�es en utilisant la pr�sence d\'une cha�ne cryptographique dont la valeur est indiqu�e pour chaque commande dans les rapports que le logiciel g�n�re.\
\

### Sceau cryptographique

Dans cette page un premier onglet intitul� "Sceau cryptographique" permet de v�rifier un sceau cryptographique particulier. Ceci permet de s'assurer que le m�canisme de sceau correspond bien � la documentation.\
\

### Chaine cryptographique

Un second onglet intitul� cha�ne cryptographique permet de v�rifier la cha�ne des sceaux cryptographiques depuis la premi�re commande jusqu\'� la derni�re enregistr�e.\
La derni�re colonne du tableau affich� indique si le sceau cryptographique enregistr� en base de donn�es correspond bien � la v�rification faite � l\'aide du calcul dynamique du sceau (en se basant sur le sceau de la commande pr�c�dente, lui-m�me v�rifi�).\
Si un seul prix, m�thode de livraison, date de valeur, ou une seule donn�e de vente d'une seule commande est modifi�e apr�s l'apposition du sceau cryptographique, c'est toute la cha�ne qui s'en trouve invalid�e. Ceci permet ainsi de garantir l'intangibilit� des donn�es issues de ce logiciel de caisse.

[Documentation logiciel de caisse](/)\
