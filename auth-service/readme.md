# Getting started
Avant de lancer le projet, vérifier que vous avez bien d'installé :

- [docker](https://docs.docker.com/desktop/install/windows-install/#:~:text=Double%2Dclick%20Docker%20Desktop%20Installer,bottom%20of%20your%20web%20browser.)
- [migrate](https://github.com/golang-migrate/migrate/blob/master/cmd/migrate/README.md)
- créer un compte [cockroachdb](https://www.cockroachlabs.com/)

# Setup config file
Une fois vos credentials en main, vous avez plus qu'à créer un fichier `config.yml`et à le remplir avec les données se trouvant dans le fichier d'exemple.
> Attention, pour la clé symétrique, gardez celle du fichier ou générez en une à 32 charactères.
# Lancer les migrations
Pour cela il vous suffit de mettre à jour la commande migrateup & migratedev présente au sein du makefile avec vos credentials.

ensuite, plus qu'à éxecuter `make migrateup`

# Docker step
Félicitation, vous avez survécu jusqu'à cette étape, maintenant plus qu'à construire une image docker du serveur et à la lancer.

```
docker build --tag ainomy-auth-service .
// puis lancer l'image
docker run -p 8080:8080 ainomy-auth-service
```
# Final step

Enjoy, and thanks for your contribution. 🎉