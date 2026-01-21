# Job Application Platform – Microservices Architecture

A backend **Job Application Platform** built using **Spring Boot Microservices**, demonstrating how a monolithic system can be decomposed into independently deployable services with synchronous inter-service communication.

This project focuses on **service design, communication, observability, containerization, and scalability concepts** used in real-world backend systems.

---

## 🧩 Microservices Overview

The application is split into the following services:

- **Job Service**
  - Manages job listings
  - CRUD operations for jobs
  - Acts as the primary service for job-related APIs

- **Company Service**
  - Manages company information
  - Maintains relationship between companies and jobs

- **Review Service**
  - Manages reviews for companies
  - Linked with company service

- **Service Registry (Eureka)**
  - Enables service discovery
  - Allows services to communicate using service names

- **API Gateway**
  - Basic setup completed
  - Advanced routing, resilience & rate limiting planned (WIP)

---

## 🔁 Inter-Service Communication

- Synchronous communication implemented using:
  - **RestTemplate**
  - **OpenFeign Clients**
- Service-to-service calls via **Eureka service discovery**
- DTO pattern used to avoid tight coupling between services

Example:
- Job Service fetching company & review details
- Aggregated job response using DTOs

---

## 🗄️ Data & Persistence

- Each microservice owns its **own database schema**
- **PostgreSQL** used as the primary database
- **Spring Data JPA & Hibernate**
- Entity relationships handled within service boundaries

---

## 🐳 Docker & Containerization

- Each microservice is containerized using **Docker**
- Multi-container setup using **Docker Compose**
- PostgreSQL runs as a separate container
- Docker networks used for inter-container communication

---

## 📊 Observability & Monitoring

- **Spring Boot Actuator**
  - Health
  - Metrics
  - Info
  - Logs
- **Distributed Tracing**
  - Zipkin integrated via Micrometer
  - Trace IDs propagated across services
  - End-to-end request visibility

---

## 🧠 Key Concepts Implemented

- Monolith → Microservices refactoring
- Service Discovery (Eureka)
- Inter-service communication
- DTO pattern
- Containerized microservices
- Distributed tracing
- Actuator-based monitoring
- Clean service boundaries

---

## 🚧 Work in Progress (Planned Next)

The following features are **intentionally planned** and will be implemented next:

- Advanced **API Gateway routing**
- Load-balanced routing via Gateway
- Fault tolerance using **Resilience4j**
  - Circuit Breaker
  - Retry
  - Rate Limiting
  - Fallback mechanisms
- Configuration Management using **Spring Cloud Config**
- Centralized configuration repository

> These enhancements are planned as part of incremental system hardening.

---

## 🏗️ Tech Stack

- **Java 21**
- **Spring Boot**
- **Spring Cloud**
- **Eureka Service Registry**
- **Spring Cloud Gateway**
- **OpenFeign**
- **Spring Data JPA**
- **PostgreSQL**
- **Docker & Docker Compose**
- **Zipkin + Micrometer**
- **Maven**

---

## 🎯 What This Project Demonstrates

✔ Real-world microservices design  
✔ Clear service boundaries  
✔ Synchronous communication patterns  
✔ Observability & tracing  
✔ Container-first mindset  
✔ Incremental system evolution  

---

## 👤 Author

**Nihal Singh**  
Backend Developer | Java | Spring Boot | Microservices

---

> This project reflects an evolving microservices system, built step-by-step following industry best practices.
