---
name: dotnet-api-dos-donts
description: Provide a fast do and don't checklist for .NET backend API work. Use when sanity-checking a design or implementation for common Minimal API, EF Core, validation, error-handling, contract, and verification anti-patterns.
---

# Dotnet API Dos Donts

## Overview

Use this skill for a short pre-flight or post-change sanity check. Focus on catching common mistakes quickly rather than re-explaining full architecture guidance.

## Workflow

1. Identify the change type: contract, feature flow, persistence, validation, or verification.
2. Compare the change against the quick guardrails in [Dos and Don'ts](../../references/dos-and-donts.md).
3. Escalate to `$dotnet-api-best-practices` when the issue is architectural rather than a simple anti-pattern.
4. Escalate to `$dotnet-api-code-review` when the user needs concrete findings on a real diff.

## Output

- Keep the checklist response short and concrete.
- Distinguish must-fix anti-patterns from optional improvements.

## References

- [Dos and Don'ts](../../references/dos-and-donts.md)
- [API Design](../../references/api-design.md)
- [EF Core](../../references/ef-core.md)
