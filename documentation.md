# Situation actuelle et souhait du client

Notre client souhaite avoir une documentation à jour (Front) répondre aux besoins des développeurs travaillant sur la partie front.

# Selection de plusieurs outils

Si un outil de plannification comme Trello est utilisé, il serait intéressant de mettre en place Jira ajouté à Confluence, un outil de gestion de travail collaboratif de la même série Atlassian.
La complémentarité des produits d'une même enseigne offre généralement fluidité et amélioration continue du workflow.

Un autre choix se porterait sur l'utilisation de Docusaurus. 
Docusaurus est un générateur de site statique monopage. Il conçoit rapidement une application interactive grâce à React. Cet outil est :
- compatible avec NX
- simple dans son utilisation
- rapidement exploitable

 # Choix et justifications
Après ces deux suggestions, je souhaite aborder le produit qui selon moi sera le plus adapté de par sa performance et sa polyvalence.
Je préconise la mise en place d'une librairie multi-fonctions nommée Storybook. Elle me semble la plus intéressante car elle fournit des services tels que :
- la création de documention
- une banque de composants réutilisables
- ...
  
Pourquoi Storybook ici : (https://www.troispointzero.fr/le-blog/storybook-developpement-de-composants/)

De plus, l'utilisation de l'outil de gestion monorepository NX facilite grandement son utilisation.
Il est installé dans le package initial. Une documentation permet sa configuration pour une utilisation automatisée qui viendra offrir un gain de temps considérable aux équipes de développement front.
Documentation NX Storybook : (https://nx.dev/nx-api/storybook)

La force de NX est de générer les plugins nécessaires à l'automatisation de la génération, des tests et de la construction de fichiers Storybook.

# Sources
