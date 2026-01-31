# MVP Scope — Personal Finance / Portfolio Tracker (single-tenant)

## Goal
Learning + portfolio project. I write code myself, using Codex for explanations and incremental reviews (no “generate everything at once”).

## In scope (MVP)
### Domain
- Account
- Category (INCOME/EXPENSE)
- Transaction (INCOME/EXPENSE)
- Transfer (between accounts)

### API
CRUD:
- /api/accounts
- /api/categories
- /api/transactions
- /api/transfers

Summary:
- GET /api/summary/balances
- GET /api/summary/cashflow?from=&to=

### Tech
- Postgres + Flyway
- Spring Boot, JPA, Validation
- OpenAPI/Swagger (springdoc)
- Dockerfile + docker-compose (local run)
- GitHub Actions CI: build + tests

### Demo mode
- Seed demo data via Flyway migration V2__demo_seed.sql
- Demo write access enabled, with minimal abuse protection (payload limits, safe defaults).

## Out of scope (explicitly NOT in MVP)
- Auth/users/roles, multi-tenant
- Budgeting, goals, recurring transactions
- Import/export (CSV/OFX), bank integrations
- Multi-currency conversions, FX rates
- Investments/positions, taxes, commissions
- Complex accounting/reconciliation, audit logs, soft delete
- Frontend UI
- Full integration tests (Testcontainers) — planned later

## MVP success criteria
- Clean domain model + CRUD + summary endpoints
- Validations + consistent error responses
- Reproducible local run via Docker
- CI passes on every PR
- Recruiter can try write operations in demo mode without breaking the app