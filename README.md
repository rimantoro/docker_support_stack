# Development Support Stack

## Create Network

This is special container for development environment. Before this container can be accessible from your container, you need to create a network ```my-shared-network``` or with other you name which you must define it on ```docker-compose.yml```

Create docker network with this command :

```
docker network create my-shared-network
```

## MySQL (MariaDB 10.1)

MySQL persistence data will be saved into ```./data/mysql``` within this root project, so it will still available if you're running ```docker-compose down```.
```
Host : 0.0.0.0:3306
User : root
Pass : {set in MYSQL_ROOT_PASSWORD in docker-compose}
```

## MongoDB (3.6)

Same with MySQL, data are persistence and will be saved in ```./data/mongodb```.
```
Host : 0.0.0.0:27017
User : None
Pass : None
```

## Redis

```
Host : 0.0.0.0:6379
User : None
Pass : None
```

## RabbitMQ (3.7.4)

Installed with management plugin.

```
Service Host : 0.0.0.0:5672
Web Management : 0.0.0.0:15672
User : guest
Pass : guest
```

You can access it with its domain `http://rabbitmq.local:15672/` after you add an entries into your host OS`/etc/hosts`.

```
0.0.0.0	rabbitmq.local
```

## PostgreSQL (10.4)

You can set your user on environment variable POSTGRES_USER & POSTGRES_PASSWORD

```
Host : 0.0.0.0:5432
```

## Adminer

```
Host : 0.0.0.0:8090
```

You can access it with its domain `http://adminer.local:8090/` after you add an entries into your host OS`/etc/hosts`.

```
0.0.0.0	adminer.local
```

## Swagger Editor

```
Host : 0.0.0.0:8091
```

You can access it with its domain `http://swagger-editor.local:8091/` after you add an entries into your host OS`/etc/hosts`.

```
0.0.0.0	swagger-editor.local
```