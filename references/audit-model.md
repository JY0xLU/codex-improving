# Audit Model

The Dream Loop should be observable.

## Required Outputs

Nightly consolidation should produce a report that answers:

- what files were read
- what changed
- what was promoted
- what was rejected
- what was archived
- what still needs cleanup

## Required Artifacts

Use these artifacts in v1:

- `ARCHIVE/` for removed or expired content
- a timestamped nightly report
- source ids preserved during promotion

## Hard Safety Rule

`AGENTS.md` must never be rewritten automatically.

If a consolidation pass believes a rule belongs in `AGENTS.md`, it should produce a proposal, not a direct write.
