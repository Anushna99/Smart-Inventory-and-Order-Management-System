#  Smart Inventory & Order Management System

An enterprise-grade microservices-based platform to manage inventory, process customer orders, auto-replenish stock, and send real-time notifications. This system demonstrates key principles of modern backend architecture including domain-driven design, event-driven communication, containerized deployment, and secure API access.

## Features

-  Role-Based Access Control via Keycloak (Admin, Customer, Warehouse Manager)
-  Inventory Management with auto-replenishment logic
-  Order Processing using event-driven Kafka architecture
-  Asynchronous Notifications (Email/SMS) via Kafka
-  Real-Time Reporting & Monitoring via Prometheus & Grafana
-  OAuth2 and JWT-secured APIs with API Gateway
-  Resilient service-to-service communication with Resilience4j circuit breakers

---

---

## 🧪 Tech Stack

- **Backend:** Spring Boot, Spring Data JPA, Spring Security, Spring Cloud
- **Messaging:** Kafka with Confluent Schema Registry
- **Authentication:** Keycloak (OAuth2 + JWT)
- **Databases:** MySQL (Relational), MongoDB (Audit Logs), Redis (Cache)
- **DevOps & Infra:** Docker, Kubernetes (Helm-ready), Prometheus, Grafana
- **Testing:** WireMock, Testcontainers
- **Documentation:** Swagger/OpenAPI (via springdoc-openapi)
- **API Clients:** Spring RestClient (formerly Feign)

---

## 🧰 Modules

| Module               | Description |
|----------------------|-------------|
| `inventory-service`  | Manages stock levels, caching, and auto-replenishment logic |
| `order-service`      | Accepts orders, publishes events to Kafka |
| `product-service`    | Handles product catalog and metadata |
| `notification-service` | Listens to Kafka events and sends notifications |
| `api-gateway`        | Central gateway to route external traffic securely |
| `config-server`      | Centralized Spring Cloud Config |
| `discovery-server`   | Eureka-based service registry |
| `common-lib`         | Shared DTOs, utilities, and Kafka schemas |
