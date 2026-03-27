# API Design

## Default posture

- Prefer Minimal APIs and route groups over controller-first designs unless the target repository already standardizes on controllers.
- Keep each slice centered on one business capability.
- Define request and response DTOs explicitly. Do not expose EF Core entities directly on the wire.

## Endpoint design

- Use resource-oriented routes with stable nouns.
- Make route, query, and body responsibilities obvious.
- Use consistent pagination, filtering, and sorting patterns across related endpoints.
- Return precise status codes instead of a generic `200` or `500`.
- Use typed results or clear response metadata so the success and failure contract stays visible.

## Contract hygiene

- Treat nullability, default values, enum serialization, and date or time formats as contract decisions.
- Keep backward compatibility unless the task explicitly allows a breaking change.
- When a contract changes, update OpenAPI metadata and add verification for serialization and validation behavior.

## Slice boundaries

- Keep transport concerns in the endpoint layer.
- Keep orchestration and business decisions in a handler or feature service.
- Keep persistence concerns behind the slice boundary, even when the code remains in the same project.

