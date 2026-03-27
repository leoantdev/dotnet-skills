# Errors And Validation

## Validation

- Validate requests at the boundary.
- Reuse the repository's existing validation mechanism when one exists.
- Keep validation rules close to the request model or slice.
- Distinguish malformed input, business-rule rejection, missing resources, and authorization failures.

## Error responses

- Prefer a consistent `ProblemDetails` shape or the repository's existing error contract.
- Return field-level validation details for invalid requests.
- Avoid leaking stack traces, connection details, or provider-specific exception messages.
- Map known failures to stable status codes instead of falling back to generic `500` responses.

## Reliability

- Pass `CancellationToken` through async operations that support it.
- Fail fast on invalid input before touching persistence.
- Log enough context to diagnose failures without duplicating the entire request payload by default.

