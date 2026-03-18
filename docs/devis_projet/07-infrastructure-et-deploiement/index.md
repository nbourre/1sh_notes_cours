# 7. Infrastructure et déploiement

Un projet n’est pas terminé quand le code fonctionne sur l’ordinateur du développeur. Il faut encore l’héberger, le rendre accessible, le sécuriser et prévoir sa mise en ligne. Cette partie est souvent sous-estimée dans les devis, alors qu’elle représente un travail réel.

## Ce que couvre l’infrastructure

Selon le contexte, il faut prévoir :

- l’hébergement;
- les environnements de développement, test et production;
- le nom de domaine;
- le certificat SSL;
- la sauvegarde;
- les journaux;
- parfois une stratégie CI/CD.

## Pourquoi cette section est souvent oubliée

Plusieurs personnes pensent au projet comme à une suite de pages et de fonctionnalités. Pourtant, sans déploiement, il n’y a pas de livraison exploitable. Même une petite application peut nécessiter la configuration d’un serveur, d’une base de données, de secrets d’environnement et de mécanismes de redémarrage.

## Questions à clarifier

- Où l’application sera-t-elle hébergée?
- Qui gère l’infrastructure?
- Faut-il prévoir plusieurs environnements?
- Le déploiement doit-il être automatisé?
- Quelles sont les attentes en disponibilité et en reprise après incident?
## Exemple

Un freelance livre une application web à un client. Le code fonctionne sur son ordinateur. Au moment de la mise en ligne, il faut : choisir un hébergeur, créer les bases de données de production, configurer les variables d'environnement, obtenir un certificat SSL, tester le domaine, mettre en place les sauvegardes automatiques et vérifier les journaux d'erreurs. Tout cela prend plusieurs heures, parfois des jours si des problèmes surviennent. Si ces activités n'ont pas été incluses dans le devis initial, le projet se termine avec un dépassement de coût.
## Éléments qui augmentent l’effort

- plusieurs environnements;
- pipeline CI/CD;
- surveillance et alertes;
- procédures de sauvegarde;
- haute disponibilité;
- contraintes réseau ou institutionnelles.

## Mini-checklist

- [ ] Le mode d’hébergement est choisi
- [ ] Les environnements requis sont définis
- [ ] Les besoins de SSL et de domaine sont prévus
- [ ] Les sauvegardes sont considérées
- [ ] Le mode de déploiement est précisé

## À retenir

Le déploiement fait partie du produit. Si cette charge n’apparaît pas dans le devis, elle réapparaîtra plus tard sous forme de dépassement.
