# How to install and run kafka server and produce and consume messages

- use the docker compose file
- ``` docker-compose up -d ``` 
to start the docker server

## Creating a topic
``` docker-compose exec kafka-server-1 kafka-topics --create --bootstrap-server kafka-server-1:9092 --replication-factor 1 --partitions 1 --topic my-topic ```

## Creating a producer
- open terminal
- ``` docker exec -it kafka-kafka-server-1-1 sh ```
-  ``` cd /usr/bin ``` 
-  ``` kafka-console-producer --bootstrap-server kafka-server-1:9092 --topic my-topic ``` 
- now you can send messages 

## Creating a consumer
- open terminal
- ``` docker exec -it kafka-kafka-server-1-1 sh``` 
- ``` cd /usr/bin ``` 
-  ``` kafka-console-consumer --bootstrap-server kafka-server-1:9092 --topic my-topic --from-beginning ``` 