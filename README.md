### Real time data processing pipeline

This project serves as a step-by-step guide to building a complete data engineering pipeline, covering everything from data ingestion to processing and storage. Here’s a detailed breakdown:

1. **Data Ingestion with Apache Airflow**:
   - **Task Orchestration**: Apache Airflow is used to manage and schedule tasks in the pipeline. It fetches random user data from the `randomuser.me` API and stores it in a PostgreSQL database.
   - **Ease of Use**: Airflow makes it easy to set up and monitor complex workflows, ensuring data is ingested reliably.

2. **Real-Time Data Streaming with Apache Kafka**:
   - **High-Throughput Streaming**: Apache Kafka streams the data from PostgreSQL to the data processing engine. It handles large volumes of data efficiently and ensures that the data flows smoothly through the pipeline.
   - **Coordination with Zookeeper**: Apache Zookeeper manages Kafka brokers, providing distributed synchronization and ensuring the system is fault-tolerant.

3. **Data Processing with Apache Spark**:
   - **Scalable Processing**: Apache Spark processes the streamed data, performing transformations and aggregations as needed. Spark's distributed computing capabilities allow it to handle large datasets and complex computations efficiently.
   - **Master and Worker Nodes**: Spark's architecture, with master and worker nodes, ensures that the processing tasks are distributed and managed effectively.

4. **Data Storage with Cassandra**:
   - **High Availability Storage**: The processed data is stored in a Cassandra database. Cassandra is chosen for its high availability and scalability, making it suitable for storing large volumes of processed data.
   - **Fast Data Retrieval**: Cassandra provides fast read and write capabilities, ensuring that the stored data can be accessed quickly for analysis and reporting.

5. **Containerization with Docker**:
   - **Simplified Deployment**: Docker is used to containerize all components of the pipeline. Each component runs in its own Docker container, making the system modular and easy to manage.
   - **Scalability and Portability**: Docker ensures that the entire pipeline can be easily deployed on any environment, from local machines to cloud servers, enhancing scalability and portability.

### Key Benefits

- **Comprehensive Learning**: You will learn how to set up and manage each component of a data engineering pipeline, from ingestion to storage.
- **Hands-On Experience**: By following this project, you’ll gain practical experience with powerful tools like Apache Airflow, Kafka, Spark, and Cassandra.
- **Scalability**: The use of Docker ensures that the pipeline can be easily scaled and deployed in different environments.
- **Real-Time Processing**: The pipeline handles data in real-time, making it suitable for applications that require timely data processing and analysis.

### Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/airscholar/e2e-data-engineering.git
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd e2e-data-engineering
   ```

3. **Install Docker**: Ensure you have Docker installed on your machine. You can download and install Docker from [here](https://www.docker.com/products/docker-desktop).

4. **Build and Run Containers**: Use Docker Compose to build and run the containers.
   ```bash
   docker-compose up --build
   ```

5. **Access Components**:
   - **Airflow Web Interface**: `http://localhost:8080`
   - **Kafka Control Center**: `http://localhost:9021`

By following these steps, you'll set up a fully functional data engineering pipeline, gaining valuable skills and insights into data engineering practices.

3. Run Docker Compose to spin up the services:
    ```bash
    docker-compose up
    ```
