---
title: "ORM"
lead: "Un ORM permet de simplifier l'accès à une base de données"
date: 2021-04-12T09:15:59+01:00
draft: false
type: "plugins"
logo: "akeneo"
description: "L'ORM permet de simplifier l'accès à une base de données"

---

### Définition
<img style="max-height: 225px" src="https://www.developpez.net/forums/attachments/p474863d1/a/a/a"/>

L'ORM pour Object-Relational Mapping désigne une technique
de programmation visant a simplifier l'accès à une base de données.

Un ORM est un ensemble de classes qui permet de manipuler les tables
d’une base de données relationnelle.

Il se place en interface entre un programme applicatif et
une base de données relationnelle pour simuler une base de données
orientée objet. Plus encore l'ORM s'occupe de définir des correspondances
entre les schémas de la base de données et les classes du programme
applicatif. Par exemple dans Symfony c'est l'ORM [Doctrine](https://symfony.com/doc/current/doctrine.html)
s'occupe de faire les correspondances.

### Les avantages d'utiliser un ORM

- Permet de préserver une homogeneité dans son code, en effet les données
  relationnelles sont manipulés à l'aide de classes, tout est objet
  pas besoin de faire des requetes sql mis à part pour des besoins
  très spécifiques. Car celui-ci se charge de transformer
  les requêtes pour les rendre compatibles avec la base de données.

- Permet un gain de temps dans le développement grâce au processus
  d'automatisation, l'ORM facilite les intéractions avec la base de
  données.

### Les limites liées à un ORM

- L'utilisation d'un ORM peut alourdir un projet de façon
  conséquente.

- Plus lents que les requêtes SQL basiques.

- Configuration parfois fastidieuse.
