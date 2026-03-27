# Reliability And Performance

## Reliability

- Keep async flows end to end.
- Flow cancellation where supported.
- Avoid hidden retries unless the repository already has a retry policy.
- Make external calls time-bound and failure-aware.

## Performance

- Avoid loading more columns or rows than the endpoint needs.
- Page collection endpoints unless the business case is truly bounded.
- Prefer projection over materializing large tracked graphs.
- Be careful with per-item database calls inside loops.

## Observability

- Keep logs structured and useful for request tracing.
- Include identifiers that help correlate a failing operation.
- Avoid noisy logs on expected validation failures unless the target repository requires them.

