# Audit Model

The Dream Loop should stay observable and rollback-friendly.

## Required Outputs

Nightly consolidation should produce a report that answers:

- what was read
- what changed
- what was promoted
- what was rejected
- what was archived
- what was rolled back or left for follow-up

## Retrieval Rule

Do not read full `ACTIVE.md` and `LEARNINGS.md` by default.

The consolidation pass should read only the minimal slices needed to resolve the current inbox and the affected memory entries.

## Required Artifacts

Use these artifacts in v2:

- `ARCHIVE/` for removed or expired content
- a timestamped nightly report
- preserved source ids
- rollback notes for anything that was reversed or superseded

## Hard Safety Rule

`AGENTS.md` must never be rewritten automatically.

If a consolidation pass believes a rule belongs in Policy, it should produce a proposal, not a direct write.
