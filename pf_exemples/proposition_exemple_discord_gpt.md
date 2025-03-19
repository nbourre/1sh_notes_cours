# Proposition formelle – Expérimentation technologique  
**Titre du projet** : Développement d’un bot Discord propulsé par CLAUDE pour l’automatisation des discussions  

**Date de remise** : 15 avril 2024  
**Étudiant(e)** : Claude Dupuis  
**Dépôt Git** : https://github.com/nbourre/1sh_notes_cours

---

# Introduction  
Depuis quelque temps, l’évolution fulgurante des agents conversationnels intelligents a transformé la manière dont nous interagissons avec la technologie. Les modèles de langage sont désormais capables d’assister les utilisateurs dans des tâches variées, allant de la simple recherche d’informations à la génération de contenus créatifs.

En tant que passionné par les communautés en ligne et les outils d’automatisation, j’ai toujours été fasciné par le potentiel des intelligences artificielles pour enrichir l’expérience des utilisateurs. J’anime moi-même un serveur Discord regroupant des passionnés de programmation et d’informatique, et je constate régulièrement la demande pour des assistants capables de répondre aux questions techniques, d’animer des discussions ou d’automatiser certaines tâches.

Ce projet vise donc à explorer le développement d’un bot Discord intégrant un modèle de langage avancé afin de faciliter l’interaction entre les membres d’une communauté. L’objectif est de concevoir un assistant conversationnel capable de répondre aux questions des utilisateurs, d’offrir un accompagnement personnalisé et d’assurer une présence active sur un serveur Discord.

---

# Prérecherche
Avant de choisir ce sujet, j'ai eu à explorer 5 idées qui sont les suivantes :  

| **Sujet exploré** | **Résumé** | **Pourquoi rejeté** |
|--------------|--------|----------------|
| Serveur MQTT pour l’IoT | Installation et configuration d’un broker MQTT pour connecter des capteurs IoT. | Trop axé sur les systèmes embarqués, peu d’interactions avec des utilisateurs. |
| Jeu avec un réseau de neurones | Utilisation d’un modèle de machine learning pour adapter l’intelligence artificielle d’un jeu. | Nécessite une puissance de calcul élevée, difficile à expérimenter sur un temps limité. |
| Web scraper pour l’analyse de tendances | Collecte et analyse de tendances à partir de données issues des réseaux sociaux. | Risques liés aux politiques de scraping et complexité de la gestion des données. |
| Déploiement d’un serveur Home Assistant | Installation et configuration d’un système domotique open source. | Sujet intéressant mais trop orienté infrastructure sans aspect conversationnel. |
| Bot Discord avec CLAUDE | Développement d’un bot conversationnel intelligent pour animer un serveur Discord. | Sujet retenu car accessible, utile et en lien avec mes intérêts. |

Le développement d’un bot Discord alimenté par une intelligence artificielle s’impose comme le choix idéal, car il permet d’allier programmation, automatisation et interaction avec une communauté en ligne.  


---

## Objectifs du projet  
**Objectif principal** : Développer un bot Discord capable de comprendre et répondre aux utilisateurs de manière contextuelle en utilisant CLAUDE.  

**Objectifs spécifiques :**  
- Comprendre le fonctionnement des bots Discord et l’utilisation des webhooks.  
- Intégrer une API de traitement du langage naturel (CLAUDE).  
- Déployer et tester le bot sur un serveur Discord.  
- Évaluer la qualité des interactions et ajuster les paramètres du modèle.  

---

## Méthodologie et plan de réalisation  
Le projet sera réalisé en plusieurs phases :  

### Phase 1 – Recherche et installation des outils *(Jour 1-2)*
- Étudier la documentation de Discord.py et OpenAI API.  
- Installer et configurer un bot sur Discord.  

### Phase 2 – Développement du bot *(Jour 3 à 7)*  
- Programmer un bot capable de récupérer les messages et d’y répondre via CLAUDE.  
- Implémenter une gestion de contexte pour rendre les réponses plus pertinentes.  

### Phase 3 – Tests et ajustements *(Jour 8)*  
- Tester le bot avec des utilisateurs réels sur un serveur Discord.  
- Ajuster les paramètres pour optimiser la pertinence des réponses.  

### Phase 4 – Analyse et rapport *(Jour 9)*  
- Rédaction du rapport expliquant les choix techniques et les résultats obtenus  
- Documentation du code et préparation des ressources pour un futur développement  

### Phase 5 – Présentation *(Jour 10)*
- Présenter le bot et les résultats obtenus lors d’une démonstration en direct.

---

## Outils et technologies utilisées  
- **Langage de programmation** : Python  
- **Bibliothèques** : Discord.py, OpenAI API, dotenv  
- **Plateformes** : Discord (serveur de test), GitHub (gestion de version)  

---

## Résultats attendus et critères de réussite  
**Résultats attendus**  
- Un bot fonctionnel capable d’interagir de manière cohérente avec les utilisateurs.  
- Un code propre, bien documenté et hébergé sur GitHub.  
- Une démonstration du bot en action sur un serveur Discord.  

**Critères de réussite**  
- Le bot répond aux utilisateurs avec des messages pertinents.  
- L’API de CLAUDE est bien intégrée et optimisée.  
- Un rapport final détaillé et structuré est fourni.  

---

## Conclusion  
Ce projet représente une opportunité d’approfondir mes compétences en programmation et d'en apprendre sur l'intelligence artificielle tout en mettant en place un outil utile pour les communautés en ligne. Il permettra d’explorer les possibilités offertes par les modèles de langage appliqués aux agents conversationnels, tout en répondant à un besoin concret d’automatisation et d’animation sur Discord.

