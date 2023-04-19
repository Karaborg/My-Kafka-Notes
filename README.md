# Kafka

## Usefull Commands:
Let's start with starting Zookeeper, Kafka and Kafdrop with the command:
`docker-compose up -d`

After making sure our containers are up and running, let's dive into our Kafka container to test:
`docker exec -it broker bash`

### Test
1. Create topic: `kafka-topics --bootstrap-server broker:9092 --create --topic <TOPIC_NAME>`
2. Enter message on topic: `kafka-console-producer --broker-list localhost:9092 --topic <TOPIC_NAME>`
3. Listen the topic: `kafka-console-consumer --bootstrap-server localhost:9092 --topic <TOPIC_NAME> --from-beginning`
4. List topics: `kafka-topics --list --bootstrap-server localhost:9092`
5. List consumers: `kafka-consumer-groups --bootstrap-server localhost:9092 --list`
6. Check if consumer has any lag: `kafka-consumer-groups --bootstrap-server localhost:9092 --group <CONSUMER_NAME> --describe`
