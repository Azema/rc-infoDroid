# Réalisation d'une application Android pour les ligues de la FFVRC
----

L'idée est de créer une application Android qui permettra de fournir un maximum
d'informations sur chaque ligue de la FFVRC (Federation Française de Voiture Radio Commandée).

Les informations pouvant être recencées et diffusées:
 - [ ] Les clubs
 - [ ] Les courses
 - [ ] Les championnats
 - [ ] Les ligues
 - [ ] Les infos diverses

## Les idées
Les informations de chaque ligue devront être disponible via une API sur Internet.
Elles devront être renseignées par les responsables de ligue ou bien par une ou plusieurs personnes désignées par les responsables de ligue.
Les informations seront renseignées via un BackOffice Web accessible sur Internet.

L'application récupera les informations a diffuser via une API REST.
L'application nécessitera une connexion internet pour fonctionner. A voir pour stocker certaines informations dans l'application plus tard, les informations stockées pourront être mises à jour lorsqu'une connexion internet sera disponible (voir wifi).

Les utilisateurs devront choisir la ligue qu'ils souhaitent consulter à l'arrivée sur l'application. Il devra être possible de garder en mémoire la ligue choisit et de ne plus proposer le choix de la ligue au démarrage de l'application. Il devra quand même être possible de choisir une autre ligue.
Un menu devra permettre de choisir parmi les éléments cités ci-dessus.

L'utilisateur devra pouvoir renseigner son numéro de licence. Le numéro de licence servira à connaitre le classement de l'utilisateur dans les différents championnats, le classement des courses, l'inscription aux courses, etc...

## Les étapes de réalisation
 - [ ] L'API REST
 - [ ] Le BackOffice Web
 - [ ] L'application Android
 - [ ] Le FrontOffice Web

### L'API REST
 * L'utilisation de l'API REST nécessitera une clef d'authentification.
 * Le format de sortie devra être du JSON.

### Le BackOffice
 * Le BackOffice servira aux ligues et à la fédération pour renseigner les informations qui seront mises à disposition des utilisateurs de l'application.
 * L'accès au BackOffice devra être protégé par une page d'identification.
 * Les utilisateurs du BackOffice se verront attribuer un rôle qui leur permettra d'accéder à des actions.
 * Les utilisateurs affiliés aux ligues ne pourront voir et modifier les données que de la ligue à laquelle ils sont affiliés.
 * Les utilisateurs de la fédération pourront accéder à toutes les informations de toutes les ligues.

### L'application Android
 * L'application Android devra utiliser l'API REST pour obtenir les informations à diffuser.
 * Elle devra répondre aux différentes résolutions en utilisant le responsive design.
 * La page d'accueil de l'application devra demander, lors de la première ouverture, la sélection de la ligue souhaitée par l'utilisateur.
 * L'utilisateur pourra par la suite sélectionner une autre ligue.
 * L'utilisateur devra pouvoir renseigner son numéro de licence.

### Le FrontOffice Web
 * Le FrontOffice Web sera une réplique de l'application Android mais en étant plus adaptée aux grands écrans.

## Les ressources
### Les clubs
#### Les données d'un club:
* Nom
* Un responsable
* Une adresse postale
* Une adresse mail
* Un numéro de téléphone
* Des coordonnées GPS
* Des photos
* Les équipements
* Particularités (électricité, eau, stands, etc...)

#### Les actions
* Fournir la liste des clubs de la ligue
* Trier la liste des clubs
* Afficher les détails d'un club
* Afficher le club sur une carte géographique
* Afficher tous les clubs sur une carte géo
* Permettre d'acceder aux courses d'un club

### Les courses

#### Les données d'une course:
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

#### Les actions
* Fournir une liste des courses
* Trier la liste des courses
* Voir le détail d'une course
* Voir les résultats d'une course
* Voir la liste des participants inscrits
* Ajout la course dans le calendrier

### Les championnats

#### Les données d'un championnat
* Une catégorie (4x2 standard, 4x2 modifié, 4x4 modifié, etc...)
* Un type (Ligue Promotion, Ligue Open, Coupe de France, etc...)

#### Les actions
* Voir tous les championnats
* Filtrer par catégorie
* Voir le détail d'un championnat
* Voir le classement du championnat
* Voir les courses du championnat

### Les ligues

#### Les données des ligues
* Le président
* Les coordonnées

#### Les actions
* Contacter la ligue

## UML
![Diagram UML](https://raw.github.com/Azema/rc-infoDroid/master/images/uml.png)
