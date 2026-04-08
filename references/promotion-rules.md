# Promotion Rules

Use these rules when deciding whether a captured observation should remain raw, move into `ACTIVE.md`, or graduate into `LEARNINGS.md` / LongTerm.

## Minimum Bar

Promote only when an item is:

- repeated or clearly stable
- generalizable beyond a single moment
- actionable as a concrete rule or practice

## Promote To `ACTIVE.md`

Use `ACTIVE.md` for the operational projection:

- high-frequency right now
- likely to matter at the start of upcoming tasks
- temporary, operational, or phase-specific

Every temporary item should include one of:

- an expiry date
- a removal condition
- a superseding condition

## Promote To `LEARNINGS.md`

Use `LEARNINGS.md` for the long-term projection:

- stable across sessions
- useful across multiple tasks
- still valuable after the current sprint or incident ends

An agent reviewer may auto-review and promote clear cases into LongTerm (`LEARNINGS.md`), but Policy changes still require human approval.

Thread-scoped context should usually stay temporary. If a thread-only pattern looks durable, rewrite it at `repo` or `global` scope before promoting it into `LEARNINGS.md`.

## Keep In `inbox/`

Do not promote yet when an item is:

- only observed once
- still ambiguous
- tightly tied to a one-off event
- too vague to become a concrete rule

## Reject Entirely

Reject or archive items that are:

- casual chatter
- trivial typos
- low-signal noise
- emotional but non-operational commentary

## Audit Requirements

Every promotion decision should capture:

- source entry id
- target file
- promotion rationale
- rejection rationale if applicable
- expiry condition when promoting into `ACTIVE.md`
- reviewer path when an agent reviewer auto-promotes into LongTerm
