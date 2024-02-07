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

- Nous avons également de plus en plus de mal à intégrer nos développeurs sur la partie front. Certains réclames des documentations ou des tests mais notre QA ne fait que des tests physiques et n'a pas le temps de faire des tests automatisés. Sur le back et l'electronique les développeurs utilisent des tests unitaires mais sur le front rien n'est fait.
- du mal à analyser les erreurs rencontrées par nos utilisateurs
- avoir des informations plus précises sur le code qui ne fonctionne pas, retours d'erreurs, etc...
- cas liés à des versions de navigateurs, ou des versions de systèmes d'exploitation, ou encore des versions de firmwares. Mais aussi des problèmes de connexions.
- avoir des informations plus précises sur ces cas là.

# Propositions
L'objectif est donc de rassembler tout nos projets dans un seul repository.   => Monorepo
Nous souhaiterions des propositions sur l'amélioration :
- du workflow de développement (éviter les npm link et les PR de sous projets) => recherches à faire Monorepo / pourquoi ? quel outil ? adapté au projet ? + créer branche develop 
- de la qualité du code et d'un code beaucoup plus homogène = linter type eslint tslint config personnalisée ou config standard (comparaison avec d'autres) / Prettier / Husky +++ / Codecov / parler de la qualité
- éviter les regressions / un code fonctionne puis ne fonctionne plus après maj => test (units) describe TDD 
- automatiser le plus de choses possibles => CI/CD (Docker), Github Actions, dockerHub, test end to end, units, build (les QA gèrent les tests) graphQL
- avoir une documentation à jour => library (storybook + comparaison autres) jira confliuence atlassian dinosorus

# Sommaire

Présentation problèmatique

Recherches IOT : 
IOT : 4 points importants / qualité sécurité réactivité monitoring
(https://www.youtube.com/watch?v=LPNMlP165v4)
=> tests fréquents = métriques ? 
(https://www.milesweb.in/blog/technology-hub/what-is-the-connection-between-iot-and-devops/)
(https://devops.com/a-devops-guide-to-iot-technology/)
=> JS IOT : (https://www.moussasoft.com/javascript-et-iot-analyse-framework-johnny-five)
Top 10 javascript framework use in IOT : (https://medium.com/@softapptechnologies5/top-10-javascript-framework-use-in-iot-f915247645b5)

# Monorepo

J'ai bien compris votre problématique qui est la complexité et la fluidité dans les étapes de déplaiement [...], c'est pourquoi je préconise la mise en place d'un monorepository. Un dossier unique qui fera office de plateforme de travail.  
[monorepo](./monorepo.md)

# Qualité
[qualité](./qualite.md)

# Automatisation
[automatisation](./automatisation.md)

# Documention
[documentation](./documentation.md)

# Conclusion



# Inspi sujet 1
- livraison continue / déploiement continu 
