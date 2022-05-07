# Kafka Config Files

## For the Server Properties:
```
advertised.listeners=PLAINTEXT://localhost
zookeeper.connect = localhost:2181
```

# Kafka Commands for Windows

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

# Kafka Commands for Linux

## Prompt 1: Starting Zookeeper
```
cd c:\kafka
bin/zookeeper-server-start.sh config/zookeeper.properties
```

## Prompt 2: Starting the Kafka Server
```
cd c:\kafka
JMX_PORT=8004 bin/kafka-server-start.sh config/server.properties
```

## Prompt 3: Starting CMAK 
```
git clone https://github.com/yahoo/CMAK.git
cd CMAK
./sbt clean dist
cd target
cd universal
unzip cmak-3.0.0.6.zip
cd cmak-3.0.0.6
cd conf
```

Change to localhost
```
cmak.zkhosts="localhost:2181"
```

Running the Server
```
bin/cmak -Dconfig.file=conf/application.conf -Dhttp.port=8080
```
