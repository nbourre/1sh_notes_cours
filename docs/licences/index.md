---
title: "Les licences logicielles : Comprendre les options et les implications"
description: "Explorez les licences open source, de la permissive MIT à la virale GPL, en passant par le cas d'étude Bambu Lab."
difficulty: "Intermediate"
duration: "1 heure 30 minutes"
tags: [open-source, licensing, gpl, agpl, lgpl, bambulab, legal-case]
prerequisites: []
learning_objectives:
  - "Distinguer les nuances entre différentes licences logicielles."
  - "Analyser l'impact du copyleft sur les œuvres dérivées à travers un cas réel."
  - "Comprendre les limites juridiques entre le code source libre et les services cloud propriétaires."
created: 2026-01-30
author: "Nicolas Bourré + LLM"
status: "published"
---

# Les licences logicielles : Comprendre les options et les implications

## Objectifs d'apprentissage

À la fin de cette leçon, vous pourrez:

* Distinguer les nuances entre différentes licences logicielles.
* Analyser l'impact du copyleft sur les œuvres dérivées à travers un cas réel.
* Comprendre les limites juridiques entre le code source libre et les services cloud propriétaires.

## Introduction

Le monde du logiciel libre repose sur des contrats légaux appelés licences. Bien qu'elles encouragent le partage, elles imposent des règles strictes qui peuvent mener à des conflits majeurs entre entreprises et développeurs indépendants. Nous allons explorer comment ces licences fonctionnent et ce qui arrive lorsqu'une entreprise tente de restreindre l'usage d'un code pourtant basé sur de l'open source.

## Concept : La Licence MIT (Permissive)

La licence MIT est l'une des licences open source les plus populaires au monde en raison de sa simplicité et de son caractère permissif. Elle permet une utilisation quasi illimitée du code, tant que l'avis de droit d'auteur original est conservé.

### Exemple 1 : Intégration commerciale

Une start-up peut copier un utilitaire de tri de données sous licence MIT, l'améliorer, et vendre le logiciel résultant sans jamais avoir à publier son propre code source.

### Exemple 2 : "As-is" (En l'état)

La licence MIT stipule que le code est fourni "tel quel", sans aucune garantie. Si le code contient un bug qui cause une perte de données, l'auteur original ne peut pas être tenu responsable juridiquement.

## Concept : La famille GPL et l'effet « viral »

La licence **GPL (General Public License)** est conçue pour garantir que le logiciel reste libre. Son principe de "copyleft" exige que si vous distribuez un logiciel basé sur du code GPL, votre projet entier doit aussi être sous licence GPL.

* **AGPL (Affero GPL)** : Une variante cruciale pour le cloud. Elle stipule que si vous modifiez un logiciel pour l'offrir comme service sur un réseau (SaaS), vous devez aussi partager votre code source.
* **Lien avec Bambu Lab** : Leur logiciel *Bambu Studio* est basé sur *PrusaSlicer*, qui est sous licence **AGPL**. Cela signifie que Bambu Lab est obligé de publier le code source de son slicer.

### Cas d'étude : Bambu Lab vs OrcaSlicer-bambulab (Mai 2026)

Ce cas illustre concrètement la tension entre la liberté accordée par une licence AGPL et la volonté d'une entreprise de contrôler l'accès à son écosystème cloud.

#### Contexte

Bambu Lab fabrique des imprimantes 3D très accessibles. Après la vente, l'entreprise a ajouté des systèmes d'authentification qui n'existaient pas à l'achat, restreignant l'usage des logiciels tiers avec leurs imprimantes. Un *slicer* est le logiciel qui traduit un modèle 3D en instructions pour l'imprimante — c'est l'outil central du flux de travail.

**Bambu Studio**, le slicer officiel de Bambu Lab, est publié sous licence **AGPL 3.0**. Il est lui-même basé sur *PrusaSlicer*, également AGPL. OrcaSlicer est un fork populaire et open source de Bambu Studio.

#### Acte 1 — La mise en demeure

Paweł Jarczak crée *OrcaSlicer-bambulab*, un fork d'OrcaSlicer qui réactivait la connexion aux services cloud de Bambu Lab, supprimée par l'entreprise pour les logiciels tiers. Bambu Lab lui envoie une correspondance l'accusant de :

* **usurpation d'identité** (*impersonation*) — son logiciel se présenterait comme Bambu Studio auprès des serveurs cloud;
* **contournement de contrôles d'autorisation**;
* **rétro-ingénierie** (*reverse engineering*);
* violation des conditions d'utilisation (*Terms of Service*).

Jarczak répond point par point et demande à Bambu Lab d'identifier précisément les fichiers, commits ou chemins de code problématiques, ainsi que la base juridique exacte de leurs allégations. Il ne reçoit pas de réponse substantielle. Il retire volontairement son dépôt, **sans admettre la validité des allégations**, pour éviter un conflit juridique prolongé.

??? info "Le détail technique de l'«usurpation»"
    Un *User-Agent* est une chaîne de texte qu'un logiciel envoie à un serveur pour s'identifier — comme le nom et la version d'un navigateur web. Bambu Lab reprochait au fork de se présenter comme « Bambu Studio » auprès de leur cloud. Or, Jarczak n'avait **pas modifié** cette partie du code : il réutilisait simplement le code AGPL original de Bambu Lab, qui porte déjà ce nom. Bambu Lab lui reprochait d'utiliser leur propre code tel quel, sous leur propre licence libre.

    Comme le résume un utilisateur Reddit cité par Rossmann : *« C'est comme ouvrir une salle de gym sur une place publique et vouloir interdire aux gens d'utiliser la place publique. »*

#### Acte 2 — Louis Rossmann offre 10 000 $

[Louis Rossmann](https://www.youtube.com/channel/UCl2mFZoRqjw_ELax4Yisf6w), militant pour le droit à la réparation (*right to repair*) et fondateur de la Futo Foundation, publie une vidéo pour encourager Jarczak à rendre son code public et à contester la mise en demeure. Ne pouvant pas se prononcer sans avoir vu les documents, il contacte Jarczak en privé.

Après avoir consulté les communications, Rossmann annonce publiquement qu'il **s'engage à couvrir les 10 000 premiers dollars de frais juridiques** si Jarczak remet son code en ligne et que Bambu Lab le poursuit effectivement. Il exprime sa confiance dans la solidité de la position de Jarczak.

#### Acte 3 — Rossmann publie le code sur son propre GitHub

Jarczak décline l'offre, réaffirmant qu'il souhaitait surtout dénoncer la violation de l'AGPL par Bambu Lab, sans s'engager dans une bataille juridique. Rossmann décide alors de **publier lui-même le code sur son propre dépôt GitHub**, s'exposant volontairement à toute poursuite.

Il détaille également un argument juridique supplémentaire : Bambu Lab avait invoqué la **section 1201 du DMCA** (*Digital Millennium Copyright Act*), une loi américaine qui criminalise le contournement de verrous numériques (*DRM*), même pour utiliser un appareil qu'on possède. C'est la même loi utilisée par Lexmark pour empêcher la vente de cartouches d'encre compatibles. Rossmann juge cette invocation sans fondement, car il n'y a ici aucun verrou numérique à contourner : le cloud de Bambu Lab acceptait simplement les requêtes.

#### Le nœud juridique central

| Question | Position de Bambu Lab | Contre-argument |
|---|---|---|
| Redistribution du code | Interdit car « impersonation » | Le code est AGPL : toute restriction supplémentaire est **explicitement interdite** par la licence |
| Accès au cloud | Régi par les ToS, pas par l'AGPL | La plainte vise le **code**, pas l'accès au service — les deux sont distincts |
| Rétro-ingénierie | Alléguée | Aucune — le code source AGPL est **public**; rien n'a été décompilé |
| DMCA §1201 | Invoqué | Aucun verrou numérique n'a été contourné; le serveur acceptait les requêtes nativement |

## Concept : La LGPL (Lesser GPL)

La **LGPL** est une version "allégée" de la GPL. Elle a été créée pour permettre aux développeurs de lier des bibliothèques libres à des logiciels propriétaires sans forcer le logiciel propriétaire à devenir libre.

* **La règle d'or** : Si vous utilisez une bibliothèque LGPL, vous ne devez publier les modifications **que si vous modifiez la bibliothèque elle-même**.
* **Lien dynamique** : Tant que votre logiciel propriétaire appelle la bibliothèque sans l'incorporer de manière indissociable (lien dynamique), vous gardez votre code fermé.

### Exemple : Utilisation de FFmpeg

De nombreux lecteurs vidéo propriétaires utilisent la bibliothèque de décodage FFmpeg (souvent sous LGPL). Ils peuvent rester payants et fermés tant qu'ils permettent à l'utilisateur de remplacer la bibliothèque FFmpeg par une autre version s'il le souhaite.

## Concept : Licences Fermées et EULA

Contrairement à l'open source, les licences propriétaires (fermées) interdisent l'accès au code. Le cas Bambu Lab montre une zone grise : le **logiciel** est libre (AGPL), mais le **service cloud** auquel il se connecte est fermé et propriétaire.

## Concept : Les CLA (Contributor License Agreements)

Lorsqu'un projet open source devient important (comme le noyau Linux, Android ou VS Code), l'organisation qui le gère demande souvent aux contributeurs de signer un **CLA**.

### Pourquoi utiliser un CLA ?

Le CLA est un document juridique par lequel un contributeur stipule qu'il détient les droits sur son code et qu'il accorde officiellement à l'organisation le droit d'utiliser, de modifier et de distribuer sa contribution.

* **Protection juridique** : Cela protège le projet contre d'éventuelles poursuites si un contributeur prétend plus tard que son code a été utilisé sans son consentement.
* **Gestion des droits** : Cela permet à l'organisation de changer la licence du projet global à l'avenir si nécessaire (par exemple, passer de GPL à Apache).

---

## Exercices

### Exercice : Choisir entre GPL et LGPL

**Temps**: 10 minutes

Vous développez une nouvelle bibliothèque de compression d'image. Vous voulez qu'elle soit utilisée par le plus grand nombre de logiciels (même commerciaux), mais vous voulez que toute amélioration de l'algorithme de compression vous soit retournée.

* Quelle licence choisissez-vous ?

??? success "Résultat attendu"
    LGPL (permet l'usage commercial tout en forçant le partage des modifications apportées à la bibliothèque elle-même).

### Exercice : Le choix du contributeur

**Temps** : 5 minutes

Vous souhaitez contribuer à un projet open source majeur. On vous demande de signer un CLA avant que votre "Pull Request" ne soit acceptée.

1. Est-ce que cela signifie que vous perdez la propriété de votre code ?
2. Pourquoi l'organisation refuse-t-elle votre code sans cette signature ?

??? success "Résultat attendu"
    Le contributeur reste généralement auteur, mais il donne une licence d'exploitation irrévocable à l'organisation pour éviter tout blocage juridique futur.

### Exercice : Analyse du cas Bambu Lab

**Temps** : 20 minutes

Bambu Lab affirme que le fork de Jarczak « usurpe » l'identité de leur client officiel parce que le logiciel envoie le même *User-Agent* que Bambu Studio lorsqu'il contacte les serveurs cloud. Sachant que Jarczak n'a **pas modifié** cette partie du code — il réutilise le code AGPL original de Bambu Lab tel quel — répondez aux questions suivantes :

1. Est-ce une violation de la licence AGPL de redistribuer du code AGPL sans le modifier ?
2. Bambu Lab invoque la section 1201 du DMCA (contournement de verrou numérique). En quoi cet argument est-il contestable dans ce contexte précis ?
3. Quelle distinction cruciale Bambu Lab tente-t-il de faire entre la licence AGPL du code et ses conditions d'utilisation (ToS) du cloud ? Cette distinction suffit-elle à justifier le retrait du dépôt ?
4. Pourquoi Louis Rossmann a-t-il décidé de publier lui-même le code sur son propre GitHub plutôt que de simplement financer les frais juridiques de Jarczak ?

??? success "Résultat attendu"
    1. Non — redistribuer du code AGPL sans modification est exactement ce que la licence autorise et encourage.
    2. La section 1201 du DMCA interdit de *contourner* un verrou numérique. Ici, le serveur de Bambu Lab acceptait les requêtes nativement; aucun verrou n'a été forcé. L'argument est sans fondement technique.
    3. Bambu Lab distingue le code (AGPL, libre) du service cloud (propriétaire, régi par les ToS). C'est une distinction légalement valide pour l'*accès au service*, mais la plainte visait le *code* lui-même, ce qui rend l'argument incohérent.
    4. En publiant le code sur son propre dépôt, Rossmann s'expose volontairement aux poursuites, ce qui lui permet de contester l'affaire en son propre nom avec les ressources juridiques de sa fondation (Futo Foundation), tout en envoyant un signal fort que la menace légale n'impressionne pas.

## Évaluation

### Questions d'Auto-Évaluation

1. Si je crée un fork d'un projet AGPL, ai-je le droit de le redistribuer?
2. Quelle licence permet de lier une bibliothèque à un code propriétaire sans ouvrir ce dernier ?
3. Pourquoi Louis Rossmann a-t-il offert 10 000 $ pour défendre le développeur du fork d'OrcaSlicer?
4. Quelle est la seule obligation réelle imposée par la licence MIT lors de la redistribution d'un logiciel?
5. Quelle est la différence majeure entre une licence logicielle (comme MIT) et un accord de contribution (CLA)?


??? note "Réponses attendues"
    1.  Oui, absolument. La licence AGPL exige seulement que vous publiiez le code source de votre fork.
    2.  La LGPL.
    3.  Pour s'opposer à l'intimidation juridique contre l'usage légitime de code open source.
    4.  Conserver l'avis de droit d'auteur original (*copyright notice*) dans toutes les copies ou portions substantielles du logiciel.
    5.  La licence MIT définit comment le logiciel peut être utilisé par tous, tandis que le CLA définit les droits que le contributeur cède à l'organisation pour protéger le projet.


## Résumé

Les licences comme la GPL et l'AGPL protègent la liberté du code, mais elles ne garantissent pas l'accès gratuit aux services cloud associés. Le cas Bambu Lab illustre parfaitement cette tension : une entreprise peut être obligée de partager son code (AGPL) tout en essayant de verrouiller son écosystème par des moyens juridiques et des serveurs privés.

## Ressources Supplémentaires

* [ChooseALicense.com - Comparaison des licences open source](https://choosealicense.com/)
* [TLDRLegal - Résumés de licences](https://tldrlegal.com/)
* [Vidéo de Louis Rossmann sur Bambu Lab](https://www.youtube.com/watch?v=1jhRqgHxEP8)
* [Article All3DP : Bambu Lab vs OrcaSlicer Fork](https://all3dp.com/4/bambu-lab-took-down-an-orcaslicer-fork-and-handed-it-a-bigger-audience/)
* [GNU.org - Pourquoi utiliser la LGPL ?](https://www.gnu.org/licenses/why-not-lgpl.fr.html)

