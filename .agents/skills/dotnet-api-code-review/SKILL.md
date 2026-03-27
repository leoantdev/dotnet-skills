---
name: dotnet-api-code-review
description: Review C#/.NET backend API changes with a production-risk-first mindset. Use when the user asks for a review or when a diff touches Minimal APIs, contracts, validation, EF Core persistence, migrations, authorization, or backend reliability.
---

# Dotnet API Code Review

## Overview

Use this skill to review backend changes for correctness and operational risk first. Focus on bugs, regressions, contract breaks, data risks, and missing verification before style comments.

## Workflow

1. Inspect the actual diff and the surrounding slice or persistence context before judging the change.
2. Prioritize findings that can break runtime behavior, client contracts, data correctness, or rollout safety.
3. Check request and response contracts, validation, auth behavior, EF Core query and write safety, and migration impact.
4. Check whether the verification performed matches the risk of the change.
5. Use the shared review rubric to keep severity and output style consistent.

## Output

- Put findings first.
- Order findings by severity.
- Cite concrete file references.
- Mention residual risks or testing gaps when there are no findings.
- Keep style or naming comments secondary unless they create real maintenance or defect risk.

## References

- [Review Rubric](../../references/review-rubric.md)
- [API Design](../../references/api-design.md)
- [Errors and Validation](../../references/errors-validation.md)
- [EF Core](../../references/ef-core.md)
- [Testing and Verification](../../references/testing-and-verification.md)
