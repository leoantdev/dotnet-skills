# Review Rubric

## Severity

- High: likely production bug, data corruption risk, security issue, breaking API contract, or missing verification for a risky change.
- Medium: correctness edge case, migration or transaction risk, performance problem, or maintainability issue likely to cause defects.
- Low: minor robustness or clarity issue with limited immediate risk.

## Review priorities

- Check behavior before style.
- Check contracts before naming polish.
- Check persistence and transaction safety before internal refactors.
- Check missing tests when behavior, schema, or contracts changed.

## Review output

- Put findings first.
- Order findings by severity.
- Include concrete file references.
- State residual risks or testing gaps when no findings are present.

