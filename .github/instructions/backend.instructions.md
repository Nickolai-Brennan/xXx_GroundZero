# Backend Instructions (FastAPI)

## Purpose
Ensure clean, modular, and scalable backend code.

---

## Structure
- Routes → API endpoints only
- Services → business logic
- Schemas → data validation (Pydantic)
- Models → database structure

---

## Rules
- Keep endpoints thin
- Move logic into services
- Validate all inputs
- Return structured responses

---

## Do NOT
- Mix business logic into routes
- Duplicate validation logic
- Write large monolithic functions

---

## Error Handling
- Use clear error responses
- Do not silently fail
- Handle edge cases explicitly

---

## Performance
- Avoid redundant queries
- Keep database calls efficient
- Use async where appropriate

---

## Naming
- Use clear, consistent naming
- Keep endpoints predictable
- Align with GraphQL where applicable

---

## Output Expectations
- Clean API structure
- Proper validation
- Modular services
- Maintainable code
