[accueil](README.md)



Créer une audience enrichie et l'activer via le catalogue de destinations
=========================================================================

Exploitons les capacités d'intelligence artificielle de la RTCDP pour créer une audience qui sera la plus à même d'acheter un accessoire de sport d'extérieur au cours des 3 prochaines semaines. Nous allons nous baser sur l'analyse des données comportementales de nos précèdents acheteurs. 
Partageons ensuite cette audience à Snapchat et vers Adobe Campaign pour peaufiner notre ciblage avec les fonctionnalités présentes dans notre outil de marketing automation (règles de pression, gestion de la deliverabilité...).


## De l'intelligence au service de vos audiences
Adobe RTCDP met à disposition des services intelligents préconfigurés pour les utilisateurs métiers. Pour y accéder cliquer sur _Services_ dan le menu _Science des données_ et cliquez sur le bouton _Ouvrir_ dans la carte IA dédiée aux clients.


![image](https://user-images.githubusercontent.com/40355195/217492668-877411a8-c47e-45c6-bdb2-62c8a6aaa3ea.png)

Sur cet écran vous pouvez créér votre propre instance du modèle d'intelligence artificielle. 
La propension à la conversion doit être utilisée lors de la prévision de résultats commerciaux favorables, ce qui implique qu'un score élevé est bon et qu'un score bas est mauvais. Vous pouvez vous en servicr pour prédire si les utilisateurs achèteront un produit, souscrirons à un abonnement ou soumettront un formulaire d'inscription.

Il est également possible de configurer le modèle pour la prévision de l'attrition (churn) comme par exemple l'annulation de l'abonnement ou non retour sur le site Web. 

Pour ce lab, l'instance a déjà été prédéfinie pour calculer un score de propension à la conversion d'accessoires de sports exterieurs au cours des 30 prochains jours. cliquez sur l'instance de service _Propensity to buy outdoor gears_

![image](https://user-images.githubusercontent.com/40355195/217497970-15da535b-f9a2-4339-9985-6ee232b27e74.png)

Le dahboard vous permet d'analyser la répartition de la population analysée en 3 clusters: 
- Rouge: ceux ayant une faible propension à l'achat (score < 24)
- Jaune: ceux ayant une moyenne propension à l'achat (score entre 25 et 74)
- Vert: ceux ayant une forte propension à l'achat (score > 75)

Le dashboard présente également les facteurs d'influences qui ont le plus contribués à la décision dans chaque cluster. Les facteurs d'influences sont eux préconfigurés dans la modèle. 
Cliquez sur  le bouton _Créér le segment_ dans la carte propension élevée pour basculer dans l'éditeur de segment et ainsi créér votre audience. 



## Créér un segment pour les clients interessés par les équipements d'exterieurs

Vous voici dans l'interface de création des segments où vous allez pouvoir mixer vos critères de ciblages en se basant sur : 
- les Attributs: toutes les informations attachées au profil temps réel sont disponibles pour segmenter votre audiences, que ce soit les données personnelles, des préfèrences utilisateurs ou des valeurs dérivées tel que le score précèdement calculés.
- les Evènements: toutes les interactions que notre profil a eu avec la marque. On peut sélectionner 0, 1 ou plusieurs évènements et définir l'intervalle de temps dans lesquels ils doivent avoir eu lieu. Les logs de Campaign sont également disponibles.
- les Audiences: Il est possible de combiner les audiences déjà présentes dans la CDP pour recouper les segments et dégager les intersections les plus pertinentes.


![image](https://user-images.githubusercontent.com/40355195/217499302-db898983-3f6b-455c-96f7-49345cdebaa6.png)

Dans notre cas, nous ciblons uniquement les profils avec un score élevé n'ayant pas cliqués sur un email dont le nom de diffusion contient _outdoor gears_ au cours des 2 dernières semaines. 

- Donnez le nom suivant à votre segment : [identifiantParticipant] - Propension ++ Sport Ext, par exemple _participant01 - Propension ++ Sport Ext_
- Ajoutez une desctiption : Audience ayant une haute propension à l'achat d'articles de sports d'exterieurs sans click sur campagne email.
- Aller sur l'onglet Evènements, filtrer les évènements en saisissant _email opened_ dans le champ texte.
- Glissez-déposez l'évènement Email Opened dans l'interface de segmentation
- Changez _Inclure_ par _Exclure_ dans le container _Règle d'évènement_
- Dans les variables de l'évènement Email Opened, saisissez _delivery name_ pour filtrer la liste disponible.
- Glissez-déposez la variable _Delivery Name_ dans la règle d'évènement et saisissez _outdoor gears_ comme valeur de comparaison
- Dans le container Evènement, changer la temporalité de _N'importe quand_ à _Dernier_ et tapez _14_ jours
- Actualisez l'estimation et cliquez sur _Enregistrer et fermer_


![segmentation](https://user-images.githubusercontent.com/40355195/217507906-1a1f2394-b80d-4967-a36d-fc586ad833d4.gif)




## Activer votre segment vers Adobe Campaign



## Activer votre segment vers Snapchat



Bravo ! Vous avez complété le troisième chapitre du lab :+1: :sparkles: :tada: :rocket: :metal:, vous pouvez aller chercher votre goodie 😛 ou retourner à [l'accueil](Readme.md)
