<div align="center">
  <img src="https://github.com/user-attachments/assets/ebc1007f-3a74-4f1a-ab42-047a8ee39967" width="100%" alt="waka code banner" />
</div>

# 👋 Hi, I'm Waddimi Saint-Louis
**Senior Full Stack Engineer | AI & Cloud**

Senior Full Stack Engineer with 5+ years of experience building scalable,
cloud-native, and AI-powered applications for business-critical products.
Strong expertise in React, Next.js, TypeScript, Node.js, Python, PostgreSQL,
microservices, and AWS.
Experienced integrating LLMs, AI APIs, and automation into production systems,
with a solid background in system architecture, cloud infrastructure, CI/CD,
performance optimization, and technical leadership.

---

## 🚀 About Me

- 🧠 Senior Full Stack Engineer focused on system design, scalability, and long-term maintainability.
- 🤖 Building AI into real products: RAG assistants, document classification, agents, and MCP services.
- 🏗️ Experienced building ERP-like platforms, dashboards, and internal business tools.
- 🔍 Strong interest in clean architecture, performance optimization, and backend-driven systems.
- 🤝 Comfortable working directly with product owners and business stakeholders.
- 👥 Active mentor for junior developers through code reviews and technical guidance.

---

## 🤖 AI Engineering

- **LLM Applications:** OpenAI APIs, RAG, document analysis, document classification, natural-language interfaces.
- **AI Agents:** Agent orchestration, tool calling, integrations with Jira, ClickUp, and GitHub for automated code and task workflows.
- **MCP & Agent Skills:** Model Context Protocol, custom MCP services, Agent Skills, reusable agent workflows.
- **AI-Assisted Engineering:** Claude Code for architecture, implementation, debugging, refactoring, code review, and end-to-end feature delivery.

---

## 🧩 Featured Projects

### 🛰️ OwnOrbit — Lead Software Engineer

_Event-driven microservices platform for property rental management · Web + mobile · ~36k LOC TypeScript_

- Designed the system architecture (Clean Architecture, SOLID, per-service data ownership) and built the Node.js/TypeScript services behind an NGINX API Gateway centralizing JWT validation, CORS, and rate limiting.
- Implemented asynchronous inter-service messaging over RabbitMQ with a dead-letter exchange and bounded retries, so a failing consumer degrades one queue instead of taking down the flow — plus real-time chat over WebSockets.
- Modeled the end-to-end rental flow as a state machine with per-actor authorization and an audit timeline, backed by MongoDB partial unique indexes that enforce the concurrency invariants at the database level.
- Developed the responsive web (React 19 + Vite + Tailwind v4) and mobile (React Native + Expo) clients, with role-based portals for owners, tenants, and lawyers.
- Built a pnpm monorepo with shared packages reused across web and mobile, and a 6-stage GitLab CI/CD pipeline including security scanning and rollback.

**Tech:** Node.js · TypeScript · Express · MongoDB · RabbitMQ · WebSockets · Docker · NGINX · React 19 · React Native (Expo) · Vite · Tailwind CSS · pnpm · GitLab CI/CD

[🔗 Live demo](https://owrnorbit-web.onrender.com/#/) · 🔒 Private commercial project — source not public

---

### 📦 StockHex — Inventory Management System with Full Audit Trail
[🔗 Landing page](https://waka-code.github.io/StockHex/) · [💻 Source](https://github.com/waka-code/StockHex)

**Tech:** .NET 8, ASP.NET Core, EF Core 8, SQL Server 2022, React 19, TypeScript, TanStack Query, xUnit + Testcontainers, Playwright, Docker Compose, GitHub Actions

- Built on a single domain invariant: **stock is never edited directly**. The only way to change it is to record a movement, and movement + stock are persisted in one transaction, so history and quantities cannot drift apart. A mistake is never deleted — it is corrected by recording its reverse movement.
- Clean architecture in four layers: Domain with no external dependencies, use cases returning `Result<T>` that never know about HTTP, controllers with no logic, and errors normalized as ProblemDetails (RFC 7807).
- Permission-based authorization: roles are editable data, 31 permissions across 9 modules declared from a single source in code and resolved per request with an invalidatable cache — revoking a permission takes effect immediately, and a guard prevents granting a permission you do not hold yourself.
- Hardened sessions: JWT with rotating refresh tokens stored only as SHA-256, reuse detection that invalidates the whole chain, per-IP rate limiting on `/api/auth`, and immediate lockout of deactivated accounts.
- Optimistic concurrency over `rowversion` with exponential-backoff retries, verified against a real SQL Server in Testcontainers: 25 concurrent movements on the same product end in 25 successes and an exact stock value.
- React 19 + TanStack Query frontend derived from the backend: menu, buttons and routes come from the API's permission catalog, never the role name; filters, search and pagination live in the URL.
- Backed by 201 API tests (xUnit, Testcontainers) and 418 E2E checks in real Chromium with Playwright; CI builds with `-warnaserror` at zero warnings and audits vulnerable dependencies, including transitive ones.
- One-command deploy: `docker compose up -d --build` brings up database, API and frontend, applies migrations and seeds the admin; nginx serves the SPA and proxies `/api` — single origin, no CORS to configure.


---

### 🧠 Nexus Expression Engine — Architect & Sole Engineer

_Business rules engine with an expression language built from scratch · Personal project · 2026_

- Built the full expression language from scratch — lexer with error recovery, recursive-descent parser, AST, evaluator, and static type checker — with no parser generator and zero third-party dependencies in the core.
- Designed a hexagonal modular monolith with module auto-discovery, its dependency rules enforced by executable architecture tests so violations fail the build instead of being caught in review.
- Versioned rules append-only in PostgreSQL, with `xmin` optimistic concurrency and a partial unique index guaranteeing exactly one active version per rule at the database level.
- Exposed a REST API with RFC 7807 problem details and OpenAPI, with the whole stack up via a single `docker compose up`.
- Set up CI running at zero warnings under `TreatWarningsAsErrors`, backed by an xUnit v3 test suite.

**Tech:** C# · .NET 10 · ASP.NET Core Minimal APIs · EF Core 10 · PostgreSQL 17 · pgvector · Docker · xUnit v3 · GitHub Actions

[💻 Source](https://github.com/waka-code/nexus)


---

## 💼 Professional Experience (Highlights)

### 🏢 Millicom — Senior Fullstack Developer

_International telecom: mobile, broadband, and digital services across Latin America · Contract engagement via Zerviz Technologies · March 2026 – Present_

- Delivered high-performance frontend applications with React, Vue.js, and Next.js, improving user experience and cutting load times across key interfaces.
- Built and scaled backend services with Node.js and Ruby on Rails, applying clean architecture principles for maintainability and reliability.
- Designed and optimized REST APIs within a microservices architecture, enabling scalable, modular system growth.
- Integrated multiple third-party services with secure authentication and authorization mechanisms protecting user data.
- Improved database performance by designing and optimizing PostgreSQL schemas and queries for high-traffic operations.
- Reduced API response times and system latency through Redis-based caching strategies.
- Streamlined deployment and release processes with Docker and CI/CD pipelines, improving delivery speed and reliability.

**Tech:** React · Vue.js · Next.js · TypeScript · Node.js · Express · Ruby on Rails · PostgreSQL · Redis · Docker · REST APIs · CI/CD · Tailwind CSS · AWS

### 🏢 Higher Bit Solutions — Senior Fullstack Engineer / Technical Lead
*Custom tech, AI, and automation solutions · Project-Based Contract · Sept 2025 – 2026* 

- Led technical roadmaps and architectural decisions across multiple production systems and client projects.
- Designed and implemented end-to-end solutions with Django, Node.js, React, Next.js, TypeScript, and PostgreSQL.
- Managed and optimized AWS infrastructure (ECS, ECR, RDS, S3, CloudFront, Cognito, VPC, IAM).
- Migrated and restructured the production architectures of Calquen, Hemisferio Norte, and Marfil, splitting staging and production while cutting monthly infrastructure costs with zero client impact.
- Rebuilt the Calquen frontend and key backend components from scratch in one month, fixing production issues and improving the scraper and data-processing pipeline.
- Designed and implemented the Iocupacional architecture and business logic from the ground up, using AI-assisted workflows to accelerate delivery.
- Mentored junior developers, ran code reviews, and established engineering best practices.

### 🏢 ProDoctivity SRL — Senior Fullstack Developer
*Business management and process automation platform · April 2023 – Sept 2026*

- Developed and scaled fullstack features using React, TypeScript, Node.js, Docker, and MongoDB.
- Designed microservices supporting core ERP business processes and backend workflows.
- Built a production-grade RAG-based AI document assistant on OpenAI LLMs, letting users upload documents and query them in natural language.
- Implemented AI-powered document classification that analyzes uploads and assigns the right document type automatically.
- Designed and implemented an independent **MCP service in Rust**, integrated with the Node.js backend to expose application data and services to AI-powered workflows.
- Acted as a technical reference for architecture, implementation decisions, and engineering best practices.
- Supervised and mentored interns through onboarding, code reviews, and continuous feedback.

### 🏢 IMarket — Fullstack Developer (Contract)
*Administrative and accounting management platform · Nov 2024 – May 2025*

- Developed RESTful APIs and implemented business logic and validations.
- Designed database models, migrations, and optimized queries, improving performance in critical operations.
- Built reusable frontend components and responsive interfaces with Angular and TypeScript.

### 🏢 Freelance Projects — Fullstack / Web Developer
*SPAs, PWAs, and fullstack systems · Nov 2020 – Apr 2023*

- Delivered multiple freelance projects, turning UI/UX designs into production-ready applications.
- Integrated frontend and backend systems through REST APIs.
- Ensured performance, accessibility, and cross-browser compatibility.

---

## 🛠️ Core Tech Stack

### Frontend
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-06B6D4?logo=tailwindcss&logoColor=white)
![MUI](https://img.shields.io/badge/MUI-007FFF?logo=mui&logoColor=white)

### Backend
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?logo=c-sharp&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?logo=swagger&logoColor=black)

### AI
![OpenAI](https://img.shields.io/badge/OpenAI%20API-412991)
![Claude Code](https://img.shields.io/badge/Claude%20Code-D97757?logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/Model%20Context%20Protocol-000000?logo=modelcontextprotocol&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-1A7F64)

### Databases
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?logo=microsoftsqlserver&logoColor=white)

### Architecture & DevOps
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?logo=terraform&logoColor=white)
![NGINX](https://img.shields.io/badge/NGINX-009639?logo=nginx&logoColor=white)
![CI/CD](https://img.shields.io/badge/CI%2FCD-4285F4?logo=githubactions&logoColor=white)

### Testing & Observability
![Jest](https://img.shields.io/badge/Jest-C21325?logo=jest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-45ba4b?logo=playwright&logoColor=white)
![PostHog](https://img.shields.io/badge/PostHog-F54E00?logo=posthog&logoColor=white)

---

## 🎓 Education & Certifications

- 🎓 **Systems Engineering** — Universidad Tecnológica de Santiago (UTESA), 2017–2024
- ☁️ AWS Certified Cloud Practitioner — *in progress*
- 🤖 Claude Code in Action — Anthropic Education
- 🤖 Building with the Claude API — Anthropic Education
- 🤖 Introduction to Model Context Protocol — Anthropic Education
- 🤖 Introduction to Agent Skills — Anthropic Education

---

## 📚 Currently Exploring

- Advanced AWS architectures and infrastructure automation
- Agentic workflows: MCP services, tool calling, and multi-agent orchestration at scale
- Rust for performance-critical services

---

## 🌍 Languages

Spanish (Native) · English (B1, technical communication) · French (A1)

---

## 📫 Contact

- 📄 [Resume](https://acortar.link/OWfefY)
- 🌐 [Portfolio](https://waka-code.github.io/CVPortfolio)
- 💼 [LinkedIn](https://www.linkedin.com/in/waddimi-saint-louis-b49424230)
- 📧 Email: shenryvladimil@gmail.com
