# Bonnes pratiques de prise de notes en Markdown

Markdown est un langage de balisage simple, idéal pour structurer rapidement du texte lisible et clair. Utilisé dans GitHub, HackMD, Obsidian ou Notion, il permet de créer des notes professionnelles et bien organisées.

---

## 1. Titres et hiérarchies

Utilisez `#` pour les titres. Chaque `#` correspond à un niveau :

```markdown
# Titre principal
## Sous-titre
### Sous-sous-titre
```

Gardez une structure cohérente pour refléter la logique de vos notes.

---

## 2. Listes

### Puces

```markdown
- Premier point
- Deuxième point
```

### Listes ordonnées

```markdown
1. Étape 1
2. Étape 2
```

Utilisez les listes pour les procédures, résumés ou concepts clés.

---

## 3. Texte enrichi

```markdown
**gras**, *italique*, ~~barré~~, `code`
```

Servez-vous du gras pour insister sur un concept clé, de l’italique pour les termes techniques, du code pour les commandes ou extraits techniques.

---

## 4. Liens et images

### Lien

```markdown
[Nom du lien](https://adresse-du-site)
```

### Image

```markdown
![Description](../assets/nom_image.png)
```

Stockez les images dans un dossier `assets/` pour garder votre structure propre.

---

## 5. Code et blocs

### Ligne de code

```markdown
Utilisez `backticks` pour du code en ligne
```

### Bloc de code

````markdown
```python
print("Hello")
````

````

Indiquez la langue pour activer la coloration syntaxique.

---

## 6. Tableaux

```markdown
| Commande | Description       |
|----------|-------------------|
| `cd`     | Changer de dossier |
| `ls`     | Lister les fichiers |
````

Les tableaux sont utiles pour comparer des options ou organiser des données.

---

## 7. Table des matières (avec VS Code)

L’extension **Markdown All in One** permet de générer automatiquement une table des matières à partir des titres.

```markdown
<!-- TOC -->
- [Titre principal](#titre-principal)
  - [Sous-titre](#sous-titre)
<!-- /TOC -->
```

### 7.1 Omettre un élément de la table des matières

Ajoutez `<!-- omit in toc -->` après le titre pour l’exclure :

```markdown
# Un titre quelconque <!-- omit in toc -->
```


---

## 8. Commentaires

Les commentaires ne sont pas visibles dans le rendu final.

```markdown
<!-- Ceci est un commentaire invisible -->
```

---

## 9. Astuce : copier-coller rapide

* Utilisez `Ctrl + Shift + V` dans VS Code pour prévisualiser en Markdown.
* Utilisez un thème sombre pour un meilleur confort visuel.
* Gardez une convention de nommage simple pour vos fichiers :

```markdown
nom-du-sujet.md
2025-05-veille.md
```

---

## En conclusion

Markdown permet de prendre des notes claires, lisibles et professionnelles sans outil complexe. C’est le langage de base de la documentation moderne, et savoir l’utiliser est un atout pour tout technicien en informatique.
