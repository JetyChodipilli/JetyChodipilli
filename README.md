<p align="center">
  <img src="./assets/github-hero-final.jpg" alt="Jety Chodipilli — Java Backend Developer" width="100%" />
</p>

---

## Professional Summary

I’m a Java Backend Developer who enjoys building systems where the backend has real responsibility — permissions, approvals, state changes, notifications, audit trails, and the rules that keep a product consistent when several roles are using it at the same time.

Most of my work is around Spring Boot applications, secure APIs, event-driven workflows, and database-backed business logic. I like projects where there is an actual flow to reason about, not just CRUD endpoints sitting behind a dashboard.

---

## Backend Tech Stack

<table>
<tr>
<td width="50%" valign="top">

**Languages**  
Java 8 / 17 / 21 · Python

**Frameworks**  
Spring Boot · Spring MVC · Spring Security · Spring Cloud · Spring Data JPA · Hibernate ORM · WebFlux

**APIs & System Design**  
REST APIs · Microservices · Event-Driven Architecture · gRPC · Protocol Buffers · API Gateway · Eureka · SOAP

**Databases**  
PostgreSQL · MySQL · MongoDB · JPA / Hibernate

</td>
<td width="50%" valign="top">

**Messaging**  
Apache Kafka — producers, consumers, topics, event-driven patterns

**Cloud & DevOps**  
AWS EC2 · RDS · SES · Docker · GitHub Actions · GitLab CI · Git

**Security**  
Spring Security · OAuth 2.0 · JWT · RBAC · BCrypt

**Testing & Tools**  
JUnit 5 · Mockito · Maven · IntelliJ IDEA · Postman · Eclipse / STS · MobaXterm

</td>
</tr>
</table>

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,postgres,mysql,mongodb,redis,kafka,docker,aws,githubactions,maven,git,linux" alt="Backend technology stack" />
</p>

---

## Selected Engineering Work

<table>
<tr>
<td width="68%" valign="top">

### BrainServe Connect
**Enterprise Visitor & Workforce Management Platform**

BrainServe Connect is the kind of backend project I enjoy because the system has to coordinate people, permissions, approvals, notifications, and permanent operational history without letting one role jump ahead of another.

The visitor flow moves through **Security intake → Reception verification → HR review → Team Lead / Employee / CEO approval → QR visitor pass → check-in / completion**.

The backend uses seven-role RBAC for System Admin, CEO, HR Admin, Team Lead, Employee, Receptionist, and Security. Kafka carries internal calls and workflow notifications, PostgreSQL stores the operational record, Redis supports fast state access, and Flyway keeps schema changes versioned with the application.

**Backend work**
- department-based employee onboarding
- Team Lead assignment and task worksheets
- employee progress tracking and HR insights
- account approval and password recovery
- profile management and termination approval
- audit trails and permanent operational logs
- Kafka-based internal calls and workflow notifications
- PostgreSQL persistence, Redis support and Flyway migrations
- Spring Security, BCrypt, RBAC and validated state transitions

**Stack:** Java 21 · Spring Boot 3 · Spring Security · Spring Data JPA · PostgreSQL · Apache Kafka · Redis · Flyway · Maven · Docker · REST APIs

[**Live Demo**](https://brain-serve-connect-vercel-demo.vercel.app/) · [**Demo Repository**](https://github.com/JetyChodipilli/Brainserve-Connect-client-demo)

</td>
<td width="32%" valign="top">

### Client Onboarding Platform

I built this around a simple problem: onboarding workflows become hard to trust when templates, permissions, projects, and audit history all change independently.

The backend stays as one Spring Boot deployable, but the domain boundaries are explicit. Published workflow versions are immutable, and onboarding starts from a snapshot so a running process does not silently change when a template is edited later.

**Highlights**
- multi-tenant backend design
- RBAC and MFA
- PostgreSQL + Flyway
- workflow versioning
- immutable onboarding snapshots
- dependency validation
- integration and architecture tests

[**Repository**](https://github.com/JetyChodipilli/Client-Onboarding)

</td>
</tr>
</table>

---

## Java Backend Architecture Approach

<p align="center">
  <img src="./assets/backend-architecture-ignition-v2.svg" alt="Java backend architecture approach" width="100%" />
</p>

<table>
<tr>
<td width="25%" valign="top">

**Request Flow**

`Client → Gateway → Security → Controller → Service → Repository → Database`

</td>
<td width="25%" valign="top">

**Event Flow**

`Service → Kafka Producer → Topic → Consumer → Notification / Workflow / Analytics`

</td>
<td width="25%" valign="top">

**Data Flow**

`Spring Boot → JPA / Hibernate → PostgreSQL`

`Spring Boot → Redis`

`Flyway → Database`

</td>
<td width="25%" valign="top">

**Delivery Flow**

`Git → Maven → JUnit / Mockito → Docker → CI/CD → AWS`

</td>
</tr>
</table>

### Architecture principles

**Security before business logic.** Authentication and authorization are handled at the edge of the backend flow, while resource-level permission checks remain inside the application.

**Database as the source of truth.** PostgreSQL / MySQL owns transactional business state. Redis supports cache or session use; it does not replace the authoritative record.

**Sync and async have different jobs.** REST or gRPC handles direct request/response work. Kafka is used when producers should not block on downstream processing.

**Delivery is part of the system.** Migrations, tests, containers, CI/CD, and deployment are treated as part of the backend architecture rather than something added at the end.

---

## More Backend Work

| Project | What I used it for |
|---|---|
| [Healthcare Patient Management System](https://github.com/JetyChodipilli/Healthcare-Patient-Management-System-Microservice) | Microservices learning build covering Patient, Billing, Analytics, Auth and API Gateway services with gRPC, Kafka, JWT, Docker and PostgreSQL |
| [Payment Processing Microservice](https://github.com/JetyChodipilli/Payment-Processing-Microservice-with-Stripe-and-MySQL) | Stripe charge flow with MySQL persistence |
| [AWS SES Email Service](https://github.com/JetyChodipilli/AWS-SES-EmailSend-SpringBoot) | Email lifecycle handling around AWS SES delivery |
| [Spring Batch Processing](https://github.com/JetyChodipilli/Spring-Batch-Processing) | CSV ingestion and chunk-based backend processing |
| [API Gateway Realtime Project](https://github.com/JetyChodipilli/API-Gateway-Realtime-Project) | API Gateway and routing experiments |
| [Spring Cloud API Gateway](https://github.com/JetyChodipilli/Spring-Cloud-ApiGateway) | Spring Cloud Gateway and Eureka exploration |

---

## Language Profile

<p align="center">
  <img src="./assets/top-languages-v2.svg" alt="Top languages across public repositories" width="70%" />
</p>

The language card is generated from public repositories inside this profile repository.

**Primary backend language:** Java  
**Secondary language from resume:** Python

---

## Contribution Trail

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
    <img width="100%" alt="GitHub contribution snake" src="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
  </picture>
</p>

---

## Current Friction

I prefer leaving a few rough edges visible instead of pretending every repo is finished.

- **BrainServe demo** is a public client walkthrough, not the production backend.
- **Client Onboarding** is stronger in workflow and architecture work than in presentation polish right now.
- **Payment Processing** still needs more production hardening around validation, idempotency, and error handling.
- I keep questioning whether a project actually needs another piece of infrastructure before adding one.

---

## If You’re Reviewing My Work

1. [**BrainServe Connect Live Demo**](https://brain-serve-connect-vercel-demo.vercel.app/) — enterprise workflow and client-facing product flow.
2. [**Client Onboarding Platform**](https://github.com/JetyChodipilli/Client-Onboarding) — workflow engine, multi-tenancy, RBAC, persistence and testing.
3. [**AWS SES Email Service**](https://github.com/JetyChodipilli/AWS-SES-EmailSend-SpringBoot) — AWS integration and delivery-state persistence.
4. [**Payment Processing Microservice**](https://github.com/JetyChodipilli/Payment-Processing-Microservice-with-Stripe-and-MySQL) — focused Spring Boot payment flow.

---

## Connect

**GitHub:** [JetyChodipilli](https://github.com/JetyChodipilli)  
**Location:** Hyderabad, India  
**Status:** Open to Opportunities

---

<sub>Java Backend Development · Spring Boot · Microservices · Kafka · PostgreSQL · AWS · Security · System Design</sub>
