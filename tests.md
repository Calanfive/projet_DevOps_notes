# Problèmes du sujet : utilisation actuelle / conséquences
- partie FRONT : manque de docs / pas de tests automatisés (back : units tests)
- erreurs fréquentes liés aux versions de navigateurs / syst expl / firmwares
- erreurs de connexion
- du mal à analyser les erreurs rencontrées par nos utilisateurs
- avoir des informations plus précises sur le code qui ne fonctionne pas, retours d'erreurs, etc...

# Souhait du client et objectif
- mettre en place des tests automatisés en back / éviter => le QA n'a pas le temps mais c'est son travail. TDD, tests units
- avoir des retours sur les erreurs => fréquence, type (log) winston ?
- régler les soucis de compatibilité => docker, image, dockerhub et conteneurisation
- automatiser le plus de choses possibles => CI/CD yml

Tendre vers le Lean management (amélioration continue et acceptation des erreurs) : types de gaspillage concernés ici : attente étapes inutiles mouvements inutiles corrections / retouches

# Tests 
Je préconise la mise en place de tests unitaires et d'avoir une approche de développement orientée Test-Driven Developement.
[SCREENSHOT TDD]

# Log
Utilisation de Winston

# Docker
Après la phase d'intégration continue, viendra la création d'une image exploitable sur Dockerhub. Cela permettra la conteneurisation de notre application, première étape du déploiement continu.

[SCREENSHOT DOCKERHUB OU IMAGE OU LES DEUX] Explication des illustrations


# Automatisation des étapes
yml

# CI
Pour répondre à ces différentes problématiques, je recommande la mise en place d'un pipeline d'intégration continue. Concernant la qualité du code, ce dispositif sera en mesure de détecter rapidement :
les conflits de code

les erreurs de compilation
les régressions
les problèmes de compatibilité
AST(Static Application Security Testing) peut être lancé en même temps que les tests unitaires DAST(Dynamic Application Security Testing) IAST(Interactive Application Security Testing)

Ensuite, il va automatiser toutes les étapes de compilation, de test, de vérification de la qualité du code et de packaging. Les phases disctinctes de ce pipeline seront lancées successivement, lors de chaque nouveau push du code sur NX.

Pour automatiser ce CI, je recommande l'utilisation de workflows paramètrables via un fichier .yml. Plus communément utilsé sur Github Actions, cet outil est également présent sur n'importe quel système CI (Jenkins, Travis, Circle CI, GitLab CI, etc.)

Dans notre cas, nous utiliserons le Circle CI NX qui permettra de :

exécuter des tâches uniquement pour les projets affectés par un PR donné
activer la mise en cache à distance
paralléliser et répartir les tâches sur plusieurs machines
[SCREENSHOT yml]

A commencer par la miste en place de tests unitaires. Ces tests pourront être implémenter et largement facilités via l'outil de gestion NX comme suit : [SCREENSHOT ? ]

Appliqués tout le long du développement, ces tests vont permettre un feedback rapide. Les demandes de correction seront alors rapidement mis en place. Ce type de test aura aussi comme intérêt de sécuriser la maintenance grâce à plus de réactivité

Choisir outil de test : JEST etc

Ensuite, il semble essentiel de créer des tests d'intégration pour tester le fonctionnement global de l'application.

Autres tests possibles : tests de performance ou d’acceptation utilisateur en préproduction, smoke tests en production afin de garantir le fonctionnement normal de l’application en production. Choix. Adapté au projet ? Screen

Après la phase d'intégration continue, viendra la création d'une image exploitable sur Dockerhub. Cela permettra la conteneurisation de notre application, première étape du déploiement continu.

[SCREENSHOT DOCKERHUB OU IMAGE OU LES DEUX] Explication des illustrations

# CD
Le déploiement en continu s’appuie sur l’intégration en continu. Lorsque le nouveau code est “ commité ” (validé et enregistré) et a passé les tests d’intégration en continu, le code est déployé automatiquement en production. Une nouvelle fois avec les fichiers yml, on peut créer des workflows de déploiement personnalisés.

Release Staging environment (simulation)

valider les changements
conteneurs qui se rapprochent toujours du livrable
tests de performance
Deploy Operate

# Sources
