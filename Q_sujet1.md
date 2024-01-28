# Mots clefs
- Secteur : consultation et R&D / industrie
- axée sur la production intellectuelle et académique 
- séparation entre les équipes techniques et resp de mise en prod 
- partie de l'équipe de recherche internationale / pratiques de travail et conventions de codage différentes
- besoin d'échanger en permanence les connaissances
- manque de moyens humains = recrute
- réunion hebdo : travail semaine dernière + semaine actuelle
- orga en fonction de la taille du projet et des compétences de chacun + communication entre collaborateurs
  
- worklow / dépôt / qualité du code / CI-CD automatisée

- 1 - Choix d'une techno (rester sur C++ et Matlab?) 
- 2 - Propositions d'améliorations /
  
  - Problèmes actuels : 
    - monolithique / energivore
    - prod et deploy manuels
    - pas de tests automatisés
    - organisation
  
- Kubernetes : k8s + orchestrateur de containers

# Cours 
en attente

# Liens - Propositions
dans le sujet
+
mise en place de sprints etc 

# Questions

Micro services
Quelles fonctionnalités spécifiques de l'application peuvent être transformées en microservices indépendants ?
Comment assurer la cohérence et la communication entre les équipes travaillant sur différents microservices ?

Containerisation avec Docker :
Comment Docker peut-il être utilisé pour containeriser chaque microservice ?
Comment gérer les dépendances entre microservices dans un environnement Dockerisé ?

Orchestration avec Kubernetes :
Pourquoi Kubernetes est-il essentiel pour orchestrer le déploiement des microservices ?
Comment garantir la flexibilité et l'évolutivité des microservices grâce à Kubernetes ?

Chaîne CI/CD Automatisée :
Comment mettre en place une chaîne CI/CD tenant compte de la séparation entre les équipes scientifiques et de production ?
Quelles étapes spécifiques doivent être automatisées pour garantir un processus CI/CD fiable ?

Tests Automatisés :
Comment intégrer des tests automatisés à chaque étape du processus CI/CD ?
Quels types de tests sont essentiels pour assurer la stabilité des microservices ?

Surveillance et Logging :
Comment mettre en place une surveillance efficace des microservices en production ?
Quels mécanismes de logging peuvent aider à identifier rapidement les problèmes potentiels ?
