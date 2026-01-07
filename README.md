# Spring Boot Service Template
A **Spring Boot** project template for **learning and personal** project development.
Pre-configured to run quickly with **Docker Compose** in a development environment.

## 🎯 Purpose
- Learn and practice Spring Boot
- Foundation for personal projects
- Experiment with Docker & Docker Compose in backend development

## 📁 Project Structure
- Java 17+
- Maven
- Docker
- Docker Compose

## 🚀 Requirements
```bash
    springboot-service-template/
    ├── src/                        # Source code
    ├── docker-compose.dev.yml      # Docker Compose for dev environment
    ├── docker-compose.prod.yml      # Docker Compose for production environment
    ├── Dockerfile                  # Dockerfile to build Spring Boot app
    ├── .env.example               # Environment configuration template
    ├── pom.xml
    └── README.md
```

## ⚙️ Environment Configuration
The project uses a ```.env``` file for environment variable configuration.
1. Create .env file
```bash
cp .env.example .env
```
2. Configure ```.env```
```bash
SPRING_PROFILES_ACTIVE=local

SERVICE_NAME=order-service
SERVER_PORT=8080

DB_HOST=order-db
DB_PORT=5432
DB_NAME=order_db
DB_USERNAME=postgres
DB_PASSWORD=postgres
IMAGE_TAG=1.0.1
```
**⚠️ The .env file is for local use only, do not commit to repository.**

## 🐳 Run with Docker Compose (Dev)
Start the application with Docker Compose:
```bash
docker compose -f docker-compose.dev.yml up -d
```
Stop the application:
```bash
docker compose -f docker-compose.dev.yml down
```
View logs
```bash
docker compose -f docker-compose.dev.yml logs -f
```
## 🌐 Access the Application
After successful startup, the application will be available at:
```bash
http://localhost:8080
```
## ▶️ Run Locally (Without Docker)
Run directly with Maven:
```bash
mvn spring-boot:run
```
Or:
```bash
./mvnw spring-boot:run
```

## 🛠 Build the Project
Build jar file:
```bash
mvn clean package
```
Build Docker image:
```bash
docker build -t springboot-service-template
```

## 🔐 Notes
- Do not commit .env file
- Use .env.example to share configuration
- This project is not production-ready, meant for learning and experimentation

## 📄 License
This project is for learning and personal use.