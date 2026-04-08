# Scope Model

## v2 Current Model

The repo standardizes on three memory scopes:

- `global` for cross-project patterns
- `repo` for project-specific memory
- `thread` for short-lived session context

This keeps the system focused on the smallest scope that can hold a useful signal.

## Scope Roles

- `global` is the broadest reusable layer and should stay stable
- `repo` captures project-local memory that should not leak into other repos
- `thread` stays narrow and transient, and should be the first place to discard stale context

## Scope Rules

- Prefer the narrowest scope that can answer the current task
- Do not expand a lookup to full memory files if a smaller slice is enough
- Do not turn thread context into policy
- Policy belongs to human-approved `AGENTS.md`, not memory scopes

## Why This Matters

This v2 model keeps retrieval cheap and reduces accidental context bloat while still supporting long-term learning through `LEARNINGS.md`.
