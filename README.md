# Myles B. Scott

**Backend engineer working on financial systems and applied AI.**

I'm a Software Engineer III at USAA, where I lead backend development on the
platform that replaced our legacy batch accounting with a real-time,
event-driven architecture: Java and Spring Boot APIs, Apache Kafka for bulk
payload processing, and Oracle Cloud GL as the system of record. I was the
team's first API engineer and established our API development standards.

Lately most of my work is AI in regulated environments: integrating
open-source LLMs into runtime accounting services and CI/CD pipelines, a
multi-agent development framework modeling a full scrum team, and a read-only
MCP server over our general ledger APIs that gives LLM tooling scoped query
access with no write path to the ledger.

The projects below are where I build in the same problem space on my own time.

**Java · Spring Boot · Apache Kafka · Python · FastAPI · TypeScript · React · React Native · PostgreSQL · Docker · OpenShift**

## Selected work

### [Arbiter](https://github.com/mscott9160-web/arbiter)

Teams adopting LLMs usually find out what inference cost them when the invoice
arrives. Arbiter sits in front of the call: it classifies each request, selects
a model tier, checks the cache, and writes an auditable per-request entry to a
cost ledger.

**Java 21 · Spring Boot · FastAPI · PostgreSQL · Redis**

A Java 21 Spring Boot gateway with a Python FastAPI classifier sidecar behind a
versioned HTTP contract. Cost calculation is fail-closed and done in
`BigDecimal`, so an unpriced model is rejected rather than silently billed at
zero, alongside tenant-scoped caching and a semantic-cache deny-list that
records an auditable reason for every skip. In active development; the
contracts and ledger event schema are public.

### [Cash Flow Simulator](https://github.com/mscott9160-web/cash-flow-simulator)

Daily cash-flow projection for people who have enough money across the month
but still risk going negative on a specific day. Projects daily balances over
a 90-day horizon, models real settlement behavior including pay-cycle timing
and weekend and federal holiday shifts, and returns a single explainable
schedule change, searching only obligations that are genuinely movable.

**Python · FastAPI · Pydantic · React · TypeScript · Vite · PostgreSQL · Expo**

A pure-Python projection and optimizer core with no framework or database
dependencies, consumed by both web and mobile clients through one versioned
API contract so financial rules are never reimplemented per platform. 44
backend tests plus Playwright end-to-end coverage.

### [Fade Society](https://github.com/mscott9160-web/fade-society)

Multi-role barber marketplace and booking platform serving customers,
barbers, studio owners, and platform administrators.

**Expo · React Native · TypeScript · Expo Router · Supabase · PostgreSQL · Vitest**

Typed domain models behind repository interfaces and an end-to-end booking
flow with explicit state-machine status transitions enforced in typed domain
logic. The server-authoritative write path is designed as a transactional
PostgreSQL routine with an idempotency key; the app currently runs on local
state, with that migration in the repo as the documented path to production.

### [Sneaker Signal](https://github.com/mscott9160-web/sneaker-signal)

Verified US sneaker release intelligence: release tracking, retailer
availability, and source verification over a Supabase-backed data foundation.

**React · TypeScript · Vite · Supabase · PostgreSQL**

A relational release model with a source hierarchy, editorial verification
states, and row-level security policies.

## What I work on

- Backend and API design in regulated financial systems
- Event-driven architecture and high-volume transaction processing
- LLM integration, agent frameworks, and MCP in production contexts
- Domain modeling, data quality, and explicit system boundaries

[Portfolio](https://myles-scott-portfolio.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/mylesbscott/)
