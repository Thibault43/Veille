---
title: "Base de données NoSQL"
lead: "Le NoSQL définit les bases de données qui n'incluent pas
uniquement du SQL (not only SQL)."
date: 2021-04-13T09:15:59+01:00
draft: false
contributors: ["Thibault Belledent"]
---
<div style="text-align: left">

### Qu'est-ce que le NoSQL

Développé à l'origine pour gérer du Big data ou des données cloud,
le NoSQL désigne les bases de données qui ne repose pas sur
l'architecture relationnelle.

Le NoSQL permet de gommer les limites des bases de données
relationnelles, en effet les bases de données NoSQL visent
à enrichir les systèmes traditionnels c'est un complément
utile des bases de données SQL relationnelles.


Le terme de transaction se rapporte aux opérations qui
touchent à la modification des données.
Par exemple une transaction peut désigner un virement bancaire
provoquant le débit du compte de l’émetteur et le crédit du compte
du bénéficiaire est une transaction.

</div>

<img style="max-height: 200px" src="https://cdn.ourcodeworld.com/public-media/articles/articleocw-5d78ebb022d1e.webp">

<div style="text-align: left">

### Pour quelles raisons utiliser le NoSQL

Les bases de données NoSQL sont apparues pour corriger les
problèmes de performance liés aux bases de données relationnelles.
En effet, le traitement de gros volumes de données peut entrainer de
lourdes pertes de performances.

Le NoSQL constitue une alternative face aux restrictions
et problèmes liés aux bases de données relationnelles.
Les bases de données NoSQL ont une meilleure scalabilité
car elles permettent d'avoir une installation distribuée sur plusieurs
serveurs. Le NoSQL prends en compte la dimension des serveurs Cloud,
la montée en charge s'effectue simplement par l'ajout de serveurs
supplémentaires.

### Les différents types de base de données NoSQL

### - Système Clé/Valeur

Dans ce type de base de données la valeur est associée à une clé
qui peut être un document, un objet complexe, ou encore une chaine de
caractères, la valeur est une donnée non structurée. Elle est
principalement faite pour le stockage temporaire.

Ces systèmes sont utilisés dans la gestion de panier d'achat mais encore dans la collecte d'évènements.
</div>

<img style="max-height:150px" src="https://itecsoftware.com/wp-content/uploads/2010/08/high-speed-redis-cache-300x200.jpg"/>

<img style="max-height:200px" src="https://www.signifytechnology.com/rails/active_storage/representations/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBemREQlE9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--99fee9b86456b609b9db8e61e1bf743d734b6f61/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCam9MY21WemFYcGxTU0lOT1RBd2VEa3dNRDRHT2daRlZBPT0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--c2f21ccfe76283a8dd7a61c6749f4ee3c5f33e43/600_464088012.jpeg"/>

<div style="text-align: left">

### - Système en colonnes

Ce système de base de données stocke des données dans des tables
qui à l'intérieur contiennent des "colonnes" à l'inverse
des bases de données relationnelles où les données sont par rangées.

Ce type de base offre de hautes performances lorsqu'il s'agit de traitements et de parcours de gros volume de données.

Ce système est utilisé dans les applications analytiques de traitements
de données ainsi que les applications Web à grande échelle.

</div>

<img style="max-height:200px" src="https://www.dblandit.com/img/educacion/cassandra.jpg"/>

<img style="max-height:200px" src="https://miro.medium.com/max/350/1*5i1_LPEiMqqEuAmYhcmcIw.png"/>

<div style="text-align: left">

### - Système orientés document

Les bases de données orientées documents utilisent des structures de
données complexes. Les documents ont habituellement un format particulier
tels que le JSON, BSON, XML et d'autres.

Ce type de base de données est principalement adapté pour les systèmes
de gestion de contenu tels que les blogs ou encore les plateformes vidéos,

</div>

<img style="max-height:125px" src="https://www.lemagit.fr/visuals/LeMagIT/hero_article/MongoDB_searchsitetablet_520X173.jpg"/>

<div style="text-align: left">
MongoDB est une base de données NoSQL
</div>
<img style="max-height:200px" src="http://allvectorlogo.com/img/2016/04/ravendb-logo.png"/>

<div style="text-align: left">

### - Système en graphes

Les bases de données en graphes se prête particulièrement bien pour certains
types de données. Basé sur le système de noeuds et d'arêtes
[cf théorie des graphes](https://fr.wikipedia.org/wiki/Th%C3%A9orie_des_graphes).
Les bases de données graphiques sont très utiles lorsque les
informations sont fortement interconnectées et offrent des performances
très nettement supérieures aux bases de données relationnelles.

Ce type de base de données est très utilisé pour les réseaux sociaux.

</div>

<img style="max-height:200px" src="https://miro.medium.com/max/2240/1*Ksia5B3z9LrSDC7NILmyWw.png"/>

