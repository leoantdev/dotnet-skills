# .NET API Skills Library

This repository stores reusable Codex skills for C#/.NET backend APIs. Canonical skills live in `.agents/skills/`. Shared guidance lives in `.agents/references/`.

## Defaults

- Assume ASP.NET Core Minimal APIs on .NET 10 unless the target repository says otherwise.
- Prefer vertical slices with feature-local endpoints, request models, response models, validators, and handlers.
- Assume EF Core first for persistence changes.
- Treat OpenAPI/Swagger visibility as part of the API contract.
- Prefer integration-heavy verification for behavior changes.

## Skill Routing

- Use `$dotnet-api-feature-slice` for endpoint, DTO, validator, handler, and feature-flow changes.
- Use `$efcore-schema-change` for entity, configuration, migration, query-shape, and transaction changes.
- Use `$openapi-contract-sync` when request or response contracts, status codes, auth requirements, or endpoint metadata change.
- Use `$dotnet-api-change-verification` after runtime, persistence, or contract changes.
- Use `$dotnet-api-best-practices` before non-trivial API design or persistence decisions.
- Use `$dotnet-api-dos-donts` for a fast anti-pattern check before landing a design or implementation.
- Use `$dotnet-api-code-review` when the user asks for review or when a substantial backend change is ready for handoff.

## Authoring Rules

- Keep each skill narrowly scoped.
- Keep `SKILL.md` frontmatter limited to `name` and `description`.
- Treat `description` as the trigger contract. State what the skill does and when to use it.
- Keep `SKILL.md` bodies concise. Move detailed guidance into `.agents/references/` and link to it directly.
- Add scripts only when the same deterministic mechanics would otherwise be rediscovered repeatedly.
- Keep `agents/openai.yaml` aligned with the skill name, purpose, and default prompt.
- When adding or revising review guidance, preserve a production-risk-first review style: findings first, ordered by severity, with file references.

## Validation

- Validate every changed skill before landing it.
- If the Codex skill validator is available, run it against each changed skill directory.
- If the validator is unavailable, manually verify folder naming, frontmatter validity, relative links, and `agents/openai.yaml` coherence.

