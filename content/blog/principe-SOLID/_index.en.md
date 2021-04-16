---
title: "Principe SOLID"
lead: "L'acronyme SOLID est un moyen mnémotechnique pour désigner
les 5 principes de bases de la programmation objet "
date: 2021-04-16T09:15:59+01:00
draft: false
contributors: ["Thibault Belledent"]
---
<div style="text-align: left">

### L'approche SOLID

L'approche SOLID définit les grandes lignes directrices
de la programmation objet pour proposer un code fiable, évolutif
et facilement maintenable.
Les principes sont : (Single Responsibility Principle,
Open/Closed Principle, Liskov Substitution Principle,
Interface Segregation Principle et Dependency Inversion Principle).

Cette approche théorique vise aussi les méthodologies de gestion de
projet tels que les méthodes agiles.

La méthode SOLID a été pensé pour combler des lacunes de développement
tels que la difficulté d'implémenter de nouvelles fonctionnalités,
la rigidité du code qui se caractérise par la difficulté
d'évolutivité du code. De plus l'approche répond au facteur
de fragilité car les changements au sein du code peuvent etre vecteurs
de casse dans le fonctionnement de l'application.

</div>

<img style="max-height: 300px" src="https://www.boxpiper.com/static/433c2c22a5faafa867405b40da29b2ab/be464/solid-design-principle-1.jpg"/>

<div style="text-align: left">

### Les grands principes SOLID

### - S : Responsabilité unique (Single Responsibility Principle)

Ce principe veut que pour une classe donnée celle-ci n'est
qu'une seule responsabilité. Un tel principe permet d'avoir une
meilleure compréhension de la classe en associant chaque classe à un role
bien précis, de cette façon on augmente la lisibilité du code.
De plus une définition précise de la responsabilité de chaque
classe dans l'application permet d'atténuer la complexité du code.

### - O : Ouverture/fermeture (Open/closed principle)

Le principe d'ouverture/fermeture définit qu'une application
ou logiciel se doit d'être ouvert pour les mises à jours (extensions)
mais doivent être fermées aux modifications.
L'ouverture/fermeture permet de rendre le code extensible sans
pour autant modifier la mécanique interne. Concrètement l'ajout
de nouvelles fonctionnalités ne doit pas poser de problèmes
au fonctionnement de celles déjà existantes.

### - L : Substitution de Liskov (Open/closed principle)

La substitution de Liskov met en garde sur les concepts d'héritage.
En effet, d'après Liskov il est important de garder les mêmes
fondamentaux pour les objets concernant les actions
d'héritage, de surcharge et de l'utilisation de propriétés des classes.
Les classes enfants doivent avoir le même comportement que les classes
qu'elles étendent. Il doit être possible de substituer une classe
"parente" par l’une de ses classes enfants.

### - I : Séparation des interfaces (Interface segregation principle)

Le principe de séparation des interfaces renvoit à l'approche qui
consiste à créer plusieures interfaces plutot qu'une seule qui serait
plus lourde. Cette conception a l'vantage de faciliter les tests
unitaires. De facon résumé il faut implémenter uniquement
les méthodes dont on a besoin.

### - D : Inversion des dépendances (Dependency inversion principle)

Les classes de haut niveau ne devraient pas dépendre directement
des classes de bas niveau, mais d’abstractions.
En effet d'après cette approche il faut dépendre des abstractions,
pas des implémentations. L’intérêt de ce principe est de
décentraliser les dépendances pour faciliter les tests unitaires,
et effectuer la gestion des objets de la meilleure des manières.

</div>







