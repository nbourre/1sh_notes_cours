# Proposition formelle – Expérimentation technologique  
**Titre du projet** : Développement d’un moteur de jeux vidéo pour système embarqué  

**Date de remise** : 15 avril 2024  
**Étudiant(e)** : Tommy Houle  
**Dépôt Git** : https://github.com/nbourre/1sh_notes_cours

---

# Introduction  

Depuis que j’ai découvert la programmation, j’ai toujours été fasciné par la manière dont un programme peut donner vie à des systèmes embarqués. Ce qui me passionne particulièrement, c’est la convergence entre l’optimisation, les mathématiques appliquées et la programmation créative. J’ai expérimenté l’Arduino dans plusieurs projets, mais jusqu’ici, je n’ai jamais eu l’occasion d’explorer un microcontrôleur plus puissant comme l’ESP32.  

Récemment, mon enseignant m’a fait découvrir la librairie LVGL, un framework permettant de créer des interfaces graphiques performantes sur microcontrôleurs. Cette découverte m’a donné envie de relever un défi : développer un moteur de jeux vidéo simple pour un système embarqué basé sur l’ESP32. Ce projet me permettra d’apprendre à manipuler des concepts avancés comme l’affichage graphique optimisé, la gestion des entrées et la programmation bas niveau adaptée aux ressources limitées d’un microcontrôleur.  

---

# Prérecherche  

Avant d’arrêter mon choix sur ce projet, j’ai exploré plusieurs idées :  

| Sujet exploré | Résumé | Pourquoi rejeté |
|--------------|--------|----------------|
| Développement d’un synthétiseur audio sur Arduino | Génération de sons en utilisant des ondes et des filtres numériques. | Trop limité par la puissance de calcul des microcontrôleurs que je connais. |
| Algorithmes de rendu 3D simplifié sur ESP32 | Expérimentation de rendu de polygones et d’effets visuels sur un microcontrôleur. | Trop complexe pour un premier projet sur ESP32. |
| Automatisation d’un bras robotique via un microcontrôleur | Contrôle précis d’un bras robotisé à l’aide de servomoteurs. | Sujet intéressant, mais moins en lien avec mes intérêts pour les jeux vidéo et la programmation graphique. |
| Optimisation d’algorithmes de tri sur système embarqué | Étude comparative des performances des algorithmes de tri sur un microcontrôleur. | Utile, mais manque d’un aspect créatif et visuel. |
| Développement d’un moteur de jeux vidéo pour système embarqué | Création d’un framework de base permettant d’afficher et d’animer des éléments sur un écran géré par un ESP32. | Sujet retenu car il combine mes intérêts pour l’embarqué, les mathématiques et la programmation visuelle. |

Le projet du moteur de jeux vidéo sur ESP32 me semble être un excellent équilibre entre apprentissage technique et expérimentation créative.  

---

# Objectifs du projet  

L’objectif est de développer une première version d’un moteur permettant de créer des jeux simples sur un microcontrôleur ESP32 en exploitant la librairie LVGL.  

Les objectifs spécifiques sont les suivants :  
- Apprendre à configurer et programmer un ESP32 pour gérer un affichage graphique.  
- Explorer les fonctionnalités de LVGL et comprendre son fonctionnement interne.  
- Développer une base permettant d’afficher des sprites, gérer les entrées utilisateur et rafraîchir l’écran efficacement.  
- Expérimenter différents algorithmes pour optimiser l’affichage et la fluidité sur un système embarqué.  
- Réaliser une démonstration sous la forme d’un mini-jeu fonctionnant sur l’ESP32.  

---

# Plan de réalisation  

Le projet sera mené sur dix jours.  

**Jour 1-2 : Prise en main de l’ESP32 et de LVGL**  
- Installation des outils nécessaires pour programmer l’ESP32 (ESP-IDF ou Arduino IDE avec extensions).  
- Exploration de la documentation de LVGL et tests d’affichage basiques.  
- Affichage des premiers éléments graphiques statiques.  

**Jour 3-4 : Développement du système de rendu et de gestion des entrées**  
- Création d’une boucle de rendu permettant d’afficher et de mettre à jour des éléments dynamiques.  
- Gestion des entrées utilisateur via des boutons ou un écran tactile.  
- Optimisation des temps de rafraîchissement pour améliorer la fluidité.  

**Jour 5-6 : Ajout de mécaniques de jeu simples**  
- Mise en place d’un gestionnaire d’objets interactifs.  
- Animation d’éléments et détection de collisions basique.  
- Implémentation d’un premier prototype de mini-jeu.  

**Jour 7-8 : Tests et ajustements**  
- Amélioration de la réactivité et de l’ergonomie de l’interface.  
- Détection et correction des problèmes de performance.  

**Jour 9 : Documentation et préparation de la démonstration**  
- Rédaction d’un rapport détaillant les choix techniques et les résultats obtenus.  
- Préparation d’une démonstration du moteur en fonctionnement.  

**Jour 10 : Présentation du projet**  
- Présentation des concepts abordés et des défis rencontrés.  
- Démonstration du mini-jeu tournant sur ESP32.

---

# Outils et technologies utilisées  

- Microcontrôleur : ESP32  
- Bibliothèque graphique : LVGL  
- Outils de développement : ESP-IDF, Arduino IDE  
- Langage de programmation : C/C++  
- Matériel supplémentaire : écran TFT ou OLED compatible avec l’ESP32  

---

# Résultats attendus  

Le projet sera considéré comme réussi si :  
- Un moteur de base fonctionnel permet d’afficher des éléments graphiques et de gérer les interactions utilisateur.  
- La fluidité de l’affichage est optimisée pour être exploitable sur un ESP32.  
- Une démonstration sous la forme d’un mini-jeu simple est présentée.  
- La documentation du projet permet à un autre développeur de comprendre et d’améliorer le moteur.  

---

## Conclusion  

Ce projet représente une occasion idéale d’approfondir mes connaissances en programmation embarquée, tout en explorant les concepts fondamentaux du développement de jeux vidéo. Il me permettra de découvrir le potentiel de l’ESP32 et de me familiariser avec la librairie LVGL, tout en me donnant l’opportunité d’appliquer des notions mathématiques et algorithmiques dans un contexte créatif.  
