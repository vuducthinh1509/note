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

### Stop all container

```
sudo docker stop $(sudo docker ps -aq)
```

### List all volumes
```
sudo docker volume ls
```
### Remove images with volumes and containers

```
sudo docker rmi <image_name>
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

# Documents

[Docker network](https://viblo.asia/p/tim-hieu-va-lam-viec-voi-docker-container-networks-p1-XqakEmmbkWK)

[About Docker](https://blog.cloud365.vn/container/tim-hieu-docker-phan-1/)


# Tips for Docker

### Hướng dẫn chạy docker không cần sudo [here](https://docs.docker.com/engine/install/linux-postinstall/#configure-default-logging-driver)

