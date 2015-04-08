# CS Games 2015
## Compétition Web
**Par [Hugo Dozois-Caouette](https://github.com/dozoisch)**

### Règles générales

- Vous avez trois heures pour compléter l’épreuve
- Vous devez téléverser tous les fichiers de sources pertinents sur le serveur de “turn-in”. Vous n’avez pas besoin d’inclure les fichiers d’images publiques fourni. Pas besoin non plus d’inclure les librairies que je vous fourni. Le taille maximum de téléversage sera limitée de toute façon.
- Compléter tous les éléments d’une catégories donne les points bonus associés à cette catégorie.
- Vous devez écrire un makefile qui permet de facilement “build” et de rouler l’application. Il important que nous n’ayons pas besoin de chercher dans la documentation des cadriciels (frameworks) pour pouvoir le rouler.
- Vous avez le droit à Internet. Une bonne connaissance de l’écosystème web est un atout.
- Vous devez fournir un readme qui liste les différentes fonctionnalités implémentées. Cela accélérera la correction.
- Soyez créatif et ayez du plaisir!


### Introduction

C’est la fin du monde... (malheureusement, vous ne pouvez rentrer à la maison et la regarder sur la télévision, désolé Xavier Caféine). Il y a quelques années, un virus zombie est apparu. Il ne semblait pas vraiment nuisible et peu de recherches furent effectuées. Toutefois, il y a 6 mois, le virus muta et une nouvelle race de zombies intelligents apparue. Vous faites parti du dernier groupe de survivants et êtes maintenus prisonnier par un groupe de zombies. Le chef de la horde vous ordonne de créer un nouveau site de rencontre pour son fils  (qui n’est pas assez laid pour être populaire avec les zombiettes).

> **spook•y** (spo͞o′kē)

>adj. spook•i•er, spook•i•est Informal

>1. Qui suggère les fantômes, spécialement dans le domaine de l’étrange et du dérangeant.
*http://www.thefreedictionary.com/spooky*

### Instructions
Il y a beaucoup de fonctionnalités. Le but est de vous limiter le moins possible et de faire ce qu’il vous plaît. Cette épreuve n’est probablement pas faisable en trois heures. À vous de bien choisir ce que vous voulez faire!

Un “Hello World” de 5 cadriciels différents est fourni dans le dossier ./src. Un makefile est disponible dans chaque dossier afin de pouvoir mettre en marche le serveur. Vous pouvez télécharger n’importe quel autre framework, en autant que vous fournissiez la procédure pour le mettre en marche dans le README.

N’oubliez pas de compléter le README! Il doit y avoir, évidemment, la procédure de mise-en-marche, mais aussi la liste des fonctionnalités que vous avez implémentées (nous ne voulons pas avoir à les deviner!). Il y a MongoDB, postgreSQL et SQLite d’installés. N’oubliez pas de fournir les scripts nécessaires (vous pouvez toujours utilisez du data “en-mémoire”)!

Vous n’avez pas à packager les images qui sont fournies avec l’application dans le dossier ./public/default_imgs, toutefois si vous en avez de supplémentaires, n’oubliez pas de les inclure!

Prenez le temps de faire le tour de toute la liste!

### Fonctionnalités
#### Authentification (bonus +2 points)
- Être capable de créer un compte (avec la page de création de compte)
- (+2 points)
- Être capable de se connecter avec un compte (+2 points)
- Se déconnecter (+2 points)
- La sécurité des mots de passes en (mémoire/base de donnée)
  - Texte pur: 0 points
  - Encryption/Hachage de basse sécurité: +1 point
  - Hachage haute sécurité: +2 points

#### Page de profil (bonus +3 points)
- Avoir un profil avec les informations suivantes (+2 points):
  - nom
  - courriel (visible seulement sur son propre profil +1 point)
  - âge
  - genre (Homme/Femme)
- Interessé par X genre (+1 point)
- Avoir une description (+1 point)
- Associer des tags (+2 points)
- Avoir de l’auto-complétion (+4 points)
- Téléverser une photo de profile (+3 points)

#### Liste des candidats (bonus +2 points)
- Affichage des noms, et d’autres informations pertinentes (+3 points )
- Affichage de seul les candidats du genre par lequel je suis intéressé (+1 point)
- Affichage de seul les candidats qui sont intéressés par mon genre (+1 point)

#### Liste des candidats avancée (bonus +3 points)
- Filtres:
  - Par tranche d’âge (+2 points)
  - Par tags (+2 points)
  - Pouvoir modifier les filtres directement depuis la liste (+2 points)
  - Avoir un filtre par défaut, qui est populé automatiquement (et pouvoir modifier de filtre - par défaut) (+2 points)
- Réordonner la liste (+2 points)

#### Messagerie (interne pas courriel) (bonus +2 points)
- Pouvoir envoyer un message interne à d’autres candidats (+3 points)
- Voir les message reçus (+2 points)
- Voir les messages envoyés (+2 points)
- Voir le fil de message (+2 points)

#### Proposer une rencontre (date) (bonus +4 points)
- La rencontre doit contenir une date, un endroit, un message (+3 points)
  - Envoyer une rencontre depuis le profil de la personne (+1 point)
  - Envoyer une rencontre depuis depuis la la messagerie (+1 point)
- Accepter une rencontre (+2 points)
- Voir les rencontres proposées et leur statut (+2 points)
- Mettre des plages de disponibilités (+2 points)
- Être capable d’envoyer une rencontre seulement si la personne est disponible (+3 points)

#### Évaluer quelqu’un (rate) (bonus +3 points)
- Mettre une évaluation (numérique/étoiles/etc.) depuis son profil (+3 points)
- Pouvoir évaluer un candidat suite à une rencontre (+1 point)
- Voir ma côte sur mon profil (+1 point)
- Commenter sur le profil de quelqu’un (+3 points)
- Pouvoir supprimer un commentaire de son propre profil (+2 points)

#### J’aime (likes Facebook style-ish) (bonus +3 points)
- Être capable d’aimer un profil de candidat et voir la liste de nos “j’aime”
- (+4 points)
- Voir la liste de personne qui nous aime (+2 points)
  - Être capable d’aimer quelqu’un en retour depuis la liste (+1 point)
- Avoir une préférence globale qui ne permet qu’au gens qu’on aime de nous écrire par la messagerie (+2 points)

#### Notifications (bonus +4 points)
- Bar/page/panneau de notification (+2 points) avec au moins un des suivants:
  - J’aime (+2 points)
  - Évaluation/Côte (+2 points)
  - Rencontres (+2 points)
  - Message (+2 points)

#### Flux du harceleur (flux d’événements/activité) (bonus +3 points)
- Voir la liste des événements (+2 points) avec au moins un des suivants:
  - j’aime (+2 points)
  - évaluation (+2 points)
  - rencontre (+2 points)
  - commentaires (+2 points)
- Filtre: Voir les activités seulement des personnes que j’aime (+2 points)
- Voir les activité d’une personne sur son profil (+3 points)

#### Fonctionnalités  bonus

- **Spookies**
  - Zombie Kitten ASCII art (+2 points)
  - Avoir un favicon spookie (+2 points)
  - Une page 404 spookie (+2 points)
  - De la musique spookie sur la page d’accueil (+3 points)
  - Un curseur spookie (+3 points)
  - Une réaction spookie au code de Konami (up up down down left right left right b a) (+3 points)

- **Bonus**
  - Support https (config nginx/apache sont acceptées) (+3 points)
    - Qui est sécuritaire à Poodle (+1 point)
  - Adapté au mobile (+2 points)
  - Avoir du rose à quelque part (+1 point)
  - Des belles icônes (ex: fontawesome) (+ point)
  - Une police personalisée (pas offerte par le navigateur) (+1 point)
  - Minification des scripts/css (+2 points)

- **Look en général (0-1-2 points)** (évalué subjectivement par le correcteur)
