Traduction de l'article : https://nmn.gl/blog/dangers-vibe-coding

# Le mouvement du *vibe coding* est considéré dangereux

Mardi dernier à 1 h du matin, je déboguais un problème critique en production dans mon outil de développement IA. En creusant à travers les couches de fonctions, j’ai soudain réalisé — contrairement à la nouvelle génération de développeurs, j’étais reconnaissant de réellement comprendre ma base de code. C’est à ce moment-là que j’ai commencé à réfléchir davantage aux récentes déclarations de Karpathy sur le *vibe coding*.

Pour ceux qui l’auraient manqué, Andrej Karpathy a récemment partagé ses réflexions sur ce qu’il appelle le *vibe coding* — qui consiste essentiellement à abandonner la compréhension du code aux outils d’IA, en espérant que tout se passe bien. Ses mots exacts ? « J’accepte tout, toujours. Je ne lis plus les différences. »

J’ai beaucoup appris de Karpathy et j’utilise des outils d’IA quotidiennement, mais il y a une énorme différence entre augmenter ses capacités et abandonner complètement sa compréhension.

# Les coûts cachés du « coding à la vibe »

Le mois dernier, j’ai rencontré un bogue particulièrement frustrant dans mon système de paiement. Le code semblait propre — (puisque ChatGPT m’avait aidé à l’écrire). Mais quand les utilisateurs ont commencé à signaler des problèmes aléatoires de paiements non reconnus, je ne pouvais pas simplement copier l’erreur dans une IA et prier. Je devais comprendre la logique sous-jacente de gestion des paiements et le déroulement exact des requêtes pour corriger le problème.

C’est là que le « coding à la vibe » s’effondre. Le vrai problème ne réside pas uniquement dans la lecture du code — c’est une question de conserver la maîtrise intellectuelle de nos systèmes. Quand Karpathy dit : « Le code dépasse ma compréhension habituelle, je devrais vraiment le relire en détail pendant un moment », il décrit un [effondrement fondamental de la responsabilité en ingénierie](https://nmn.gl/blog/ai-illiterate-programmers).

# Une dette technique exponentielle

La dette technique croît de façon exponentielle lorsqu’on ne comprend pas son propre code. Chaque solution « improvisée à la vibe » devient une boîte noire, et ces boîtes noires se multiplient. Rapidement, on construit des systèmes entiers sur des fondations qu’on ne comprend pas.

Une fonctionnalité que j’ai récemment implémentée a d’abord suivi cette voie. La solution générée par l’IA fonctionnait, mais lorsque j’ai voulu l’optimiser pour la performance, j’étais bloqué. On ne peut pas optimiser ce qu’on ne comprend pas. J’ai fini par tout réécrire depuis zéro, en m’assurant cette fois de comprendre chaque ligne de code.


# Cauchemar de sécurité

Les [implications en matière de sécurité](https://nmn.gl/blog/vibe-coding-fantasy) du *vibe coding* sont… irréelles. Quand on ne comprend pas son code, on ne peut pas correctement en évaluer les vulnérabilités.

La semaine dernière, j’ai examiné du code d’authentification généré par une IA, qui semblait parfaitement correct au premier coup d'œil. Mais en y regardant de plus près, les clés API d’OpenAI étaient exposées à toute personne sachant inspecter les appels réseau. Ce genre d’erreur se produit quand on fait confiance à l’IA sans comprendre les bonnes pratiques de sécurité.

# Une meilleure voie à suivre

Le véritable danger ne réside pas dans l’utilisation de l’IA — mais dans le fait de lui abandonner notre compréhension. Programmer « à la vibe » peut fonctionner pour un projet de fin de semaine, mais c’est catastrophique pour tout logiciel sérieux.

En développant mon IA destinée à [accélérer le développement logiciel](https://gigamind.dev/), j’ai mis en place une approche rigoureuse qui équilibre l’assistance de l’IA avec l’exigence de qualité en ingénierie :

* **Avant d’utiliser des outils d’IA**, commencez par une vision architecturale claire. Avant de générer une seule ligne de code, documentez vos exigences, vos contraintes et le comportement attendu. Ce document devient votre cadre de validation pour tout code généré par l’IA.

* **Plutôt que d’accepter des fonctions ou des composants entiers**, décomposez-les en morceaux plus petits et compréhensibles. J’ai développé un processus en trois étapes :

  1. Générer de petits blocs de fonctionnalités ciblées
  2. Revoir et comprendre chaque bloc en profondeur
  3. Intégrer seulement après validation et tests

* [**L’IA doit avoir une compréhension complète de votre projet**](https://gigamind.dev/), incluant :

  * La raison d’être du projet
  * La logique d’affaires (le « pourquoi », pas seulement le « comment »)
  * L’interaction entre les différentes parties du projet
  * L’utilisation et l’intégration des dépendances tierces importantes
  * L’explication du schéma de données et des modèles

* **Élaborez une stratégie de tests qui vous oblige à comprendre le code** :

  * Rédiger les tests avant d’accepter du code généré par l’IA
  * Tester explicitement les cas limites
  * Mettre en place des tests d’intégration pour vérifier le comportement global du système (ou le faire manuellement à défaut)

* **Même en tant que développeur solo**, je maintiens un processus strict de révision de code pour tout ce qui est généré par IA :

  * Revoir chaque portion de code comme si elle avait été écrite par un développeur junior
  * Vérifier les implications en matière de sécurité
  * S’assurer d’un bon traitement des erreurs

