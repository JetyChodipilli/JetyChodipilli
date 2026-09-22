<table>
<tr>
<td width="64%" valign="top">

# Jety Chodipilli

### Java Backend Engineer

I build backend systems with **Java, Spring Boot, PostgreSQL, Kafka and Redis**.  
Most of my work is around workflow-heavy applications, API design, data consistency and the unglamorous parts that keep systems reliable.

<p>
  <img src="https://img.shields.io/badge/Java-15324B?style=flat-square&logo=openjdk&logoColor=F6F3EC" alt="Java" />
  <img src="https://img.shields.io/badge/Spring_Boot-3F776B?style=flat-square&logo=springboot&logoColor=F6F3EC" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/PostgreSQL-315A75?style=flat-square&logo=postgresql&logoColor=F6F3EC" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Kafka-3E4850?style=flat-square&logo=apachekafka&logoColor=F6F3EC" alt="Kafka" />
  <img src="https://img.shields.io/badge/Redis-A6533D?style=flat-square&logo=redis&logoColor=F6F3EC" alt="Redis" />
  <img src="https://img.shields.io/badge/Docker-3F77A1?style=flat-square&logo=docker&logoColor=F6F3EC" alt="Docker" />
</p>

**Build systems that are understandable, reliable and maintainable.**

[BrainServe live demo](https://brain-serve-connect-vercel-demo.vercel.app/) · [All repositories](https://github.com/JetyChodipilli?tab=repositories)

</td>
<td width="36%" align="center" valign="top">

<img src="https://res.cloudinary.com/dtl11fi8q/image/upload/v1774869278/IMG_20260330_164201_qdj4z0.png" width="260" alt="Jety Chodipilli" />

<sub><b>Backend first. Real systems. Keep building.</b></sub>

</td>
</tr>
</table>

---

## Core expertise

<table>
<tr>
<td width="32%" valign="top">

**Backend**  
Java · Spring Boot · REST APIs · Spring Security

</td>
<td width="26%" valign="top">

**Data & messaging**  
PostgreSQL · MySQL · Redis · Kafka · Flyway

</td>
<td width="42%" valign="top">

**System work**  
Multi-tenancy · RBAC · workflow engines · event-driven flows · CI/CD · Docker

</td>
</tr>
</table>

---

## Selected engineering work

<table>
<tr>
<td width="68%" valign="top">

### Client Onboarding Platform — flagship

A multi-tenant B2B onboarding system built as a **Spring Boot modular monolith** with a Next.js frontend and PostgreSQL as the source of truth.

The part I care about most is the workflow engine: published workflow versions are immutable, onboarding starts from a snapshot, dependencies are validated, and tenant-authored conditions never execute arbitrary code.

**On `main` now:** identity, tenancy, RBAC, MFA, clients, contacts, services, projects and the Phase 3 workflow engine.

**Stack:** Java 17 · Spring Boot 4.1 · PostgreSQL 17 · Flyway · Next.js 16 · React 19 · Testcontainers · Playwright · Docker

[Repository](https://github.com/JetyChodipilli/Client-Onboarding)

</td>
<td width="32%" valign="top">

### BrainServe Connect

The public repo is a **browser demo**, not a fake production backend.

It lets a client move through eight role workspaces, sample appointment flows, reports and the connection-recovery experience without passwords or infrastructure.

**Demo evidence:** production tests stayed green; the demo browser suite covers desktop/mobile Chromium flows.

[Live demo](https://brain-serve-connect-vercel-demo.vercel.app/)  
[Demo repository](https://github.com/JetyChodipilli/Brainserve-Connect-client-demo)

</td>
</tr>
</table>

### Supporting work

- [**Payment Processing Microservice**](https://github.com/JetyChodipilli/Payment-Processing-Microservice-with-Stripe-and-MySQL) — Spring Boot → Stripe → MySQL payment flow.
- [**AWS SES Email Service**](https://github.com/JetyChodipilli/AWS-SES-EmailSend-SpringBoot) — persists email state around AWS SES delivery.
- [**Spring Batch Processing**](https://github.com/JetyChodipilli/Spring-Batch-Processing) — CSV ingestion and chunk-oriented processing.
- [**Spring Boot File Processing API**](https://github.com/JetyChodipilli/Spring-Boot-File-Processing-API) — file upload and conversion experiments.

---

## Architecture snapshot

This is the current Client Onboarding shape. I kept it as a modular monolith on purpose; Redis and Kafka are **not** in this project because the current workload does not justify them.

```mermaid
flowchart LR
    Browser["Browser"] --> Web["Next.js"]
    Web --> API["Spring Boot /api/v1"]
    API --> DB[("PostgreSQL")]
```

That project makes one trade-off very explicit: **keep module boundaries strong before paying the cost of distributed services.**

---

## Stack in rotation

<p>
  <img src="https://skillicons.dev/icons?i=java,spring,postgres,mysql,redis,kafka,docker,aws,githubactions,maven,git,linux,nextjs,ts" alt="Technology stack" />
</p>

---

## Current friction

I would rather show the rough edges than pretend everything is finished.

- **Client Onboarding:** `main` currently stops at Phase 3. Client invitation and portal work are not merged there yet.
- **BrainServe demo:** the build still reports a large JavaScript chunk warning. The browser verification is Chromium-based; Firefox, WebKit and real mobile devices are still outside the current demo test pass.

---

## Scraps & sandboxes

Small repos where I isolate one idea instead of dressing everything up as a flagship project.

- [BasicAuthentication](https://github.com/JetyChodipilli/BasicAuthentication)
- [CustomUserDetailsService](https://github.com/JetyChodipilli/CustomUserDetailsService)
- [API-Gateway-Realtime-Project](https://github.com/JetyChodipilli/API-Gateway-Realtime-Project)
- [Spring-Cloud-ApiGateway](https://github.com/JetyChodipilli/Spring-Cloud-ApiGateway)

---

## Contribution journey

<table>
<tr>
<td width="72%" valign="top">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
  <img alt="GitHub contribution snake" src="https://raw.githubusercontent.com/JetyChodipilli/JetyChodipilli/output/github-contribution-grid-snake.svg" />
</picture>

</td>
<td width="28%" valign="top">

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=JetyChodipilli&layout=compact&hide_border=true&bg_color=F6F3EC&title_color=15324B&text_color=43525D" alt="Top languages" />

</td>
</tr>
</table>

---

## Live evidence

**BrainServe Connect client demo:**  
https://brain-serve-connect-vercel-demo.vercel.app/

The demo is intentionally sample-data driven. No live database, JWT sign-in, email, OTP, Kafka, Redis or backend export jobs are running behind that public walkthrough.

---

<sub>Java backend engineering · system design · data flows · testing · reliability</sub>
