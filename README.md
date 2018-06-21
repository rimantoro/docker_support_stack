# Development Support Stack

## Create Network

This is special container for development environment. Before this container can be accessible from your container, you need to create a network ```my-shared-network``` or with other you name which you must define it on ```docker-compose.yml```

Create docker network with this command :

```
docker network create my-shared-network
```

## MySQL

MySQL persistence data will be saved into ```./data/mysql``` within this root project, so it will still available if you're running ```docker-compose down```.
```
Host : 0.0.0.0:3306
User : root
Pass : masukaja
```

## MongoDB

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

## RabbitMQ

Installed with management plugin.

```
Service Host : 0.0.0.0:5672
Web Management : 0.0.0.0:15672
User : rabbitmq
Pass : rabbitmq
```

You can access it with its domain `http://rabbitmq.local:15672/` after you add an entries into your host OS`/etc/hosts`.

```
0.0.0.0	rabbitmq.local
```