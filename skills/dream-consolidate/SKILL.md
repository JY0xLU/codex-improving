---
name: dream-consolidate
description: Use when a nightly or manual Dream Loop pass should keep `ACTIVE.md` hot, strengthen `LEARNINGS.md` as route memory, and record audit-first updates without rewriting policy.
---

# Dream Consolidate

Use this skill during off-hours or explicit maintenance passes.

Its job is to refine the public two-layer model and keep the supporting audit trail clean. It does not capture new signal from the current task.

## Use This Skill When

- the user asks for nightly memory maintenance
- an automation is reviewing recent inbox entries
- the user wants hot routes refreshed or route memory strengthened
- stale or superseded routes should be archived cleanly

## Do Not Use This Skill When

- the task is still actively unfolding and only needs capture
- the user only needs capability discovery during active work
- the user is asking to rewrite `AGENTS.md`

## Read These Files

- `D:\CodexData\.codex\memory\inbox\`
- the relevant slices of `D:\CodexData\.codex\memory\ACTIVE.md`
- the relevant slices of `D:\CodexData\.codex\memory\LEARNINGS.md`
- `D:\CodexData\.codex\memory\ARCHIVE\` when needed for lineage

## Main Actions

1. review recent inbox evidence and current public memory
2. keep `ACTIVE.md` hot by revising or retiring stale entries
3. strengthen `LEARNINGS.md` with validated winning routes
4. merge duplicate evidence when multiple entries support the same route
5. archive losing, stale, rejected, or superseded routes instead of deleting them
6. rewrite vague or relative dates into clearer absolute references
7. append an audit report with source trace and route rationale

## Public-Memory Decisions

Refresh `ACTIVE.md` when:

- the route or rule should affect behavior immediately
- the value is clearly temporary, urgent, or phase-specific

Strengthen `LEARNINGS.md` when:

- the route has already proved reusable
- the next task should be able to reuse it directly
- the evidence explains why it wins

Archive when:

- the route is no longer hot
- a better route replaced it
- the evidence no longer supports keeping it public

Keep evidence in `inbox/` when:

- it is still too early to surface publicly
- it is useful as trace, but not yet strong enough to shape behavior

## Hard Constraints

- never auto-edit `AGENTS.md`
- never invent learnings without source trace
- never silently delete evidence; archive it
- every promotion, rejection, or archive should be explainable
- keep `capture-memory` lightweight; own review and promotion here
- keep one final winning route when routes compete
- use reviewer or subagent cross-checks for promotion, rejection, archive, or conflict decisions
- use a single-agent fast path only for low-risk cleanup with no meaningful judgment call
- retrieve only the relevant global, repo, or thread slice needed for the decision; do not load whole files when a targeted read is enough

## Required Output

Produce a report covering:

- files read
- files changed and why
- which `ACTIVE.md` entries were refreshed, revised, or retired
- which `LEARNINGS.md` routes were added, strengthened, revised, or rejected
- which alternative routes were considered and why they lost
- reviewer or subagent disagreements and final resolution
- archive actions
- remaining gaps for the next round
