# Problèmes du sujet : utilisation actuelle / conséquences

Amélioration de la qualité du code et code beaucoup plus homogène 
pas de retour erreurs code / rien de précis
erreurs fréquentes liés aux versions de navigateurs / syst expl / firmwares
erreurs de connexion

Lean management (amélioration continue et acceptation des erreurs) : types de gaspillage concernés ici :
attente
étapes inutiles
mouvements inutiles
corrections / retouches

# Souhait du client et objectif 
automatiser le plus de choses possibles => CI/CD (Docker), yml, dockerHub, test end to end, units, build (les QA gèrent les tests) graphQL

# CI
Pour répondre à ces différentes problématiques, je recommande la mise en place d'un pipeline d'intégration continue. Concernant la qualité du code, ce dispositif sera en mesure de détecter rapidement :
- les conflits de code
- les erreurs de compilation
- les régressions
- les problèmes de compatibilité

Ensuite, il va automatiser toutes les étapes de compilation, de test, de vérification de la qualité du code et de packaging.
Les phases disctinctes de ce pipeline seront lancées successivement, lors de chaque nouveau push du code sur NX.

# Tests
A commencer par la miste en place de tests unitaires. Ces tests pourront être implémenter et largement facilités via l'outil de gestion NX comme suit :
[SCREENSHOT ? ]

Appliqués tout le long du développement, ces tests vont permettre un feedback rapide. Les demandes de correction seront alors rapidement mis en place.
Ce type de test aura aussi comme intérêt de sécuriser la maintenance grâce à plus de réactivité

Ensuite, il semble essentiel de créer des tests d'intégration pour tester le fonctionnement global de l'application.
code coverage

Autres tests possibles : tests de performance ou d’acceptation utilisateur en préproduction, smoke tests en production afin de garantir le fonctionnement normal de l’application en production.
Choix. Adapté au projet ?
Screen


Après la phase d'intégration continue, je propose la création d'une image exploitable sur Dockerhub. Cela permettra la conteneurisation de notre application. 

# CD
Release
Deploy
Operate

# Monitoring : surveillance des métriques
Sélection de 3 métriques
Pertinence / qualité et sécurité des données relevées = précision ++ (air, eau etc)

# Sources
-


# Sources
-
