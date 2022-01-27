# Kafka Cluster
## Introduction
This is a simple kafka cluster consisting of three brokers, run in docker.
It is part of the HPWV prototype.

## Preparation

Install `docker` and `docker-compose`.

Run `docker compose build` to build the docker containers ahead of running them.

## Running

To run the kafka cluster with three brokers, simply run
`docker compose up` if you want to see the log output in the current terminal session or `docker compose up -d` if you
want to start it in the background

## Stopping

In order to stop the cluster, run `docker compose down`.
