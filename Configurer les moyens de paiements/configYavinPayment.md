## 

# Yavin : Configurer les paiements CB avec un TPE bancaire

Les terminaux Yavin permettent d\'accepter les paiements par carte bancaire : CB, Visa, Mastercard, American Express, avec ou sans contact.\
Vous pouvez utiliser le contrat mon�tique Yavin ou celui de votre banque.

Notre logiciel est compatible avec deux m�thodes d'int�gration Yavin : via Yavin Cloud (1 tablette + 1 terminal) ou directement sur le terminal Yavin.

## Int�gration avec Yavin Cloud

Cette m�thode permet de piloter votre terminal Yavin � distance via Wi-Fi. Le logiciel transmet automatiquement le montant � encaisser au terminal.

Un bouton d�di� dans l'interface de caisse permet d'initier un paiement ou une annulation.

Important : cette m�thode ne permet pas l\'impression des tickets directement sur le terminal Yavin.

Pour configurer l'int�gration :

- Rendez-vous dans votre interface administrateur Yavin : [https://my.yavin.com](https://my.yavin.com){target="_blank"}
- R�cup�rez votre cl� secr�te et l\'identifiant de votre terminal (Menu R�glages \> � propos \> Num�ro de s�rie)
- Saisissez ces informations en page **Config \> Options g�n�rales \> M�thodes de Paiements**
- Dans l'interface Yavin, configurez le Webhook :\
  `https://caisse.enregistreuse.fr/workers/NIPYavin.php`

## Int�gration directe sur le terminal Yavin

Vous pouvez �galement installer notre application directement sur votre terminal Yavin depuis le store int�gr�.

Cette m�thode ne n�cessite aucune configuration suppl�mentaire.

Pour obtenir votre terminal, rendez-vous sur : [www.yavin.com](https://yavin.com/?utm_source=caisseenregistreuse){target="_blank"}

[Inscrivez-vous maintenant](/Yavin/)\
