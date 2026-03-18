# 2. Utilisateurs et rôles

Un devis sérieux doit préciser qui utilise le système. Cette question semble simple, mais elle influence fortement la structure de l’application, la sécurité, les interfaces et la charge de développement.

## Identifier les profils d’utilisateurs

Dans un projet web, il existe rarement un seul type d’utilisateur. On retrouve souvent :

- un administrateur;
- un utilisateur authentifié;
- un invité;
- parfois un gestionnaire, un modérateur ou un partenaire externe.

Chaque profil possède des besoins, des permissions et des parcours différents. Plus le nombre de rôles augmente, plus le système devient complexe à concevoir et à tester.

## Ce qu’il faut documenter

Pour chacun des rôles, le devis devrait préciser :

- ce que la personne peut voir;
- ce qu’elle peut modifier;
- ce qu’elle peut supprimer;
- les restrictions particulières;
- les volumes d’utilisateurs attendus.

Cette étape permet d’éviter un piège classique : écrire « tableau de bord admin » dans un devis sans détailler les actions réellement permises.

## Impact sur l’estimation

Les rôles ont un impact direct sur plusieurs composantes :

- gestion des accès;
- navigation et menus;
- écrans distincts selon le profil;
- validations métier;
- cas de test supplémentaires.

Un système avec trois rôles bien distincts peut nécessiter beaucoup plus de travail qu’un système avec une seule interface commune.

## Exemple

Imagine une plateforme de réservation de locaux pour un établissement scolaire. À première vue, c'est « juste un calendrier ». Mais une fois les rôles analysés, on découvre :

- l'étudiant peut consulter les disponibilités et faire une demande;
- l'enseignant peut réserver directement pour un cours;
- le responsable technique peut bloquer un local pour entretien;
- l'administrateur peut gérer les locaux, les horaires et les utilisateurs.

Chacun de ces profils a ses propres écrans, ses règles de validation et ses cas de test. Ce qui ressemblait à une fonctionnalité unique devient rapidement quatre expériences distinctes. Sans ce découpage, le devis initial sera largement insuffisant.

## Erreurs fréquentes

- Réduire les utilisateurs à une simple liste de comptes
- Oublier les permissions détaillées
- Sous-estimer les différences d’interface selon les rôles
- Ignorer la croissance future du nombre d’utilisateurs

## Mini-checklist

- [ ] Les types d’utilisateurs sont définis
- [ ] Les permissions principales sont identifiées
- [ ] Les parcours par rôle sont décrits
- [ ] Le volume d’utilisateurs est estimé
- [ ] Les cas sensibles sont notés

## À retenir

Quand on comprend bien les utilisateurs et leurs rôles, on peut mieux évaluer la vraie portée du projet. C’est souvent là que la complexité réelle apparaît.
