# Kafka Commands

## Prompt 1
```
cd c:/kafka
.\bin\windows\kafka-server-start.bat .\config\server.properties
```

## Prompt 2
```
cd c:/kafka
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```

## Prompt 3
```
cd c:/kafka
.\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic TestTopic
```
