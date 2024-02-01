# Mots-clefs

- iot dans le contrôle qualité (air, eau, sol, biodiversité)
- logiciel : config, mise à jour, calibration des paramètrages produit
- projet application mobile pour config depuis tel (IOS Android)
- techno : JS - TS - React Native (app) - Electron (deskstop)
- besoin humain : ++ dev seniors full stack JS au fait de ReactNative et Electron

- 5 teams de 10 dev (postes à revoir?)
- j'intègre l'équipe de DX pour ce projet

## Problèmes rencontrés
- Repos différents => souhaite gérer les modifs (et les déployer) de manière centralisée
- modif actuel de REPO = long process / trop d'étapes / trop contraignant 
- besoin de modifier toute les parties lorsque maj produit (ex firmware)
        => Actuellement, si l'on modifie un repository, il faut faire une pull request, attendre la validation, puis faire une release, puis attendre la validation, puis déployer, puis attendre la validation. Et seulement après, il                 faudrait faire la même chose pour les autres repositories concernés par la modification.
          Si je modifie le firmware du capteur d'air. Il faudra changer l'application mobile, l'application desktop, le backend, et le frontend web.
- partie FRONT : manque de docs / pas de tests automatisés (back : units tests)
- pas de retour erreurs code / rien de précis
- erreurs fréquentes liés aux versions de navigateurs / syst expl / firmwares 
- erreurs de connexion

# Propositions
L'objectif est donc de rassembler tout nos projets dans un seul repository.   => Monorepo
Nous souhaiterions des propositions sur l'amélioration :
- du workflow de développement (éviter les npm link et les PR de sous projets) => recherches à faire + créer branche develop 
- de la qualité du code et d'un code beaucoup plus homogène = linter type eslint (comparaison avec d'autres) / Prettier / Husky +++
- éviter les regressions / un code fonctionne puis ne fonctionne plus après maj => test (units) describe 
- automatiser le plus de choses possibles => CI/CD, microservices? Github Actions, Docker
- avoir une documentation à jour => library (storybook + comparaison autres)

# Cours

## Rappel : qu'est ce que le DevOps ? 
Le DevOps est ensemble de pratiques qui met l'emphase sur l'automatisation des processus entre les équipes de développement, et les équipes en charge du maintien en conditions opérationnelles de l'application développée.
Outils mais pas que : histoire de culture et de collaboration entre les développeurs et les opérateurs. Réelle volonté de travailler ensemble.
Le DevOps résout, en premier lieu, des problèmes humains, des problèmes de communication et des problèmes de responsabilités entre équipes. Dans ce sens, le DevOps se rapproche de l'agilité, mais en incluant d'autres équipes comme les opérations, les testeurs, les designers, les développeurs, les chefs de projet, et en règle générale, toute personne dont les aptitudes sont requises afin de délivrer un produit de qualité.
(COURS ANTHO)

- IAC : infrastructure as code
- Test-Driven-Development (TDD) ou le Behavior-Driven-Development (BDD) + tests de performance, les tests de charge ou même les tests de bout-en-bout
Sur ces types de tests, il est nécessaire d'avoir un environnement configuré correctement pour simuler des contraintes de production, ou des chaînes complètes entre applications. Comme les tests et l'infrastructure sont versionnés au même niveau que le code, tout changement de l'une de ces trois briques (tests, infrastructure et code) relance automatiquement toute la chaîne dans un processus complet. Dès lors, il est facile de rejouer des campagnes de tests de non-régression complète en quelques minutes, ou en quelques heures si la chaîne de bout en bout couvre une grande partie des fonctionnalités.
- Lean management (amélioration continue et acceptation des erreurs) : types de gaspillage concernés ici :
                  - attente 
                  - étapes inutiles
                  - mouvements inutiles
                  - corrections / retouches
- KPI ? indicateurs de performance / mesurer l'utilité
- SRE Site Reliability Engineer : Service Level Indicator / Service Level Objective : latence, trafic, erreurs et saturation

- CI : Détection précoce des problèmes / Livraisons plus fréquentes / Confiance dans le code / Collaboration facilitée / Historique des modifications
- - - - - Compilation : compiler avec Maven, Ant, Gradle, MSBuild, NAnt, Gulp ou Grunt.
- - - - - Tester le code : tests unitaires pour garantir la qualité du code (+ de tests = + de sûreté). Doit être maintenu dans le temps en fonction des évolutions du code.
- - - - - Qualité du code : minimiser la dette technique (exprimé en heures de correction, le temps nécessaire à la correction de bugs ou à l’ajout de nouvelles fonctionnalités lorsque nous ne respectons pas les règles de coding).
- - - - - Sécurité du code : détection des failles de sécurité, et d'autres métriques comme le nombre de vulnérabilités au sein du code, la couverture de test, mais aussi les code smells (qui sont des mauvaises pratiques à ne pas                   implémenter), la complexité cyclomatique (complexité du code applicatif) ou la duplication de code.
- - - - - La création des livrables : le packaging et les artefacts ????? Conteneurs ?
Orchestration et mise en place un pipeline CI/CD
- - - - - Le Workflow : définition d'un product backlog puis sprint backlog / respect de la "Definition of Ready" définie au préalable
- - - - - Compilation et test en continu : 
- - - - - stucture du dépôt git, 2 modèles (trunk-based development / gitflow)
- - - - - pipeline d'intégration continue : objectif principal, détecter rapidement les conflits de code, les erreurs de compilation, les régressions et les problèmes de compatibilité.
          automatiser toutes les étapes de compilation, de test, de vérification de la qualité du code et de packaging. Les phases de ce pipeline seront lancées successivement, lors de chaque nouveau push 
          du code sur le repository. Build / Tests / Cache / Job / Image pour l'execution du script
- - - - - Tests : 1 fail = stop du pipeline
- - - - - Unitaires (enjeux) : - appliqués tout le long du développement = feeaback rapide
                               - sécuriser la maintenance : regressions signalées après modifications de programme
                               - tests en rapport avec l'application = documentation
          Ces tests doivent être relancées après chaque modif. Si bug = modifier code ou test.
- - - - - Autres tests possibles : tests de performance ou d’acceptation utilisateur en préproduction, smoke tests en production afin de garantir le fonctionnement normal de l’application en production.
- - - - - Mesure de la qualité du code : - AST(Static Application Security Testing) peut être lancé en même temps que les tests unitaires
                                         - DAST(Dynamic Application Security Testing)
                                         - IAST(Interactive Application Security Testing)
- - - - - Conteneurisation de l'application
- - - - - 
- - - - - 
- - - - - 






# Sources à lire
IAC (https://www.ibm.com/fr-fr/topics/infrastructure-as-code)
https://about.gitlab.com/topics/devops/
https://management-digital.macertif.com/DevOps/
https://www.qrpinternational.fr/blog/faq/10-profils-devops/
https://www.atlassian.com/fr/devops/what-is-devops
https://www.softfluent.fr/blog/mettre-en-place-methode-devops/
https://carrieres.groupeozitem.com/blog/challenges-devops-sysops
https://www.atlassian.com/fr/continuous-delivery/continuous-integration/trunk-based-development
https://www.atlassian.com/fr/git/tutorials/comparing-workflows/gitflow-workflow

# Inspi sujet 1
