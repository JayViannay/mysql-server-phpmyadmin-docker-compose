# mysql-server && PhpMyAdmin Environnement with DOCKER
> This docker-compose file can be used to deploy the mysql server and phpmyadmin easily on your machine.

## Requirements :
- [Docker && Docker Compose](https://docs.docker.com/compose/install/compose-desktop/)


## Installation :
> At first, you need to install docker and docker-compose. <br>
> Clone this repository on your machine, go to the folder : `cd ~/mysql-server-phpmyadmin-docker-compose` <br>
> Then, you can install the mysql server and phpmyadmin easily with the following command :

```bash
docker-compose up -d
```

> mysql-server and phpmyadmin are now running on your machine. <br>
> mysql-server unning on port 3307, phpmyadmin running on port 8889 : you can visit `http://localhost:8889`. <br>
> You can access to the mysql-server with terminal : <br>

```bash
docker ps
```
> Keep the container id of the mysql-server and run :

```bash
docker exec -it <CONTAINER_ID> mysql -u root -p
```

> password : `somecomplexpassword` <br>
> You can change the value of the password directly in the file.