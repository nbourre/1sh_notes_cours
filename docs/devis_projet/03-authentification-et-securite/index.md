# 3. Authentification et sécurité

La sécurité ne doit jamais être ajoutée à la fin d’un devis comme une note secondaire. Dès qu’un système gère des comptes, des données ou des permissions, il faut prévoir les mécanismes d’authentification, d’autorisation et de protection des informations.

## Ce que couvre cette section

Dans un devis, l’authentification et la sécurité peuvent inclure :

- connexion par courriel et mot de passe;
- connexion avec un fournisseur externe comme Google ou Microsoft;
- récupération de mot de passe;
- double facteur d’authentification;
- gestion des sessions;
- journalisation et traçabilité;
- protection des données sensibles.

## Pourquoi cela influence fortement le coût

Une simple page de connexion ne représente qu’une petite partie du travail. Il faut aussi prévoir :

- la validation des entrées;
- le stockage sécurisé des mots de passe;
- la gestion des erreurs;
- les expirations de session;
- les contrôles d’accès selon les rôles;
- les obligations légales ou institutionnelles.

Chaque exigence de sécurité augmente les tests, la conception et parfois même l’infrastructure.

## Points à clarifier avec le client

- Qui doit pouvoir se connecter?
- Quels rôles ont accès à quelles sections?
- Faut-il utiliser un fournisseur SSO ou OAuth?
- Le système manipule-t-il des données personnelles ou sensibles?
- Existe-t-il des contraintes de conformité?

## Exemple

Un client demande un système de gestion de commandes pour ses employés. Il dit simplement « il faut se connecter ». Derrière cette phrase se cachent plusieurs décisions : connexion par courriel et mot de passe ou liaison avec le compte Google de l'entreprise? Que se passe-t-il si un employé part? Faut-il un journal des actions pour tracer qui a modifié quoi? Le client ne sait pas forcément que ces questions existent, mais elles ont un impact direct sur le temps de développement. Les poser tôt évite des malentendus coûteux.

## Cas souvent oubliés

Plusieurs devis oublient des fonctionnalités pourtant essentielles :

- réinitialisation du mot de passe;
- verrouillage d’un compte après plusieurs tentatives;
- audit des actions critiques;
- gestion des utilisateurs inactifs;
- messages d’erreur sécuritaires.

## Mini-checklist

- [ ] Le mode d’authentification est choisi
- [ ] Les permissions sont définies
- [ ] Les données sensibles sont identifiées
- [ ] Les obligations de conformité sont connues
- [ ] Les cas de récupération et de journalisation sont prévus

## À retenir

La sécurité coûte toujours moins cher quand elle est prévue au début. Dans un devis, elle doit être traitée comme un bloc fonctionnel à part entière.
