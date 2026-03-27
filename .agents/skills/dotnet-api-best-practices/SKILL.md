---
name: dotnet-api-best-practices
description: Provide design and implementation guidance for C#/.NET backend APIs. Use before or during non-trivial decisions about Minimal API design, vertical-slice boundaries, validation, error handling, EF Core usage, reliability, or performance.
---

# Dotnet API Best Practices

## Overview

Use this skill to turn broad backend guidance into concrete project-local recommendations. Prefer advice that fits the repository's established patterns instead of generic textbook rules.

## Workflow

1. Inspect the target repository's current API style, slice structure, validation pattern, persistence setup, and test posture.
2. Start from the repository's existing conventions where they are coherent.
3. Give actionable recommendations for contract design, validation, error handling, EF Core usage, and reliability.
4. Call out tradeoffs when a recommendation improves one quality attribute at the expense of another.
5. Point to `$dotnet-api-dos-donts` for quick anti-pattern checks and `$dotnet-api-code-review` for change-specific review.

## Output

- Prefer short, prioritized guidance.
- Separate hard risks from optional improvements.
- Anchor advice in the target repository's actual constraints.

## References

- [API Design](../../references/api-design.md)
- [Errors and Validation](../../references/errors-validation.md)
- [EF Core](../../references/ef-core.md)
- [Reliability and Performance](../../references/reliability-and-performance.md)
- [Testing and Verification](../../references/testing-and-verification.md)
