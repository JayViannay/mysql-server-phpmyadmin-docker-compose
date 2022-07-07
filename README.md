# MySql Serveur && PhpMyAdmin Environnement

> This docker-compose file can be used to deploy the mysql server and phpmyadmin easily on your machine.

## Requirements :

- [Docker && Docker Compose](https://docs.docker.com/compose/install/compose-desktop/)


## Installation :

> At first, you need to install docker and docker-compose.
> Clone this repository on your machine, go to the folder : `cd ~/docker-compose-mysql-phpmyadmin`
> Then, you can install the mysql server and phpmyadmin easily with the following command :

```bash
docker-compose up -d
```

> MySql server and phpmyadmin are now running on your machine.
> MySql server running on port 3307, phpmyadmin running on port 8889.
> You can access to the mysql server with terminal : 

- First : 
```bash
docker ps
```
- Then keep the container id of the mysql server and run :

```bash
docker exec -it <CONTAINER_ID> mysql -u root -p
```

- password : `somecomplexpassword`

You can change the value of the password directly in the file.