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

- les API privées : utilisable uniquement en interne
- les API partenaires : partagée avec certains partenaires de l'entreprise
- les API publiques : accessible à tous

## Sécurité des API
Le développeur de l'API doit choisir les ressources qu'il souhaite partager et avec qui.
C'est pourquoi lorsque vous voulez utiliser une API, une connexion est très souvent demandée.

#### 1 - Basic Authentication : HTTP
Ce système utilise une combinaison username/password encodée en base 64 et envoyée dans l'entête Header du navigateur.
Ce type de connexion est très peu recommandée due aux nombreuses failles exploitables.

#### 2 - Baerer Authentication : HTTP
Ce type utilise des jetons de sécurité pour se connecter.

#### 3 - Utilisation de clé API (API Key)
Les clés d'API sont un correctif aux problèmes liés à l'authentification de base HTTP.
La valeur générée est unique et peut être attribuée qu'à un seul utilisateur.
Lors d'une connexion, cette clé est utilisée pour prouver qu'il est le même utilisateur que la dernière fois.
Cette clé unique doit être placée dans l'entête d'Autorization du navigateur.

##### OAuth

## Les différents types d'API
REST, SOAP...

## Format retourné

## Glossaire

- https://developer.mozilla.org/fr/docs/Glossary/API
- https://www.redhat.com/fr/topics/api/what-are-application-programming-interfaces
- https://apifriends.com/api-management/what-is-an-api/
