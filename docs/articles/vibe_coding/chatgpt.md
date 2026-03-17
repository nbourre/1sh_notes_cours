# Cours-synthèse : Vibe Coding

## Contexte

Ce cours est le **dernier cours de votre formation**.

L’objectif n’est PAS :

* d’utiliser l’IA pour aller vite
* ni de produire un projet impressionnant visuellement

L’objectif est de démontrer que vous êtes capable de :

* travailler **comme un professionnel**
* utiliser l’IA **sans perdre le contrôle**
* comprendre ce que vous livrez

---

!!! important

    L’IA peut écrire du code.  
    **Mais vous êtes responsable de ce code.**

---

## 1) C’est quoi le vibe coding?

Le *vibe coding* consiste à :

Décrire ce que vous voulez en langage naturel, et laisser une IA générer le code.

Ensuite :

* vous testez
* vous corrigez
* vous ajustez vos instructions

C’est une boucle de conversation avec l’IA. **C'est comme le développement itératif.**

Le *vibe coding* permet de transformer une idée en code via des prompts.

---

### Exemple concret

#### Sans IA (traditionnel)

```python
def calculer_total(prix, taxes):
    return prix * (1 + taxes)
```

#### Avec vibe coding

Prompt :

> "Crée une fonction Python qui calcule un prix avec taxes, avec validation des entrées."

---

!!! warning

    Si vous ne comprenez pas le code généré,  
    vous êtes en train de faire du **mauvais vibe coding**.

---

## 🔹 Exercice 1 — Comprendre vs utiliser

On te donne ce code généré :

```javascript
function validateEmail(email) {
  return /\S+@\S+\.\S+/.test(email);
}
```

### Questions

1. Est-ce que tu comprends ce que fait la fonction ?
2. Que signifie `/\S+@\S+\.\S+/` ?
3. Donne un email valide qui pourrait échouer
4. Donne un email invalide qui pourrait passer

---

??? info "Indice"

    `\S = caractère non espace`

---

## 2) Les deux façons de faire du vibe coding

### Mode exploratoire

* prototype rapide
* test d’idée

✔️ rapide
❌ fragile

---

### Mode professionnel

* validation
* tests
* sécurité
* structure

---

!!! tip

    Le marché ne paie pas pour du code rapide.  
    Il paie pour du code **fiable**.

---

## 3) Ce qui change vraiment

Avant :

* écrire du code

Maintenant :

* guider
* valider
* corriger

---

??? info "Concept important"

    L’humain garde le jugement.  
    L’IA exécute.

---

## 4) Les boucles de travail

### Boucle micro

1. Décrire
2. Générer
3. Tester
4. Corriger

---

### Exemple

Prompt :

> "Ajoute une validation si la valeur est négative"

---

## 🔹 Exercice 2 — Corriger avec IA

Code :

```python
def diviser(a, b):
    return a / b
```

### Problème

* crash si b = 0

---

### Tâche

1. Écris un prompt pour corriger
2. Teste mentalement :
    * diviser(10, 2)
    * diviser(10, 0)
    * diviser("a", 2)

---

!!! tip

    Ton prompt doit inclure validation + gestion d’erreur

---

### Boucle macro

1. Idée
2. Prototype
3. Amélioration
4. Validation
5. Déploiement

---

## 5) Les risques

### Risque 1 — Ne pas comprendre

Exemple :

* code fonctionne
* mais incompris

---

### Risque 2 — Sécurité

```python
query = "SELECT * FROM users WHERE name = '" + name + "'"
```

---

### Risque 3 — Illusion que ça marche

* fonctionne dans un cas
* casse ailleurs

---

!!! danger

```
"Ça fonctionne" ≠ "C’est bon"
```

---

## 🔹 Exercice 3 — Identifier les risques

Code :

```python
def get_user(name):
    query = "SELECT * FROM users WHERE name = '" + name + "'"
    return execute(query)
```

### Questions

1. Quel est le problème ?
2. Donne une attaque possible
3. Propose une correction

---

??? info "Indice"

```
' OR 1=1 --
```

---

## 6) Les tests (version simple)

Test = vérifier que ça marche

---

### Exemple

```python
def addition(a, b):
    return a + b
```

Tests :

* normal → 2 + 3 = 5
* limite → 0 + 0 = 0
* erreur → "a" + 3

---

!!! tip

```
Tester, c’est vérifier, pas deviner.
```

---

## 🔹 Exercice 4 — Écrire des tests

Code :

```python
def multiplier(a, b):
    return a * b
```

### Tâche

* 1 test normal
* 1 test limite
* 1 test erreur

---

## 7) Risques et limites

À inclure dans votre projet :

* ce qui peut casser
* ce que vous ne comprenez pas
* ce qui n’est pas sécurisé

---

## 🔹 Exercice 5 — Réflexion critique

Projet : app de tâches

### Tâche

* 2 limites
* 2 risques
* 1 amélioration

---

!!! important

```
Un bon dev sait dire :  
"ce n’est pas prêt"
```

---

## 8) Projet final (MVP)

### Contraintes

* IA utilisée
* tests simples
* analyse des risques
* code compréhensible

---

### Exemple

#### Mauvais

* code généré
* aucun test

#### Bon

* validation
* erreurs gérées
* tests

---

## 9) Utiliser l’IA correctement

### Mauvais prompt

> "Fais une app"

---

### Bon prompt

> "Crée une app Flask avec validation des entrées"

---

### Excellent prompt

> "Crée une app Flask avec :

* validation
* gestion d’erreurs
* séparation logique/UI
* explication des choix"

---

## 🔹 Exercice 6 — Améliorer un prompt

Prompt :

> "Crée une app de tâches"

---

### Tâche

Améliore-le avec 3 contraintes

---

## 10) Grille mentale

Avant d’accepter du code :

* Est-ce que je comprends ?
* Est-ce que c’est correct ?
* Est-ce sécuritaire ?
* Est-ce testable ?

---

!!! important

```
Si tu ne peux pas expliquer,  
tu ne dois pas utiliser.
```

---

## 🔹 Exercice 7 — Niveau finissant

Une app fonctionne parfaitement.

### Questions

1. Pourquoi ce n’est pas suffisant ?
2. Que vérifier avant de livrer ?
3. Que l’IA ne garantit pas ?

---

!!! warning

```
"Ça marche" n’est jamais une preuve de qualité.
```

---

## 11) Message final

Aujourd’hui :

👉 tout le monde peut générer du code

Mais :

👉 peu de gens peuvent **valider, comprendre et assumer**

---

??? success "Votre valeur comme finissant"

    Vous êtes évalué sur votre capacité à :
    - comprendre
    - juger
    - corriger
    - assumer


