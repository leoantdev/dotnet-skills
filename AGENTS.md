# .NET API Skills

## Defaults

- Assume .NET 10, ASP.NET Core Minimal APIs, vertical slices, and EF Core first unless the target repository says otherwise.
- Treat OpenAPI as part of the contract and prefer integration-heavy verification for behavior changes.

## Skill Routing

- Use `$dotnet-api-feature-slice` for endpoint, DTO, validation, handler, or feature-flow changes.
- Use `$efcore-schema-change` for entity, configuration, migration, query, or transaction changes.
- Use `$openapi-contract-sync` for route, contract, status code, auth, or metadata changes.
- Use `$dotnet-api-change-verification` after runtime, persistence, or contract changes.
- Use `$dotnet-api-best-practices` before non-trivial API or persistence decisions.
- Use `$dotnet-api-dos-donts` for a quick anti-pattern check.
- Use `$dotnet-api-code-review` for review requests or substantial backend diffs.

## Skill Rules

- Keep skills narrow.
- Keep `SKILL.md` frontmatter to `name` and `description`; use `description` as the trigger contract.
- Keep bodies concise, move shared detail to `.agents/references/`, and add scripts only for repeated deterministic work.

## Validation

- Validate changed skills with the bundled validator when available; otherwise manually check frontmatter, links, folder naming, and `agents/openai.yaml`.
