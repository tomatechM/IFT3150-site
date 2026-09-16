---
title: Suivi du projet
---

<style>
    @media screen and (min-width: 76em) {
        .md-sidebar--primary {
            display: none !important;
        }
    }
</style>

# Suivi de projet

---

## Semaine 1-2 (7-19 septembre)

### Objectifs de la période
- Clarifier la problématique.
- Étudier les articles scientifiques sur le code review.
- Lire la documentation du projet.
- Compléter une vue d'ensemble du projet ainsi qu'une méthodologie initiale.
- Tester l'application en tant qu'utilisateur.

### Travail réalisé

!!! abstract "Avancement"
    - [x] Clarifier la problématique
    - [x] Étudier plus au sujet du code review
    - [x] Compléter une vue d'ensemble initiale du projet
    - [x] Tester l'application en tant qu'utilisateur
    - [ ] Lire la documentation du projet



### Décisions et ajustements

- Les résultats des outils automatisés seront vérifiés manuellement avant d'être considérés comme des problèmes confirmés.
- Après la lecture de la documentation, je me suis aperçu qu'il y a déjà des analyses statiques effectuées avec des outils tels que Ruff et Mypy. Donc la section de l'analyse statique énoncé dans la vue d'ensemble sera mise de côté pour d'autres sections plus importantes.


### Difficultés rencontrées

!!! warning "Difficultés"
    - Problème de l'éxecution de l'application
        - Dans le README, il est indiqué que, pour lancer l'application FinScope, il suffit d'installer les dépendances dans `requirements.txt` mais ce n'est pas le cas.
        - Résolu après installé les dépendances dans `requirements-dev.txt` du côté développeur.
