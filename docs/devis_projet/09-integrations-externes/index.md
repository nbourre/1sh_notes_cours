# 9. Intégrations externes

Un projet web moderne dépend rarement uniquement de son propre code. Paiement, courriels, SMS, cartes, stockage, authentification ou CRM : chaque intégration externe ajoute de la valeur, mais aussi du temps, des dépendances et des risques.

## Pourquoi une intégration coûte plus qu’on pense

Connecter une API externe ne consiste pas seulement à appeler un endpoint. Il faut aussi :

- lire la documentation;
- configurer les accès;
- gérer les erreurs;
- tester les cas limites;
- surveiller les changements de version;
- parfois gérer une facturation ou des quotas.

Même une intégration simple peut demander plusieurs allers-retours de validation.

## Exemples courants

Dans un devis, on voit souvent :

- Stripe ou une autre passerelle de paiement;
- envoi de courriels transactionnels;
- SMS;
- API gouvernementales ou institutionnelles;
- webhooks;
- SSO ou OAuth.

## Ce qu’il faut clarifier

- Quels services externes sont obligatoires?
- Qui fournit les accès et les clés?
- Y a-t-il un environnement de test?
- Que doit-il se passer en cas d’échec?
- L’intégration est-elle synchrone ou asynchrone?

## Exemple

Un client demande un système de réservation avec paiement en ligne via Stripe. En apparence, c'est « juste une ligne de code ». En pratique, il faut créer un compte Stripe, comprendre le flux webhooks pour confirmer les paiements, gérer les remboursements, tester avec les cartes de test, gérer les erreurs réseau et journaliser les transactions. L'intégration demande typiquement entre 8 et 15 heures selon la complexité. Si elle n'est pas explicitement chiffrée dans le devis, elle sera absorbée dans la marge ou causera un dépassement.

## Risques associés

Une intégration externe introduit des éléments hors de votre contrôle : pannes, limitations, changements de politique, délais de réponse variables, approbations manuelles ou contraintes contractuelles. Le devis doit donc intégrer une marge réaliste.

## Mini-checklist

- [ ] Les services externes sont listés
- [ ] Les accès nécessaires sont identifiés
- [ ] Les scénarios d’erreur sont prévus
- [ ] Les environnements de test sont confirmés
- [ ] Le risque d’intégration est pris en compte

## Questions de compréhension

1. Pourquoi une intégration externe ajoute-t-elle du risque dans un projet?
2. Nomme deux tâches à prévoir lors d'une intégration API.
3. Quelle information doit être clarifiée tôt avec le client pour éviter les blocages?

<!-- 
Réponses :
1. Parce qu'elle dépend d'un service hors de contrôle de l'équipe (pannes, quotas, changements d'API, délais).
2. La gestion des erreurs et la validation du flux complet dans un environnement de test.
3. Qui fournit les accès, les clés API et les comptes nécessaires à l'intégration.
-->

## À retenir

Chaque intégration externe mérite son propre bloc d’analyse. Dans un devis, la connecter n’est jamais « juste un petit plus ».

