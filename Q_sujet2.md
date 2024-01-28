# Mots-clefs

- iot dans le contrôle qualité (air, eau, sol, biodiversité)
- logiciel : config, mise à jour, calibration des paramètrages produit
- projet application mobile pour config depuis tel (IOS Android)
- techno : JS - TS - React Native (app) - Electron (deskstop)
- besoin humain : ++ dev seniors full stack JS au fait de RN et Electron

- 5 teams de 10 dev (postes à revoir?)
- j'intègre l'équipe de DX pour ce projet

## Problèmes rencontrés
- Repos différents => souhaite gérer les modifs (et les déployer) de manière centralisée
- modif actuel de repo = long process / trop d'étapes / trop contraignant 
- besoin de modifier toute les parties lorsque maj produit (ex firmware)
- partie front : manque de docs / pas de tests automatisés (back : units tests)
- pas de retour erreurs code / rien de précis
- erreurs fréquentes liés aux versions de navigateurs / syst expl / firmwares 
- erreurs de connexion

# Propositions
L'objectif est donc de rassembler tout nos projets dans un seul repository.   => Monorepo
Nous souhaiterions des propositions sur l'amélioration :
- du workflow de développement (éviter les npm link et les PR de sous projets) => recherches à faire + créer branche develop
- de la qualité du code et d'un code beaucoup plus homogène = linter type eslint (comparaison avec d'autres) / Prettier / Husky +++
- éviter les regressions => test (units)
- automatiser le plus de choses possibles => CI/CD, Github Actions, Docker
- avoir une documentation à jour => library (storybook + comparaison autres)

# Cours
# Sources
# Inspi sujet 1
