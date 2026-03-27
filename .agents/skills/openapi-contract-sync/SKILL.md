---
name: openapi-contract-sync
description: Keep ASP.NET Core API contracts and OpenAPI metadata in sync with implementation changes. Use when routes, request or response DTOs, status codes, auth requirements, validation behavior, summaries, tags, or other endpoint metadata change.
---

# OpenAPI Contract Sync

## Overview

Use this skill when the implementation changed in a way that clients can observe. Treat OpenAPI visibility as part of the contract, not optional documentation.

## Workflow

1. Identify the externally visible change: route, input shape, output shape, status codes, auth requirements, content type, or pagination behavior.
2. Update endpoint metadata so the generated contract matches reality.
3. Check that success, validation, not-found, conflict, and authorization cases are represented where relevant.
4. Verify serialization-sensitive changes such as enum shape, nullability, defaults, and date or time formats.
5. Coordinate with `$dotnet-api-feature-slice` for feature-flow changes and `$efcore-schema-change` for persistence-driven contract changes.
6. Finish with `$dotnet-api-change-verification` so the contract and runtime behavior are both checked.

## Output

- Keep API metadata aligned with runtime behavior.
- Call out breaking changes and client-visible behavior changes explicitly.

## References

- [API Design](../../references/api-design.md)
- [Errors and Validation](../../references/errors-validation.md)
- [Testing and Verification](../../references/testing-and-verification.md)
