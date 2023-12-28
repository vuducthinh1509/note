# Docker command

### Listing Containers

```
docker ps -a
```

### Listing Image
```
docker image ls -a
```

### Start container

```
docker start [OPTIONS] CONTAINER
```

### Start container

```
docker stop [OPTIONS] CONTAINER
```

### Remove container
! Stop before remove
```
docker rm CONTAINER
```


### Access to container

```
docker exec -it 55c52c1e57a9 sh
```

# Application


## Run redis-stack with Docker

### redis/redis-stack-server
To start Redis Stack server using the redis-stack-server image, run the following command in your terminal:

```
docker run -d --name [tagname] -p [client_port]:6379 redis/redis-stack-server:latest
```
### redis/redis-stack
To start a Redis Stack container using the redis-stack image, run the following command in your terminal:

```
docker run -d --name [tagname] -p [client_port]:6379 -p [client_port]:8001 redis/redis-stack:latest
```
The docker run command above also exposes RedisInsight on port 8001. You can use RedisInsight by pointing your browser to localhost:8001.