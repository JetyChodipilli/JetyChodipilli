<table>
<tr>
<td width="67%" valign="middle">

### Hi there, I'm

# Jety Chodipilli

## Java Backend Developer

I build backend systems with **Java, Spring Boot, PostgreSQL, Kafka and Redis**, with most of my work centered around secure APIs, workflow-heavy applications, event-driven systems and data consistency.

<p>
  <img src="https://img.shields.io/badge/Java-17%20%2F%2021-15324B?style=flat-square&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring_Boot-3.x-3F776B?style=flat-square&logo=springboot&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring_Security-RBAC%20%2F%20JWT-315A75?style=flat-square&logo=springsecurity&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-Primary_Data-15324B?style=flat-square&logo=postgresql&logoColor=white" />
</p>

<p>
  <img src="https://img.shields.io/badge/Apache_Kafka-Event_Driven-315A75?style=flat-square&logo=apachekafka&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-Cache_%2F_Session-A6533D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-Containers-315A75?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-Cloud-D69A45?style=flat-square&logo=amazonaws&logoColor=white" />
</p>

📍 **Hyderabad, India**
💼 **Open to backend development opportunities**

[**BrainServe Live Demo**](https://brain-serve-connect-vercel-demo.vercel.app/) · [**Browse Repositories**](https://github.com/JetyChodipilli?tab=repositories)

</td>
<td width="33%" align="center" valign="middle">

<img src="https://res.cloudinary.com/dtl11fi8q/image/upload/v1774869278/IMG_20260330_164201_qdj4z0.png" width="270" alt="Jety Chodipilli" />

### Backend First

`Build → Secure → Test → Ship → Improve`

</td>
</tr>
</table>

---

# Professional Summary

I’m a Java Backend Developer who enjoys working on systems where the backend has real responsibility — permissions, approvals, state changes, notifications, audit trails, and the rules that keep a product consistent when several roles are using it at the same time.

Most of my work is around Spring Boot applications, secure APIs, event-driven workflows, and database-backed business logic. I like projects where there is an actual flow to reason about, not just CRUD endpoints sitting behind a dashboard.

---

# Backend Tech Stack

<table>
<tr>
<td width="50%" valign="top">

### Core Backend

**Languages**
Java 8 · Java 17 · Java 21 · Python

**Spring Ecosystem**
Spring Boot
Spring MVC
Spring Security
Spring Cloud
Spring Data JPA
Hibernate ORM
Spring WebFlux

**API & Architecture**
REST APIs
Microservices
Event-Driven Architecture
gRPC
Protocol Buffers
API Gateway
Eureka
SOAP

</td>
<td width="50%" valign="top">

### Data, Security & Delivery

**Databases**
PostgreSQL
MySQL
MongoDB
JPA / Hibernate

**Messaging & Fast State**
Apache Kafka
Redis

**Security**
Spring Security
OAuth 2.0
JWT
RBAC
BCrypt

**Cloud & DevOps**
AWS EC2
AWS RDS
AWS SES
Docker
GitHub Actions
GitLab CI
Maven
Git

</td>
</tr>
</table>

### Testing & Development Tools

`JUnit 5` · `Mockito` · `Testcontainers` · `Postman` · `IntelliJ IDEA` · `Eclipse / STS` · `MobaXterm`

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,postgres,mysql,mongodb,redis,kafka,docker,aws,githubactions,maven,git,linux" alt="Backend technology stack" />
</p>

---

# Selected Engineering Work

<table>
<tr>
<td width="68%" valign="top">

## 01 · BrainServe Connect

### Enterprise Visitor & Workforce Management Platform

BrainServe Connect is the kind of backend project I enjoy because the system has to coordinate people, permissions, approvals, notifications, and permanent operational history without letting one role jump ahead of another.

The visitor flow moves through:

`Security Intake → Reception Verification → HR Review → Team Lead / Employee / CEO Approval → QR Visitor Pass → Check-in → Completion`

The backend uses seven-role RBAC for:

* System Admin
* CEO
* HR Admin
* Team Lead
* Employee
* Receptionist
* Security

Kafka carries internal calls and workflow notifications. PostgreSQL stores the operational record. Redis supports fast state access. Flyway keeps database changes versioned with the application.

### Backend Work

* department-based employee onboarding
* Team Lead assignment and task worksheets
* employee progress tracking
* HR insights and administrative workflows
* visitor approval lifecycle
* QR visitor-pass flow
* account approval and password recovery
* employee profile management
* termination approval workflow
* audit trails and permanent operational logs
* Kafka-based internal calls
* workflow notifications
* PostgreSQL persistence
* Redis integration
* Flyway migrations
* Spring Security
* BCrypt
* role-based authorization
* validated state transitions

### Stack

`Java 21` · `Spring Boot 3` · `Spring Security` · `Spring Data JPA` · `PostgreSQL` · `Apache Kafka` · `Redis` · `Flyway` · `Maven` · `Docker` · `REST APIs`

[**Open Live Demo →**](https://brain-serve-connect-vercel-demo.vercel.app/)

[**View Demo Repository →**](https://github.com/JetyChodipilli/Brainserve-Connect-client-demo)

</td>
<td width="32%" valign="top">

## 02 · Client Onboarding

### Multi-Tenant Workflow Platform

I built this around a simple problem: onboarding workflows become hard to trust when templates, permissions, projects, and audit history all change independently.

The backend stays as one Spring Boot deployable, but the domain boundaries are explicit. Published workflow versions are immutable, and onboarding starts from a snapshot so a running process does not silently change when someone edits a template later.

### Highlights

* multi-tenant architecture
* RBAC
* MFA
* organizations and memberships
* client and project lifecycle
* workflow templates
* versioned workflow definitions
* immutable workflow snapshots
* dependency graphs
* cycle validation
* safe workflow conditions
* idempotent onboarding start
* PostgreSQL
* Flyway
* architecture tests
* integration tests
* Testcontainers

### Stack

`Java 17` · `Spring Boot 4.1` · `Spring Security` · `Spring Data JPA` · `PostgreSQL 17` · `Flyway` · `JUnit` · `ArchUnit` · `Testcontainers` · `Docker`

[**View Repository →**](https://github.com/JetyChodipilli/Client-Onboarding)

</td>
</tr>
</table>

---

# Java Backend Architecture Approach

Instead of treating architecture as a collection of boxes, I think about it as several connected flows.

## 01 · Request Flow

<table>
<tr>
<td align="center">

### Client

Web / Mobile

</td>
<td align="center">

### →

</td>
<td align="center">

### API Gateway

Routing
Edge controls
Load balancing

</td>
<td align="center">

### →

</td>
<td align="center">

### Spring Security

Authentication
Authorization
Request filtering

</td>
<td align="center">

### →

</td>
<td align="center">

### Spring Boot

Controllers
Services
Domain logic

</td>
</tr>
</table>

`Client → API Gateway → Spring Security Filter Chain → JWT / OAuth2 / RBAC → Controller → Service`

---

## 02 · Service & Persistence Flow

<table>
<tr>
<td width="33%" align="center">

### Spring Boot Services

Business rules
Workflow validation
State transitions

</td>
<td width="33%" align="center">

### Spring Data JPA / Hibernate

Repositories
Transactions
ORM

</td>
<td width="34%" align="center">

### PostgreSQL / MySQL

Primary business data
Audit history
Operational records

</td>
</tr>
</table>

`Service → Repository → JPA / Hibernate → PostgreSQL`

PostgreSQL or MySQL owns transactional business state.

Redis supports fast access where appropriate, but it does not replace the authoritative database record.

---

## 03 · Event-Driven Flow

<table>
<tr>
<td align="center">

### Domain Service

Creates event

</td>
<td align="center">

### →

</td>
<td align="center">

### Kafka Producer

Publishes event

</td>
<td align="center">

### →

</td>
<td align="center">

### Kafka Topic

Stores event stream

</td>
<td align="center">

### →

</td>
<td align="center">

### Consumers

Notifications
Internal workflows
Analytics

</td>
</tr>
</table>

`Service → Kafka Producer → Topic → Consumer → Notification / Internal Workflow / Analytics`

Kafka is useful when one part of the system should not block while another part finishes its work.

---

## 04 · Supporting Infrastructure

<table>
<tr>
<td width="25%" valign="top">

### Redis

Cache
Session state
Fast operational access

</td>
<td width="25%" valign="top">

### Flyway

Schema migrations
Version control
Repeatable deployment

</td>
<td width="25%" valign="top">

### Docker

Consistent runtime
Packaging
Container deployment

</td>
<td width="25%" valign="top">

### AWS

EC2
RDS
SES
Infrastructure

</td>
</tr>
</table>

---

## 05 · Delivery Pipeline

```text
Developer
    │
    ▼
Git Commit
    │
    ▼
Maven Build
    │
    ▼
JUnit / Mockito / Integration Tests
    │
    ▼
Docker Image
    │
    ▼
GitHub Actions / GitLab CI
    │
    ▼
AWS Deployment
    │
    ▼
Application Monitoring
```

---

# Architecture Principles

<table>
<tr>
<td width="25%" valign="top">

### Security First

Authentication and authorization are handled before business logic.

Resource-level permissions are still validated inside the application.

</td>
<td width="25%" valign="top">

### One Source of Truth

Transactional business data belongs in PostgreSQL or MySQL.

Redis is supporting infrastructure.

</td>
<td width="25%" valign="top">

### Sync ≠ Async

REST and gRPC handle direct communication.

Kafka handles work that does not need to block the caller.

</td>
<td width="25%" valign="top">

### Delivery Matters

Migrations, tests, containers and deployment are part of the architecture.

Not an afterthought.

</td>
</tr>
</table>

---

# More Backend Work

| Project                                                                                                                     | What it covers                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| [Healthcare Patient Management System](https://github.com/JetyChodipilli/Healthcare-Patient-Management-System-Microservice) | Five-service learning build covering Patient, Billing, Analytics, Auth and API Gateway services with gRPC, Kafka, JWT, Docker and PostgreSQL |
| [Payment Processing Microservice](https://github.com/JetyChodipilli/Payment-Processing-Microservice-with-Stripe-and-MySQL)  | Stripe payment flow through Spring Boot with MySQL persistence                                                                               |
| [AWS SES Email Service](https://github.com/JetyChodipilli/AWS-SES-EmailSend-SpringBoot)                                     | QUEUED → AWS SES → SENT / FAILED email lifecycle                                                                                             |
| [Spring Batch Processing](https://github.com/JetyChodipilli/Spring-Batch-Processing)                                        | CSV ingestion and chunk-oriented backend processing                                                                                          |
| [Spring Boot File Processing API](https://github.com/JetyChodipilli/Spring-Boot-File-Processing-API)                        | File processing API experiments                                                                                                              |
| [API Gateway Realtime Project](https://github.com/JetyChodipilli/API-Gateway-Realtime-Project)                              | Gateway and service-routing work                                                                                                             |
| [Spring Cloud API Gateway](https://github.com/JetyChodipilli/Spring-Cloud-ApiGateway)                                       | Spring Cloud Gateway and Eureka exploration                                                                                                  |
| [BasicAuthentication](https://github.com/JetyChodipilli/BasicAuthentication)                                                | Spring Security fundamentals                                                                                                                 |
| [CustomUserDetailsService](https://github.com/JetyChodipilli/CustomUserDetailsService)                                      | Custom authentication and user-details experiments                                                                                           |

---

# Current Friction

I prefer leaving a few rough edges visible instead of pretending every repository is finished.

**BrainServe Connect Demo**
The public deployment is meant for client walkthroughs. It is not the production backend and does not expose the live database, authentication infrastructure, Kafka, Redis, email, OTP, or internal services.

**Client Onboarding**
The architecture and workflow engine are ahead of the presentation layer right now. The public `main` branch is implemented through Phase 3.

**Payment Processing**
The learning repo still needs production hardening around request validation, idempotency, error handling, and package cleanup.

---

# Language Profile

### Primary

`Java`

Java is the language I use for most backend work across Spring Boot, security, persistence, messaging, and API development.

### Secondary

`Python`

Used as a secondary language for scripting, experimentation, and data-oriented work.

---

# Contribution Trail

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
  <img width="100%" alt="GitHub contribution snake" src="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
</picture>

---

# If You're Reviewing My Work

Start with these:

### 1. BrainServe Connect

Enterprise workflow, role-based access, Kafka, PostgreSQL, Redis and real client demo.

[Live Demo](https://brain-serve-connect-vercel-demo.vercel.app/) · [Repository](https://github.com/JetyChodipilli/Brainserve-Connect-client-demo)

### 2. Client Onboarding

Multi-tenancy, RBAC, MFA, immutable workflow versions, dependency validation and backend testing.

[Repository](https://github.com/JetyChodipilli/Client-Onboarding)

### 3. AWS SES Email Service

A smaller integration project where delivery state is persisted around the SES call.

[Repository](https://github.com/JetyChodipilli/AWS-SES-EmailSend-SpringBoot)

### 4. Payment Processing

Focused Spring Boot → Stripe → MySQL payment flow.

[Repository](https://github.com/JetyChodipilli/Payment-Processing-Microservice-with-Stripe-and-MySQL)

---

# Connect

<p>
  <a href="https://github.com/JetyChodipilli">
    <img src="https://img.shields.io/badge/GitHub-JetyChodipilli-15324B?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://brain-serve-connect-vercel-demo.vercel.app/">
    <img src="https://img.shields.io/badge/BrainServe-Live_Demo-3F776B?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
</p>

**Hyderabad, India**
**Open to backend development opportunities**

---

<p align="center">
  <strong>Java Backend Development · Spring Boot · Microservices · Kafka · PostgreSQL · AWS · Security · System Design</strong>
</p>
