# 4. Données et modèle

Tout projet web repose sur des données : comptes utilisateurs, produits, rendez-vous, documents, messages, états de processus, historiques, etc. Avant de chiffrer un développement, il faut comprendre ce qui sera stocké, comment ces éléments sont liés et quelles contraintes s’appliquent.

## Définir les entités principales

Une bonne analyse commence par l’identification des objets importants du système. Par exemple, dans une application scolaire, on pourrait retrouver :

- étudiants;
- enseignants;
- cours;
- remises;
- évaluations.

Ensuite, il faut préciser les relations entre ces entités : un-à-plusieurs, plusieurs-à-plusieurs, dépendances hiérarchiques, historique des modifications, etc.

## Pourquoi c’est crucial pour le devis

La structure des données influence :

- la base de données à utiliser;
- la complexité des écrans CRUD;
- les règles de validation;
- les performances;
- les migrations futures.

Un système avec quelques tables simples n’a pas le même coût qu’un système avec des relations multiples, des états métiers et des contraintes d’intégrité complexes.

## Questions à se poser

- Quelles données sont obligatoires?
- Quelles données sont sensibles?
- Faut-il conserver un historique ou un audit?
- Quel volume de données est attendu?
- Les données doivent-elles être importées ou exportées?

## Exemple

Un client demande un catalogue de produits en ligne. En surface : des produits avec un nom, une description et un prix. En creusant : les produits ont des variantes (taille, couleur), certains sont archivés sans être supprimés, les prix peuvent changer selon le client, et l'historique des ventes doit rester intègre même après une modification de produit. Ce qui semblait être une simple table `produits` devient un modèle relationnel avec versionnement, entités liées et règles d'intégrité. Sans ce travail en amont, la première estimation ne tient plus.

## Complexité cachée

Les devis sous-estiment souvent les cas où les données changent dans le temps : versionnement, archivage, suppression logique, permissions sur certains champs, synchronisation avec des systèmes externes. Ce sont pourtant des facteurs majeurs de charge.

## Mini-checklist

- [ ] Les entités principales sont listées
- [ ] Les relations importantes sont connues
- [ ] Les données sensibles sont identifiées
- [ ] Les besoins d’historique sont notés
- [ ] Les volumes approximatifs sont estimés

## Questions de compréhension

1. Pourquoi le modèle de données influence-t-il autant le devis?
2. Quelle différence y a-t-il entre une suppression logique et une suppression physique?
3. Donne un exemple de complexité cachée liée aux données.

<!-- 
Réponses :
1. Parce qu'il détermine la complexité des CRUD, les validations, la performance et les efforts de maintenance ou migration.
2. La suppression logique conserve l'information en l'archivant, tandis que la suppression physique retire la donnée de façon définitive.
3. Le besoin d'historiser les changements dans le temps, comme les versions de prix ou les modifications d'état d'un dossier.
-->

## À retenir

Le modèle de données constitue le squelette du projet. Plus il est clair tôt dans le processus, plus le devis est stable et plus les risques de refonte diminuent.

