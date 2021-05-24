# Kafka with sarama client package
this project will use `docker-compose.yml` to build up a kafka cluster. Create a topic `victor-topic`. Also provide a producer example and consumer group example by sarama client package.
## process
1. build up kafka cluster : execute ``docker-compose up -d`` in this package.
2. Create a topic : 
```
   1. docker exec -it [broker1 container id] bash
   2. cd /opt/kafka/bin
   3. bash kafka-topics.sh --zookeeper [zookeeper container id]:2181 --create --topic [topic-name] --partitions [partition number for topic] --replication-factor [replica number, 1 means no replication]
```
3. run producer : `go run cmd/producer/producer.go`
4. run consumer : `go run cmd/consumer_group/consumer_group.go`
