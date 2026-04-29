---
name: dream-consolidate
description: Use when a nightly or manual Dream Loop pass should keep ACTIVE.md hot, strengthen LEARNINGS.md, and drain only unresolved inferred signal from inbox.
---

# Dream Consolidate

Use this skill during off-hours or explicit maintenance passes.

Its job is to refine public memory and resolve leftover uncertainty. It is not supposed to keep explicit strong signal waiting in inbox.

## Use This Skill When

- the user asks for nightly memory maintenance
- an automation is reviewing unresolved inbox evidence
- hot routes should be refreshed or retired
- reusable routes should be strengthened
- stale or losing routes should be archived cleanly

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

1. review unresolved inbox evidence and current public memory
2. treat `inbox/` as a short-lived quarantine buffer for inferred or unresolved signal
3. move or rewrite any misplaced strong signal out of `inbox/` immediately
4. keep `ACTIVE.md` hot by revising or retiring stale entries
5. merge duplicate evidence when multiple entries support the same route
6. strengthen `LEARNINGS.md` with validated winning routes
7. archive losing, stale, rejected, or superseded routes instead of deleting them
8. append an audit report with source trace and route rationale

## Public-Memory Decisions

Direct-land guidance should already have happened during active work when the signal was explicit and the destination was clear.

Refresh `ACTIVE.md` when:

- the route or rule should affect behavior immediately
- the value is clearly temporary, urgent, or phase-specific

Strengthen `LEARNINGS.md` when:

- the route has already proved reusable
- the next task should be able to reuse it directly
- the evidence explains why it wins
- the entry already reads like an executable preference, route, capability choice, or failure pattern

Only keep items in `inbox/` when they are:

- inferred rather than directly stated
- still ambiguous or still competing with another route
- only seen once and not yet strong enough to shape future behavior
- useful as evidence later, but not yet good enough for `ACTIVE.md` or `LEARNINGS.md`

Auto-land from `inbox/` only when all of these are true:

- the entry has survived at least one consolidation cycle, which defaults to 6 hours in the recurring automation
- no later user correction, reviewer objection, or contradictory source invalidates it
- the entry has source trace and is already written in short executable form
- the destination is clear

Require stronger evidence before landing in `LEARNINGS.md` for inferred routes, failures, or capability choices. Explicit user directives and explicit user corrections should not linger in `inbox/`.

Archive when:

- the route is no longer hot
- a better route replaced it
- the evidence no longer supports keeping it public
- the unresolved signal has already waited long enough and still does not justify promotion

## Hard Constraints

- never auto-edit `AGENTS.md`
- never invent learnings without source trace
- never silently delete evidence; archive it
- every promotion, rejection, or archive should be explainable
- age alone is not enough for promotion
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
