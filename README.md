# .NET API Agent Skills

Reusable Codex skills for C#/.NET backend APIs.

This repository is opinionated toward:

- ASP.NET Core Minimal APIs
- vertical-slice organization
- EF Core first
- OpenAPI-aware API design
- integration-heavy verification
- production-risk-first code review

## Repository Layout

```text
.
├── AGENTS.md
├── README.md
├── .agents/
│   ├── references/
│   └── skills/
└── templates/
    └── dotnet-api-project-AGENTS.md
```

- `AGENTS.md`: instructions for working on this repository itself
- `.agents/skills/`: the canonical skill definitions
- `.agents/references/`: shared guidance linked from multiple skills
- `templates/dotnet-api-project-AGENTS.md`: a starter `AGENTS.md` for downstream .NET API repos

## Skill Catalog

- `$dotnet-api-feature-slice`
  - Add or revise Minimal API feature slices, endpoints, DTOs, validators, and handlers.
- `$efcore-schema-change`
  - Handle EF Core entities, configuration, queries, migrations, and transaction-sensitive persistence work.
- `$openapi-contract-sync`
  - Keep API behavior and OpenAPI metadata aligned.
- `$dotnet-api-change-verification`
  - Choose the right verification plan for backend API changes.
- `$dotnet-api-best-practices`
  - Apply .NET API design, reliability, EF Core, and validation guidance.
- `$dotnet-api-dos-donts`
  - Run a quick anti-pattern check on a design or implementation.
- `$dotnet-api-code-review`
  - Review backend diffs with a correctness and production-risk-first lens.

## Using These Skills In Another Repository

1. Copy this repository's `.agents/skills/` directory into the target repository's `.agents/skills/`, or vendor the skills you want.
2. Copy `templates/dotnet-api-project-AGENTS.md` into the target repository root as `AGENTS.md`.
3. Replace placeholder commands and project-specific assumptions in that template.
4. Keep only the routing rules that match the target repository's actual stack and workflow.

## Authoring Principles

- Keep each skill narrowly scoped.
- Put trigger conditions in `SKILL.md` frontmatter `description`.
- Keep `SKILL.md` concise and procedural.
- Put shared detail in `.agents/references/`.
- Add scripts only for repeated deterministic work.
- Keep review guidance focused on correctness, regressions, contracts, persistence, and verification gaps before style.

## Notes

- The skills in this repository are written for Codex-style discovery under `.agents/skills/`.
- The bundled validator from the upstream skill-creator tooling requires `PyYAML`. If it is unavailable, validate frontmatter and metadata manually.
