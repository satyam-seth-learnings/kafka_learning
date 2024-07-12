# How to run

```sh
docker run -p 2181:2181 zookeeper
```

```sh
docker run -p 9092:9092 -e KAFKA_ZOOKEEPER_CONNECT=<ip_address>:2181 -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://<ip_address>:9092 -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1 confluentinc/cp-kafka
```

```sh
node consumer.js <group_name>
```

```sh
node producer.js
```