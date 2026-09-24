<table>
<tr>
<td width="68%" valign="middle">

### Hi, I'm

# Jety Chodipilli

## Java Backend Developer

I build backend systems with **Java, Spring Boot, PostgreSQL, Kafka and Redis** — mainly secure APIs, workflow-heavy applications, event-driven processing and database-backed business logic.

<p>
  <img src="https://img.shields.io/badge/Java-17%20%2F%2021-15324B?style=flat-square&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring_Boot-3.x-3F776B?style=flat-square&logo=springboot&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring_Security-JWT%20%2F%20RBAC-315A75?style=flat-square&logo=springsecurity&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-Primary_Data-15324B?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Kafka-Event_Driven-315A75?style=flat-square&logo=apachekafka&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-Cache_%2F_Session-A6533D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-Containers-315A75?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-Cloud-D69A45?style=flat-square&logo=amazonaws&logoColor=white" />
</p>

📍 **Hyderabad, India**  
💼 **Open to Java Backend / Spring Boot opportunities**

[**BrainServe Live Demo**](https://brain-serve-connect-vercel-demo.vercel.app/) · [**Repositories**](https://github.com/JetyChodipilli?tab=repositories) · [**Portfolio**](https://jetychportfolio.netlify.app/)

</td>
<td width="32%" align="center" valign="middle">

<img src="https://res.cloudinary.com/dtl11fi8q/image/upload/v1774869278/IMG_20260330_164201_qdj4z0.png" width="250" alt="Jety Chodipilli" />

**Backend Development · Security · System Design · Event Driven Architecture**

</td>
</tr>
</table>

---

## Professional Summary

I’m a Java Backend Developer who enjoys building systems where the backend has real responsibility — permissions, approvals, state changes, notifications, audit trails and data that needs to remain consistent across multiple roles.

Most of my work is around Spring Boot applications, secure REST APIs, event-driven workflows and relational data. I prefer understanding the full request and data flow instead of stopping at controller-level CRUD.

---

## Core Backend Skills

| Area | Skills |
|---|---|
| **Java & Spring** | Java 8 / 17 / 21, Spring Boot, Spring MVC, Spring Security, Spring Cloud, Spring Data JPA, Hibernate |
| **API & Architecture** | REST APIs, Microservices, Event-Driven Architecture, gRPC, Protocol Buffers, API Gateway, Eureka |
| **Data** | PostgreSQL, MySQL, MongoDB, JPA / Hibernate, Flyway |
| **Messaging & State** | Apache Kafka, Redis |
| **Security** | JWT, OAuth 2.0, RBAC, BCrypt, request validation |
| **Testing** | JUnit 5, Mockito, Testcontainers, integration testing, ArchUnit |
| **Cloud & Delivery** | Docker, Maven, GitHub Actions, GitLab CI, AWS EC2 / RDS / SES, Git |
| **Tools** | IntelliJ IDEA, Postman, Eclipse / STS, MobaXterm |

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,postgres,mysql,mongodb,redis,kafka,docker,aws,githubactions,maven,git,linux" alt="Backend technology stack" />
</p>

---

## Featured Projects

### 01 · BrainServe Connect
**Enterprise Visitor & Workforce Management Platform**

BrainServe Connect handles visitor approvals, employee operations and internal communication across seven roles: System Admin, CEO, HR Admin, Team Lead, Employee, Receptionist and Security.

The main visitor flow is:

`Security Intake → Reception Verification → HR Review → Team Lead / Employee / CEO Approval → QR Visitor Pass → Check-in / Completion`

My backend work centers on role-based access, approval-state transitions, PostgreSQL persistence, Kafka-driven internal calls and notifications, Redis-backed operational state, Flyway migrations and audit history.

**Backend:** `Java 21` · `Spring Boot 3` · `Spring Security` · `Spring Data JPA` · `PostgreSQL` · `Kafka` · `Redis` · `Flyway` · `Docker`

[**Live Demo →**](https://brain-serve-connect-vercel-demo.vercel.app/) · [**Demo Repository →**](https://github.com/JetyChodipilli/Brainserve-Connect-client-demo)

---

### 02 · Client Onboarding Platform
**Multi-Tenant Workflow & Relationship Management**

I built this around a problem that shows up quickly in onboarding software: workflow definitions change, but work already in progress still needs to remain explainable and stable.

The backend is a Spring Boot modular monolith with multi-tenancy, RBAC, MFA, client/project management and a versioned workflow engine. Published workflow versions are immutable, and onboarding starts from a stored snapshot so active runs do not silently change when a template is edited later.

**Backend:** `Java 17` · `Spring Boot 4.1` · `Spring Security` · `PostgreSQL 17` · `Flyway` · `Testcontainers` · `ArchUnit` · `Docker`

[**Repository →**](https://github.com/JetyChodipilli/Client-Onboarding)

---

### 03 · Healthcare Patient Management System
**Microservices Learning Build**

A five-service system covering Patient, Billing, Analytics, Auth and API Gateway services.

It explores service-to-service communication with gRPC + Protocol Buffers, Kafka-based analytics events, JWT authentication behind Spring Cloud Gateway, PostgreSQL persistence and Dockerized services.

**Backend:** `Spring Boot` · `Spring Cloud Gateway` · `gRPC` · `Protocol Buffers` · `Kafka` · `JWT` · `PostgreSQL` · `Docker`

[**Repository →**](https://github.com/JetyChodipilli/Healthcare-Patient-Management-System-Microservice)

---

## Backend Architecture Approach

This is the backend shape I aim for across my Spring Boot projects. The exact components change by product, but the responsibilities stay separated: **edge/security, application logic, data, messaging, platform configuration, observability and delivery**.

```text
┌──────────────────────────── CLIENT LAYER ────────────────────────────┐
│  Web / Mobile / Internal UI / External API Consumer                │
└───────────────────────────────┬──────────────────────────────────────┘
                                │ HTTPS / REST
                                ▼
┌────────────────────────────── EDGE LAYER ────────────────────────────┐
│  Load Balancer / API Gateway                                       │
│  • Routing              • CORS                                     │
│  • Rate limiting        • Correlation / Request ID                 │
│  • JWT pre-validation   • Service discovery / load balancing       │
└───────────────────────────────┬──────────────────────────────────────┘
                                ▼
┌──────────────────────────── SECURITY LAYER ──────────────────────────┐
│  Spring Security Filter Chain                                      │
│  JWT / OAuth2 · RBAC · BCrypt · resource-level authorization       │
└───────────────────────────────┬──────────────────────────────────────┘
                                ▼
┌────────────────────────── APPLICATION LAYER ─────────────────────────┐
│  Controller                                                         │
│     │                                                               │
│     ├─ Request DTO / Bean Validation                                │
│     ├─ DTO ↔ Entity / Domain Mapping                                │
│     └─ Global Exception Handler / Problem Response                  │
│                                                                     │
│  Service / Domain Layer                                             │
│     • business rules        • workflow / state transitions          │
│     • @Transactional        • idempotency                           │
│     • authorization checks  • audit/event creation                  │
│                                                                     │
│     ├──────── Sync calls ───────► REST / gRPC / OpenFeign           │
│     ├──────── Cache/session ────► Redis                             │
│     ├──────── Files ────────────► S3-compatible object storage      │
│     └──────── Async events ─────► Transactional Outbox / Producer   │
└───────────────────┬───────────────────────────────┬──────────────────┘
                    │                               │
                    ▼                               ▼
┌──────────────── DATA / PERSISTENCE ─────────┐   ┌──────── MESSAGING ────────┐
│ Spring Data JPA / Hibernate                │   │ Apache Kafka              │
│ Repository layer                           │   │ Producer → Topic          │
│                                            │   │          → Consumer Group │
│ PostgreSQL / MySQL                         │   │          → DLT / Retry    │
│ • transactional data                       │   │                           │
│ • audit history                            │   │ Notifications             │
│ • idempotency keys                         │   │ Internal workflows        │
│                                            │   │ Analytics / integrations │
│ Flyway → versioned schema migrations       │   └───────────────────────────┘
└─────────────────────────────────────────────┘

┌──────────────────────── PLATFORM / CONFIG ───────────────────────────┐
│ application.yml / Spring Profiles / Environment Variables           │
│ Externalized secrets / deployment secrets                           │
│ Centralized config when a distributed system needs it               │
│ Scheduler / background workers where the workflow requires them     │
└──────────────────────────────────────────────────────────────────────┘

┌──────────────────────── EXTERNAL INTEGRATIONS ───────────────────────┐
│ Email / AWS SES · Payment provider · Object storage · External APIs │
└──────────────────────────────────────────────────────────────────────┘

┌────────────────────────── OBSERVABILITY ─────────────────────────────┐
│ Structured logs · Spring Actuator · Health / Readiness              │
│ Metrics / Prometheus · Distributed tracing / Zipkin                 │
│ Dashboards / Grafana where the project requires them                │
└──────────────────────────────────────────────────────────────────────┘

┌──────────────────────────── DELIVERY ────────────────────────────────┐
│ Git                                                                │
│  ↓                                                                 │
│ Maven Build                                                        │
│  ↓                                                                 │
│ JUnit / Mockito / Testcontainers / Integration Tests               │
│  ↓                                                                 │
│ Static / Architecture Checks                                       │
│  ↓                                                                 │
│ Docker Image                                                       │
│  ↓                                                                 │
│ GitHub Actions / GitLab CI                                         │
│  ↓                                                                 │
│ Flyway Migration → Deploy → Health Check                            │
│  ↓                                                                 │
│ AWS EC2 / RDS / SES or project-specific runtime                    │
└──────────────────────────────────────────────────────────────────────┘
```

### How I separate responsibilities

- **Edge and security:** the gateway handles routing, rate limits and request-level concerns; Spring Security handles authentication and authorization before protected business operations run.
- **API boundary:** controllers accept DTOs, validation rejects invalid input early, and a global exception layer returns consistent API errors.
- **Domain layer:** services own business rules, state transitions, transactions, idempotency and resource-level permission checks.
- **Persistence:** repositories isolate JPA/Hibernate access; PostgreSQL or MySQL remains the source of truth, with Flyway owning schema evolution.
- **Caching and coordination:** Redis is used for cache, session, rate-limit or short-lived coordination data where it adds value.
- **Synchronous communication:** REST, gRPC or OpenFeign is used when the caller needs an immediate result.
- **Asynchronous communication:** Kafka is used for decoupled work such as notifications, internal workflows and analytics; outbox/inbox, retry and dead-letter patterns are used when delivery guarantees matter.
- **Files and integrations:** object storage, email, payment and other external APIs stay behind dedicated adapters/services instead of leaking into domain code.
- **Configuration:** environment-specific settings stay outside business code through Spring profiles, environment variables and deployment secrets; centralized configuration is added only when the system actually needs it.
- **Observability:** health/readiness, structured logs, metrics and tracing are part of operating the backend, not just debugging it locally.
- **Delivery:** tests, migrations, containerization, CI/CD and post-deploy health checks are treated as part of the backend lifecycle.

---

## More Backend Work

| Repository | Focus |
|---|---|
| [Healthcare Patient Management System](https://github.com/JetyChodipilli/Healthcare-Patient-Management-System-Microservice) | Five-service microservices build using Spring Boot, Spring Cloud Gateway, gRPC, Protocol Buffers, Kafka, JWT, PostgreSQL and Docker |
| [Payment Processing Microservice](https://github.com/JetyChodipilli/Payment-Processing-Microservice-with-Stripe-and-MySQL) | Spring Boot → Stripe → MySQL payment flow |
| [AWS SES Email Service](https://github.com/JetyChodipilli/AWS-SES-EmailSend-SpringBoot) | Email delivery state around AWS SES |
| [Employee Management System](https://github.com/JetyChodipilli/EmployeeManagementSystem) | Spring Boot / Spring MVC application for employee records, search, action history, PDF ID-proof upload, report generation and MySQL persistence |
| [OpsHub](https://github.com/JetyChodipilli/OpsHub) | Workforce, delivery and operations platform baseline using a Spring Boot modular monolith, PostgreSQL, Kafka outbox/inbox patterns, optional Redis and resource-scoped authorization |
| [SeatEngine](https://github.com/JetyChodipilli/SeatEngine) | Distributed movie-booking system with Spring Boot microservices, JWT gateway security, Redis/JPA seat locking, idempotent booking/payment, Kafka outbox events, resilience patterns and observability |

---

## Contribution Activity

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
    <img width="100%" alt="GitHub contribution snake" src="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
  </picture>
</p>

---

## Contact

<p>
  <a href="https://github.com/JetyChodipilli">
    <img src="https://img.shields.io/badge/GitHub-JetyChodipilli-15324B?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://brain-serve-connect-vercel-demo.vercel.app/">
    <img src="https://img.shields.io/badge/BrainServe-Live_Demo-3F776B?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
</p>

**Hyderabad, India** · **Open to Java Backend / Spring Boot opportunities**

---

<p align="center">
  <strong>Java · Spring Boot · Spring Security · PostgreSQL · Kafka · Redis · Docker · AWS</strong>
</p>
