# Automation Design

Use a single nightly automation for the Dream Loop.

The public model stays small:

- `ACTIVE.md` for what is hot now
- `LEARNINGS.md` for reusable winning routes

Everything else is support machinery.

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
- `.codex/memory/ARCHIVE/` only when lineage matters

## Outputs

The automation may:

- refresh or retire stale `ACTIVE.md` entries
- strengthen `LEARNINGS.md` with validated winning routes
- merge duplicate evidence that supports the same route
- move stale or losing routes into `ARCHIVE/`
- append a minimal audit report
- preserve rollback context for reversions and superseded routes

The automation must not:

- rewrite `AGENTS.md`
- invent learnings with no source trace
- delete raw evidence without archiving it
- keep multiple conflicting “best routes” alive when one clear winner exists
