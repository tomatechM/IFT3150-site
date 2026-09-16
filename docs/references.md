---
title: Travail réalisé
---

<style>
    @media screen and (min-width: 76em) {
        .md-sidebar--primary {
            display: none !important;
        }
    }
</style>

# Références

> :bulb: Cette page rassemble les **principales sources et ressources utilisées dans le cadre du projet**.  
> 
> Elle permet également de préciser **comment ces ressources ont contribué au travail réalisé**.


## Références utilisées

> Selon la nature du projet, vous pouvez notamment référencer :
>
> * articles scientifiques ou techniques ;
> * livres et ouvrages de référence ;
> * documentation officielle ;
> * normes et spécifications ;
> * bibliothèques, frameworks et outils importants ;
> * jeux de données et API ;
> * projets ou solutions existantes étudiées ;
> * rapports, études ou publications institutionnelles ;
> * ressources Web pertinentes.
>
> Il n'est pas nécessaire de répertorier chaque page consultée. Privilégiez les références qui ont **réellement soutenu, orienté ou influencé votre travail**.

### Présentation des références

> Pour chaque référence importante, fournissez :
>
> * les informations permettant d'identifier et de retrouver la source ;
> * une courte justification de **1 à 2 phrases** expliquant son rôle dans le projet.
>
> La justification peut notamment indiquer si la référence a servi à :
>
> * comprendre le problème ;
> * comparer des approches ;
> * orienter un choix technique ;
> * concevoir ou implémenter une solution ;
> * définir une méthode d'évaluation ;
> * interpréter des résultats.

### Exemple

> **Mozilla Developer Network.** *Web APIs*.
> https://developer.mozilla.org/
>
> Cette documentation a été utilisée comme référence principale pour comprendre le fonctionnement des API Web exploitées dans l'application et valider certains choix d'implémentation.

> **Nom de l'auteur.** *Titre de l'article*. Nom de la publication, année.
>
> Cet article a permis de comparer différentes approches au problème étudié et a contribué au choix de la méthode retenue dans le projet.

## Utilisation de l'intelligence artificielle

> Documentez les principaux usages de **systèmes d'intelligence artificielle générative ou d'assistants basés sur des modèles de langage** dans le cadre du projet.
>
> L'objectif n'est pas de retranscrire l'ensemble des conversations ou requêtes effectuées, mais de rendre explicite **le rôle joué par ces outils dans votre démarche**.

### Pour chaque outil utilisé

> Indiquez, lorsque pertinent :
>
> * le nom de l'outil ou du modèle utilisé ;
> * les principales tâches pour lesquelles il a été employé ;
> * la manière dont les résultats produits ont été vérifiés, adaptés ou intégrés au projet ;
> * les limites ou problèmes rencontrés lors de son utilisation.

### Exemple

> **ChatGPT — OpenAI**
>
> Utilisé principalement pour explorer différentes stratégies de traitement des données et générer des pistes d'implémentation. Les propositions obtenues ont été vérifiées à partir de la documentation officielle et adaptées à l'architecture du projet avant leur intégration.

> **GitHub Copilot**
>
> Utilisé ponctuellement pour assister la rédaction de code répétitif et de tests. Le code généré a été révisé et testé par l'équipe avant d'être conservé dans le projet.

## Références

### Articles scientifiques sur la revue de code

#### George David Apostolidis - Evaluation of Python code quality using multiple source code analyzers

>George David Apostolidis. Evaluation of Python code quality using multiple source code analyzers. 2023. ResearchGate.

Cette thèse a servi à mieux comprendre les différents outils d'analyse de revue de code pour Python. Cela a permis de déterminer les outils qui seront utiles à la revue de code de FinScope.

#### Bacchelli et Bird — Expectations, Outcomes, and Challenges of Modern Code Review

> Bacchelli, A. et Bird, C. Expectations, Outcomes, and Challenges of Modern Code Review. Proceedings of the International Conference on Software Engineering (ICSE), 2013. IEEE.
Microsoft Research

Cet article a servi à mieux comprendre le rôle de la revue de code moderne. Les auteurs montrent que, bien que la détection de défauts constitue une motivation importante, les revues de code amènent aussi d'autres bénéfices, comme le transfert de connaissances et l'amélioration de la compréhension du code. Cette étude a contribué à orienter le projet vers une revue qui ne se limite pas à la recherche de bugs, mais qui examine également la conception, la maintenabilité et la compréhension du logiciel.

#### Mäntylä et Lassenius — What Types of Defects Are Really Discovered in Code Reviews?

> Mäntylä, M. V. et Lassenius, C. What Types of Defects Are Really Discovered in Code Reviews? IEEE Transactions on Software Engineering, vol. 35, no. 3, 2009, pp. 430–448.
Référence — Aalto University

Ce papier a servi à mieux comprendre que les commentaires en lien avec la lisibilité, les bugs et la maintenabilité ont un plus grand pourcentage de résolution que ceux de l'architecture et la conception du code. 

#### Rigby et Bird — Convergent Contemporary Software Peer Review Practices

> Rigby, P. C. et Bird, C. Convergent Contemporary Software Peer Review Practices. Proceedings of the 2013 9th Joint Meeting on Foundations of Software Engineering (ESEC/FSE), 2013. ACM.
Microsoft Research

Cet article a servi à approfondir la compréhension des pratiques générales de ceux qui font de la revue de code dans un contexte industriel et open source. 

### Ressources méthodologiques pour la revue de code

#### Google Engineering Practices — Code Review

> Google. Google Engineering Practices — Code Review.
[Google Engineering Practices](https://google.github.io/eng-practices/review/reviewer/looking-for.html)

### Sécurité

#### OWASP — Secure Code Review Cheat Sheet

> OWASP. Secure Code Review Cheat Sheet. [OWASP Cheat Sheet Series](https://github.com/OWASP/www-project-code-review-guide).

Cette ressource est utilisée pour structurer l'analyse de sécurité de FinScope. Elle fournit notamment des recommandations concernant l'architecture, les points d'entrée, la validation des données, l'authentification, l'autorisation, les flux de données, la logique métier, la gestion des erreurs et la configuration. Elle sert également à identifier les aspects qui nécessitent une vérification manuelle en complément des outils automatisés.

### Documentation du projet FinScope

#### FinScope — dépôt GitHub

> Syriani, E. et collaborateurs. FinScope. GitHub. https://github.com/esyriani/FinScope

#### Développement assisté par l'intelligence artificielle

> OpenAI — Codex

#### Outils d'analyse

Ruff

> Astral. Ruff — An extremely fast Python linter and code formatter.
[Documentation Ruff](https://docs.astral.sh/ruff/)

Ruff est utilisé pour effectuer une partie de l'analyse statique du code Python.

Mypy

> Mypy Project. Mypy — Optional Static Typing for Python.
[Documentation Mypy](https://mypy.readthedocs.io/)

Mypy est utilisé pour analyser statiquement le typage du code Python.

Bandit

> PyCQA. Bandit — Security oriented static analyser for Python.
[Documentation Bandit](https://bandit.readthedocs.io/)

Bandit est utilisé pour rechercher automatiquement certaines constructions potentiellement dangereuses dans le code Python.