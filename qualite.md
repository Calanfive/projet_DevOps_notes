# Problèmes du sujet : utilisation actuelle / conséquences
Actuellement, le client est confronté à de nombreuses erreurs dans son code. C'est une perte de temps de les rechercher et de les corriger.

# Souhait du client et objectif 
Pour améliorer la qualité du code et le rendre bien plus homogène, je préconise l'utilisation d'un Linter.

# Linter
Un linter est un outil d'analyse statique de code source. Il sert à détecter :
- des erreurs (très utile sur des langages interprétés comme JavaScript qui n'ont pas de phase de compilation) ;
- des problèmes de syntaxe et de non-respect de style (tabulation vs espaces, indentation, etc.).

Selection de 3 linters
J'ai selectionné trois outils afin d'évaluer celui qui serait le plus adapté aux problèmatiques citées précedemment.
Comparaison des Linter
(https://www.sitepoint.com/comparison-javascript-linting-tools/)

Je recommande donc l'utilisation et l'exploitation du linter ESLint qui par chance est compris dans le setup installé lors de la génération du workspace NX.

Config perso
Vous trouverez ci-dessous un exemple de configuration de l'outil ESLint. Cette configuration est a effectuer dans le fichier .eslintrc.json comme suit :
[SCREENSHOT CONFIG ESLINT]
Comme vous le constatez, un grand nombre de règles peuvent être appliquées à l'ensemble de l'espace de travail. Toutes ces règles sont disponibles sur la documentation d'ESLint : (https://eslint.org/docs/latest/rules/)

Ceci aura pour effet immédiat d'instaurer des règles communes à tous les projets et ce de façon automatique grâce à l'affichage d'erreurs en phase de développement et des propositions de solutions comme l'indique l'exemple ci-dessous :
[SCREENSHOIT ERREUR + PROPOSITIONS AUTO ESLINT]

Selon le choix des équipes, ces règles peuvent être appliquées à certains projets seulement. C'est pourquoi il serait intéressant de mettre en place des enquêtes auprès du personnel concerné. Ces enquêtes permetteraient d'être à l'écoute des préférences des équipes techniques. Une démarche évolutif et inclusive, (côté mise à jour à mettre en avant) va éviter d'imposer les mêmes règles à tous les projets (souligner les conflits probables entre electron et react native). 

Enfin, il est également possible de configurer son linter de façon plus rapide. En effet, lors de l'installation de l'outil, il nous est proposé d'utiliser un mode dit 'standard' ou 'xo'. Les modes les plus connus sont 'airbnb' et 'google' mais après simulation j'ai réalisé qu'ils n'étaient plus d'actualité à ce jour. 

# Prettier
Le package NX comprend également l'utilisation d'un formateur Prettier. 
Cet outil supplémentaire va assurer la cohérence du formatage du code et automatiser le processus. Alors qu'ESLint sera charger de détecter les erreurs, le formateur lui va avoir la capacité de les corriger. 

Pour ce faire, il suffit de configurer des règles dans le fichier .prettierrc comme suit :
[SCREENSHOT CONFIG PRETTIER]

Dans le cas de conflits entre ESLint et Prettier, la configuration par ce fichier donnera automatiquement la priorité au Prettier sur le linter.

Ces outils offrent un choix d'utilisation personnalisé grâce à leurs extensions accessibles sur VScode.

Conclusion...

# Sources

