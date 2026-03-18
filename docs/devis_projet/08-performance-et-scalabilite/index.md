# 8. Performance et scalabilité

Tous les projets n’ont pas besoin d’une architecture massivement scalable, mais tous les projets doivent avoir un niveau de performance minimal acceptable. Cette section du devis sert à préciser les attentes de rapidité, de volume et de stabilité.

## Comprendre le besoin réel

La première question n’est pas « comment optimiser? », mais « quel usage doit-on supporter? ». Un portail interne utilisé par dix personnes n’a pas les mêmes contraintes qu’une plateforme publique consultée en continu.

Il faut donc clarifier :

- le nombre d’utilisateurs simultanés;
- la fréquence des requêtes;
- le volume de données;
- les temps de réponse attendus;
- la présence ou non de temps réel.

## Pourquoi cela change le devis

Quand les exigences de performance montent, il faut souvent prévoir :

- de la mise en cache;
- de la pagination;
- une meilleure indexation;
- des optimisations de requêtes;
- parfois un CDN, Redis ou une architecture plus distribuée.

Ces choix ajoutent du temps de développement, de validation et de surveillance.

## Exemple

Une école veut un tableau de bord pour suivre en temps réel la présence dans ses ateliers. À première vue, c'est une fonctionnalité simple. Mais « temps réel » signifie ici que les données doivent se mettre à jour toutes les 10 secondes, pour 200 postes simultanément. Sans cette précision, un développeur peut produire une solution qui fonctionne en démo avec 5 utilisateurs mais qui crashe le jour de la mise en ligne. Identifier ce besoin tôt permet de prévoir WebSockets ou Server-Sent Events, d'ajuster le dimensionnement et d'intégrer ce coût au devis.

## Cas typiques

Certaines situations justifient une attention particulière :

- tableaux de bord mis à jour fréquemment;
- flux d’événements en temps réel;
- recherche dans de grands ensembles de données;
- importation ou exportation volumineuse;
- applications utilisées à des heures de pointe.

## Erreurs fréquentes

- Supposer que la performance se règlera plus tard sans impact
- Ne pas chiffrer les besoins de temps réel
- Confondre « rapide » avec une exigence mesurable
- Surconcevoir pour des besoins très modestes

## Mini-checklist

- [ ] Les attentes de performance sont formulées
- [ ] Les volumes d’usage sont estimés
- [ ] Les besoins de temps réel sont identifiés
- [ ] Les optimisations nécessaires sont connues
- [ ] Le niveau de scalabilité visé est proportionné

## À retenir

La performance fait partie des exigences du produit. Si elle n’est pas définie, elle devient une source d’ambiguïté et de surprises dans le devis.
