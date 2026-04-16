# Nightly Dream Loop Automation

## Recommended Schedule

- daily
- local off-hours
- example: 02:00 local time

## Recommended Prompt

```text
This is the nightly Dream Loop maintenance pass for a Codex-native route-memory system.

Read:
- D:\CodexData\.codex\memory\inbox\
- the relevant slices of D:\CodexData\.codex\memory\ACTIVE.md
- the relevant slices of D:\CodexData\.codex\memory\LEARNINGS.md
- D:\CodexData\.codex\memory\ARCHIVE\ when needed for lineage

Goals:
1. keep ACTIVE.md hot by removing expired or stale entries
2. strengthen LEARNINGS.md as a reusable path-memory library
3. merge duplicate evidence from inbox items when they support the same route
4. archive losing, stale, or superseded routes instead of deleting them silently
5. rewrite vague timing into clear absolute dates when needed
6. preserve a minimal audit trail for promotion, rejection, archive, and rollback decisions

Review mode:
1. let the main agent propose the current winning route first
2. use reviewer or subagent cross-checks for promotion, rejection, archive, or conflict decisions
3. keep one final winning route, not multiple competing long-term strategies
4. allow a single-agent fast path only for low-risk cleanup such as obvious noise, date normalization, or uncontroversial archive moves
5. retrieve only the relevant slice needed for each decision; avoid full-file loading when a targeted read is enough

Hard constraints:
- do not rewrite AGENTS.md
- do not invent learnings with no traceable source
- do not silently delete evidence; archive it

Output a report that includes:
- files read
- files changed and why
- which ACTIVE entries were refreshed or retired
- which LEARNINGS routes were added, strengthened, revised, or rejected
- which alternative routes were considered and why they lost
- whether the main agent and reviewer disagreed
- how disagreements were resolved
- archive actions
- remaining gaps for the next round
```
