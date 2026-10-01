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

## Semaine 3-4 (20 septembre - 3 octobre)

### Objectifs de la période
- Éxécuter les tests implémentés et étudier la couverture des tests
- Finir la lecture de la documentation
- Commencer l'analyse de l'architecture du code

### Travail réalisé

!!! abstract "Avancement"
    - [x] Éxécution des tests implémentés et étude de la couverture des tests
        - 1365 tests passés avec une couverture de tests de 93%
    - [x] Finir la lecture de la documentation
    - [x] Commencer l'analyse de l'architecture du code
        - La première analyse a été réalisé pour le module /transactions, un module important qui comporte 10 fichiers de code.
        - L'analyse s'est basé sur 3 points :
            - La lisibilité du code (la qualité des commentaires)
            - Le code respecte-t-il les règles d'architecture de la documentation AGENTS.md ?
            - Le code respecte-t-il les normes de qualité logiciel (faible couplage et forte cohésion)

### Décisions et ajustements

!!! info "Décisions"
    - Suite à la première analyse, il y aura un changement sur le plan de l'analyse. 
    -  Plus précisemment, au lieu de regrouper les problèmes observés et en recommander des corrections :
        - Développer une généralisation des problèmes qui se répètent à plusieurs reprises partout dans le code. Cela permettra de déterminer les points faibles et les mauvaises pratiques à prendre en compte lors de l'utilisation d'un agent IA
        - Ensuite, de ces généralisations, déterminer des solutions applicables pour chaque cas.
