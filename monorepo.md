# La gestion de projet en monorepo : 
- offre une gestion du code centralisée. Tout le code source est accessible par toutes les équipes
- permet de soumettre toutes les modifications effectués sur plusieurs plusieurs parties du projet avec une seule pull request
- permet un partage des mêmes méthodes de programmation et des outils de développement
- fluidifie toutes les étapes de livraison de l'application
- évite les régressions

Les problèmes gérés par cette technique n’arrivent qu’à partir d’une certaine échelle.

Approche hybride poly-as-mono :
-  utiliser plusieurs dépôts et employer un outil de colocalisation pour les maintenir synchronisés, le faisant ressembler à un mono-repo mais avec plus de flexibilité.

POURQUOI ? 
# Inconvénients d'un multi repository : utilisation actuelle 
arguments
- Partage de code fastidieux
- Duplication de code importante
- Modifications coûteuses entre dépôts croisés pour les bibliothèques partagées et les consommateurs + effort de coordination du versioning et de la publication des packages
- Outillage incohérent
- PR long trop d'étapes 
- npm link (https://medium.com/@ammarameer/linking-multiple-repositories-using-npm-for-seamless-local-development-2a1c2ca14257)

[SCHEMA COMPARATIF]

# Avantages d'une transition en mono repository
+ Tout dans ce commit actuel fonctionne ensemble. Les changements peuvent être vérifiés dans toutes les parties concernées de l’organisation.+ Facile à diviser le code en modules composables
- Gestion des dépendances plus facile
- Une configuration de chaîne d'outils
- Les éditeurs de code et les IDE prennent en compte « l'espace de travail »
- Expérience de développeur cohérente + Mobilité des développeurs

- La possibilité d'exécuter n'importe quelle commande sur plusieurs machines tout en développant localement (la visualisation du graphique de dépendance est accèssible via l'outil de gestion)
- Détection des projets/packages concernés (pour exécuter uniquement les projets concernés par la génération/test)

Malgré ce que disent les gens, ils :
- Offrez-vous plus de flexibilité de déploiement
- Vous permettent de mettre en place des politiques de propriété précises
- Fournissez plus de structure à votre code source
- Évoluez bien à l’aide d’outils familiers

DEFIS:
- Le développement basé sur le tronc est beaucoup plus important
- Tous les services ne fonctionnent pas bien avec les monorepos
- Nécessite une configuration CI plus sophistiquée
- Vous obliger à réfléchir à des changements à grande échelle

problèmes: consultation des historiques et chargement plus lents dûs à la densité du code
et surtout mise en garde sur l'utilisation de ce type de repo qui exige un mode de gestion particulier :
- il est important que les équipes ::: ne puissent pas aller modifier le code des équipes :::
- s'assurer que les projets backend n'importent pas ceux du frontend
- Contraintes et visibilité du projet

Plus l'espace de travail s'agrandit, plus vous aurez besoin d'outils pour vous aider à le maintenir rapide, compréhensible et gérable.

Un monorepository contient différents projets dont les relations sont bien définies. 
Pour ceci, je recommande un outil de gestion ... 

# Préconisation d'un outil de gestion
Selection de 3 outils (https://monorepo.tools/)
Moon / Nx / Pants 
[AFFICHER LOGOS]

Comparaison 
+ Rapide 
Mise en cache des calculs locaux
Orchestration des tâches locales
Mise en cache des calculs distribués
Exécution de tâches distribuées -> Pants Nx
Exécution à distance transparente -> Pants
Détection des projets/packages concernés
+ Compréhensible
Analyse de l'espace de travail
Visualisation du graphique de dépendance -> Pants pas inclus
+ Maniable
Partage de Code
Outillage cohérent
Génération de code
Contraintes et visibilité du projet -> Pants pas inclus

Choix 
Adapté au projet ? pourquoi?
CF situation actuelles et réponses apportées

[SCREENSHOTS] graph type / +++ / config cool via l'extension NX

C'est pourquoi le choix de ::: me paraît le plus pertinent pour améliorer le workflow du développement de :::

# Mises en garde pour une transition sans encombre 

Il a fallu découper la transition en plusieurs étapes pour éviter un trop gros changement qui aurait pu déclencher une indisponibilité de service, sans possibilité de revenir en arrière. Nous avons donc effectué un long travail de préparation et de validation :

Découpage de la migration en plusieurs phases en intégrant l’impact potentiel !! pour les collègues.
Test de chaque étape en amont lorsque cela était possible.
Détail de chaque étape avec une liste de tâches “prête à l’emploi” pour le jour J.
Planification des jalons de la migration lors de périodes de faible affluence.
Simulation de scénarios de crise pour anticiper les problèmes et prévoir les actions à mettre en oeuvre.
Notre équipe a aussi élaboré des procédures de documentation des incidents pour permettre le rétropédalage dans une certaine mesure.

# Sources 
- Monorepo vs multi : (https://kinsta.com/fr/blog/mono-repo-vs-multi-repo/#:~:text=L'approche%20mono%2Drepo%20consiste,entreprise%20%E2%80%93%20dans%20un%20seul%20d%C3%A9p%C3%B4t.)
- Monorepo JS : (https://blog.kbdev.io/dev/2021/09/07/monorepo-with-lerna.html)
- Listes d'outils de gestion Monorepo 2021 : (https://blog.bitsrc.io/11-tools-to-build-a-monorepo-in-2021-7ce904821cc2)
- Exemple Avantages Inconvénients : (https://news.infomaniak.com/monorepo-collaborer-efficacement/)
- Exemple JS Lerna Darva : (https://www.darva.com/fr/2023/03/02/a-la-decouverte-des-monorepos-pour-partager-son-code-js/)
- 
