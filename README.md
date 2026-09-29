<table>
<tr>
<td width="68%" valign="middle">

### Hi, I'm

# Jety Chodipilli

## Java Backend Developer · Spring Boot · System Design

**Jr. Java Developer @ Brainserve Groups Pvt. Ltd.**

I work on Java/Spring Boot backends where **authorization, workflow state, transactions, asynchronous processing and recovery** need to stay correct as the application grows.

My day-to-day stack is **Java, Spring Boot, PostgreSQL, Kafka, Redis and Docker**.

<p>
  <img src="https://img.shields.io/badge/Java-17%20%2F%2021-15324B?style=flat-square&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring_Boot-Backend-3F776B?style=flat-square&logo=springboot&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-Data-315A75?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Kafka-Events-315A75?style=flat-square&logo=apachekafka&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-State-A6533D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-Delivery-315A75?style=flat-square&logo=docker&logoColor=white" />
</p>

📍 **Hyderabad, India**  
💼 **Current:** Jr. Java Developer @ Brainserve Groups Pvt. Ltd.  
🔎 **Open to Java Backend / Spring Boot opportunities**

[**BrainServe Live Demo**](https://brain-serve-connect-vercel-demo.vercel.app/) · [**Portfolio**](https://jetychportfolio.netlify.app/) · [**LinkedIn**](https://www.linkedin.com/in/jetychodipilli) · [**Resume**](https://res.cloudinary.com/dtl11fi8q/image/upload/v1790238840/Jety_Chodipilli_Java_Backend_Developer_eyd961.pdf)

</td>
<td width="32%" align="center" valign="middle">

<img src="https://res.cloudinary.com/dtl11fi8q/image/upload/v1774869278/IMG_20260330_164201_qdj4z0.png" width="245" alt="Jety Chodipilli" />

**Backend Engineering**  
**Security · Workflows · Distributed Systems**

</td>
</tr>
</table>

---



# Current Engineering Work · BrainServe Connect

### Enterprise Visitor & Workforce Operations Platform

[**Live Demo →**](https://brain-serve-connect-vercel-demo.vercel.app/) · [**Public Demo →**](https://github.com/JetyChodipilli/Brainserve-Connect-client-demo) · [**Public Implementation Snapshot →**](https://github.com/JetyChodipilli/V2_Brainserve_Connect_gstack)

[![BrainServe Snapshot CI](https://github.com/JetyChodipilli/V2_Brainserve_Connect_gstack/actions/workflows/ci.yml/badge.svg)](https://github.com/JetyChodipilli/V2_Brainserve_Connect_gstack/actions/workflows/ci.yml)

BrainServe Connect is the main system I work on at Brainserve Groups.

The working repository is private; the public demo and implementation snapshot provide reviewable product and architecture evidence without exposing the production codebase.

It uses a **React/TypeScript frontend and Java 21 Spring Boot backend** to handle visitor intake, approvals, employee operations, notifications, reporting and audit history across multiple organizational roles.

### Backend details

- **Java 21 · Spring Boot 3.5.7 · Spring Modulith**
- **PostgreSQL 17.2** for application data
- **3-node Kafka KRaft cluster** for internal-call delivery
- **Redis 7.4.1** for OTP state, rate limits and dashboard caching
- Spring Security with JWT and role/scope checks
- Flyway database migrations
- transactional email/outbox processing
- private file storage with malware scanning and controlled downloads
- health/readiness endpoints and metrics
- verified snapshot: **263 automated source/regression checks passed**, with separate browser verification

### Visitor flow

```mermaid
flowchart LR
    A["Security Intake"] --> B["Reception Verification"]
    B --> C{"Visit route"}
    C -->|Employee / Client| D["HR Review"]
    D --> E["Team Lead Approval"]
    C -->|CEO / Emergency| F["Manager Approval"]
    F --> G["CEO Approval"]
    E --> H["Approved Pass"]
    G --> H
    H --> I["Forward / Check-in"]
    I --> J["Check-out & Audit"]
```

Authorization and workflow state are enforced by the backend rather than relying on UI controls.

---

## Selected Engineering Work

### Client Onboarding Platform
**Multi-tenant onboarding · versioned workflows · secure assets · client portal**

[![Client Onboarding CI](https://github.com/JetyChodipilli/Client-Onboarding/actions/workflows/ci.yml/badge.svg)](https://github.com/JetyChodipilli/Client-Onboarding/actions/workflows/ci.yml)

A Spring Boot modular monolith for organizations, clients, projects and onboarding workflows.

I kept the backend as one deployable application deliberately: the harder problem here is maintaining tenant boundaries, workflow state and audit history consistently while the product evolves.

Published workflow versions are immutable, so active onboarding runs keep the exact version they started with even when templates change later.

The current public implementation includes tenant RBAC, TOTP MFA, secure client invitations, questionnaires, private asset uploads, ClamAV scanning and architecture verification with Testcontainers and ArchUnit.

**Verified Phase 6 gate:** 55 backend tests · 12 frontend unit tests · 89 browser scenarios passed.

**Stack:** Java 17 · Spring Boot · Spring Security · PostgreSQL · Flyway · MFA · Testcontainers · ArchUnit

[**Repository →**](https://github.com/JetyChodipilli/Client-Onboarding)

---

### SeatEngine / SeatSure
**Distributed booking · locking · idempotency**

A booking-system project focused on one concrete concurrency problem: multiple users can request the same limited resource, but only one booking should win.

The project explores Redis, pessimistic and optimistic JPA locking, database-backed idempotency, payment compensation, Kafka outbox delivery, consumer deduplication and dead-letter handling.

**Stack:** Spring Boot · Redis/JPA locking · JWT gateway security · Kafka outbox events · idempotent booking/payment

[**Repository →**](https://github.com/JetyChodipilli/SeatEngine)

## Backend Decisions I Care About

- authorization is enforced server-side; hiding a control in the UI is not a security boundary
- transaction boundaries follow the business change that must succeed or fail together
- schema changes are versioned with Flyway instead of being applied manually
- Kafka is used when asynchronous or durable delivery solves a real workflow problem
- Redis is used for short-lived state, caching and coordination rather than as the source of truth
- retries are designed together with idempotency and recovery behavior
- tests cover integration boundaries and failure paths, not only happy-path methods

---

## Backend Engineering Stack

The tools I use most often to build, secure, test and operate backend applications.

### Core Backend

<p>
  <img src="https://img.shields.io/badge/Java_17%2F21-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java 17/21" />
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white" alt="Spring Security" />
  <img src="https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white" alt="Spring Data JPA" />
  <img src="https://img.shields.io/badge/Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white" alt="Hibernate" />
  <img src="https://img.shields.io/badge/Spring_Modulith-6DB33F?style=flat-square&logo=spring&logoColor=white" alt="Spring Modulith" />
</p>

### Data · Messaging · State

<p>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white" alt="Flyway" />
  <img src="https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" alt="Apache Kafka" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
</p>

### Security · Testing · Delivery

<p>
  <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white" alt="JWT" />
  <img src="https://img.shields.io/badge/RBAC-44546A?style=flat-square" alt="RBAC" />
  <img src="https://img.shields.io/badge/MFA-44546A?style=flat-square" alt="MFA" />
  <img src="https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=junit5&logoColor=white" alt="JUnit 5" />
  <img src="https://img.shields.io/badge/Mockito-78A641?style=flat-square" alt="Mockito" />
  <img src="https://img.shields.io/badge/Testcontainers-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Testcontainers" />
  <img src="https://img.shields.io/badge/ArchUnit-4C566A?style=flat-square" alt="ArchUnit" />
  <img src="https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white" alt="Maven" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions" />
</p>

### Engineering Areas

**REST APIs · transaction boundaries · workflow design · idempotency · concurrency · transactional outbox · retries & recovery · health/readiness · system design**

#### Typical Backend Flow

`Client / Frontend` → `Spring Boot API` → `Security` → `Business Logic` → `PostgreSQL / Redis` → `Kafka` → `External Services`

---

## More Backend Repositories

| Repository | Focus |
|---|---|
| [Healthcare Patient Management System](https://github.com/JetyChodipilli/Healthcare-Patient-Management-System-Microservice) | microservices learning build using Spring Boot, Kafka, gRPC, JWT, PostgreSQL and Docker |
| [Payment Processing Microservice](https://github.com/JetyChodipilli/Payment-Processing-Microservice-with-Stripe-and-MySQL) | payment integration and persistence |
| [AWS SES Email Service](https://github.com/JetyChodipilli/AWS-SES-EmailSend-SpringBoot) | email delivery with AWS SES |
| [Employee Management System](https://github.com/JetyChodipilli/EmployeeManagementSystem) | employee records, uploads and reporting |
| [Spring Batch Processing](https://github.com/JetyChodipilli/Spring-Batch-Processing) | batch processing |
| [Spring Boot File Processing API](https://github.com/JetyChodipilli/Spring-Boot-File-Processing-API) | file-processing APIs |

---



## Contribution Activity

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
    <img width="100%" alt="GitHub contribution activity" src="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
  </picture>
</p>

---

## Professional Links

[**LinkedIn**](https://www.linkedin.com/in/jetychodipilli) · [**Resume**](https://res.cloudinary.com/dtl11fi8q/image/upload/v1790238840/Jety_Chodipilli_Java_Backend_Developer_eyd961.pdf) · [**Portfolio**](https://jetychportfolio.netlify.app/) · [**BrainServe Demo**](https://brain-serve-connect-vercel-demo.vercel.app/) · [**ORCID**](https://orcid.org/0009-0008-8585-051X)

**Java Backend · Spring Boot · Security · System Design**
