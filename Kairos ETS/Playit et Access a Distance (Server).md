# Configuration et Gestion d'une Application avec `systemd`

## Introduction

Ce guide explique comment configurer et gérer un service sur un système Linux en utilisant `systemd`. Nous utiliserons un exemple où l'application est située dans le répertoire `/home/gallagher/Téléchargements/playit-linux-amd64`.

## Étapes de Configuration

### 1. Créer un Fichier de Service `systemd`

Les fichiers de service `systemd` sont stockés dans le répertoire `/etc/systemd/system/`. Pour créer un nouveau service appelé `kairos`, suivez les étapes ci-dessous :

`sudo nano /etc/systemd/system/kairos.service`

### 2. Ajouter la Configuration du Service

Ajoutez la configuration suivante dans le fichier kairos.service :
```
[Unit]
Description=Kairos Service
After=network.target

[Service]
ExecStart=/home/gallagher/Téléchargements/playit-linux-amd64
Restart=always
User=gallagher
WorkingDirectory=/home/gallagher/Téléchargements
StandardOutput=append:/var/log/kairos.out.log
StandardError=append:/var/log/kairos.err.log

[Install]
WantedBy=multi-user.target
```

### 3. Recharger systemd et Démarrer le Service

Une fois le fichier de service créé et enregistré, rechargez systemd pour prendre en compte la nouvelle configuration :

`sudo systemctl daemon-reload`

Ensuite, démarrez le service :

`sudo systemctl start kairos.service`

### 4. Activer le Service au Démarrage

Pour que le service démarre automatiquement au démarrage du système, utilisez la commande suivante :

`sudo systemctl enable kairos.service`

### 5. Vérifier le Statut du Service

Pour vérifier si le service est bien en cours d'exécution, utilisez la commande suivante :

`sudo systemctl status kairos.service`

Cela affichera l'état actuel du service ainsi que les journaux récents.

### 6. Gérer le Service avec systemd

Voici quelques commandes courantes pour gérer le service :

- Arrêter le service :
    `sudo systemctl stop kairos.service`
  

- Redémarrer le service :
    `sudo systemctl restart kairos.service`
  

- Désactiver le démarrage automatique :
    `sudo systemctl disable kairos.service`
  

### 7. Consulter les Journaux

Les journaux du service sont accessibles via journalctl. Pour afficher les journaux en temps réel du service kairos, utilisez la commande suivante :

`sudo journalctl -u kairos.service -f`

## Conclusion

Avec cette configuration, vous avez maintenant un service systemd qui démarre automatiquement au boot, redémarre en cas de panne, et enregistre les journaux de sortie et d'erreur. Vous pouvez gérer le service avec les commandes systemctl et consulter les journaux via journalctl.