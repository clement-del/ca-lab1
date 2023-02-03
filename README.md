# Lab 1 - Création d'un parcours avec Adobe Campaign augmenté

Adobe Campaign s'utilise conjointement avec Adobe Real Time Customer Data Platform (RTCDP) pour enrichir l'expérience client avec un ensemble de fonctionnalités additionnelles. Vous allez ainsi pouvoir exploiter :

- La collecte de données  en temps réel, au plus proche des utilisateurs et les segmenter à la volée en fonction de leurs comportements online, très utile pour personaliser le contenus sur les propriétés digitales en fonction de leur appétences.
- Un  orchestrateur de parcours client pour réagir en temps réel à des évènements générés par vos utilisateurs, et déterminer le meilleur itinéraire pour vos contacts. 
- Des modèles d'intelligence artificielle pour scorer vos contacts et déterminer leur propension à acheter un produit, ou leur propension à quitter les services de votre marque pour la concurrence. 
- Un vaste catalogue de destination pour activer vos audiences sur les canaux de votre choix: réseaux sociaux, email marketing, search & display, site web, CRM etc..
- Appliquer des règles de gouvernance de la donnée et vous assurer que les données de vos utilisateurs soit uniquement utilisées à bon escient, et éviter tout risque de partage malencontreux vers un tiers, ou une utilisateur de la donnée client qui n'a pas été consentie par votre contact. 


Au cours de ce lab, nous allons utiliser une marque fictive d'équipement sportif - intitulée Luma - pour illustrer ces fonctionnalités au travers d'un parcous client composé de 3 chapitres: 

1: L'acquisition de nouvelles données clients depuis le site web Luma. Grace a la collecte en temps réel, nous allons récolter les interactions des visiteurs, même anonymes, et personnaliser le site web en temps réel en fonction de leurs comportements de navigation. Lorsque un utilisateur crééra son compte, son comportement en tant que visiteur anonyme sera automatiquement rattaché à son profil connu et complétera la vision 360° dans RTCDP et dans Adobe Campaign. 
2: La conversion et l'abandon de panier. En exploitant le moteur d'orchestration, nous allons pouvoir définir des messages personalisés à chacune des étapes du process de paiement en ligne. De l'ajout de produit dans un panier, à la finalisation du paiment, nous pouvons interagir à travers des communication personalisés avec nos futurs clients, et également les recibler si ils ne terminent pas le processus d'achat. Pour le routage des messages, faisons confiance à Adobe Campaign !
3: Le cross sell. Exploitons les capacités d'intelligence artificielle de la RTCDP pour calculer une audience qui sera la plus à même d'acheter un accessoire de sport extérieur au cours des 3 prochaines semaines en nous basant sur l'analyse des données comportementales de nos précèdents clients. Partageons ensuite cette audience à Snapchat et vers Adobe Campaign et peaufiner notre ciblage (règles de pression, gestion de la deliverabilité...) 


des parcours clients complètement individualisé orchestrés en temps réel. Grâce au moteur d'orchestration 1:1 vous allez pouvoir réagir à des évènements directement générés par vos utilisateurs. Par exemple, lorsqu'un prospect ou client interagit avec votre le site web ou l'application mobile de votre marque  (ouverture d'un push, visualisation d'une page produit, contact avec un chatbot..), vous allez pouvoir capter cette interaction et définir un parcours client compsé d'activité, d'autres évènements, de messages et de branches pour définir quelle va etre le meilleur contenu à lui proposer au meilleur moment. 


## Objectifs d'apprentissages
- Visualiser le profil temps réel dans RTCDP
- Naviguer dans le graph d'identité  
- Configurer un parcours client avec un message personalisé 
- Créer un segment utilisant les scores calculés par les services intelligents de RTCDP
- Activer ce segment vers Adobe Campaign et les réseaux sociaux


## Prérequis

- Accès à [RTCDP](https://experience.adobe.com/#/@demosystem4/sname:emea-france-sc/platform/home)
- Accès à la [webmail de demo](https://campaignfr.adobedemo.com/webmail)

Les login & mots de passe vous seront communiqués sur place. 


## Exercices

[Acquisition](./ca-lab1-acquisition.md): Naviguer sur le site internet de demo et générer des données pour ensuite les visualiser dans RTCDP

[Conversion](./ca-lab1-conversion.md): Configurer le message personalisé lors de l'abandon d'un panier sur le site e-commerce.

[Cross Sell](./ca-lab1-cross-sell.md): Créer une audience enrichie et l'activer au travers le catalogue de destinations.


## Architecture en place

Les diagrammes ci-dessous mettent en évidence les composants utilisés pour accomplir les trois chapitres.






