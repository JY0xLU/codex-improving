---
name: dream-consolidate
description: Use when a nightly or manual Dream Loop pass needs to generate candidates, review them with audit-first discipline, and promote only approved memory into the right state.
---

# Dream Consolidate

Use this skill during off-hours or explicit maintenance passes.

Its job is to refine memory, not to capture new signal from the current task.

## Use This Skill When

- the user asks for nightly memory maintenance
- an automation is reviewing recent inbox entries
- the user wants candidate generation, promotion, or rejection with an audit trail
- the user wants expired operational rules retired cleanly

## Do Not Use This Skill When

- the task is still actively unfolding and only needs capture
- the user is asking to initialize the entire memory system from scratch
- the user is asking to rewrite `AGENTS.md`

## Read These Files

- `D:\CodexData\.codex\memory\inbox\`
- the relevant slices of `D:\CodexData\.codex\memory\ACTIVE.md`
- the relevant slices of `D:\CodexData\.codex\memory\LEARNINGS.md`
- `D:\CodexData\.codex\memory\FEATURE_REQUESTS.md`
- `D:\CodexData\.codex\memory\ARCHIVE\` when needed for lineage

## Main Actions

1. build candidate lists from inbox items and active memory
2. deduplicate repeated observations
3. decide whether each candidate is Observed, Candidate, Operational, LongTerm, or Archived
4. move expired temporary items out of `ACTIVE.md`
5. rewrite vague or relative dates into clearer absolute references
6. use reviewer-assisted review for promotion, rejection, archive, or conflict decisions
7. append a nightly report with source trace and rationale

## Promotion Rules

Observed:

- raw capture that remains in inbox or source notes
- single-event material that is not ready for a decision

Candidate:

- proposed for promotion, rejection, or archival
- carries rationale, scope, and source trace

Promote to `ACTIVE.md` as `Operational` when the item is:

- high-frequency now
- operationally important now
- temporary or phase-specific

Promote to `LEARNINGS.md` as `LongTerm` when the item is:

- stable across sessions
- reusable across tasks
- still valuable after the current phase ends
- better expressed at `global` or `repo` scope than as thread-local context

Archive as `Archived` when the item is:

- superseded
- expired
- rejected
- resolved and no longer needed in active memory

Keep as a candidate or raw observation when the item is:

- ambiguous
- one-off
- not yet generalizable

## Hard Constraints

- never auto-edit `AGENTS.md`
- never invent learnings without source trace
- never silently delete evidence; archive it
- every promotion, rejection, or archive should be explainable
- keep `capture-memory` lightweight; own candidate generation and review here
- use reviewer-assisted auto-review to promote to `LongTerm` when the evidence is stable
- keep policy-like guidance proposal-only unless a human approves it
- use a single-agent fast path only for low-risk cleanup with no meaningful judgment call
- retrieve only the relevant global, repo, or thread slice needed for the decision; do not load whole files when a targeted read is enough

## Required Output

Produce a report covering:

- files read
- files changed and why
- candidates generated
- items reviewed by reviewers
- main-agent/reviewer disagreements and final resolution
- promotions made
- promotions rejected and why
- archive actions
- remaining cleanup
