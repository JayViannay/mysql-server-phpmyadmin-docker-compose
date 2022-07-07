# mysql-server && PhpMyAdmin for Local Environnement with DOCKER
> This docker-compose file can be used to deploy the mysql-server and phpmyadmin easily only on your machine without any installation or configuration.
> **/!\ This is not for production /!\**

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
> phpmyadmin running on port 5050, you can visit it at [http://localhost:5050](http://localhost:5050). <br>
> You can access to the mysql-server with your terminal : <br>


```bash
➜ docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED         STATUS         PORTS                                    NAMES
b8943a71134f   phpmyadmin/phpmyadmin   "/docker-entrypoint.…"   3 minutes ago   Up 3 minutes   0.0.0.0:5050->80/tcp       mysql-server-phpmyadmin-docker-compose-phpmyadmin-1
1bcb7df4eabd   mysql:5.7               "docker-entrypoint.s…"   3 minutes ago   Up 3 minutes   3306/tcp, 33060/tcp, 0.0.0.0:3307->3307/tcp   mysql-server-phpmyadmin-docker-compose-db-1
```
> Keep the **CONTAINER ID** of mysql:5.7 then run :

```bash
docker exec -it CONTAINER_ID mysql -u root -p
```

> password : `somepassword` <br>
> You can change the value of the password directly in the file if you want. (You will need to restart the container).