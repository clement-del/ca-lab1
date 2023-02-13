<p align="center">
<img src="https://user-images.githubusercontent.com/40355195/218433960-efb1147f-d81f-4a8a-80a4-a28451960311.png" />
</p>

# Lab 1 - Création d'un parcours avec Adobe Campaign augmenté

Adobe Campaign s'utilise conjointement avec Adobe Experience Platform (AEP) pour enrichir l'expérience client avec un ensemble de fonctionnalités additionnelles. Vous allez ainsi pouvoir exploiter :

- La collecte de données  en temps réel, au plus proche des utilisateurs et les segmenter à la volée en fonction de leurs comportements online, très utile pour personaliser le contenus sur les propriétés digitales en fonction de leur appétences.
- Un  orchestrateur de parcours client pour réagir en temps réel à des évènements générés par vos utilisateurs, et déterminer le meilleur itinéraire pour vos contacts. 
- Des modèles d'intelligence artificielle pour scorer vos contacts et déterminer leur propension à acheter un produit, ou leur propension à quitter les services de votre marque pour la concurrence. 
- Un vaste catalogue de destination pour activer vos audiences sur les canaux de votre choix: réseaux sociaux, email marketing, search & display, site web, CRM etc..
- Appliquer des règles de gouvernance de la donnée et vous assurer que les données de vos utilisateurs soit uniquement utilisées à bon escient, et éviter tout risque de partage malencontreux vers un tiers, ou une utilisateur de la donnée client qui n'a pas été consentie par votre contact. 


---

Au cours de ce lab, nous allons utiliser une marque fictive d'équipement sportif - intitulée **Luma** - pour illustrer ces fonctionnalités au travers d'un parcous client composé de 3 chapitres: 

- **L'acquisition de nouvelles données clients** depuis le site web Luma. Grace a la collecte en temps réel, nous allons récolter les interactions des visiteurs, même anonymes, et personnaliser le site web en temps réel en fonction de leurs comportements de navigation. Lorsque un utilisateur crééra son compte, son comportement en tant que visiteur anonyme sera automatiquement rattaché à son profil connu et complétera la vision 360° dans Adobe Experience Platform et dans Adobe Campaign. 

- **La conversion et l'abandon de panier**. En exploitant le moteur d'orchestration, nous allons pouvoir définir des messages personalisés à chacune des étapes du process de paiement en ligne. De l'ajout de produit dans un panier, à la finalisation du paiment, nous pouvons interagir à travers des communication personalisés avec nos futurs clients, et également les recibler si ils ne terminent pas le processus d'achat. Pour le routage des messages, faisons confiance à Adobe Campaign !

- **Le cross sell**. Exploitons les capacités d'intelligence artificielle de la Adobe Experience Platform pour calculer une audience qui sera la plus à même d'acheter un accessoire de sport extérieur au cours des 3 prochaines semaines en nous basant sur l'analyse des données comportementales de nos précèdents clients. Partageons ensuite cette audience à Snapchat et vers Adobe Campaign et peaufiner notre ciblage (règles de pression, gestion de la deliverabilité...) 


## Objectifs d'apprentissages
- Visualiser le profil temps réel et le graph d'identité dans Adobe Experience Platform
- Configurer un parcours client avec un message personalisé 
- Créer un segment utilisant les scores calculés par les services intelligents de Adobe Experience Platform
- Activer ce segment vers Adobe Campaign et les réseaux sociaux


## Prérequis
- Un navigateur web avec les onglets suivants ouverts en mode incognito, ceci afin de ne pas mélanger l'identifiant de connexion Adobe utilisé pour le lab avec celui de votre entreprise. 
 * Accès à [Adobe Experience Platform](https://experience.adobe.com/#/@demosystem4/sname:emea-france-sc/platform/home) - Si lors de la connexion on vous demande un numéro de téléphone, veuillez clicker sur _Not Now_.
 * Accès au [site web de demo](https://builder.adobedemo.com/web/delaland-04QF/home) - Si l'on vous demande de vous logger, utilisez les identifiants que l'onn vous a remis.
 * Accès à la [webmail de demo](https://campaignfr.adobedemo.com/webmail) - Utiliser le login et mot de passe fourni.


**Les logins & mots de passe vous seront communiqués sur place.**


## Exercices

[Acquisition](./ca-lab1-acquisition.md): Naviguer sur le site internet de demo et générer des données pour ensuite les visualiser dans Adobe Experience Platform.

[Conversion](./ca-lab1-conversion.md): Configurer le message personalisé lors de l'abandon d'un panier sur le site e-commerce.

[Cross Sell](./ca-lab1-cross-sell.md): Créer une audience enrichie et l'activer au travers le catalogue de destinations.








