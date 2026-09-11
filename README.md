# Myles B. Scott

**Backend engineer working on financial systems and applied AI.**

I'm a Software Engineer III at USAA, where I lead backend development on the platform that replaced our legacy batch accounting with a real-time, event-driven architecture — Java and Spring Boot APIs, Apache Kafka for bulk payload processing, and Oracle Cloud GL as the system of record. I was the team's first API engineer and established our API development standards.

Lately most of my work is AI in regulated environments: integrating open-source LLMs into runtime accounting services and CI/CD pipelines, a multi-agent development framework modeling a full scrum team, and a read-only MCP server over our general ledger APIs that gives LLM tooling scoped query access with no write path to the ledger.

The projects below are where I build in the same problem space on my own time.

**Java · Spring Boot · Apache Kafka · Python · FastAPI · TypeScript · React · React Native · PostgreSQL · Docker · OpenShift**

## Selected work

### [Cash Flow Simulator](https://github.com/mscott9160-web/cash-flow-simulator)

Daily cash-flow projection for people who have enough money across the month but still risk going negative on a specific day. Projects daily balances over a 90-day horizon, models real settlement behavior including pay-cycle timing and weekend and federal holiday shifts, and returns a single explainable schedule change — searching only obligations that are genuinely movable.

**Python · FastAPI · Pydantic · React · TypeScript · Vite · PostgreSQL · Expo**

A pure-Python projection and optimizer core with no framework or database dependencies, consumed by both web and mobile clients through one versioned API contract so financial rules are never reimplemented per platform. 38 backend tests plus Playwright end-to-end coverage.

### [Fade Society](https://github.com/mscott9160-web/fade-society)

Multi-role barber marketplace and booking platform serving customers, barbers, studio owners, and platform administrators.

**Expo · React Native · TypeScript · Expo Router · Supabase · PostgreSQL · Vitest**

Typed domain models behind repository interfaces, an end-to-end booking flow with state-machine status transitions, and double-booking protection backed by a transactional PostgreSQL RPC. Currently a demo and architecture foundation with a documented path to server-authoritative operations.

### [Sneaker Signal](https://github.com/mscott9160-web/sneaker-signal)

Verified US sneaker release intelligence — release tracking, retailer availability, and source verification over a Supabase-backed data foundation.

**React · TypeScript · Vite · Supabase · PostgreSQL**

A relational release model with a source hierarchy, editorial verification states, and row-level security policies.

## What I work on

- Backend and API design in regulated financial systems
- Event-driven architecture and high-volume transaction processing
- LLM integration, agent frameworks, and MCP in production contexts
- Domain modeling, data quality, and explicit system boundaries

[LinkedIn](https://www.linkedin.com/in/mylesbscott/)
