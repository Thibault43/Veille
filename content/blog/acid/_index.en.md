---
title: "ACID"
lead: "ACID est un acronyme désignant les propriétés de transactions
de base de données"
date: 2021-04-13T09:15:59+01:00
draft: false
contributors: ["Thibault Belledent"]
---
<div style="text-align: left">

### Définition

Le terme ACID est un moyen mnémotechnique pour se souvenir
de chacune des caractéristiques essentielles d'une transaction en
base de données : Atomicity (atomicité), Consistency (cohérence),
Isolation, Durability (durabilité).

Le terme de transaction se rapporte aux opérations qui
touchent à la modification des données.
Par exemple une transaction peut désigner un virement bancaire
provoquant le débit du compte de l’émetteur et le crédit du compte
du bénéficiaire est une transaction.

</div>

<img style="max-height: 300px" src="https://blog.cellenza.com/wp-content/uploads/2013/11/acid1.jpg">

<div style="text-align: left">

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

### - Durabilité

  La durabilité des transaction garantit que celles-ci perdurent.
  Si une transaction est interrompue inopinément dans le cas ou
  un problème survient empêchant sa validation complète,
  la transaction en question puisse être correctement terminée
  lors de la disponibilité du système.

### - Commandes SQL

```
-- Début de notre transaction
BEGIN TRANSACTION

-- nos instructions Sql
-- Par exemple une requête UPDATE et/ou DELETE

-- validation de nos instructions
COMMIT TRANSACTION

-- annulation de nos instructions
ROLLBACK TRANSACTION

-- on utilise soit un commit soit un rollback en fin de transaction
```

</div>
