# Initial Spring Boot App

A minimal Spring Boot REST application demonstrating project setup, SSL configuration, Spring profiles (dev/test), and a basic greeting endpoint.

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Spring Boot | Application framework |
| Spring Web | REST controller |
| Spring Security | SSL and security config |
| Maven Wrapper | Build tool |

---

## Project Structure

```
initial-boot-app/
└── src/main/java/com/dwiveddi/boot/
    └── InitialBootAppApplication.java  # Entry point + inline REST controller
└── src/main/resources/
    ├── application.yml                 # SSL config + dev/test profiles
    └── application_Old.properties      # Legacy config (port 8000)
```

---

## Features

- **REST Endpoint** — `GET /api/greeting` returns `"Hello from the world of API"`
- **SSL** — JKS keystore configured (`keystore.jks`, alias `divyashree`)
- **Spring Profiles**
  - `dev` — runs on port `8000`
  - `test` — runs on port `9000`

---

## Getting Started

1. **Run with default profile**
   ```bash
   ./mvnw clean spring-boot:run
   ```

2. **Run with a specific profile**
   ```bash
   ./mvnw spring-boot:run -Dspring-boot.run.profiles=dev
   ```

3. **Test the endpoint**
   ```bash
   curl http://localhost:8080/api/greeting
   ```

4. **Run tests**
   ```bash
   ./mvnw test
   ```
