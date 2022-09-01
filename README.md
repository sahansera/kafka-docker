# Kafka on Docker
A quick way to get a local Kafka instance up and running with Docker.

Related blog post: https://sahansera.dev/setting-up-kafka-locally-for-testing/

## Usage

Run at the root:

```sh
docker-compose up -d
```

### Producer
```sh
docker exec --interactive --tty broker \
kafka-console-consumer --bootstrap-server localhost:9092 \
                       --topic example-topic \
                       --from-beginning
```


### Consumer

```sh
docker exec --interactive --tty broker \
kafka-console-producer --bootstrap-server localhost:9092 \
                       --topic example-topic
```
