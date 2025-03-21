# MySQL Docker Setup

This project provides a simple way to set up and run MySQL using Docker and Docker Compose.

## Prerequisites

Ensure you have the following installed on your system:
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

### 1. Clone the Repository
```bash
git clone <https://github.com/bikundkumar/MySQL_Using_Docker_Compose.git>
cd mySQL-Docker
```

### 2. Configure Environment Variables
Modify the `docker-compose.yml` file if needed to set your MySQL credentials (username, password, database name).

### 3. Start the MySQL Container
```bash
docker-compose up -d
```
This command will:
- Pull the required MySQL image (if not already available locally).
- Start a MySQL container in detached mode.

### 4. Verify the Container
Check if the container is running using:
```bash
docker ps
```

### 6. Stop the MySQL Container
To stop and remove the MySQL container, run:
```bash
docker-compose down
```
## Connecting MySQL Workbench

[MySQL Workbench](https://dev.mysql.com/downloads/workbench/) is a graphical tool for managing MySQL databases. Follow these steps to connect it to your MySQL Docker container:

1. **Download and Install MySQL Workbench**
    
    - Visit the [MySQL Workbench download page](https://dev.mysql.com/downloads/workbench/).
    - Select your operating system and follow the installation instructions.
2. **Open MySQL Workbench and Create a New Connection**
    
    - Click on the `+` icon to create a new connection.
    - Set the following parameters:
        - **Connection Name**: Any descriptive name
        - **Connection Method**: Standard TCP/IP
        - **Hostname**: `localhost` (or the container’s IP address)
        - **Port**: `3306` (default MySQL port, change if needed)
        - **Username**: `root` (or any user set in `docker-compose.yml`)
        - **Password**: Click `Store in Vault` and enter your MySQL password.
    - Click `Test Connection` to verify the connection.
    - Click `OK` to save.
3. **Start Managing Your Database**
    
    - Once connected, you can execute queries, manage databases, and visualize table structures using MySQL Workbench.

