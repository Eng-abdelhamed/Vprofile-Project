# VProfile Dockerized Microservices Architecture

This project demonstrates how to deploy a **multi-tier web application** using **Docker and Docker Compose**. The system simulates a production-style environment consisting of a reverse proxy, application server, database, caching layer, and message broker.

The application is containerized and orchestrated to show how modern DevOps practices can be applied to traditional Java web applications.

---

## Architecture Overview

The system architecture includes several interconnected services:

User → Nginx (Reverse Proxy / Load Balancer) → Application Server (Tomcat) → Backend Services

Backend services include:

- MySQL database
- Memcached caching system
- RabbitMQ message broker

These components work together to provide scalability, caching, asynchronous messaging, and persistent storage.

---

## Architecture Diagram

```
Users
   │
   ▼
Load Balancer
   │
   ▼
NGINX (Reverse Proxy)
   │
   ▼
Apache Tomcat (Java Web Application)
   │
   ├── MySQL (Database)
   │
   ├── Memcached (Caching Layer)
   │
   └── RabbitMQ (Message Broker)
```

---

## Technologies Used

- Docker
- Docker Compose
- Nginx
- Apache Tomcat
- Java
- MySQL
- Memcached
- RabbitMQ

---

## Project Structure

```
VProfileProject
│
├── App/                # Java application Dockerfile
├── WebServer/          # Nginx reverse proxy configuration
├── Database/           # MySQL Dockerfile and database dump
├── docker-compose.yml  # Service orchestration
└── .env                # Environment variables
```

---

## Services

| Service | Description |
|--------|-------------|
| vproweb | Nginx reverse proxy |
| vproapp | Java web application running on Tomcat |
| vprodb | MySQL database |
| vprocache01 | Memcached caching server |
| vpromq01 | RabbitMQ message broker |

---

## Prerequisites

Make sure the following tools are installed:

- Docker
- Docker Compose

Check installation:

```
docker --version
docker compose version
```

---

## Running the Project

Clone the repository:

```
git clone https://github.com/YOUR_USERNAME/VProfileProject.git
cd VProfileProject
```

Start all services:

```
docker compose up --build
```

Docker will build the images and start all containers.

---

## Accessing the Application

After containers start successfully:

Application (via Nginx)

```
http://localhost
```

Tomcat Application

```
http://localhost:8080
```

RabbitMQ Management UI

```
http://localhost:15672
```

Default RabbitMQ credentials:

```
username: guest
password: guest
```

---

## Docker Containers

You can view running containers using:

```
docker ps
```

Stop all services:

```
docker compose down
```

---

## Features Demonstrated

- Multi-container architecture
- Reverse proxy with Nginx
- Container networking
- Service communication
- Database initialization with Docker
- Caching layer with Memcached
- Message queue integration with RabbitMQ
- Docker Compose orchestration

---

## Learning Objectives

This project is useful for learning:

- Docker containerization
- Microservices architecture basics
- DevOps practices
- Service orchestration with Docker Compose
- Infrastructure design for scalable applications

---

## Author

Developed by **Eng. Abdelhamed**
