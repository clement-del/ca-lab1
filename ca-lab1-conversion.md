[Accueil](README.md)



Personaliser le parcours de conversion et la relance sur panier abandonné
=========================================================================


Nous allons maintenant personaliser le parcours de conversion via le moteur d'experience client de la RTCDP. On l'appelle Profile Orchestration (anciennement Journey Orchestration). Dans notre interface de demo il se nomme Journey Optimizer. 

L'objectif de notre parcours client est double : 

- Recibler les utilisateurs du site Luma qui ont abandonné le process d'achat.
- Envoyer un message de confirmation aux utilisateurs qui ont confirmé leurs commandes.


--- 

## L'interface de Profile Orchestration

Cliquez sur les 9 points en haut à droite de l'interface et sur le lien _Journey Optimizer_ du menu déroulant

![image](https://user-images.githubusercontent.com/40355195/216600072-bdbc3a9e-e702-4d77-832f-5f2c07de1f3c.png)


Vous êtes maintenant dans le moteur d'orchestration de la RTCDP. 
Nous pouvons accéder au parcours directement depuis la page d'accueil ou alors en cliquant sur le lien _Parcours_ situé dans le menu de gauche.

---

## Le canevas de Parcours
Le canevas de parcours client est le point central de création d'expérience client en temps réel. L'interface vous permet de drag & drop 3 types d'activités : 
- des évènements: Ce sont les actions utilisateurs (ou générées par un système tiers) qui arrivent en temps réel dans la CDP, et sur lesquels vous souhaitez interagir. 
- des activités d'orchestrations:  utile pour filter et temporiser les clients qui entrent dans votre parcours.
- des actions: nécessaires pour comuniquer avec vos clients et votre écosystème d'entreprise. 


![image](https://user-images.githubusercontent.com/40355195/216953101-53853c4b-a710-45e6-826d-c8351ccbe258.png)


Le parcours a été prédéfini pour ce lab. L'évènement entrant s'active automatiquement lorsqu'un utilisateur du site Luma clique sur le bouton _Proceed_. Cet évènement contient un ensemble de donnée telle que le contenu du panier et les identifiants clients.
Un deuxième évènement intitulé _LumaPurchaseEvent_ est lui déclenché lorsque le client complète l'acte d'achat. Lorsqu'il est activé, on invoque Adobe Campaign, via l'action _OrderConfirmation_ pour envoyer le récapitulatif de la commande par email. 


On va également pouvoir tirer profit de la non réception d'un évènement pour recibler nos contact qui sont entrés dans le parcours avec une communication appropriée. En effet le chemin inférieur de l'évènement _LumaPurchaseEvent_ se déclenchera automatiquement au bout d'une période d'inactivité donnée (configurée ici à 20 secondes pour ce lab), permettant de router nos clients vers un chemin alternatif. 

---

## La personalisation de messages avec Adobe Campaign 

Afin de réengager nos clients qui n'ont pas terminé le process d'achat, nous allons utiliser une activité d'action. Celle-ci va nous permettre de communiquer instantanément avec la brique transactionnelle d'Adobe Campaign pour envoyer un message invitant le client à retourner sur le site web.

- Selectioner l'activité _CampaignCartAbandonment_ dans le menu Activités
- Glissez Dépossez la dans le chemin inférieur du parcours client pour qu'elle soit relié à l'évènement précèdent
- Dans le champ _Email_, cliquer sur le crayon puis sélectionner _ LumaCheckoutEvent -> demosystem4 -> identification -> core -> Email_ puis cliquez sur _OK_
- Dans le champ _Name_, cliquer sur le crayon puis taper _first_ pour filtrer les attributs et sélectionner le premier attribut _firstName_ puis cliquez sur _OK_
- Reliez l'event _LumaPurchaseEvent1_ à la transition de l'activité _CampaignCartAbandonment_

![Conversion01](https://user-images.githubusercontent.com/40355195/216963232-a9fcb13a-65bf-4fd6-b9d6-973322b0987a.gif)

--- 

## Tester votre parcours
Il est maintenant temps de tester votre parcours ! 
- Dans le canevas activez le _test mode_, retournez sur le site web et ajoutez un article dans votre panier et cliquez sur le bout _Shopping Cart_
en haut à droite de l'interface. cliquez sur le bouton _Checkout_ puis _Proceed_. 
- Retournez dans Profile Orchestration et visualisez l'avance de votre utilisateur dans le parcours client. Au bout d'une période d'inactivité donné (configurée à 10 secondes dans ce lab), l'utilisateur est considéré comme ayant abandonné le process d'achat et l'email que vous avez configuré au préalable est envoyé avec un lien pour reprendre le panier. 
- Allez dans la [webmail]([url](https://campaignfr.adobedemo.com/webmail)) et cliquer sur le lien dans le nouvel email reçu, celui ci vous ramène au panier ou vous pouvez ainsi finaliser l'achat en ligne. 

![rushConversion02](https://user-images.githubusercontent.com/40355195/217293720-50b1f970-028f-40f1-939a-18b5ed9dde4c.gif)



Bravo ! Vous avez complété le deuxième chapitre du lab :+1: :sparkles: :tada:, rendez-vous sur à la [prochaine étape](ca-lab1-cross-sell.md) ou retournez à [l'accueil](Readme.md)
