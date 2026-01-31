# Package structure (MVP)

## Style
Package-by-feature.

Base package: com.anton415.financetracker

## Features
- account
- category
- transaction
- transfer
- summary
- common (config, error handling, shared utils)

## Layer rules
- domain: JPA entities + enums only
- api: controllers + DTOs only (no entities exposed)
- service: business logic + transactions
- repo: Spring Data repositories only
- common/error: global exception handling + error DTO