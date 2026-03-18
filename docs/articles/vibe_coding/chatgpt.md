# Cours-synthèse : Vibe Coding

## Contexte

Ce cours est le **dernier cours de votre formation**.

L’objectif n’est pas de produire un projet impressionnant visuellement ni d’utiliser l’IA seulement pour aller vite.

L’objectif est de démontrer que vous êtes capable de :

* travailler **comme une personne professionnelle**
* utiliser l’IA **sans perdre le contrôle**
* comprendre ce que vous livrez
* expliquer vos choix
* reconnaître les limites d’une solution générée

!!! important

    L’IA peut écrire du code.  
    **Mais vous êtes responsable de ce code.**

## 1) C’est quoi le vibe coding?

Le *vibe coding* consiste à décrire ce que vous voulez en langage naturel, puis à utiliser une IA pour générer du code, proposer des correctifs, restructurer une solution ou accélérer le développement.

En pratique, cela ressemble souvent à ceci :

1. vous décrivez votre besoin
2. l’IA génère une première version
3. vous testez
4. vous corrigez
5. vous redemandez une amélioration

Autrement dit, ce n’est pas simplement « laisser l’IA coder à votre place ». C’est une **boucle de collaboration** où l’humain garde le jugement.

### Exemple

#### Sans IA

```python
def calculer_total(prix, taxes):
    return prix * (1 + taxes)
```

#### Avec IA

Prompt :

> Crée une fonction Python qui calcule un prix avec taxes et valide les entrées.

L’IA pourrait générer :

```python
def calculer_total(prix, taxes):
    if not isinstance(prix, (int, float)) or not isinstance(taxes, (int, float)):
        raise TypeError("prix et taxes doivent être numériques")
    if prix < 0 or taxes < 0:
        raise ValueError("prix et taxes doivent être positifs")
    return prix * (1 + taxes)
```

Dans ce cas, l’IA a peut-être été plus vite. Mais ce n’est utile que si vous comprenez ce qu’elle a produit.

!!! warning

    Si vous ne comprenez pas le code généré,  
    vous êtes en train de faire du **mauvais vibe coding**.

## Exercice guidé 1 — Comprendre vs utiliser

On vous donne ce code généré :

```javascript
function validateEmail(email) {
  return /\S+@\S+\.\S+/.test(email);
}
```

### Questions

1. Est-ce que vous comprenez ce que fait cette fonction?
2. Que signifie l’expression régulière `/\S+@\S+\.\S+/`?
3. Donnez un exemple d’adresse valide qui pourrait échouer selon le contexte
4. Donnez un exemple d’entrée invalide qui pourrait quand même passer

??? info "Indice"

    `\S` représente un caractère qui n’est pas un espace.

<!--
Réponses suggérées :

1. La fonction vérifie si la chaîne ressemble à une adresse courriel simple.
2. \S+ = un ou plusieurs caractères non espaces, puis @, puis encore des caractères non espaces, puis un point, puis encore des caractères non espaces.
3. Certaines adresses valides plus complexes ou avec des règles métiers précises pourraient être rejetées selon les besoins réels.
4. Une chaîne comme "abc@def.ghi" passerait même si elle n’est pas forcément souhaitée dans tous les contextes.
-->

## 2) Les deux façons de faire du vibe coding

On peut distinguer deux grands usages du vibe coding.

### 2.1 Mode exploratoire

Le mode exploratoire sert à :

* tester rapidement une idée
* créer un prototype
* vérifier si une interface ou une fonctionnalité est prometteuse

Exemple :

* générer une mini application de prise de notes en quelques minutes
* explorer une interface de tableau de bord
* tester un concept de jeu ou de simulation

Avantages :

* rapide
* motivant
* utile pour démarrer

Inconvénients :

* code parfois fragile
* structure parfois médiocre
* peu fiable si on ne vérifie pas

### 2.2 Mode professionnel

Le mode professionnel est celui qu’on vise dans ce cours.

Il inclut :

* validation
* gestion d’erreurs
* tests minimaux
* réflexion sur la sécurité
* structure du code
* documentation
* responsabilité

Exemple :

Vous créez une application de suivi d’étude. Elle ne doit pas seulement « marcher chez vous ». Elle doit aussi :

* gérer les erreurs de saisie
* éviter les comportements absurdes
* être compréhensible par une autre personne
* être testable
* être expliquée clairement

!!! Truc

    Le marché ne paie pas simplement pour du code rapide.  
    Il paie pour du code **fiable, compréhensible et maintenable**.


## 3) Ce qui change vraiment

Avant l’arrivée de ces outils, une grande partie du travail consistait à écrire manuellement beaucoup de syntaxe.

Aujourd’hui, une partie du travail consiste à :

* bien décrire un besoin
* valider ce que l’IA propose
* corriger les erreurs
* refuser une mauvaise solution
* choisir entre plusieurs approches

Votre rôle devient donc plus large.

Vous ne faites pas qu’écrire du code. Vous devez aussi agir comme :

* personne qui analyse
* personne qui vérifie
* personne qui décide
* personne qui assume le résultat final

??? info "Concept important"

    L’IA peut produire du texte, du code et des suggestions.  
    Elle ne porte pas la responsabilité du livrable.  
    **Cette responsabilité reste humaine**.

## 4) Les deux boucles de travail

## 4.1 La boucle micro : travailler sur un morceau de code

La boucle micro concerne une tâche précise.

Exemple :

* corriger une fonction
* ajouter une validation
* refactoriser un morceau de code
* écrire quelques tests

Étapes typiques :

1. décrire la tâche
2. générer une première version
3. exécuter ou lire le code
4. trouver les problèmes
5. corriger
6. recommencer

### Exemple

Prompt :

> Modifie cette fonction pour refuser les valeurs négatives et retourner un message d’erreur clair.

Vous utilisez donc l’IA comme un outil de travail localisé sur un problème précis.

## Exercice guidé 2 — Corriger avec IA

On vous donne cette fonction :

```python
def diviser(a, b):
    return a / b
```

### Tâche

1. Écrivez un prompt pour demander une correction
2. Testez mentalement les cas suivants :
     * `diviser(10, 2)`
     * `diviser(10, 0)`
     * `diviser("a", 2)`

!!! Truc

    Un bon prompt précise le problème à corriger, les contraintes et le comportement attendu.

<!--
Réponses suggérées :

1. Exemple de prompt :
   "Modifie cette fonction Python pour gérer la division par zéro et valider que les deux entrées sont numériques. Retourne des erreurs claires."

2.
   - diviser(10, 2) -> 5
   - diviser(10, 0) -> erreur de division par zéro
   - diviser("a", 2) -> erreur de type
-->

## 4.2 La boucle macro : travailler sur le produit

La boucle macro concerne le projet dans son ensemble.

Exemple :

* idée initiale
* première version fonctionnelle
* ajout de fonctionnalités
* validation
* amélioration
* préparation à la démonstration ou au déploiement

### Exemple

Projet :

> Application de suivi d’étude pour une session

Évolution possible :

* version 1 : ajout de cours
* version 2 : ajout de tâches
* version 3 : progression visuelle
* version 4 : validation des entrées
* version 5 : correction de bugs
* version 6 : démonstration claire et documentation

Cette boucle est importante parce qu’un projet n’est pas seulement une suite de petites fonctions. C’est aussi un produit avec un objectif, des limites et des choix.

## 5) Les risques du vibe coding

Le vibe coding peut être très utile. Mais il comporte aussi plusieurs risques.

## 5.1 Risque 1 — Ne pas comprendre ce qui a été généré

Vous demandez une fonctionnalité. L’IA produit du code qui semble bon. Vous l’acceptez. Pourtant, vous ne comprenez pas vraiment :

* la logique
* les conditions
* les cas limites
* les impacts

Exemple :

* l’IA génère une requête SQL
* elle fonctionne
* mais vous ne voyez pas qu’elle est dangereuse ou incorrecte

C’est l’un des plus grands pièges : confondre **code qui a l’air bon** et **code réellement maîtrisé**.

## 5.2 Risque 2 — Sécurité faible ou absente

Certaines solutions générées peuvent contenir des pratiques dangereuses.

Exemple :

```python
query = "SELECT * FROM users WHERE name = '" + name + "'"
```

Ce genre de construction peut permettre une injection SQL.

Autre exemple :

* Mot de passe écrit en clair dans le code
* Clé API directement dans le dépôt
* Absence de validation d’entrée utilisateur

Même si vous n’avez presque pas vu la sécurité en profondeur, vous devez au minimum développer le réflexe suivant :

> Est-ce qu’une entrée utilisateur pourrait briser, contourner ou manipuler mon système?

## 5.3 Risque 3 — Illusion que « ça marche »

Un programme peut sembler fonctionner dans **un seul cas simple**.

Mais il peut échouer :

* avec une mauvaise entrée
* avec plusieurs utilisateurs
* avec un réseau lent
* avec des données vides
* avec un comportement non prévu

!!! danger

    "Ça fonctionne chez moi" ne veut pas dire "la solution est bonne".

## Exercice guidé 3 — Identifier les risques

Analysez ce code :

```python
def get_user(name):
    query = "SELECT * FROM users WHERE name = '" + name + "'"
    return execute(query)
```

### Questions

1. Quel est le principal problème?
2. Donnez un exemple d’attaque ou d’abus possible
3. Proposez une correction en français simple


??? Indice

    Pensez à une entrée comme :  
    `' OR 1=1 --`

<!--
Réponses suggérées :

1. Le principal problème est l’injection SQL.
2. Une personne pourrait entrer quelque chose comme ' OR 1=1 -- pour modifier la requête.
3. Il faut utiliser des requêtes paramétrées et ne jamais concaténer directement l’entrée utilisateur dans la requête SQL.
-->

## 6) Les tests, version simplifiée

Vous avez peu vu les tests. Ce n’est pas grave. Voici l’essentiel à retenir pour ce cours.

Un test sert à vérifier qu’un comportement attendu se produit réellement.

Un test simple peut répondre à des questions comme :

* est-ce que le cas normal fonctionne?
* est-ce que le cas limite fonctionne?
* est-ce que le cas d’erreur est géré?

### Exemple simple

```python
def addition(a, b):
    return a + b
```

Exemples de tests à imaginer :

* cas normal : `addition(2, 3)` retourne `5`
* cas limite : `addition(0, 0)` retourne `0`
* cas d’erreur ou de comportement étrange : `addition("a", 3)`

Ici, le dernier cas peut révéler un problème ou au moins montrer que le comportement n’est pas clairement défini.

### Pourquoi tester avec de l’IA?

Parce que l’IA peut produire du code qui semble cohérent, mais qui n’a jamais été réellement vérifié.

Vous pouvez demander à l’IA :

* d’écrire des tests simples
* de proposer des cas limites
* de générer un petit jeu de tests

Mais vous devez quand même lire les tests et comprendre ce qu’ils vérifient.

!!! Truc

    Tester, ce n’est pas être paranoïaque.  
    C’est vérifier avant de livrer.

## Exercice guidé 4 — Écrire des tests simples

On vous donne cette fonction :

```python
def multiplier(a, b):
    return a * b
```

### Tâche

Proposez :

* un test normal
* un test limite
* un test d’erreur ou de comportement ambigu

<!--
Réponses suggérées :

- test normal : multiplier(2, 3) == 6
- test limite : multiplier(0, 100) == 0
- test d’erreur ou ambigu : multiplier("a", 3)
  En Python, cela donne "aaa", ce qui montre qu’il faut réfléchir au contrat de la fonction.
-->

## 7) Risques et limites à inclure dans votre projet

Dans votre projet final, il ne suffit pas de montrer ce qui marche.

Vous devez aussi être capables d’indiquer :

* ce qui peut casser
* ce que vous ne comprenez pas complètement
* ce qui n’est pas encore robuste
* ce qui n’est pas suffisamment sécurisé
* ce que vous feriez ensuite pour améliorer le projet

### Exemple

Supposons que votre application de suivi d’étude permet :

* d’ajouter une tâche
* de marquer une tâche comme complétée

Exemples de limites possibles :

* les données ne sont pas sauvegardées de façon permanente
* il n’y a pas d’authentification
* aucune validation sérieuse n’est faite sur les champs
* les erreurs réseau ne sont pas gérées
* plusieurs utilisateurs en même temps n’ont pas été testés

Exemples de risques possibles :

* perte de données
* saisie invalide
* comportement imprévu
* bug silencieux
* mauvaise manipulation par l’utilisateur

!!! important

    Un bon développeur ne dit pas seulement "regardez ce que ça fait".  
    Il est aussi capable de dire "voici ce qui n’est pas encore prêt".

## Exercice guidé 5 — Réflexion critique sur un mini-projet

Vous développez une petite application de tâches avec deux fonctionnalités :

* ajouter une tâche
* marquer une tâche comme terminée

### Tâche

Identifiez :

1. deux limites techniques
2. deux risques
3. une amélioration possible

<!--
Réponses suggérées :

1. Limites techniques :
   - pas de sauvegarde persistante
   - pas de gestion de plusieurs utilisateurs

2. Risques :
   - perte de données au redémarrage
   - saisie invalide ou vide

3. Amélioration :
   - ajouter une base de données simple et une validation des entrées
-->

## 8) Votre projet final : un MVP sérieux

Dans ce cours, vous devez créer une application simple, mais crédible.

Un MVP n’est pas une version parfaite. C’est une version minimale qui démontre une valeur réelle, avec un minimum de rigueur.

### Ce qu’on attend

* l’IA fait partie de votre flux de travail
* vous gardez une trace de vos prompts
* vous expliquez vos décisions
* vous montrez un minimum de validation
* vous reconnaissez les limites du projet
* vous êtes capables de justifier vos choix

### Exemple d’idée de projet

* outil de suivi d’étude
* mini générateur de quiz
* tableau de bord simple
* planificateur personnel
* outil d’aide pour un contexte collégial

### Exemple de contraste

#### Version faible

* projet généré presque entièrement
* peu compris
* aucun test
* aucune limite nommée
* démonstration superficielle

#### Version solide

* projet simple mais cohérent
* structure compréhensible
* au moins quelques vérifications
* limites reconnues
* démonstration claire
* décisions justifiées

## 9) Comment utiliser l’IA correctement

Le résultat dépend énormément de la qualité du prompt.

### Mauvais prompt

> Fais-moi une application de gestion de tâches.

Pourquoi il est faible :

* trop vague
* aucune contrainte
* aucune précision sur la technologie
* aucune exigence de structure ou de validation

### Bon prompt

> Crée une petite application Flask qui permet d’ajouter et d’afficher des tâches avec validation des entrées.

Pourquoi il est meilleur :

* technologie précisée
* fonctionnalités ciblées
* une attente claire sur la validation

### Meilleur prompt

> Crée une application Flask simple pour ajouter et afficher des tâches. Sépare la logique métier et l’interface, valide les entrées utilisateur, gère les erreurs de base et explique les choix de structure.

Ici, on guide mieux l’outil.

## Exercice guidé 6 — Améliorer un prompt

Prompt de départ :

> Crée une application de gestion de tâches.

### Tâche

Améliorez ce prompt en ajoutant au moins trois contraintes ou attentes précises.

<!--
Réponses suggérées :

Exemple :
"Crée une application web simple en Flask pour ajouter et afficher des tâches. Valide les entrées, gère les erreurs de base, garde une structure simple et explique les choix de conception."

Autres contraintes possibles :
- pas de dépendance inutile
- stockage en mémoire ou en fichier
- prévoir des tests minimaux
- interface simple
-->

## 10) Grille mentale à utiliser avant d’accepter du code

Avant d’accepter un morceau de code généré, posez-vous ces questions :

1. Est-ce que je comprends ce bloc?
2. Est-ce qu’il répond vraiment au besoin?
3. Est-ce qu’il y a un risque évident?
4. Est-ce que je pourrais le tester simplement?
5. Est-ce qu’une autre personne pourrait le relire et le reprendre?

!!! important

```
Si vous ne pouvez pas expliquer un code,  
vous ne devriez pas l’utiliser tel quel.
```

## Exercice guidé 7 — Niveau finissant

On vous dit :

> L’application fonctionne parfaitement.

### Questions

1. Pourquoi cette phrase n’est-elle pas suffisante?
2. Donnez trois choses à vérifier avant de livrer
3. Donnez une chose que l’IA ne peut pas garantir à votre place

<!--
Réponses suggérées :

1. Parce que "fonctionne" ne dit rien sur la qualité, la sécurité, les cas limites, la compréhension ou la maintenabilité.
2. Exemples :
   - validation des entrées
   - gestion d’erreurs
   - tests de base
   - absence de secrets dans le code
   - compréhension du fonctionnement
3. L’IA ne peut pas garantir la responsabilité, le jugement professionnel ou l’adéquation réelle au contexte.
-->

## 11) Mini défi optionnel

En 15 minutes :

1. générez une mini application avec IA
2. trouvez :

   * un bug
   * une limite
   * un risque

??? success "Pourquoi faire cet exercice?"

```
Parce qu’un code généré rapidement a presque toujours  
quelque chose à corriger, à clarifier ou à renforcer.
```

## 12) Message final

Aujourd’hui, beaucoup de personnes peuvent générer du code.

Mais peu de personnes peuvent :

* le comprendre
* le valider
* le corriger
* l’assumer

Votre valeur comme finissante ou finissant n’est pas seulement votre vitesse de frappe.

Votre valeur, c’est votre capacité à :

* raisonner
* juger
* vérifier
* expliquer
* améliorer
* assumer un livrable

??? success "Votre valeur comme finissant"

```
Vous n’êtes pas évalué seulement sur votre capacité à produire du code.  
Vous êtes évalué sur votre capacité à :

- comprendre
- juger
- corriger
- assumer
```

## Références

* Google Cloud, *What is vibe coding?*
* GitHub Docs, documentation sur GitHub Copilot et l’assistance à la programmation
* Documentation de tests du langage ou framework utilisé dans votre projet
* OWASP, ressources d’introduction sur les risques applicatifs courants
* Documentation officielle de votre stack de projet

Si tu veux, je peux maintenant te faire une **version encore plus “publication MkDocs finale”**, avec une meilleure hiérarchie des sections, des titres plus pédagogiques et quelques blocs `??? question` ou `??? example` en plus.
