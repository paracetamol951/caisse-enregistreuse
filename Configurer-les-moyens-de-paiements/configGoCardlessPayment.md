# Configurer les paiements par prélèvement avec GoCardless

GoCardless permet de prélever automatiquement vos clients sur leur compte bancaire après signature d'un mandat.

Une fois le mandat signé, plus besoin d'action de la part du client : le paiement est initié directement depuis la caisse.

## Création d'un compte GoCardless

- Rendez-vous sur le site de GoCardless pour créer votre compte professionnel.
- Si vous souhaitez faire des tests, créez un compte bac à sable ici : <https://manage-sandbox.gocardless.com/sign-up>

## Connexion de votre compte GoCardless

1.  Accédez à **Config \> Options générales \> Paiement**.
2.  Activez l'option **Paiement GoCardless**.
3.  Indiquez si vous utilisez un compte bac à sable ou un compte réel.
4.  Cliquez sur le bouton **GoCardless** pour connecter votre compte.

Une fois la connexion réalisée, un bouton GoCardless est automatiquement ajouté à l'interface de vente.

## Encaissement avec GoCardless

Lors de l'encaissement, cliquez sur le bouton GoCardless pour initier un paiement.

Deux cas sont possibles :

- Le client a déjà signé son mandat : le prélèvement est automatique.
- Le client n'a pas encore de mandat : il reçoit un email pour le remplir (2 minutes).

Les notifications de prélèvement sont gérées automatiquement par GoCardless.

En cas d'annulation ou de remboursement, le logiciel annule le prélèvement automatiquement.

## Paiement groupé de créances

Vous pouvez également encaisser plusieurs dettes client en une seule fois :

1.  Rendez-vous sur **Config \> Clients**.
2.  Sélectionnez une créance client, puis choisissez le paiement GoCardless.

Frais : 0.20? + 1% GoCardless + 1% Caisse enregistreuse

  
  
<a href="https://manage.gocardless.com/signup" class="button green">Créer un compte GoCardless</a>  

