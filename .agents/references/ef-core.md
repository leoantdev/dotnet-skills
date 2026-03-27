# EF Core

## Modeling

- Keep entities persistence-focused. Do not reuse them as API contracts.
- Prefer explicit configuration through `IEntityTypeConfiguration<T>` or the repository's established equivalent.
- Configure keys, lengths, indexes, relationships, delete behavior, and conversions intentionally.

## Querying

- Use `AsNoTracking()` for read-only flows unless tracking is required.
- Project to DTOs close to the query to avoid over-fetching.
- Watch for N+1 queries, accidental client evaluation, and unbounded result sets.
- Load related data intentionally rather than relying on implicit navigation access.

## Writing

- Keep write flows explicit about transactional boundaries.
- Use concurrency tokens or equivalent checks when concurrent updates matter.
- Avoid hidden side effects in `SaveChanges` hooks unless the repository already relies on them.

## Migrations

- Review the generated migration before trusting it.
- Confirm column nullability, defaults, indexes, renamed objects, and data movement behavior.
- Flag destructive or backfill-heavy migrations clearly so the target repository can plan rollout safely.

