# Kafka Commands

## Prompt 1: Starting Zookeeper
```
cd c:\kafka
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```

## Prompt 2: Starting the Kafka Server
```
cd c:\kafka
.\bin\windows\kafka-server-start.bat .\config\server.properties
```

## Prompt 3: Creating a Partition via Command Promt
```
cd c:\kafka
.\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic TestTopic
```
