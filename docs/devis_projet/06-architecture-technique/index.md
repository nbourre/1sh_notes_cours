# 6. Architecture technique

Après avoir clarifié les besoins, il faut décider comment le système sera construit. L’architecture technique regroupe les choix structurants : frontend, backend, base de données, API, organisation du code et stratégie globale de déploiement logiciel.

## Les décisions typiques

Dans un devis, cette section peut inclure :

- le framework frontend;
- la technologie backend;
- le type d’API;
- la base de données;
- l’architecture monolithique ou modulaire;
- les services tiers nécessaires.

Le but n’est pas de produire un document d’architecture complet, mais de repérer les décisions qui influencent fortement le temps, le risque et la maintenance.

## Pourquoi ces choix changent l’estimation

Une architecture simple et connue par l’équipe réduit généralement le temps de développement. À l’inverse, une architecture plus distribuée, ou bâtie sur des technologies moins maîtrisées, peut exiger davantage de temps en mise en place, intégration, débogage et observabilité.

Par exemple, une application monolithique avec API REST et base PostgreSQL sera souvent plus rapide à démarrer qu’une solution microservices complète avec files de messages, passerelle API et plusieurs déploiements séparés.

## Questions pertinentes

- Faut-il séparer frontend et backend?
- Le projet nécessite-t-il une API publique?
- L’équipe connaît-elle bien les technologies choisies?
- Le système doit-il être très modulaire ou simplement maintenable?
- Y a-t-il des contraintes institutionnelles sur la pile technologique?

## Exemple

Un groupe d'étudiants veut construire une application de suivi de présences pour leur établissement. Leur première idée : microservices, Kubernetes, GraphQL et une application mobile native. Après réflexion sur les objectifs, le délai et leurs compétences, ils optent pour une API REST simple avec un serveur Node.js, une base de données PostgreSQL et une interface React. Ce choix réduit la complexité de déploiement, accélère le développement et correspond mieux aux besoins réels. L'architecture la plus sobre qui répond aux besoins est presque toujours la meilleure pour un premier devis.

## Pièges fréquents

- Choisir une architecture trop ambitieuse pour le contexte
- Décider d’un empilement technique avant d’avoir clarifié les besoins
- Sous-estimer le coût de la maintenance technique
- Confondre flexibilité future et complexité immédiate

## Mini-checklist

- [ ] Les technologies principales sont identifiées
- [ ] Les raisons de ces choix sont claires
- [ ] L’architecture est proportionnelle au projet
- [ ] Les risques techniques sont connus
- [ ] Les besoins de maintenance sont considérés

## Questions de compréhension

1. Pourquoi l'architecture doit-elle être proportionnelle au projet?
2. Quelle est une question utile avant de choisir une pile technologique?
3. Donne un exemple d'arbitrage architectural pertinent dans un devis.

<!-- 
Réponses :
1. Une architecture trop ambitieuse augmente la complexité, les délais et les risques sans nécessairement apporter de valeur immédiate.
2. Il faut vérifier si l'équipe maîtrise réellement les technologies envisagées.
3. Choisir un monolithe simple plutôt qu'une architecture microservices quand les besoins et les ressources sont limités.
-->

## À retenir

L’architecture technique doit soutenir les objectifs du projet, pas les compliquer. Dans un devis, la bonne question n’est pas « quelle architecture est la plus impressionnante? », mais « quelle architecture est la plus adaptée? »

