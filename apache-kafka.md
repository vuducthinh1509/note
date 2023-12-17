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


