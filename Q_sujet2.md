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
- du workflow de développement (éviter les npm link et les PR de sous projets) => recherches à faire Monorepo / pourquoi ? quel outil ? adapté au projet ? + créer branche develop 
- de la qualité du code et d'un code beaucoup plus homogène = linter type eslint tslint config personnalisée ou config standard (comparaison avec d'autres) / Prettier / Husky +++ / Codecov / parler de la qualité
- éviter les regressions / un code fonctionne puis ne fonctionne plus après maj => test (units) describe TDD choisir métriques (qualité mesure des données, air eau etc ...) (demander confirmation), code coverage
- automatiser le plus de choses possibles => CI/CD (Docker), Github Actions, dockerHub, test end to end, units, build (les QA gèrent les tests) graphQL
- avoir une documentation à jour => library (storybook + comparaison autres) jira confliuence atlassian dinosorus

# Sommaire

Présentation DevOps
Présentation problèmatique

# Rédaction

J'ai bien compris votre problématique qui est la complexité et la fluidité dans les étapes de déplaiement [...], c'est pourquoi je préconise la mise en place d'un monorepository. Un dossier unique qui fera office de plateforme de travail.  
[workflow](./monorepo.md)


# Inspi sujet 1
- livraison continue / déploiement continu 
