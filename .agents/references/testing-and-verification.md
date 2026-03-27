# Testing And Verification

## Default posture

- Prefer integration tests for endpoint behavior, persistence behavior, and contract changes.
- Add unit tests when isolated business logic is substantial enough to justify them.
- Reuse the repository's existing test infrastructure before introducing a new test style.

## High-value integration coverage

- Happy path for the endpoint or handler.
- Validation failures and domain-rule failures.
- Not-found, conflict, and authorization behavior where applicable.
- Serialization, status code, and response-shape assertions for contract changes.
- Persistence effects for write flows.

## Verification checklist

- Build the solution and run the affected tests.
- If OpenAPI is generated, verify that the new contract is visible there.
- For EF Core changes, confirm migration shape and runtime behavior.
- Note any missing automation or unverified risk explicitly.

