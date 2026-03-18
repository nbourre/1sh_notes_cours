# 5. Fonctionnalités

Le cœur d’un devis, c’est la description de ce que le système doit faire. Cette partie semble évidente, mais elle demande plus que de simples mots-clés comme « dashboard », « formulaire » ou « CRUD ». Il faut découper les besoins en fonctionnalités observables et estimables.

## Décrire les fonctions de manière utile

Une fonctionnalité bien formulée précise généralement :

- l’action réalisée;
- le rôle concerné;
- les données manipulées;
- les règles métier;
- le résultat attendu.

Par exemple, « gérer les rendez-vous » est trop vague. Une meilleure formulation serait : « permettre à un client de créer une demande, permettre à un employé de confirmer l’horaire et envoyer une notification lors d’un changement ».

## Pourquoi le découpage compte

Plus les fonctionnalités sont découpées finement, plus l’estimation devient réaliste. Cela permet de distinguer :

- les fonctionnalités simples;
- les fonctionnalités moyennes;
- les fonctionnalités à fort risque;
- les éléments optionnels ou de phase 2.

Ce découpage aide aussi à prioriser un MVP.

## Exemples de blocs fréquents

Dans un projet web, on retrouve souvent :

- opérations CRUD;
- recherche, tri et filtres;
- notifications;
- téléversement de fichiers;
- tableaux de bord;
- workflows d’approbation;
- exports PDF ou CSV.

## Exemple

Un client dit : « je veux pouvoir gérer mes clients ». Dans le devis, cette phrase pourrait valoir entre 5 heures et 50 heures selon ce qu'elle signifie réellement. Une analyse rigoureuse révèle :

- créer un client avec ses coordonnées;
- modifier ses informations;
- désactiver un client sans le supprimer;
- chercher un client par nom, courriel ou numéro;
- exporter la liste en CSV;
- associer des notes internes à un client.

Chacun de ces éléments est une tâche estimable. L'ensemble représente un bloc cohérent, bien délimité, qu'on peut intégrer dans un devis précis.

## Risques d’une mauvaise formulation

Si une fonctionnalité est mal définie, le devis devient fragile. On peut croire avoir prévu « la gestion des documents », puis découvrir plus tard qu’il faut aussi la prévisualisation, la version, la validation de format, le partage et l’historique.

## Mini-checklist

- [ ] Les fonctionnalités sont formulées en actions concrètes
- [ ] Les rôles concernés sont précisés
- [ ] Les règles métier importantes sont documentées
- [ ] Les dépendances entre fonctionnalités sont connues
- [ ] Les options de phase 2 sont séparées

## À retenir

Un bon devis repose moins sur une longue liste de mots à la mode que sur un découpage clair des comportements attendus du système.
