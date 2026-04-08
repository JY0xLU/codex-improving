---
name: dream-consolidate
description: Use when the user wants a scheduled or manual Dream Loop consolidation pass that deduplicates inbox items, expires stale temporary rules, rewrites dates clearly, and promotes only repeated, generalizable, actionable memory into ACTIVE.md or LEARNINGS.md.
---

# Dream Consolidate

Use this skill during off-hours or explicit maintenance passes.

Its job is to refine memory, not to capture new signal from the current task.

## Use This Skill When

- the user asks for nightly memory maintenance
- an automation is reviewing recent inbox entries
- the user wants to deduplicate or clean memory files
- the user wants promotion decisions with an audit trail

## Do Not Use This Skill When

- the task is still actively unfolding and only needs capture
- the user is asking to initialize the entire memory system from scratch
- the user is asking to rewrite `AGENTS.md`

## Read These Files

- `.codex/memory/inbox/`
- `.codex/memory/ACTIVE.md`
- `.codex/memory/LEARNINGS.md`
- `.codex/memory/FEATURE_REQUESTS.md`
- `.codex/memory/ARCHIVE/` when needed for lineage

## Main Actions

1. deduplicate repeated inbox observations
2. move expired temporary items out of `ACTIVE.md`
3. rewrite vague or relative dates into clearer absolute references
4. use subagent cross-review for promotion, rejection, archive, or conflict decisions
5. promote repeated, generalizable, actionable guidance
6. append a nightly report

## Promotion Rules

Promote to `ACTIVE.md` when the item is:

- high-frequency now
- operationally important now
- temporary or phase-specific

Promote to `LEARNINGS.md` when the item is:

- stable across sessions
- reusable across tasks
- still valuable after the current phase ends

Keep in raw memory when the item is:

- ambiguous
- one-off
- not yet generalizable

## Hard Constraints

- never auto-edit `AGENTS.md`
- never invent learnings without source trace
- never silently delete evidence; archive it
- every promotion or rejection should be explainable
- keep `capture-memory` lightweight; reserve subagent-heavy work for review and audit decisions
- use a single-agent fast path only for low-risk cleanup with no meaningful judgment call

## Required Output

Produce a report covering:

- files read
- files changed and why
- items reviewed by subagents
- main-agent/subagent disagreements and final resolution
- promotions made
- promotions rejected and why
- archive actions
- remaining cleanup
