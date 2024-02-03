# La gestion de projet en monorepo : 
- offre une gestion du code centralisée. Tout le code source est accessible par toutes les équipes
- permet de soumettre toutes les modifications effectués sur plusieurs plusieurs parties du projet avec une seule pull request
- permet un partage des mêmes méthodes de programmation et des outils de développement
- fluidifie toutes les étapes de livraison de l'application


Les problèmes gérés par cette technique n’arrivent qu’à partir d’une certaine échelle.

Approche hybride poly-as-mono :
-  utiliser plusieurs dépôts et employer un outil pour les maintenir synchronisés, le faisant ressembler à un mono-repo mais avec plus de flexibilité.

POURQUOI ? 
# Inconvénients d'un multi repository : utilisation actuelle 
arguments

exemple vscode : npm link et PR de sous projets

# Avantages d'une transition en mono repository

problèmes: consultation des historiques et chargement plus lents dûs à la densité du code
et surtout mise en garde sur l'utilisation de ce type de repo qui exige un mode de gestion particulier :
- il est important que les équipes ::: ne puissent pas aller modifier le code des équipes :::
-
-
Pour ceci, je recommande un outil de gestion ... 

# Préconisation d'un outil de gestion

Selection de 3 outils  Check docs tools
Comparaison 
Choix 
 adapté au projet ? pourquoi?

C'est pourquoi le choix de ::: me paraît le plus pertinent pour améliorer le workflow du développement de :::
branch develop

# Notes
- outils de gestion de monorepo comme Lerna (installation des dependances dans les sous-dossiers etc évite les duplications)

# Mises en garde pour une transition sans encombre 


# Sources 
- Monorepo vs multi : (https://kinsta.com/fr/blog/mono-repo-vs-multi-repo/#:~:text=L'approche%20mono%2Drepo%20consiste,entreprise%20%E2%80%93%20dans%20un%20seul%20d%C3%A9p%C3%B4t.)
- Monorepo JS : (https://blog.kbdev.io/dev/2021/09/07/monorepo-with-lerna.html)
- Listes d'outils de gestion Monorepo 2021 : (https://blog.bitsrc.io/11-tools-to-build-a-monorepo-in-2021-7ce904821cc2)
- Exemple Avantages Inconvénients : (https://news.infomaniak.com/monorepo-collaborer-efficacement/)
- Exemple JS Lerna Darva : (https://www.darva.com/fr/2023/03/02/a-la-decouverte-des-monorepos-pour-partager-son-code-js/)
- 
