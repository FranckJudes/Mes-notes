
-> docker-compose est un orchestrateur de conteneur
		-> partage facile
		 -> versionning
		 -> meilleur gestion de dépendance (réseau,volume)
		 
-> lancement du service:
    +- `docker-composer build` :  construire uniquement des images
	+- `docker-compose up` : build et run des images
	+- `docker-compose up -d` : mode détaché (docker run -d)
    +-  `docker-compose ps` : Etat des services
	+- `docker-compose start`: redemande le services
	+- `docker-compose stop`: arrêt des conteneurs ou services
	+- `docker-compose rm` : supprime le services
	+- `docker-compose scale SERVICE=3` : lancer 3 instance 
	+- `docker-compose pull` : mettre a jour un conteneur (distante ou local)
	+- `docker network ls` : permet de voir tout les réseaux disponible pour tes conteneurs
	+- `docker volume ls` : permet de voir tout les volumes disponible pour tes conteneurs
	
	

-> DockerFile permet de créer image applicative

-> La gestion de volumes par docker-compose:
		-- Intérêt de volume :
				*En cas de perte d'un conteneur qu'on puisse ne pas perdre ces données
				*Partage de données entre conteneurs (Exemple si on créer un nouveau conteneur, pouvoir regreffer les informations déçu pour ne pas pouvoir les perdres)
				
  -> Portainer CE est une solution d’administration de conteneurs **Docker** puissante et conviviale. Il **simplifie l’administration des conteneurs Docker** en offrant une interface graphique **intuitive** pour une gestion plus facile et plus efficace.