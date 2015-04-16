# Programmation à relais de Radialpoint

Nos défis sont groupés autour d’un système de location de vélo.

## Analyse de données
Afin d’offrir un service de location de vélo hors pair, il est essentiel de bien comprendre comment les usagers utilisent le service.  Avec l’aide des données historiques, aidez les administrateurs du service de location à répondre aux questions suivantes.


### Données historiques

> Les données sont fournies sous le format CSV (valeurs séparées par des virgules) dans le  fichiers **hour.csv**.  Elles contiennent les fréquences d’usage du système de location de vélo  (locations) pour chaque période d’une heure. Les données couvrent une période de 2 ans.

*Fanaee-T, Hadi, and Gama, Joao, Event labeling combining ensemble detectors and background knowledge, Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg.*

Voici l’interprétation de chaque colonne

- instant: indice de l’entrée
- dteday : date (du 1 janvier, 2011 au 31 décembre 2012)
- season : saison
    1. hiver
    2. printemps
    3. été
    4. automne
- yr : année (0: 2011, 1:2012)
- mnth : mois (1 to 12)
- hr : heure (0 to 23)
- holiday : congé ou non
- weekday : jour de la semaine
- workingday : 1 si un jour de semaine qui n’est pas congé, sinon 0
- weathersit : (doit-être interprété de [1] meilleur condition climatique à la pire condition [4])
    1. dégagé, partiellement nuageux
    2. nuageux à brumeux
    3. neige ou pluie faible, orages faibles
    4. averses de pluie ou de neige fortes, grésil, orages forts et brouillard
- temp : température normalisée, les valeurs sont divisées par la température maximale 41 C
- atemp: température ressentie normalisée, les valeurs sont divisées par la température ressentie maximale 50 C
- hum: humidité relative
- windspeed: vitesse des vents normalisé, les valeurs sont divisées par la vitesse maximale 67 km/h
- casual: nombre d’usagers occasionnels ayant utilisé le service durant cette heure
- registered: nombre d’abonnés ayant utilisé le service durant cette heure
- cnt: total d’usagers (abonnés et occasionnels) durant cette heures

### Instructions
Pour répondre aux questions suivantes, fournissez une application sur la ligne de commande ou un script, écrit dans le **language de votre choix**, qui accepte en paramètre les données historiques dans **leur format original** et retourne les réponses en sortie.  Documentez clairement toute étape supplémentaire pour rouler votre programme.  Les nombres mentionnés plus bas sont seulement à titre d’exemples.

Aidez à comprendre les habitudes d’utilisation du service en répondant aux questions suivantes:

0. (10%) Quel est le nombre **maximal de locations dans une heure** (i.e. colonne cnt) durant la période couverte par les données? Affichez le jour et l’heure sous le format `YYYY-mm-dd HH:mm:ss` où l’heure prend des valeurs entre 0 et 23 et le nombre de locations de vélo:
    - 2011-01-26 16:00:00 with 5 rentals

0. (10%) Quels sont les jours et les heures où le nombre de **locations dans une heure** est égal ou plus grand que 90% du nombre trouvé plus haut?  Affichez un résultat par ligne avec le jour et l’heure dans le format précédent et le nombre de l’occations en ordre chronologique:
    - 2011-01-26 16:00:00 with 5 rentals
    - 2011-01-27 17:00:00 with 6 rentals
    - 2012-02-11 09:00:00 with 2 rentals

    **Observez:** les résultats montrent une nette augmentation des l’occations en 2012.

0. (15%) Quel est le nombre **maximal de locations dans une journée** durant la période de 2 ans couverte par les données?  Prenez comme hypothèse que le nombre de locations dans une journée est égale à la somme des locations de chaque heure.  Affichez le jour et le nombre de locations pour cette journée:
    - 2011-01-26 with 100 rentals


0. (15%) Quels sont les jours où le **nombre de locations est égal** ou plus grand que 90% du nombre maximal de locations de la question 3?  Affichez un résultat par ligne avec le jour et le nombre de locations en **ordre croissant**:
    - 2011-01-27 with 90 rentals
    - 2011-02-11 with 97 rentals
    - 2011-01-26 with 100 rentals

    **Observez:** l’automne est une merveilleuse saison pour le vélo!

0. (15%) De quelle façon les conditions climatique affectent l’utilisation du service?  Donnez le **nombre moyen de locations dans une heure** pour chaque condition climatique.
    - weather: 1 average hourly rentals: 234
    - weather: 2 average hourly rentals: 23
    - weather: 3 average hourly rentals: 105
    - weather: 4 average hourly rentals: 403

0. (15%) De quelle façon les saisons affectent l’utilisation du service?   Donnez le **nombre moyen de locations** dans un jour pour chacune des quatres saisons:
    - spring average rentals: 56
    - summer average rentals: 90
    - fall average rentals: 97
    - winter average daily rentals: 40

0. (20%) Les données contiennent une mine d’information sur l’utilisation du système.  Explorez les données et dites-nous ce que vous avez trouvé.   Est-ce qu’il y a plus d’usager durant les jours de congé ou durant les jours ouvrables?  Est-ce que la fréquence d’utilisation des usagers occasionnels diffère beaucoup de celle des abonnées?   Est-ce que les conditions climatiques ont plus d’impact sur l’utilisation du service que les saisons?  Quels sont les meilleurs signaux (condition climatique, température, congé, …) pour prédire le taux d’utilisation pour un jour donné?
