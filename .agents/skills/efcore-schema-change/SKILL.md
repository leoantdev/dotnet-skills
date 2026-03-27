---
name: efcore-schema-change
description: Plan and implement EF Core model, query, and schema changes for .NET backend APIs. Use when updating entities, DbContext configuration, relationships, indexes, migrations, write flows, query shape, or transactional behavior.
---

# EF Core Schema Change

## Overview

Use this skill when persistence changes are part of the feature, not an afterthought. Keep entity modeling, migration safety, query behavior, and write consistency explicit.

## Workflow

1. Inspect the existing persistence pattern, provider, entity configuration style, and migration history before changing the model.
2. Define the intended schema or query-shape outcome before editing entities or generating migrations.
3. Make modeling decisions explicit: nullability, key shape, lengths, indexes, delete behavior, conversions, and concurrency handling.
4. Review reads for projection, tracking mode, navigation loading, and bounded result sets.
5. Review writes for transaction boundaries, concurrency, and side effects around `SaveChanges`.
6. Review generated migrations instead of trusting them blindly. Flag destructive operations, backfills, or rename-sensitive changes.
7. Coordinate with `$openapi-contract-sync` when persistence changes alter the public contract, and finish with `$dotnet-api-change-verification`.

## Output

- Keep schema and query intent obvious in the implementation.
- Call out migration and rollout risks explicitly.
- Point to missing verification when database behavior cannot be confirmed locally.

## References

- [EF Core](../../references/ef-core.md)
- [Reliability and Performance](../../references/reliability-and-performance.md)
- [Testing and Verification](../../references/testing-and-verification.md)
