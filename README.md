# Réalisation d'une application Android pour les ligues de la FFVRC
----

L'idée est de créer une application Android qui permettra de fournir un maximum
d'informations sur chaque ligue de la FFVRC (Federation Française de Voiture Radio Commandée).

Les informations pouvant être recencées et diffusées:
- [ ] Les clubs
- [ ] Les courses
- [ ] Les championnats
- [ ] Les résultats
- [ ] Les coordonnées de la ligue
- [ ] Les infos diverses


+ Les informations de chaque ligue devront être disponible via une API sur Internet.
+ Elles devront être renseignées par les responsables de ligue ou bien par une ou plusieurs
personnes désignées par les responsables de ligue.
+ Les informations seront renseignées via un BackOffice Web accessible sur Internet.

+ L'application récupera les informations a diffuser via une API REST.
+ L'application nécessitera une connexion internet pour fonctionner. A voir pour stocker
certaines informations dans l'application plus tard, les informations stockées pourront 
être mises à jour lorsqu'une connexion internet sera disponible (voir wifi).

+ Les utilisateurs devront choisir la ligue qu'ils souhaitent consulter à l'arrivée sur 
l'application. Il devra être possible de garder en mémoire la ligue choisit et de ne plus
proposer le choix de la ligue au démarrage de l'application. Il devra quand même être possible
de choisir une autre ligue.
+ Un menu devra permettre de choisir parmi les éléments cités ci-dessus.

## Les clubs

### Les données d'un club:
* Nom
* Un responsable
* Une adresse postale
* Une adresse mail
* Un numéro de téléphone
* Des coordonnées GPS
* Des photos
* Les équipements
* Particularités (électricité, eau, stands, etc...)

### Les actions
* Fournir la liste des clubs de la ligue
* Trier la liste des clubs
* Afficher les détails d'un club
* Afficher le club sur une carte géographique
* Afficher tous les clubs sur une carte géo
* Permettre d'acceder aux courses d'un club

## Les courses

### Les données d'une course:
* une date
* coordonnées (voir club ou différent)
* type (indoor ou outdoor)
* catégories (4x2 1/10, 4x4 1/10, short course 1/10)
* Un organisateur
* Un numéro de téléphone
* Une adresse mail
* Lien vers un formulaire d'inscription
* Une liste de participants
* Les classements par catégories (après course)

### Les actions
* Fournir une liste des courses
* Trier la liste des courses
* Voir le détail d'une course
* Voir les résultats d'une course
* Voir la liste des participants inscrits
* Ajout la course dans le calendrier

## Les championnats

### Les données d'un championnat

### Les actions

## Les résultats

### Les données de résultats

### Les actions

## La ligue

### Les données de la ligue
* Le président
* Les coordonnées

### Les actions
* Contacter la ligue