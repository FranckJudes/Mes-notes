### **1. Playbook**
Un **playbook** est un document (souvent automatisé) utilisé pour orchestrer des tâches répétitives ou complexes dans un environnement DevOps. Il est principalement utilisé pour l’automatisation des processus.
#### **Caractéristiques principales** :

- **Automatisé** : Implémenté via des outils comme Ansible, Chef ou Puppet.
- **Orienté tâches** : Définit des séries d'étapes pour exécuter des actions spécifiques.
- **Idéal pour la gestion d’infrastructure** : Exemple : configurer des serveurs, déployer une application, gérer des mises à jour.
### **2. Runbook**

Un **runbook** est une documentation détaillée ou une série d'instructions pour résoudre des incidents, effectuer des maintenances ou suivre des procédures manuelles ou semi-automatiques. Il s’agit souvent de guides écrits destinés à des opérateurs ou ingénieurs.

#### **Caractéristiques principales** :

- **Manuel ou semi-automatique** : Peut être suivi par un humain ou partiellement automatisé.
- **Axé sur la résolution de problèmes** : Sert pour des opérations récurrentes ou d’urgence.
- **Structure claire** : Explique les étapes pour diagnostiquer et corriger un problème ou exécuter une tâche.


. le DevOps :  le passage de l'ere artisanal a l'ere de l'IT
. le Pipeline : c'est une chaine de production (automatisation/standardisation)et le devops vise a realiser cela par le billet d'automatisation

devops : 
Planifier ->  coder -> compiler -> tester -> livrer -> deployer -> superviser -> planifier ---etc (pratique devops)


`La CI (continuous Integration)` =  Build/test/merge (le but est de construire le livrable)
`La Continuous delivery` =  Pousse l'application dans son depot , un etat deployable
`Continous deployment` : deploiement (installation) de l'application jusqu'en production

Mes Technologie : 
->  Scheduler  : Jenkins
-> Orchestrateur : Ansible
-> depot : gitlab
-> livrable : image docker
-> gestionnaire de projet : Maven
