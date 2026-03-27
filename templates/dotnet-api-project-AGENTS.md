# .NET Backend API

This repository uses shared Codex skills for C#/.NET backend API work.

## Project Defaults

- Target framework: replace with the actual project baseline.
- API style: Minimal APIs unless this repository already standardizes on controllers.
- Architecture: prefer the repository's existing vertical-slice or feature-first structure.
- Persistence: replace with the actual data-access approach if it differs from EF Core.
- API contract visibility: keep OpenAPI and runtime behavior aligned.

## Required Skills

- Use `$dotnet-api-feature-slice` for endpoint, DTO, validator, handler, and feature-flow changes.
- Use `$efcore-schema-change` for entity, configuration, migration, query-shape, and transaction changes.
- Use `$openapi-contract-sync` when request or response contracts, status codes, auth requirements, or endpoint metadata change.
- Use `$dotnet-api-change-verification` after runtime, persistence, or contract changes.
- Use `$dotnet-api-best-practices` before non-trivial API design or persistence decisions.
- Use `$dotnet-api-dos-donts` for a quick anti-pattern pass before landing a change.
- Use `$dotnet-api-code-review` when the user asks for review or when a substantial backend change is ready for handoff.

## Local Commands

Replace these with the repository's real commands.

- Build: `dotnet build`
- Test: `dotnet test`
- Run: `dotnet run`
- Format: `dotnet format`

## Review And Verification Rules

- Treat build success as necessary but not sufficient for runtime changes.
- Prefer integration tests for endpoint, persistence, and contract changes.
- Call out unverified migration, transaction, or serialization risk explicitly.
- Keep review output findings-first and ordered by severity.

## Project-Specific Overrides

Replace this section with any repository-specific rules, such as:

- controller-first routing instead of Minimal APIs
- MediatR or another request pipeline
- PostgreSQL, SQL Server, or another provider-specific migration guidance
- auth or tenant rules
- logging or observability requirements

