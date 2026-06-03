# SwiftPay - Payment Processing Platform

Real-Time Event-Driven P2P Payment Platform built with Java 21, Spring Boot, Kafka, Redis, PostgreSQL and Docker.

## Architecture

SwiftPay is split into two microservices:

- **Transaction Gateway** — Accepts payment requests, validates, and publishes events to Kafka
- **Ledger Service** — Consumes Kafka events and maintains debit/credit records in PostgreSQL

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Java 21, Spring Boot |
| Messaging | Apache Kafka |
| Caching | Redis |
| Database | PostgreSQL |
| Containerization | Docker, Docker Compose |
| CI/CD | GitHub Actions |
| API Docs | Swagger / OpenAPI |

## Key Features

- Asynchronous communication between services via Kafka
- Redis-based idempotency layer to prevent duplicate payments
- Atomic debit/credit operations using PostgreSQL transactions
- REST APIs with full Swagger/OpenAPI documentation
- Containerized with Docker for consistent deployment
- Automated CI/CD pipeline using GitHub Actions

## Repositories

| Service | Link |
|---------|------|
| Transaction Gateway | https://github.com/syedshareena/swiftpay-transaction-gateway |
| Ledger Service | https://github.com/syedshareena/swiftpay-ledger-service |

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /v1/payments | Initiate a payment |
| GET | /v1/ledger/transactions | Get transaction history |

## Author

Shareena Syed
https://linkedin.com/in/syedshareena
