# Project Description

This project showcases a local deployment using **Kubernetes with Minikube** to simulate a microservices-based architecture.
The environment is structured to demonstrate how various components, such as API gateways, Kafka clusters, and Flink consumers, can be orchestrated to work together for real-time data processing.

<div style="display: flex; justify-content: space-between;">
  <img src=".ignore/architecture.png" alt="POC Architecture" style="width: 69%;" />
</div>

## Key Components:
1. **API Gateway**: Acts as an entry point for user requests, balancing the load across multiple backend API instances.
2. **Load Balancer**: Distributes traffic evenly across multiple backend API instances to ensure high availability and fault tolerance.
3. **Backend API**: A microservice responsible for handling business logic, producing events to Kafka, and interacting with other services.
4. **Redis Cache**: Used as an in-memory data store to optimize performance by caching frequently accessed data, reducing load on the backend services and databases.
5. **Kafka Cluster**: Handles event-driven communication, producing and consuming messages through topics like `mock-user-topic`.
6. **Flink Consumer**: Ingests data from Kafka, performing ETL (Extract, Transform, Load) tasks and pushing the processed data to a **Data Warehouse**.
7. **Node Consumer**: Ingests data from Kafka,  performing ETL (Extract, Transform, Load) tasks and pushing the processed data to a **Data Warehouse**.
8. **Data Warehouse (DW)**: Stores processed data, making it accessible for analysis and reporting.
9. **Monitoring and Logging**: Services such as Prometheus and Grafana are used to track system health, performance metrics, and logs.
10. **Data Dictionary**: Present on the data-dictionary directory which you can execute it locally.
11. **Scripts**: The project contains scripts to populate the oracle DW, and scripts to backup and load the oracle database.
