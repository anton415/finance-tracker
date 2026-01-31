# API Conventions (MVP)

- Base path: /api
- JSON only
- Dates: ISO-8601 LocalDate (yyyy-MM-dd)
- Money: BigDecimal with scale=2 (validation), currency fixed ("RUB") in MVP
- IDs: long

## Error format
Use a single consistent JSON error shape for:
- validation errors
- not found
- business rule violations
- unexpected errors