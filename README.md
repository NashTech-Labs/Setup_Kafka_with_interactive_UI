# Local Kafka Cluster with KafkaUI

This repository contains a Docker Compose file to set up a local Kafka cluster along with Provectus KafkaUI for a graphical interface to manage the Kafka Cluster.

## Prerequisites
- Docker
- Docker Compose

## Components
The setup includes the following services:
- **Zookeeper:** A centralized service for maintaining configuration information, naming, providing distributed synchronization, and providing group services.
- **Kafka:** A distributed streaming platform that lets you publish and subscribe to streams of records, store streams of records in a fault-tolerant way, and process streams of records as they occur.
- **KafkaUI:** A web tool for Kafka cluster management with a user-friendly interface.

## To get started
1. Clone the repository to your local machine.
2. Navigate to the directory containing the `docker-compose.yml` file.
3. Run the following command to start all services:
```
docker compose -f kafka.yaml up -d
```
## Accessing KafkaUI
Once all services are up and running, you can access the KafkaUI at `http://localhost:7070` in your web browser.

## Default Credentials for KafkaUI
- **Username:** admin
- **Password:** pass

## Configuration
The services are pre-configured as follows:
- Zookeeper is accessible on port `2181`.
- Kafka is accessible on ports `9092` for Kafka brokers and `9090` for JMX metrics.
- KafkaUI is accessible on port `7070`.

## Volumes
The following volumes are created and used:
- `zookeeper_data` for Zookeeper data.
- `kafka_data` for Kafka data.
- `kafka_ui_conf` for KafkaUI configuration.
