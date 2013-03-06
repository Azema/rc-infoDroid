# API
---

L'API sera développée en PHP. Il s'agira d'une API HATOAS du type HAL.

L'API devra pouvoir répondre dans les deux formats suivants: json & xml.
Les types de contenu retournés seront donc : application/hal+TYPE (TYPE: json / xml).

Les erreurs seront retournées du type : application/api-problem+TYPE (TYPE: json / xml).

L'API sera documentée directement en ligne, il suffira d'appeler la méthode 'documentation' du point d'entrée de l'API.

En fonction des paramètres fournis au point d'entrée, le retour sera soit une collection, soit une ressource.

Tous les liens de relations seront définit dans la propriété '_links'.
Les éléments enfants d'une ressource seront définit dans la propriété '_embedded'.

Voici deux exemples:

Une collection: 
```json
	{
        "_links": {
            "first": {
                "href": "http://localhost:8080/api/status/public"
            },
            "last": {
                "href": "http://localhost:8080/api/status/public?page=26"
            },
            "next": {
                "href": "http://localhost:8080/api/status/public?page=14"
            },
            "prev": {
                "href": "http://localhost:8080/api/status/public?page=12"
            },
            "self": {
                "href": "http://localhost:8080/api/status/public?page=13"
            }
        },
        "count": 77,
        "page": 13,
        "per_page": 3,
        "_embedded": {
            "status": [
                {
                    "_links": {
                        "self": {
                            "href": "http://localhost:8080/api/status/user/rob/bcb075767861776065ba599f97e06bc90520a291"
                        }
                    },
                    "id": "bcb075767861776065ba599f97e06bc90520a291",
                    "image_url": null,
                    "link_title": null,
                    "link_url": null,
                    "text": "I can haz new user!",
                    "timestamp": "1358457081",
                    "type": "status",
                    "user": "rob"
                },
                {
                    "_links": {
                        "self": {
                            "href": "http://localhost:8080/api/status/user/matthew/4b4a40e12ec6e578c8cc9a8ec6c56cb0580e90a0"
                        }
                    },
                    "id": "4b4a40e12ec6e578c8cc9a8ec6c56cb0580e90a0",
                    "image_url": null,
                    "link_title": null,
                    "link_url": null,
                    "text": "Text describing image",
                    "timestamp": "1358287885",
                    "type": "status",
                    "user": "matthew"
                },
                {
                    "_links": {
                        "self": {
                            "href": "http://localhost:8080/api/status/user/matthew/a2f4c22a7508b20ac6f2fa42884b5b4a840fe67d"
                        }
                    },
                    "id": "a2f4c22a7508b20ac6f2fa42884b5b4a840fe67d",
                    "image_url": null,
                    "link_title": null,
                    "link_url": null,
                    "text": "Text describing image",
                    "timestamp": "1358287885",
                    "type": "status",
                    "user": "matthew"
                }
            ]
        }
    }
```

Une ressource:
```json
	{
        "_links": {
            "self": {
                "href": "http://localhost:8080/api/status/user/rob/af53e16abdbfc27570ae04b6fe49034c38baf40b"
            }
        },
        "id": "af53e16abdbfc27570ae04b6fe49034c38baf40b",
        "image_url": null,
        "link_title": null,
        "link_url": null,
        "text": "Posting my status!",
        "timestamp": 1358619199,
        "type": "status",
        "user": "rob"
	}
```