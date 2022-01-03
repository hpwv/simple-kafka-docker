# Kafka Cluster Docker compose Setup
## Preparation
Install `docker` and `docker-compose`

Create the data folders for data persistence on the host:

`mkdir /tmp/zookeeper /tmp/kafka-1 /tmp/kafka-2 /tmp/kafka-3`

## Running
To run the kafka cluster with three brokers, simply run 
`docker compose up` if you want to see the log output in the current terminal session
 or `docker compose up -d` if you want to start it in the background

## Start from scratch
If you want to start from scratch, clean up the tmp directories and start with the preparation step again:

`rm -rf /tmp/zookeeper /tmp/kafka*`
