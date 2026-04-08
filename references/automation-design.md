# Automation Design

Use a single nightly automation for MVP v1.

## Schedule

Recommended:

- daily
- off-hours
- after normal work concludes

## Inputs

Read:

- `.codex/memory/inbox/`
- `.codex/memory/ACTIVE.md`
- `.codex/memory/LEARNINGS.md`
- `.codex/memory/FEATURE_REQUESTS.md`

## Outputs

The automation may:

- merge duplicate inbox entries
- promote repeated operational guidance into `ACTIVE.md`
- promote stable reusable patterns into `LEARNINGS.md`
- move expired items into `ARCHIVE/`
- append a nightly report

The automation must not:

- rewrite `AGENTS.md`
- invent learnings with no source trace
- delete raw evidence without archiving it
