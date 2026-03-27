---
name: dotnet-api-change-verification
description: Decide and run the right verification for .NET backend API changes. Use after modifying endpoints, handlers, validation, EF Core persistence, OpenAPI metadata, or any runtime behavior where build success alone is not enough.
---

# Dotnet API Change Verification

## Overview

Use this skill to choose the smallest credible verification set for the change while keeping behavior risk visible. Prefer integration-heavy checks for API and persistence changes.

## Workflow

1. Classify the change: contract only, feature flow, persistence, auth, validation, or mixed.
2. Start from the repository's existing build and test commands.
3. Prefer endpoint or persistence integration tests when behavior changed.
4. Add unit tests only when isolated logic is substantial enough to justify them.
5. For contract changes, confirm OpenAPI visibility and serialization behavior.
6. For EF Core changes, check migration shape and runtime persistence behavior.
7. Report what was verified, what was not verified, and the remaining risk.

## Output

- Keep the verification plan proportional to the change.
- Make gaps and unrun checks explicit instead of implying full confidence.

## References

- [Testing and Verification](../../references/testing-and-verification.md)
- [Reliability and Performance](../../references/reliability-and-performance.md)
- [Review Rubric](../../references/review-rubric.md)
