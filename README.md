# Go Secure API

A high-performance, containerized REST API built in Golang, demonstrating production-grade backend infrastructure. 

## Architecture
- **Language:** Golang (1.21+)
- **Database:** PostgreSQL 15
- **Routing:** `go-chi/chi`
- **Infrastructure:** Docker & Docker Compose
- **CI/CD:** GitHub Actions (Automated build and test pipeline)

## Features
- Containerized multi-service architecture (API + Database).
- Secure SQL parameterization to prevent SQL Injection.
- Environment-based configuration.
- Automatic database table initialization on startup.
- Graceful panic recovery and request logging middleware.

## Quick Start

1. Clone the repository:
```
git clone [https://github.com/Variosity/go-secure-api.git](https://github.com/Variosity/go-secure-api.git)
cd go-secure-api
```
2. Spin up the infrastructure:
```
docker compose up --build
```
4. Verify the system is operational:
```
curl http://localhost:8080/health
```
4. Create a new user:
```
curl -X POST http://localhost:8080/users \
   -H "Content-Type: application/json" \
   -d '{"email": "test@example.com", "hash": "securehash"}'
