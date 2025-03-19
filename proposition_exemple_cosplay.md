# Proposition formelle – Expérimentation technologique  
**Titre du projet** : Effets interactifs pour costumes Cosplay avec microcontrôleurs  

**Date de remise** : 15 avril 2024  
**Étudiant(e)** : Gabriel Lavoie  
**Dépôt Git** : https://github.com/nbourre/1sh_notes_cours 

---  

# Introduction  

Depuis plusieurs années, je participe à des événements de cosplay, des jeux d’évasion et des activités de type Grandeur Nature. Ce sont des univers immersifs où les costumes jouent un rôle clé dans l’expérience des participants. Bien que l’aspect visuel soit primordial, il manque souvent un élément interactif pour donner encore plus de vie aux personnages.  

Ce projet vise à explorer l’intégration de technologies embarquées dans un costume Cosplay afin d’ajouter des effets lumineux et interactifs en réponse aux mouvements du porteur ou aux actions des autres joueurs. Mon objectif est de rendre un costume plus immersif, en combinant programmation, électronique et design pratique.  

---  

# Prérecherche  

Avant de choisir ce sujet, j’ai réfléchi à plusieurs options :  

| Sujet exploré | Résumé | Pourquoi rejeté ? |
|--------------|--------|------------------|
| **Petit jeu avec PowerShell** | Créer un mini-jeu textuel interactif dans la console. | Trop limité graphiquement, manque d’expérimentation matérielle. |
| **Interpréteur BrainF*ck avec Godot** | Intégrer un interpréteur de langage minimaliste dans un moteur de jeu. | Peu d’application pratique, ne correspond pas à un projet expérimental. |
| **IA pour les pools de hockey** | Utiliser des modèles statistiques pour prédire les résultats des matchs. | Sujet purement logiciel, ne touche pas aux systèmes embarqués. |
| **Arduino et Rust** | Expérimenter la programmation bas niveau en Rust sur microcontrôleur. | Trop complexe à maîtriser en si peu de temps. |
| **Effets interactifs en Cosplay** | Intégration de capteurs et d’éclairage programmable dans un costume. | Sujet retenu : il combine mes intérêts personnels et un défi technique accessible. |

L’intégration de microcontrôleurs dans un costume m’attire particulièrement, car cela allie la créativité du design de costume à la programmation embarquée et aux effets visuels interactifs.  

---  

# Objectifs  

Ce projet a pour but de concevoir un système embarqué interactif pour un costume Cosplay.  

Les objectifs sont les suivants :  
- Concevoir un module portable et léger qui peut être intégré dans un costume.  
- Programmer un microcontrôleur pour contrôler un ensemble de LED RGB adressables.  
- Utiliser des capteurs (mouvement, pression, toucher) pour déclencher des effets lumineux en fonction des actions du porteur.  
- Tester et ajuster l’interactivité en conditions réelles.  

L’idée est de créer un système réutilisable qui pourrait être adapté à d’autres costumes ou scénarios de jeu immersifs.  

---  

# Plan de réalisation  

Étant donné que le cours est intensif et se déroule sur 10 jours, la réalisation sera organisée en phases rapides.  

**Jour 1 : Exploration et choix du matériel**  
- Étude des microcontrôleurs adaptés aux costumes (Arduino Nano, ESP32, Raspberry Pi Pico).  
- Choix des capteurs et des LED en fonction des contraintes de taille, de poids et d’autonomie.  
- Premiers tests de connexion et programmation de base.  

**Jour 2 à 4 : Prototype du circuit et premiers tests**  
- Assemblage du circuit sur une plaque d’essai (breadboard).  
- Écriture du code initial pour allumer et animer les LED RGB.  
- Tests des capteurs et validation des premières interactions.  

**Jour 5 à 8 : Intégration au costume et optimisations**  
- Installation des composants sur un costume réel.  
- Ajustements pour améliorer la réactivité des capteurs.  
- Optimisation de la gestion de l’énergie pour maximiser l’autonomie de la batterie.  

**Jour 9 : Tests finaux et documentation**  
- Rédaction du rapport de projet et documentation du code.  
- Réflexion sur les améliorations possibles et extensions futures.  

**Jour 10 : Présentation et démonstration**
- Présentation du costume et des fonctionnalités devant le groupe.


---  

# Technologies et matériel utilisé  

- **Microcontrôleur** : ESP32 (Wi-Fi/Bluetooth intégré pour futures améliorations)  
- **Capteurs** : Accéléromètre (MPU6050) pour détecter les mouvements, capteur tactile pour interactions manuelles  
- **Éclairage** : LED RGB WS2812B (NeoPixels)  
- **Batterie** : Li-Po 3.7V avec régulateur de tension  
- **Environnement de développement** : Arduino IDE, PlatformIO, Python pour l’analyse des données  

---  

# Résultats attendus  

Si tout se déroule comme prévu, le costume sera équipé d’un système interactif réactif aux mouvements et aux gestes.  

Ce projet sera réussi si :  
- Le circuit fonctionne de manière autonome sans câbles encombrants.  
- Les effets lumineux s’adaptent bien aux actions du porteur.  
- Le code est optimisé et bien documenté.  
- Le système est confortable à porter et facilement réutilisable pour d’autres projets.  

Une démonstration vidéo du costume en fonctionnement sera fournie avec le rapport final.  

---  

# Conclusion  

Ce projet me permet de lier mes intérêts pour le Cosplay, les jeux immersifs et la technologie embarquée. Il offre un défi technique accessible, tout en étant pratique et applicable pour des événements futurs. L’ajout d’un système interactif à un costume ouvre la porte à de nouvelles façons d’explorer les technologies dans le domaine du spectacle et du jeu immersif.  

