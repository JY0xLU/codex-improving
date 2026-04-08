# Automation Design

Use a single nightly automation for the Dream Loop.

## Schedule

Recommended:

- daily
- off-hours
- after normal work concludes

## Inputs

Read:

- `.codex/memory/inbox/`
- only the relevant slices of `.codex/memory/ACTIVE.md`
- only the relevant slices of `.codex/memory/LEARNINGS.md`
- `.codex/memory/FEATURE_REQUESTS.md` when a gap is being tracked

## Outputs

The automation may:

- merge duplicate inbox entries
- promote repeated operational guidance into `ACTIVE.md`
- promote stable reusable patterns into `LEARNINGS.md`
- move expired items into `ARCHIVE/`
- append a nightly audit report
- preserve rollback context for reversions and superseded items

The automation must not:

- rewrite `AGENTS.md`
- invent learnings with no source trace
- delete raw evidence without archiving it
