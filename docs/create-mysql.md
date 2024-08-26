## Setup MySQL <a name="setup-mysql"></a>
If you have docker you can run [Mysql image](https://hub.docker.com/_/mysql) from docker and use it.

<Instruction>

`docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=dbpass -e MYSQL_DATABASE=hackernews -d mysql:latest`
now run `docker ps` and you should see our mysql image is running:
```
CONTAINER ID        IMAGE                                                               COMMAND                  CREATED             STATUS              PORTS                  NAMES
8fea71529bb2        mysql:latest                                                        "docker-entrypoint.s…"   2 hours ago         Up 2 hours          3306/tcp, 33060/tcp    mysql

```

## Create MySQL database <a name="create-mysql-database"></a>
You have already started `mysql` instance in the previous step. Now we will need to create our `hackernews` database in that instance.
To create the database run these commands.

<Instruction>

`docker exec -it mysql bash`

It will open the bash terminal inside `mysql` instance.


In the next step we will open `mysql` repl as the root user:

`mysql -u root -p`


It will ask you for root password, enter `dbpass` and enter.

Now we are inside `mysql` repl. To create the database, run this command:

`CREATE DATABASE hackernews;`

</Instruction>
