# 11. Tests et qualité

Un système qui fonctionne « en apparence » n’est pas forcément prêt à être livré. Les tests et la qualité assurent que le produit répond aux attentes, résiste aux cas limites et demeure stable lorsque le projet évolue.

## Les différentes formes de validation

Selon la nature du projet, on peut prévoir :

- des tests unitaires;
- des tests d’intégration;
- de la validation manuelle;
- des tests multi-navigateurs;
- des tests d’acceptation;
- parfois des tests de charge ou de sécurité.

Le bon niveau de qualité dépend du contexte. Un prototype n’aura pas les mêmes exigences qu’un système utilisé en production.

## Pourquoi il faut le chiffrer explicitement

Quand les tests ne sont pas inclus dans le devis, ils deviennent souvent une activité invisible absorbée en fin de projet. Résultat : dépassements, bogues non détectés ou réduction forcée de la qualité.

Prévoir du temps pour la qualité permet de :

- détecter les régressions;
- valider les parcours critiques;
- fiabiliser les livraisons;
- réduire le coût des corrections tardives.

## Exemple

Une équipe livre une fonctionnalité de remise de travaux pour une plateforme scolaire. Sans tests planifiés, les vérifications manuelles sont faites à la va-vite avant la démo. Un cas limite n'est pas testé : que se passe-t-il si deux étudiants soumettent en même temps avec le même nom de fichier? L'application écrase l'un des deux fichiers silencieusement. Ce bogue, découvert trois semaines après la mise en ligne, nécessite une correction urgente, une analyse des données affectées et une communication aux enseignants. Prévoir deux heures de tests structurés aurait évité plusieurs jours de gestion de crise.

## Questions à poser

- Quel niveau de qualité est attendu?
- Quelles fonctionnalités sont critiques?
- Qui fera les tests d’acceptation?
- Quels navigateurs ou appareils doivent être pris en charge?
- Faut-il automatiser une partie des tests?

## Mini-checklist

- [ ] Le niveau de test attendu est clarifié
- [ ] Les parcours critiques sont identifiés
- [ ] Les responsabilités de QA sont définies
- [ ] Les plateformes à couvrir sont connues
- [ ] Le temps de correction est considéré

## Questions de compréhension

1. Pourquoi les tests doivent-ils apparaître explicitement dans le devis?
2. Quelle différence entre tests unitaires et tests d'intégration?
3. Quel est un effet fréquent d'une QA sous-estimée?

<!-- 
Réponses :
1. Parce qu'ils demandent du temps et réduisent le risque de régressions, de bogues critiques et de corrections coûteuses en fin de projet.
2. Les tests unitaires valident un composant isolé, alors que les tests d'intégration valident l'interaction entre plusieurs composants.
3. Des bogues détectés après livraison, entraînant des urgences et une perte de confiance.
-->

## À retenir

Les tests ne sont pas un luxe. Dans un devis, ils représentent une assurance qualité qui protège à la fois le client et l’équipe de développement.

