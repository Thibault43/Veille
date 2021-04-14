---
title: "Sécurité Web"
description: ""
lead: ""
date: 2021-04-13T15:33:58+02:00
lastmod: 2021-04-13T15:33:58+02:00
draft: true
weight: 50
images: ["securite-web.jpg"]
contributors: ["Sebastien Parrat"]
---

## Qu'est ce que la sécurité web ?
La sécurité web consiste à protéger les sites web contre l'accès, l'utilisation, la modification,
la destruction ou la perturbation non autorisées.

## Les différentes menaces du web
Open Web Application Security Project (OWASP) est une communauté en ligne travaillant sur la sécurité des applications Web.
Sur leur site Internet on peut retrouver le [Top 10](https://owasp.org/www-project-top-ten/) des risques liés à la
sécurité des applications Web.

Nous avons décidé de vous parler uniquement des trois plus grandes vulnérabilités du web.

#### Cross-Site Scripting (XSS)
Ce type d'attaque à pour principe d'injecter des scripts qui sont enregistrés dans la base de données et qui ensuite,
sont exécutés côté-client. Comme le code injecté provient du site web le navigateur web le considère comme sûr, l'utilisateur
malveillant peut alors récupérer le cookie d'authentification et se faire passer pour l'utilisateur.

#### Injection SQL
L'injection SQL est une technique qui permet d'exécuter du code SQL frauduleux sur une base de données. Ainsi, le hackeur
peut modifier, ajouter, supprimer des données sans avoir les droits.

#### Cross-Site Request Forgery (CSRF)
Cette vulnérabilité à pour but d'exécuter des actions à l'aide des identifiants d'un autre utilisateur sans que cet utilisateur
ne le sache. Pour récupérer les informations d'une personne, la personne malveillante récupère les informations passées
lors d'une requête HTTP POST.

## HTTPS
HTTPS, pour `HyperText Transfer Protocol Secure`, est la combinaison du HTTP avec une couche de chiffrement comme SSL
ou TLS. C'est un protocole de communication Internet qui protège l'intégrité ainsi que la confidentialité des données.
HTTPS est affiché sur une URL lorsqu'un site web est protégé par un certificat SSL.

## SSL/TLS
TLS, pour `Transport Layer Security`, et SSL pour `Secure Sockets Layer` sont des protocoles conçus pour assurer la
sécurité de la connexion Internet et la protection des données sensibles.

TLS est en fait une nouvelle version, plus sûre, de SSL et est constitué de plusieurs niveaux de protection :

- chiffrement : coder les données échangées afin de les protéger
- intégrité des données : les informations ne peuvent être ni modifiées, ni corrompues durant leur transfert sans être
  détectées.
- authentification : prouve que les internautes communiquent avec le bon site Web

Le protocole TLS vise principalement à assurer la confidentialité et l'intégrité des données entre plusieurs applications.

## CORS
CORS pour `Cross-origin Resource Sharing`, est un mécanisme de sécurité qui consiste à ajouter des en-têtes HTTP
permettant à une page Web d'un domaine d'accéder à une ressource d'un autre domaine.
Sans CORS, les sites Web sont limités à l'accès aux ressources de la même origine, c'est-à-dire de leur propre domaine.

### Qu'est-ce que l'origine (Origin) ?
L'origine comprend la combinaison du protocole, du domaine et du port. Par exemple, `https://api.mondomaine.com` et
`https://mondomaine.com` sont en fait des origines différente.
De la même manière, `http://localhost:9000` et `http://localhost:8080` ont également des origines différentes.

### Comment fonctionne CORS ?
Lorsque vous naviguez sur un site internet, le navigateur ajoute automatiquement l'entête `Origin`.

```
GET /widgets/ HTTP/1.1
Host: api.kiboko.fr
Origin: https://www.kiboko.fr
```

Le serveur web vérifie ensuite l'entête `Origin` de la demande. Si cette valeur est autorisée, elle définit
`Access-Control-Allow-Origin` avec comme valeur l'entête Origin.

```
HTTP/1.1 200 OK
Access-Control-Allow-Origin: https://www.kibko.fr
Content-Type: application/json
```

Enfin, lorsque le navigateur reçoit la réponse venant du server, il vérifie l'entête `Access-Control-Allow-Origin` pour voir
s'il correspond à l'Origin de l'onglet.
La vérification réussit si `Access-Control-Allow-Origin` correspond exactement à l'origine ou contient `*`.

## Content Security Policy
Content Security Policy (CSP) permet d'améliorer la sécurité des sites web en détectant et réduisant certains types
d'attaques.

Pour activer CSP, il suffit de configurer vos serveurs web afin d'ajouter un en-tête de réponse HTTP `Content-Security-Policy`.

Une autre possibilité consiste à utiliser l'élément HTML <meta>
```html
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; img-src https://*; child-src 'none';">
```

## Les algorithmes de hachage cryptographique
Ce sont des fonctions qui génèrent un résultat de longueur fixe à partir d'une donnée.

La donnée d'entrée de ces fonctions est souvent appelée message.
La valeur de sortie est souvent appelée valeur de hachage, empreinte numérique, empreinte, ou encore haché
(en anglais, message digest ou digest, hash).

Un algorithme de hachage est conçu pour être une fonction unidirectionnelle, c'est-à-dire impossible à
inverser.

Afin d'écrire la meilleure fonction de hachage cryptographique, il faut prendre en compte ces points :
- un même message aura toujours la même valeur de hachage
- la valeur de hachage d'un message se calcule facilement
- pour une valeur de hachage donnée, il est impossible de construire un message ayant cette valeur, c'est ce qu'on
  appelle la `résistance à la préimage`
- la valeur de hachage doit être unique : deux messages différents doivent avoir une valeur de hachage différente, c'est
  ce qu'on appelle la `résistance aux collisions`

Les algorithmes de hachage sont utilisés pour les signatures numériques, les codes d'authentification de message (MAC)
et d'autres formes d'authentification.

#### MD5
MD5 est l'un des algorithmes de hashing le plus connu permettant d'obtenir une valeur de hachage de 128 bits.
Cependant, il est désormais compromis et de nombreuses vulnérabilités sont exploitables.
En effet, il suffit juste de taper le hachage sur Google pour obtenir sa valeur réelle !

#### Famille des SHA
SHA pour `Secure Hash Algorithm`, est une fonction de hachage cryptographique conçue par la NSA des États-Unis.
SHA-0 et SHA-1 étant compromis, nous allons parler de SHA-2.

SHA-2 comprend plusieurs fonctions de hachage : SHA-224, SHA-256, SHA-384, SHA-512.
Ces fonctions produisent des hachés de taille différente qui est déterminée par le suffixe.

Aujourd'hui nous en sommes à la 3ème version (SHA-3) qui est sortie en 2015.

### Scrypt
Le Scrypt est l'un des algorithmes les plus sécurisés au monde.

Scrypt fait un hachage en utilisant une clé, une série de points clés marquée dans l'algorithme de hachage et en
ajoutant beaucoup de bruit. Le bruit dans Scrypt est en fait une série de nombres aléatoires qui sont générés par
l'algorithme et stockés en mémoire. Le but de ces nombres est de camoufler les données clés de l'algorithme, de rendre
le travail de cassage des hachages plus complexe.

### Bcrypt
Bcrypt est un algorithme de hachage qui utilise Eksblowfish et est évolutif en fonction du serveur qui le lance.
Le `b` vient du nom Blowfish et `crypt` du nom de la fonction de hachage utilisée par le système de mot de passe UNIX.

Cette technique utilise un salt (séquence qu'on va rajouter à un password pour en améliorer la sécurité) qui a une
valeur aléatoire. En utilisant Bcrypt, il est possible de choisir le nombre d'itérations pour le rendre plus lent
et donc plus difficile encore à bruteforcer.

Voici à quoi ressemble un hash bcrypt :
```text
$2y$10$0IexiTnFtZ6BeARkfVvidemnnAuPydkcH2tEpVbnE60o97K3UZn26
```

Vous pouvez distinguer trois valeurs, délémitées par des "$" :

- 2y identifie la version de l'algorithme bcrypt qui a été utilisé.
- 10 est le nombre d'itérations effectuées par l'algorithme pour augmenter la charge de travail
- 0IexiTnFtZ6BeARkfVvidemnnAuPydkcH2tEpVbnE60o97K3UZn26 est le salt, la valeur encodée (en base64) puis concaténée.

## Glossaire

- [https://developer.mozilla.org/fr/docs/Learn/Server-side/First_steps/Website_security](https://developer.mozilla.org/fr/docs/Learn/Server-side/First_steps/Website_security)
- [https://developers.google.com/search/docs/advanced/security/https?hl=fr](https://developers.google.com/search/docs/advanced/security/https?hl=fr)
- [https://developer.mozilla.org/fr/docs/Web/HTTP/CORS](https://developer.mozilla.org/fr/docs/Web/HTTP/CORS)
- [https://developer.mozilla.org/fr/docs/Web/HTTP/CSP](https://developer.mozilla.org/fr/docs/Web/HTTP/CSP)
- [https://blog.jscrambler.com/hashing-algorithms/](https://blog.jscrambler.com/hashing-algorithms/)
