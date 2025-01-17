# Learning Docker with Astronomer and Apache Airflow

## Project Overview
This project serves as an introduction to Docker while working with Apache Airflow and Astronomer. By setting up and running an Airflow environment using Docker containers, you will gain practical knowledge of containerization and workflow orchestration.

## Key Objectives
- Understand the basics of Docker and containerization.
- Set up and run Apache Airflow locally using Docker.

## Project Structure
The project contains the following key files and directories:

- **`dags/`**: Contains Python files for your Airflow DAGs.
  - Example DAG: `example_astronauts`, showcasing a simple ETL pipeline using the TaskFlow API and dynamic task mapping.

- **`Dockerfile`**: Defines the Astronomer Runtime Docker image for the Airflow environment. You can customize this file to execute additional commands or apply overrides at runtime.

- **`include/`**: A folder for storing any additional project-specific files. It is empty by default.

- **`packages.txt`**: A file for listing OS-level packages required for the project. Currently empty.

- **`requirements.txt`**: A file for listing Python dependencies for the project. Currently empty.

- **`plugins/`**: A directory for adding custom or community plugins for Airflow. Currently empty.

- **`airflow_settings.yaml`**: A local-only configuration file to define Airflow Connections, Variables, and Pools during development, bypassing the need to set these in the UI.

## Learning Docker Through Airflow Setup
This project provided me with hands-on experience with Docker by setting up a multi-container environment:

1. **Components**:
   - **Postgres**: Airflow's metadata database.
   - **Webserver**: Hosts the Airflow UI at [http://localhost:8080](http://localhost:8080).
   - **Scheduler**: Monitors and triggers tasks.
   - **Triggerer**: Manages deferred tasks.

2. **Commands**:
   - Start the Airflow environment:
     ```bash
     astro dev start
     ```
   - Verify running containers:
     ```bash
     docker ps
     ```
   - Access the Airflow UI at [http://localhost:8080](http://localhost:8080). Use `admin` for both username and password.
   - Connect to the Postgres database at `localhost:5432/postgres`.


## Learning Outcomes
- Gain hands-on experience with Docker and container orchestration.
- Understand how to manage an Airflow environment using Docker.
- Learn to build, test, and run containerized applications locally and on Astronomer.
