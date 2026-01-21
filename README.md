# 🛍️ ModuMart

A microservices-based e-commerce platform built with Spring Boot. Handles user management, product catalog, orders, reviews, and notifications.

## What's Included

- User authentication & management
- Product inventory with stock tracking
- Order processing & lifecycle management
- Product reviews & ratings
- Event-driven notifications via Kafka
- API Gateway for unified access
- Service discovery with Eureka
- Full observability stack (Grafana, Prometheus, Zipkin)

## Tech Stack

**Backend**: Spring Boot 3.x, Spring Cloud  
**Database**: PostgreSQL (per-service databases)  
**Messaging**: Apache Kafka  
**Service Discovery**: Netflix Eureka  
**Monitoring**: Prometheus, Grafana, Zipkin, Loki, Tempo  
**Containerization**: Docker & Docker Compose

## Quick Start

**Prerequisites**: Java 17+, Maven 3.6+, Docker & Docker Compose
```bash
# Clone the repo
git clone <repository-url>
cd ModuMart-main

# Run everything with Docker
docker-compose -f deployment/docker-compose.yaml up -d
```

**Development mode** (run services locally):
```bash
# Start infrastructure only
docker-compose -f deployment/docker-compose-infra.yaml up -d

# Build and run services
mvn clean install
cd eureka-service && mvn spring-boot:run
# Repeat for other services
```

## Access Points

- **API Gateway**: http://localhost:8080
- **Swagger UI**: http://localhost:8080/swagger-ui.html
- **Grafana**: http://localhost:3000
- **Prometheus**: http://localhost:9090
- **Zipkin**: http://localhost:9411

## Services

- **api-gateway** (8080) - Entry point
- **eureka-service** - Service registry
- **user-service** - User accounts
- **auth-service** - Authentication
- **inventory-service** - Products & stock
- **order-service** - Order processing
- **reviews-service** - Product reviews
- **notification-service** - Event notifications

---

Built with Spring Boot & microservices architecture
