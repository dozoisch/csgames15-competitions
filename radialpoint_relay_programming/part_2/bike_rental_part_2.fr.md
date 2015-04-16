# Programmation à relais de Radialpoint
Nos défis sont groupés autour d’un système de location de vélo.

## Application web de location de vélo
Le service de vélo collectif Bixi est devenu un phénomème international et nos voisins newyorkais ont adopté le service depuis quelques années sous le nom Citi Bike.

Vous avez été approché par Citi Bike pour construire une nouvelle application web à l’usage des cyclistes et des employés de Citi Bike. L’application met de l’avant une nouvelle fonctionalité de réservation permettant aux usagers de réserver leurs locations de vélo à l’avance.  Citi Bike a aussi une équipe de répartiteurs dont la tâche quotidienne est de transporter des vélos des stations pleines vers celles qui sont vides.  Citi Bike envisage aussi l’ajout de fonctionalités pour aider les répartiteurs à planifier leurs journées en leur permettant de répondre rapidement lorsqu’une station est à pleine capacité.

Notez que pour cette étape du relais vous aurez accès à internet.  Vous pouvez donc incorporer des sources de données externes ou des services de tiers (e.g. Google Maps).  Nous avons inclus quelques librairies sous Framework_UI mais vous êtes libre de télécharger et d’utiliser vos librairies préférées.

## Backend & Storage
Lors de cette étape, l’emphase est mise sur le frontend.  Vous pouvez tout de même intégrer un backend si cela vous facilite la vie (e.g. flask, node, meteor) mais ceci n’est pas requis. Les juges vont seulement évaluer ce qui “roule” dans le navigateur.

Certaines des fonctionalités requièrent que des données soient persistées.  Même sans backend vous avez quelques options:
- HTML5 local storage
- MongoLab REST API
- meteor.com

Tout est permis dans la mesure où la solution fonctionne dans un navigateur.

Nous vous encourageons fortement à prendre des outils avec lesquels vous êtes familiers et de garder votre solution aussi simple que possible.
Données de location de vélo
Citi Bike a un API live disponible [ici-même](http://www.citibikenyc.com/stations/json).

Au cas où l’API ne serait pas disponible, nous avons inclus un exemple de réponse **live_data_sample.json**. Nous vous recommandons d’avoir un mécanisme simple permettant de faire un fall back vers les données statiques si il advenait que nous rencontrions des problèmes avec l’API (e.g. limite sur la bande passante).

Des données historiques sont aussi disponibles pour [téléchargement](http://www.citibikenyc.com/system-data) et nous avons inclus le mois d’août 2014 pour vous faciliter la vie **201407-citibike-tripdata.zip**.

Certaines des fonctionalités proposées ont déjà été implémentées par Citi Bike. Libre à vous d’imiter la fonctionalité existante ou d’implémenter votre version améliorée.

## Répartition

### Setup
- (5%) Un fichier Readme incluant des explications claires sur la façon de rouler votre application web et une liste des fonctionalités supportées.  Mentionnez aussi le navigateur idéal pour tester votre app.

### Fontionalités de base
- (5%) Réserver une location de vélo
- (5%) Énumérer mes locations de vélo
- (5%) Annuler une réservation
- (5%) Afficher la capacité à une borne (# de vélos présents à une borne)
- (5%) Afficher les vélos disponibles à un instant donné (# de vélos présents moins les vélos qui ont déjà été réservés par les autres usagers)
- (5%) Afficher une carte des bornes et de leur capacité (e.g. sur une carte Google Map)

### Fonctionalités avancées
- (10%) Ordonner la liste des bornes par leur proximité à la position de l’usager
- (10%) Diriger les usagers vers la borne libre la plus proche ou la borne avec des vélos disponibles la plus proche
- (10%) Afficher une historique de la capacité d’une borne durant les dernières 24 heures
- (10%) Créer une route pour un répartiteur
- (15%) Prédire la disponibilité de vélos basé sur les données historiques.

### Surprenez-nous
- (10+%) Implementez votre propre fonctionalité.  Des points bonis seront attribués aux fonctionalités hors du commun.
