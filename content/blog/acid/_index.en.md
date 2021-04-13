---
title: "ACID"
lead: "ACID est un acronyme désignant les propriétés de transactions
de base de données"
date: 2021-04-13T09:15:59+01:00
draft: false
type: "plugins"
logo: "akeneo"

---

### Définition

Le terme ACID est un moyen moyen mnémotechnique pour se souvenir
de chacune des caractéristiques essentielles d'une base de
données: Atomicity (atomicité), Consistency (cohérence),
Isolation, Durability (durabilité).

Le terme de transaction se rapporte aux opérations qui
touchent à la modification des données.
Par exemple une transaction peut désigner un virement bancaire
provoquant le débit du compte de l’émetteur et le crédit du compte
du bénéficiaire est une transaction.

<img style="max-height: 300px" src="https://blog.cellenza.com/wp-content/uploads/2013/11/acid1.jpg">

### Les termes

### - Atomicité
  Ce terme signifie que la transaction doit s'effectuer dans
  son entièreté ou pas du tout. En effet la transaction ne
  doit jamais s'éxécuter partiellement car ceci peut avoir
  de lourdes conséquences. Dans le processus de création,
  des étapes sont souvent dépendantes d'autres, ce qui peut
  provoquer des actions erronées bien loin de ce l'on attends.

### - Cohérence
  La cohérence dans les transactions signifie qu'elles doivent
  respecter les [contraintes d’intégrité](https://fr.wikipedia.org/wiki/Contrainte_d%27int%C3%A9grit%C3%A9)
  des données de la base de données.

### - Isolation

  Le principe d'isolation renvoit au fait que la lecture et
  l'écriture d'une transaction n'est pas affectée par d'autres
  transactions car chacune des transaction est isolée des autres.
  On parle de transactions optimistes et péssimistes.
  Dans le cas des transactions optimistes, on part du principe
  que la transaction a réussi

### Les limites liées à un ORM

- L'utilisation d'un ORM peut alourdir un projet de façon
  conséquente.

- Plus lents que les requêtes SQL basiques.

- Configuration parfois fastidieuse.
