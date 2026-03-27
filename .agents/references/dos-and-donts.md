# Dos And Don'ts

## Do

- Keep API contracts explicit and stable.
- Keep slices cohesive around one feature.
- Validate requests before mutating state.
- Keep EF Core modeling and query behavior intentional.
- Verify contract and persistence changes with integration-focused checks.

## Don't

- Do not return EF entities directly from endpoints.
- Do not hide business rules in endpoint lambdas.
- Do not trust generated migrations without review.
- Do not leave status codes, error shapes, or auth requirements implied.
- Do not treat a successful build as sufficient verification for API behavior changes.

