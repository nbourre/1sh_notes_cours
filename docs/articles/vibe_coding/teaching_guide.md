# Cours-synthèse : Vibe coding

## Contexte
Ce cours est conçu comme **dernier cours de la formation**. L’objectif n’est pas de faire du « wow IA », mais de démontrer une pratique professionnelle : utiliser l’IA pour accélérer le développement **sans perdre la compréhension, la qualité ni la responsabilité**.

Référence principale : [What is vibe coding? (Google Cloud)](https://cloud.google.com/discover/what-is-vibe-coding)

---

## 1) Intention pédagogique

À la fin de ce cours, l’étudiante ou l’étudiant sera capable de :

1. Définir le *vibe coding* et distinguer ses deux usages :
	- **exploratoire** (« prototype rapide »);
	- **professionnel responsable** (revue, tests, sécurité, déploiement).
2. Comparer *vibe coding* et programmation traditionnelle selon le contexte (coût, vitesse, maintenabilité, risques).
3. Concevoir un mini-projet full stack orienté produit en mode IA-assisté.
4. Évaluer la qualité d’un livrable généré avec IA (code, tests, documentation, sécurité).
5. Argumenter des décisions techniques devant un jury (ou la classe).

---

## 2) Préalables

- Avoir complété les cours de programmation, web, bases de données, tests et déploiement.
- Maîtriser Git/GitHub (branch, pull request, revue).
- **Être capable de lire du code généré automatiquement et de l’expliquer.**

---

## 3) Notions clés (résumé structuré)

### 3.1 Définition
Le *vibe coding* est une approche où l’on décrit une intention en langage naturel, et l’IA génère du code qu’on itère par conversation (prompt → code → test → retour → correction).

### 3.2 Les 2 boucles de travail

1. **Boucle code (micro)**
	- Décrire la tâche
	- Générer
	- Exécuter
	- Corriger
	- Répéter

2. **Boucle produit (macro)**
	- Idée
	- Génération du prototype
	- Raffinement des fonctionnalités
	- Validation (qualité/sécurité/tests)
	- Déploiement (*vibe deploying*)
<!-- TODO : Expliquer les concepts de micro et macro -->

### 3.3 Ce qui change vraiment

- Avant : on écrivait surtout la syntaxe.
- Maintenant : on orchestre, on valide, on décide.
- Donc : la compétence critique devient **jugement d’ingénierie** + **capacité de vérification**.

---

## 4) Outils (vue pédagogique)

Selon la référence Google, les outils s’alignent sur des besoins différents :
<!-- TODO : Trouver des outils au-delà de ceux de Google pour montrer la variété -->
- **AI Studio** : prototypage très rapide d’idée.
- **Firebase Studio** : génération d’app complète avec backend intégré.
- **Code Assist / IDE** : travail dans un vrai projet existant.
- **CLI / agent terminal** : automatisation et itération en ligne de commande.

Dans ce cours, l’outil précis est secondaire :
on évalue surtout la **démarche professionnelle**.

---

## 5) Déroulement de la séance (3 h 45)

## Bloc A — Mise en situation (30 min)

### Activité
- Discussion guidée : « Est-ce qu’un produit qui fonctionne vite est forcément un bon produit? »
- Mise en commun : vitesse vs qualité vs responsabilité.

### Livrable éclair
- Une position personnelle (5 à 7 lignes) :
  - *Quand le vibe coding est pertinent?*
  - *Quand il est dangereux?*

## Bloc B — Démo enseignante (35 min)

### Démo 1 : boucle micro
- Prompt d’une fonction simple.
- Génération, exécution, bug volontaire, correction.
- Ajout de tests minimaux.

### Démo 2 : boucle macro
- Prompt produit (mini-app).
- Raffinement UI + logique métier.
- Déploiement (ou simulation de déploiement).

### Point d’arrêt critique
Les étudiants identifient :
- ce que l’IA a bien fait;
- ce que l’humain devait absolument vérifier.

## Bloc C — Atelier final (2 h)

### Mandat
En équipe de 2, livrer un **MVP fonctionnel** d’une application utilitaire pour un contexte collégial.

Exemples de sujets :
- planificateur d’étude;
- outil de suivi de stages;
- générateur de quiz de révision;
- mini-tableau de bord d’équipe.

### Contraintes obligatoires

1. Utiliser l’IA dans le flux de développement (prompts documentés).
2. Garder une **trace des décisions** (journal court).
3. Inclure des tests minimaux (unitaires ou intégration légère).
4. Produire une section « risques et limites ».
5. Présenter une démonstration en direct (5 minutes).

### Livrables

- Dépôt Git (code + README).
- Fichier `PROMPTS.md` : prompts utilisés + ajustements.
- Fichier `DECISIONS.md` : 5 décisions techniques justifiées.
- Fichier `VALIDATION.md` :
  - cas testés,
  - erreurs rencontrées,
  - correctifs apportés.

## Bloc D — Présentations + rétroaction (40 min)

Chaque équipe présente :
- le besoin visé;
- une décision que l’IA a proposée mais qu’elle a rejetée (et pourquoi);
- une limite non résolue;
- le plan d’amélioration post-cours.

---

## 6) Évaluation (100 points)

### A. Produit et fonctionnement (30 pts)
- MVP exécutable et cohérent avec le besoin.
- Flux principal sans erreur bloquante.

### B. Qualité d’ingénierie (25 pts)
- Structure du code lisible.
- Gestion d’erreurs de base.
- Absence de secrets dans le code.

### C. Validation et tests (20 pts)
- Présence de tests pertinents.
- Preuve d’exécution des tests.
- Cas limites minimaux couverts.

### D. Maîtrise du processus IA (15 pts)
- Prompts documentés et améliorés.
- Capacité à expliquer le code généré.
- Rejet explicite d’au moins une proposition IA inadéquate.

### E. Communication technique (10 pts)
- Démo claire, concise, professionnelle.
- Réponses justifiées aux questions.

---

## 7) Grille d’analyse « vibe coding responsable »

Avant d’accepter du code IA, valider :

1. **Compréhension** : puis-je expliquer ce bloc sans lire l’explication de l’outil?
2. **Exactitude** : répond-il vraiment au besoin métier?
3. **Sécurité** : y a-t-il des clés, injections, accès non contrôlés?
4. **Robustesse** : que se passe-t-il en cas d’entrée invalide ou d’échec réseau?
5. **Testabilité** : puis-je écrire un test simple qui prouve le comportement?
6. **Maintenabilité** : un pair peut-il reprendre ce code dans 3 mois?

---

## 8) Exemples de prompts pédagogiques

### Prompt initial (produit)
« Génère une application web de suivi d’études pour 1 session. Je veux : création de cours, tâches hebdomadaires, progression visuelle, et export CSV. Utilise une architecture simple et documente les choix. »

### Prompt de qualité
« Refactorise cette partie pour séparer logique métier et interface. N’ajoute pas de dépendance externe. Explique les compromis. »

### Prompt de sécurité
« Analyse ce module comme si tu faisais une revue sécurité. Donne les 5 risques prioritaires, puis propose un correctif minimal pour chacun. »

### Prompt de validation
« Écris des tests unitaires pour les cas nominal, cas limite et cas d’erreur. Montre la commande d’exécution et l’interprétation attendue. »

---

## 9) Discussion de fin de programme

### Message central
Le marché ne demande plus seulement « coder vite ».
Il demande :

- des personnes capables de **piloter des systèmes assistés par IA**;
- de **vérifier** ce qui est généré;
- de **prendre responsabilité** sur ce qui est déployé.

Autrement dit : en finissant le DEC, votre valeur n’est pas de rivaliser avec l’IA sur la vitesse de frappe, mais de surpasser l’IA sur la **rigueur, le jugement et l’éthique technique**.

---

## 10) Ressources complémentaires

- Source de base : [Google Cloud — What is vibe coding?](https://cloud.google.com/discover/what-is-vibe-coding)
- Lecture critique : [Les dangers du vibe coding](../dangers-vibe-coding.md)
- Lecture critique : [Vibe-coding = programmeurs sans réflexion](../vibe_coding_gambling.md)

---

## 11) Option d’épreuve synthèse (si utilisé comme examen final)

Si ce cours sert d’évaluation terminale, ajouter :

- **Partie individuelle (30%)** : courte défense orale (3 min) sur une décision technique personnelle.
- **Partie équipe (70%)** : MVP + documentation + démonstration.

Critère éliminatoire possible :
> Incapacité à expliquer le fonctionnement d’un module critique généré par IA.

