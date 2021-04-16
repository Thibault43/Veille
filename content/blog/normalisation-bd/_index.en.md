---
title: "Normalisation d'une base de données"
lead: "La normalisation d'une base de données est un processus
qui permet d'éliminer les informations redondantes"
date: 2021-04-15T09:15:59+01:00
draft: false
contributors: ["Thibault Belledent"]
---
<div style="text-align: left">

### Qu'est-ce que la normalisation d'une base de données

La normalisation d'une base de données implique une restructuration
du schéma de celle-ci.

Une base est dite normalisée lorsque les règles du modèle conceptuel
réponds à des critères tels que :

- l'intégrité des données qui renvoit aux principes que les
  informations stockées dans la base de données doivent rester
  complètes, exactes et fiables, indépendamment de leur durée
  de stockage et du nombre de fois que l’on y accède.

- la facilité de mise à jour des données.

- la non redondance des données, Les tables ne doivent pas
  contenir des groupes de données répétitives

L'intérêt de la normalisation réside dans le fait de simplifier
l'ajout, l'éffacement ou la modification d'un champs en modifiant
une seule table grâce aux relations définit entre elles.

### Quels sont les avantages de la normalisation des données

Ce processus permet tout d'abord de réduire efficacement la
réplication des données en vue de réduire sa taille. La normalisation
des données permet également de simplifier la maintenance de la base,
ce processus permet une organisation plus logique des données. En effet
les données d'applications sont plus faciles à maintenir.


### Quels sont les limites au processus de normalisation des données

La normalisation permet donc une meilleure structuration du schéma
de base de données cependant les opérations de traitement peuvent
se retrouver ralenties. La restructuration du système peut passer
par de nombreuses jointures, les requêtes sur les données peuvent être
très lentes par la présence de nombreuses clés étrangères entre les
différentes tables.

### - Les formes de normalisation

|Forme|Implication|
|--- |--- |
|1NF First Normal Form|Chaque table doit avoir une clef primaire.Il faut éliminer les colonnes en doublon. Chaque ligne doit contenir une seule valeur.|
|2NF Second Normal Form|Si une table dispose d'une clef, toutes les propriétés doivent en dépendre : les données que l'on retrouve dans plusieurs lignes doivent être sorties dans une table séparée.|
|3NF Third Normal Form|Les données d'une table ne dépendent que de la clef, et pas d'une autre colonne de la table : toute colonne dépend non seulement de la clef, mais également d'une autre colonne qui doit être sortie dans sa propre table.|
|BCNF Boyce-Cod Normal Form|Aucune propriété faisant partie de la clef d'une relation 3NF, ne doit dépendre d'une propriété ne faisant pas partie de la clef primaire. Il faut donc créer une nouvelle table dont la clef primaire sera la propriété dont provient la relation.|
|4NF Fourth Normal Form|Il ne doit y avoir qu'une et une seule dépendance multivaluée élémentaire.|
|5NF Fifth Normal Form|Toute dépendance de jointure est impliquée par des clefs candidates de la relation.|
|Domaine/key Normal Form|Il ne doit exister aucune contrainte sinon celles de domaine ou de clef.|
|6NF Sixth Normail Form|La sixième forme, encore récente, demande à prendre en compte la dimension temporelle.|

La normalisation est pertinente que si elle permet vraiment de
décomposer des relations complexes en des relations plus simples,
en outre si elle offre réellement une meilleure organisation des données
car parfois elle peut amener à une structure inutilement complexe.

</div>







