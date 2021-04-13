---
title: "API"
description: "Dans cet article, nous allons vous expliquer en détails ce qu'est une API."
lead: ""
date: 2021-04-12T09:19:42+01:00
lastmod: 2021-04-12T09:19:42+01:00
draft: false
weight: 50
images: ["api.png"]
contributors: ["Sebastien Parrat"]
---

## Qu'est ce qu'une API ?

Une API, Application Programming Interface, ou Interface de Programmation d'Applicaion en français,
permet de faire communiquer et de connecter plusieurs logiciels pour effectuer des échanges
de données ou de fonctionnalités.

## Quelle est l'utilité d'une API ?
Avoir une API permet de simplifier le développement d'applications et donc de gagner du temps. En plus de cela,
les API offrent plus de flexibilité et permettent donc de créer de nouvelles applications plus facilement.

Grâce à cet outil, la collaboration entre les équipes métiers et informatiques est facilitée.
En effet, une API permet aux développeurs de pouvoir utiliser un programme sans avoir à se soucier du
fonctionnement complexe d'une application.

## Les différents accès aux API

Il existe trois différents accès aux API :

- les API privées : conçues pour un usage interne
- les API partenaires : partagées avec certains partenaires de l'entreprise
- les API publiques : accessibles à tous

## Sécurité des API
Le développeur de l'API doit choisir les ressources qu'il souhaite partager et avec qui.

### Les piliers de la sécurité applicative
AAA, ou triple A, signifiant `Authentication, Authorization, Accountability`.

#### Authentication
L’authentification, c’est savoir qui appelle notre API. À partir d’un ensemble d’informations, il est possible de savoir
de qui vient l’appel HTTP.

```
GET /v1/some-resource
Host: some.api
Accept: application/json
I-Am: Renaud Dahl
```
#### Authorization
L’autorisation consiste à savoir ce que cette personne a le droit de faire.

```
GET /v1/some-resource
Host: some.api
Accept: application/json
I-Am: Renaud Dahl
I-Can: do pretty much anything
```


#### Accountability (Traçabilité)
Il s’agit de savoir qui a fait quoi, quand, avec quelles ressources.

- Quoi
  - La ressource consommée
  - Le verbe HTTP appelé sur cette ressource
  - Le code HTTP de la réponse
- Qui
  - L’utilisateur final à l’origine de l’appel, propriétaire de la ressource
  - L’application qu’utilise cet utilisateur
- Quand
  - Le moment où a été exécutée la requête (par pitié utilisez ISO-8601)

### Les différents protocoles existants
#### Basic Authentication : HTTP
Ce système utilise une combinaison username/password encodée en base 64 et envoyée dans l'entête Header du navigateur.
Ce type de connexion est très peu recommandée due aux nombreuses failles exploitables.

#### Bearer Authentication : HTTP
Ce type d'authentification utilise des jetons de sécurité pour se connecter. Un jeton de sécurité est
un JSON Web Token dont le rôle est d'indiquer que l'utilisateur qui accède aux ressources est bien authentifié.

#### Utilisation de clé API (API Key)
Les clés d'API sont un correctif aux problèmes liés à l'authentification de base HTTP.
La valeur générée est unique et peut être attribuée qu'à un seul utilisateur.
Lors d'une connexion, cette clé est utilisée pour prouver qu'il est le même utilisateur que la dernière fois.
Cette clé unique doit être placée dans l'entête d'Autorization du navigateur.

```
GET /v1/some-resource
Host: some.api
Accept: application/json
X-API-KEY: MyAwes0m3API_KeY
```

##### OAuth
OAuth2 est un protocole utilisé pour autoriser des applications à utiliser l'API sécurisée d'un autre site web
pour le compte d'un utilisateur. On parle de `délégation d'autorisation` via le consentement de l’utilisateur.

#### OpenID Connect
OpenID Connect est une couche d'identification basée sur OAuth 2.0 qui autorise les applications à vérifier l'identité d'un utilisateur.

## Format retourné
Très souvent, le format retourné est le JSON (JavaScript Objet Notation).
Mais pourquoi ce format ?
Tout d'abord, le JSON est assez facile à lire par les humains et facile à comprendre pour les machines. En effet, ce format
permet de stocker des données de manières organisée et lisible.
De plus, ce type de fichier est léger ce qui facilite le traitement côté serveur et le rend plus rapide.

Le XML (eXtensible Markup Language) est aussi utilisé comme format de retour par certaines APIs.
Ce type de fichier permet de transmettre des informations entre les applications.

## Les différents types d'API
Alors que l'API suit un ensemble spécifique de règles qui déterminent la manière
dont les programmes communiquent entre eux. REST, SOAP et gRPC définissent la présentation de l'API.
Chacun a des fonctionnalités similaires mais présente plusieurs différences clés et cas d'utilisation.

REST, pour `Representational State Transfer`, est un ensemble de principes architecturaux et utilise le format JSON.
Ce style architectural utilise des méthodes HTTP (GET, POST, PUT, DELETE) pour récupérer et publier des données.
En utilisant le protocole HTTP, les API REST permettent aux logiciels d’un appareil de communiquer avec les logiciels
d’un autre appareil même s’ils utilisent des systèmes d’exploitation et des architectures différents.

SOAP, pour `Simple Object Access Protocol`, est un protocole standard initialement conçu pour que des applications développées avec différents
langages sur différentes plateformes puissent communiquer. Lorsqu'une requête de données est envoyée à une API SOAP,
elle peut être gérée par n'importe quel protocole de couches de l'application : HTTP (pour les navigateurs web),
SMTP (pour les e-mails), TCP et autres.
La réponse du serveur est retournée en format XML.

gRPC, pour `Remote Procedure Call`, est une infrastructure moderne permettant de communiquer entre les applications.
gRPC utilise les contrats HTTP/2, streaming, Protobuf et message pour créer des services haute performance et en temps réel.

## Glossaire

- https://developer.mozilla.org/fr/docs/Glossary/API
- https://www.redhat.com/fr/topics/api/what-are-application-programming-interfaces
- https://apifriends.com/api-management/what-is-an-api/
- https://www.bigcommerce.com/blog/what-is-an-api/#what-is-an-api-request
