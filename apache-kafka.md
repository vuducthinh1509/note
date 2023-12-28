# Apache Kafka Quickstart
1. Download Apache Kafka [here](https://www.apache.org/dyn/closer.cgi?path=%2Fkafka%2F3.1.0%2Fkafka_2.13-3.1.0.tgz)
2. Extract and cd into it
```
tar -xzf kafka_2.13–3.1.0.tgz
cd cd kafka_2.13–3.1.0
```
3. Start the Kafka Environment

Run the Zookeeper
```
bin/zookeeper-server-start.sh config/zookeeper properties
```
Run the Kafka broker
```
bin/kafka-server-start.sh config/server.properties
```


Getting started
redis/redis-stack-server
To start Redis Stack server using the redis-stack-server image, run the following command in your terminal:

```
docker run -d --name redis-stack-server -p 6379:6379 redis/redis-stack-server:latest
```
redis/redis-stack
To start a Redis Stack container using the redis-stack image, run the following command in your terminal:

```
docker run -d --name redis-stack -p 6379:6379 -p 8001:8001 redis/redis-stack:latest
```
The docker run command above also exposes RedisInsight on port 8001. You can use RedisInsight by pointing your browser to localhost:8001.