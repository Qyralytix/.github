# Qyralytix

**Internal analytical intelligence for modern engineering teams.**

Qyralytix is a secure, read-only AI system that helps internal teams ask clear questions about their operational data and receive **verifiable, auditable answers backed by real evidence**.

This organization contains the systems, services, and tooling that make Qyralytix possible.

---

## What Qyralytix Is

Qyralytix is **not a chatbot**.  
It is **not “ChatGPT for your company.”**

Qyralytix is an **internal analytical layer** designed to sit safely on top of production data and help teams understand:

- What is happening  
- Why it is happening  
- What changed  

The core promise is simple:

> **If Qyralytix gives you an answer, it can show you exactly where that answer came from.**

---

## The Problem We’re Solving

Inside most companies today:

- Critical data lives in Postgres databases  
- Understanding that data requires SQL, dashboards, or context-switching  
- Non-technical teams rely on engineers for answers  
- Engineers waste time answering repeat questions  
- Existing AI tools hallucinate, overreach, or can’t be trusted  

Qyralytix exists to **reduce friction between people and their own data** — without sacrificing safety, correctness, or control.

---

## Core Principles

Everything in this organization follows these rules:

### 1. Read-only by default
Qyralytix never mutates customer data.  
**No writes. No side effects.**

### 2. Evidence-first, not opinion-first
Every answer is grounded in retrieved facts.  
Explanations always reference sources.

### 3. Scoped access
Qyralytix can only see what the user is allowed to see.

### 4. Auditability
Every query, generated SQL, and response is logged and inspectable.

### 5. Boring is good
Predictable, conservative behavior is a feature — not a bug.

---

## What We’re Building (MVP Scope)

The MVP focuses on **Postgres-only analytical intelligence**.

### Supported capabilities

- Connect to a Postgres database (read-only)
- Introspect schema and metadata
- Understand natural language analytical questions
- Generate and validate safe SQL
- Execute bounded queries
- Return human-readable explanations
- Show evidence and query lineage
- Maintain full audit logs

### Explicitly out of scope (for now)

- Writes or actions
- Cross-database joins
- Vector search over documents
- Autonomous agents
- Model training on customer data

---

## High-Level Architecture

Qyralytix is built as a **modular backend system** with clear separation of concerns:

- Authentication & Identity
- Data Source Management
- Schema Introspection & Metadata
- Query Understanding & Intent Classification
- Safe SQL Generation & Validation
- Data Retrieval & Evidence Normalization
- Explanation & Response Generation
- Audit Logging & Guardrails

Each module is independently testable and designed to **fail safely**.

---

## Technology Stack (Current)

- **Backend:** FastAPI (Python)
- **Internal Database:** Postgres
- **Customer Data Source:** Postgres (read-only)
- **LLMs:** Inference-only (no training on customer data)
- **Infrastructure:** Docker-based, environment-isolated
- **Frontend:** Minimal, evidence-first UI (Next.js)

The stack is chosen for **clarity, reliability, and long-term maintainability** — not hype.

---

## Repository Structure (Planned)

This organization will host multiple repositories, including but not limited to:

- `qyralytix-api` — Core backend service
- `qyralytix-frontend` — Internal web interface
- `qyralytix-connectors` — Data source connectors
- `qyralytix-docs` — Architecture & product documentation
- `qyralytix-infra` — Deployment and infrastructure configs

Each repository will have **clear ownership, scope, and documentation**.

---

## Security & Trust Model

Qyralytix is built with **enterprise trust** in mind:

- Encrypted credentials at rest
- Explicit table allow-lists
- Hard query limits and timeouts
- SQL validation and explain plans
- Full request and response auditing

Security is treated as a **first-class feature**, not a checkbox.

---

## Who This Is For

Qyralytix is designed for:

- Engineering teams
- Operations teams
- Product teams
- Finance and support teams in data-heavy organizations
- Anyone who needs answers — without waiting on SQL or dashboards

---

## Status

Qyralytix is currently in **active development**.

The focus right now is **correctness, safety, and architectural clarity** — not feature breadth.

---

## Philosophy

This organization is built with a **long-term mindset**.

We value:

- Clear reasoning over clever hacks
- Explicit constraints over hidden magic
- Systems that explain themselves

If you believe internal tools should be **trusted, not just impressive**, you’re in the right place.
