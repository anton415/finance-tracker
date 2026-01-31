# Definition of Done (MVP)

A feature/issue is "done" when:
- API contract is implemented (controller + DTO + validation)
- Business rules covered by unit tests where meaningful
- Errors are mapped to consistent JSON format (problem details or custom)
- Flyway migration updated if schema changed
- OpenAPI updated automatically via annotations/DTOs (no manual edits)
- Docker local run still works
- CI passes: mvn test + build