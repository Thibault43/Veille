---
title: "Cache"
description: "Dans cet article, nous allons vous expliquer en détails ce qu'est le cache et comment ça marche."
lead: ""
date: 2021-04-13T09:19:42+01:00
lastmod: 2021-04-13T09:19:42+01:00
draft: false
weight: 50
images: ["cache.png"]
contributors: ["Sebastien Parrat"]
---

## Qu'est-ce que le cache ?
Il s'agit d'un système de mémoire intermédiaire numérique qui conserve les données consultées en vue d’un accès
ultérieur. Il permet de réduire le temps d’accès à ces données. Le cache est une couche invisible entre l’utilisateur et la source des données

Les serveurs web disposent de leur propre cache qui peut enregistrer temporairement le contenu d’un site.

## Quels sont les avantages d'un cache ?
Avoir un cache permet d'améliorer la vitesse de navigation sur un site web.
Dans la mesure où un cache permet de réduire fortement le temps de chargement, la charge sur le système est
considérablement réduite.

## Les différents types de cache
Il existe 2 types de cache : hardware et software.

Un cache hardware est une mémoire intermédiaire rapide qui réduit les temps d’accès à la mémoire de données.

Un cache software peut dépasser la taille de la ressource devant laquelle il se trouve.

Nous allons nous intêresser au cache software.

### CDN
CDN, pour `Content Delivery Networks`, est une plateforme de serveurs permettant de réduire le temps de chargement des
pages Web.

### Cache côté client (navigateur)
Vous devez savoir que de nombreuses données sont stockées temporairement sur votre appareil lorsque vous naviguez sur Internet.
En général, ce sont les ressources fréquemment utilisées (images, vidéos) qui sont stockées dans le cache du navigateur
de l’appareil.

### Cache côté serveur web
En général c'est un serveur, qui est installé sur le réseau et est dédié à la sauvegarde en local de différents contenus Internet (pages Web)
Un cache Web enregistre les documents Web, comme les pages HTML, les images, les feuilles de styles ou les fichiers JavaScript en vue d’une réutilisation
Ce type de serveur permet un accès hors ligne aux contenus.

#### Outils de mise en cache
##### Redis
Redis, pour `Remote Dictionary Server`, est un système de stockage de données en mémoire qui peut être utilisé pour
une base de données, le cache, le courtier de messages et la file d'attente. Les données sont
situées dans la mémoire principale du serveur ce qui permet de réduire la latence d'accès aux données,
d'augmenter le débit et d'alléger la charge de votre base de données.

##### Memcached
Memcached est un système de cache utilisé pour accroître la vitesse de réponse des sites web possédant
des bases de données quelque peu chargées. Ce système est simple à déployer et facile à utiliser contrairement à Redis.

### DNS
Les requêtes DNS ayant déjà reçu une réponse sont mises en cache sur l’appareil.
Cependant, l’utilisation du cache DNS peut également engendrer des problèmes, par exemple lorsqu’un domaine a changé
d’adresse IP dans le cas notamment d’un changement de serveur et que l’ancienne adresse est encore dans le cache DNS local.

## Glossaire

- [https://www.ionos.fr/digitalguide/hebergement/aspects-techniques/quest-ce-quun-cache/](https://www.ionos.fr/digitalguide/hebergement/aspects-techniques/quest-ce-quun-cache/)
- [https://aws.amazon.com/fr/caching/](https://aws.amazon.com/fr/caching/)
- [https://aws.amazon.com/fr/redis/](https://aws.amazon.com/fr/redis/)
- [https://betterprogramming.pub/optimizing-your-application-with-redis-caching-5df5fb9acbd4](https://betterprogramming.pub/optimizing-your-application-with-redis-caching-5df5fb9acbd4)
