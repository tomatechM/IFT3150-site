---
title: Vue d'ensemble du projet
---

<style>
    @media screen and (min-width: 76em) {
        .md-sidebar--primary {
            display: none !important;
        }
    }
</style>

# Vue d'ensemble du projet

!!! info "Informations générales"
    **Session**: Automne 2026  
    **Auteur(s)**: Mohamed Atmani (20218934) <!-- Nom de chaque membre (matricule)  -->  
    **Thème(s)**: Revue de code de FinScope<!-- Thèmes principaux abordés dans le projet  -->  
    **Superviseur(s)**: Eugene Syriani (DIRO)<!-- Nom du superviseur (affiliation)  -->  

## Description du projet

FinScope est une application Web locale de gestion des finances personnelles. Elle permet d'importer des relevés bancaires, de catégoriser les transactions, de gérer des règles de catégorisation, de réviser les marchands inconnus et d'analyser les dépenses et les revenus au fil du temps. L'application a aussi des fonctionnalités liées aux comptes, aux catégories, aux étiquettes, aux remboursements et aux activités récurrentes. Elle supporte l'utilisation en français et en anglais ainsi que différents modes d'affichage.

Le projet FinScope a été développé à l'aide d'une approche de « vibe coding », en utilisant l'agent Codex pour générer le code source, la documentation et les tests. Le code a fait l'objet d'une révision manuelle limitée, donc il est fort probable qu'il y ait des problèmes de qualité, des code smells et d'autres défauts encore présents dans le code.

Dans le cadre de ce projet, l'objectif n'est donc pas de développer de nouvelles fonctionnalités pour FinScope, mais de faire une revue systématique de son code existant et d'évaluer sa qualité, d'identifier les problèmes susceptibles de nuire à sa fiabilité, sa sécurité, sa maintenabilité et son évolution future.

### Contexte

L'utilisation croissante d'outils d'intelligence artificielle générative transforme de plus en plus les pratiques de développement logiciel. Des agents comme Codex peuvent produire rapidement des applications relativement complètes, générer des tests et créer de la documentation à partir d'instructions en langage naturel. Cette approche permet d'accélérer considérablement le développement, mais elle soulève également des questions concernant la qualité, la cohérence et la maintenabilité du logiciel produit.

Le projet FinScope est un cas d'étude intéressant puisqu'il a été développé entièrement avec du vibe coding. L'application possède déjà une architecture relativement complète, comprenant notamment une couche Web, une gestion de données avec SQLAlchemy, des bases SQLite/MySQL, des traitements en arrière-plan, une interface Web et une suite de tests automatisés. 

Dans ce contexte, une revue de code permet de mettre en évidence les forces et les faiblesses d'un logiciel produit à l'aide d'un agent. Elle permet également de mieux comprendre dans quelle mesure les outils de génération de code peuvent produire un système qui respecte les principes de qualité logicielle et les bonnes pratiques de développement.

### Problématique

Le développement assisté par des agents permet de produire rapidement une grande quantité de code, mais la rapidité de génération ne garantit pas nécessairement sa qualité. Du code généré automatiquement peut contenir des erreurs fonctionnelles, des vulnérabilités, des duplications, des choix architecturaux discutables, des dépendances inutiles ou encore des tests insuffisants.

Dans le cas de FinScope, ces problèmes sont particulièrement importants puisque l'application manipule des données financières personnelles. Une erreur fonctionnelle ou une faiblesse de sécurité pourrait donc avoir des conséquences importantes pour les utilisateurs.

La problématique centrale du projet est donc la suivante :

> **À quel point est-ce que le code généré par une approche de « vibe coding » pour FinScope respecte-t-il les principes de qualité logicielle, et quels problèmes pourraient compromettre sa fiabilité, sa sécurité, sa maintenabilité ou son évolutivité?**

### Proposition et objectifs

Le projet propose de réaliser une revue de code structurée et systématique de FinScope. L'analyse combinera différentes techniques afin de couvrir à la fois les aspects statiques, dynamiques, fonctionnels et architecturaux de l'application.

Les principaux objectifs sont les suivants :

* Évaluer la qualité générale du code en identifiant les mauvaises pratiques, les code smells, les duplications, la complexité excessive et les problèmes de maintenabilité.
* Identifier les vulnérabilités et problèmes de sécurité, particulièrement ceux qui concernent l'authentification, l'autorisation, la gestion des entrées utilisateur, les données financières, les secrets, les accès à la base de données et les communications avec des services externes.
* Évaluer la robustesse fonctionnelle de l'application en recherchant des comportements incorrects, des cas limites non traités et des incohérences entre les fonctionnalités attendues et leur implémentation.
* Analyser l'architecture et la conception du logiciel afin d'identifier les responsabilités mal réparties, le couplage excessif, les dépendances problématiques et les violations potentielles des principes de conception.
* Évaluer la qualité et la couverture des tests en vérifiant si les fonctionnalités importantes et les scénarios critiques sont suffisamment bien testés.
* Identifier le code inutile, redondant ou difficilement justifiable, afin de déterminer les possibilités de simplification et de réduction de la dette technique.
* Produire un rapport de revue de code reproductible, regroupant les problèmes observés, leur gravité, leurs conséquences potentielles et, lorsque pertinent, des recommandations de correction.

### Méthodologie

La revue sera réalisée progressivement afin de combiner plusieurs sources d'information et d'éviter de dépendre d'une seule technique d'analyse.

#### Compréhension du système
- Une première étape consistera à étudier la structure générale de FinScope, sa documentation, son architecture et ses principales fonctionnalités. Le dépôt contient notamment les répertoires src/finance_app, tests et docs, ainsi que la configuration nécessaire aux outils de développement et d'intégration continue
- Cette étape permettra d'établir une compréhension de référence du système avant d'évaluer individuellement ses composants.

#### Analyse statique
- Des outils d'analyse statique comme Ruff, Mypy et Bandit seront utilisés pour rechercher automatiquement différents types de problèmes :

    1. complexité excessive
    2. duplication de code
    3. erreurs potentielles
    4. mauvaises pratiques
    5. problème de typage
    6. problème de style
    7. dépendances problématiques
    8. vulnérabilités connues
    9. code mort

Les résultats automatiques seront ensuite examinés manuellement afin de distinguer les véritables problèmes des faux positifs.

#### Revue manuelle du code
Une revue manuelle sera réalisée sur les parties importantes de l'application afin d'identifier les problèmes qui ne peuvent pas être détectés correctement par des outils automatisés.

#### Analyse des tests
La suite de tests existante sera analysée afin d'évaluer :

- les fonctionnalités couvertes
- les fonctionnalités insuffisamment couvertes
- la présence de tests unitaires et d'intégration
- la qualité des assertions
- les cas limites
- les scénarios d'erreur
- la facilité d'exécution et de maintenance des tests


#### Tests dynamiques et scénarios d'utilisation
L'application sera exécutée afin de vérifier son comportement réel dans différents scénarios. Des cas normaux, des cas limites et des entrées invalides seront utilisés pour essayer de provoquer des comportements inattendus.

Cette étape va permettre de comparer le comportement observé avec celui attendu à partir de la documentation et des fonctionnalités annoncées.

#### Classification et priorisation des problèmes
Chaque problème identifié sera documenté et classifié selon sa nature, par exemple :

- défaut fonctionnel
- vulnérabilité de sécurité
- problème de conception
- problème de maintenabilité
- duplication ou redondance
- problème de test
- problème de performance
- problème de documentation

Les problèmes vont être ensuite priorisés selon leur gravité et leur facilité de correction

#### Synthèse

Les résultats des différentes analyses seront regroupés afin de produire une vue d'ensemble de la qualité du projet. Cette synthèse permettra de déterminer les catégories de problèmes les plus fréquentes et les zones du code présentant le plus de risques.

### Validation et Évaluation

La qualité de la revue sera évaluée à partir de plusieurs indicateurs quantitatifs et qualitatifs.

Les principaux indicateurs vont être :

- nombre total de problèmes identifiés
- nombre de problèmes par catégorie
- nombre de problèmes selon leur niveau de gravité
- nombre de vulnérabilités détectées
- niveau de couverture des tests
- nombre de tests réussis et échoués
- nombre de duplications ou de problèmes de complexité détectés
- proportion des problèmes confirmés manuellement parmi ceux détectés automatiquement
- nombre de fonctionnalités critiques couvertes correctement par les tests
- reproductibilité des problèmes identifiés

(Maybe) Les résultats des outils automatisés seront comparés à ceux de la revue manuelle. Pour les problèmes importants, des scénarios de reproduction seront documentés pour qu'un autre développeur puisse confirmer le problème.

## Échéancier

!!! info
    Le suivi complet est disponible dans la page [Suivi de projet](suivi.md).

| Activités                      | Début   |   Fin   | Livrable                            | Statut      |
|--------------------------------|---------|---------|-------------------------------------|-------------|
| Ouverture de projet            | 4 mai   | 15 mai  | Proposition de projet               | ✅ Terminé  |
| Études préliminaires           | 4 mai   | 22 mai  | Document d'analyse                  | 🔄 En cours |
| Présentation + Rapport         | 7 aout  | 14 aout | Présentation + Rapport              | ⏳ À venir  |
