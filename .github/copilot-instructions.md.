# Repository Wide Copilot Instructions

## Project Context
This repository is a full-stack application composed of:
- Frontend: React / TanStack ecosystem
- Backend: FastAPI (Python)
- Database: PostgreSQL
- API Layer: GraphQL (primary contract layer)

The system follows a strict separation of concerns:
- Frontend = UI + client state only
- Backend = business logic, validation, orchestration
- Database = persistence, constraints, indexing
- GraphQL = typed contract between frontend and backend

Do not blur responsibilities across layers.

---

## Architecture Rules
- Do not place business logic in UI components or route handlers
- Backend services own all core logic
- GraphQL resolvers call services, not database directly
- Database access must go through defined query/service layers
- Avoid duplicating logic across frontend/backend

---

## Directory Standards
Follow these conventions when generating or modifying code:

Frontend:
- src/components → reusable UI components
- src/features → domain-specific modules
- src/hooks → custom hooks
- src/lib → shared utilities
- src/types → shared TypeScript types

Backend:
- backend/routes → API route definitions only
- backend/services → business logic
- backend/schemas → request/response models
- backend/db → database models, queries, migrations
- backend/utils → helpers/utilities

GraphQL:
- graphql/schema → type definitions
- graphql/resolvers → resolver logic
- graphql/types → shared contract types

Do not create new top-level folders unless necessary.

---

## Naming Conventions
- Use clear, descriptive names (no abbreviations)
- Components: PascalCase
- Functions/variables: camelCase
- Files: kebab-case or match framework standard
- Database tables: snake_case
- Avoid generic names like `data`, `utils`, `helper`

---

## Code Style and Cleanup
- Remove unused imports, variables, and dead code
- Do not leave commented-out code
- Avoid placeholder or mock logic unless explicitly required
- Prefer small, focused functions
- Extract repeated logic after second real reuse
- Keep components and functions readable and modular

---

## Reuse and Abstraction Rules
- Prefer existing utilities before creating new ones
- Centralize shared logic in `lib`, `services`, or `utils`
- Avoid premature abstraction
- Do not duplicate validation logic across layers unless intentional

---

## API and Data Contracts
- GraphQL is the source of truth for frontend/backend communication
- Maintain strict typing between layers
- When modifying schemas, update all dependent layers
- Validate all external inputs at the backend level

---

## Database Rules
- Use PostgreSQL best practices:
  - Index frequently queried fields
  - Avoid N+1 queries
  - Use joins efficiently
- Do not embed business logic inside raw SQL unless necessary
- Keep migrations clean, incremental, and reversible
- Maintain referential integrity and constraints

---

## Performance Guidelines
- Avoid over-fetching data
- Use pagination for large datasets
- Avoid unnecessary re-renders in frontend
- Keep expensive operations out of request-critical paths

---

## Security Rules
- Never hardcode secrets or credentials
- Use environment variables via config layer
- Validate and sanitize all inputs
- Protect sensitive routes and operations

---

## Testing Standards
- Add tests for core logic and critical paths
- Keep tests near related code or in dedicated test folders
- Cover:
  - Services (backend)
  - Key utilities
  - Critical UI flows (if applicable)

---

## Documentation Standards
- Document non-obvious logic
- Update README or relevant docs when:
  - Adding features
  - Changing architecture
  - Modifying contracts
- Explain why, not just what

---

## Change Management Rules
- Prefer minimal, focused diffs
- Do not refactor unrelated code
- Do not rename files without reason
- Preserve existing patterns unless intentionally improving them
- When changing shared logic, update all dependent code

---

## General Principles
- Write production-ready code, not scaffolding
- Avoid unnecessary complexity
- Prioritize clarity over cleverness
- Keep the codebase clean, consistent, and maintainable
