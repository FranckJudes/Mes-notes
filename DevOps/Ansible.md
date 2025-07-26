**Ansible** est un outil open-source d'automatisation informatique qui permet de gérer la configuration, le déploiement et l'orchestration d'infrastructures de manière simple et efficace. Développé par **Red Hat**, Ansible est conçu pour automatiser des tâches répétitives et complexes, réduisant ainsi les erreurs manuelles et améliorant l'efficacité des équipes IT.
### Fonctionnalités clés d'Ansible :

1. **Configuration de systèmes** : Automatisation de la configuration d'ordinateurs, serveurs, routeurs, etc.
2. **Déploiement d'applications** : Simplifie le processus de déploiement d'applications sur des machines locales ou distantes.
3. **Orchestration** : Coordonne les tâches sur plusieurs machines en même temps, comme lors de la mise à jour d'une infrastructure complète.
4. **Provisionnement** : Crée des machines virtuelles ou configure des services cloud sur des fournisseurs comme AWS, Azure ou Google Cloud.

Quelques termes a retenir : 
	*Inventory* : Listes des serveurs et variables
	*Taches* : Une Action a realiser
	*Module* : Fonction appellee par des taches
	*Role :* regroupement de taches visant a deployer/installer un bloc specifique et coherent
	*Playbook :* Definition des roles devant etre joues sur quel groupe de serveurs(inventory)
	*Groupes :* Division regroupant des serveurs par categorie au sein de l'inventory
	*Variable :*