---
name: dotnet-api-feature-slice
description: Plan and implement ASP.NET Core Minimal API changes in vertical slices. Use when adding or changing endpoints, route groups, request or response DTOs, validators, handlers, feature-local services, or feature-flow logic in C#/.NET backend APIs.
---

# Dotnet API Feature Slice

## Overview

Use this skill to add or revise a backend API feature without smearing concerns across the codebase. Keep the change centered on a single slice and preserve a clear transport, business, and persistence flow.

## Workflow

1. Inspect the existing route-group and slice pattern before introducing new structure.
2. Define the contract first: route, request shape, response shape, status codes, auth requirements, and validation behavior.
3. Keep endpoint code thin. Put orchestration and business rules in a handler or feature service instead of the route lambda.
4. Keep DTOs and validation feature-local. Do not expose persistence entities directly.
5. If the feature requires schema, query-shape, or transaction changes, use [EF Core](../../references/ef-core.md) and hand off to `$efcore-schema-change`.
6. If the public contract changes, use [API Design](../../references/api-design.md) and hand off to `$openapi-contract-sync`.
7. After implementation, use [Testing and Verification](../../references/testing-and-verification.md) and hand off to `$dotnet-api-change-verification`.

## Output

- Keep the slice coherent and minimal.
- Make contracts and failure cases explicit.
- Call out follow-on tasks when schema, OpenAPI, or verification work is required.

## References

- [API Design](../../references/api-design.md)
- [Errors and Validation](../../references/errors-validation.md)
- [EF Core](../../references/ef-core.md)
- [Testing and Verification](../../references/testing-and-verification.md)
