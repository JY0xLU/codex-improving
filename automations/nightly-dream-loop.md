# Nightly Dream Loop Automation

## Recommended Schedule

- Daily
- Local off-hours
- Example: 02:00 local time

## Recommended Prompt

```text
This is the nightly Dream Loop consolidation pass for a Codex-native memory system.

Read:
- D:\CodexData\.codex\memory\inbox\
- the relevant slices of D:\CodexData\.codex\memory\ACTIVE.md
- the relevant slices of D:\CodexData\.codex\memory\LEARNINGS.md
- D:\CodexData\.codex\memory\FEATURE_REQUESTS.md

Goals:
1. generate candidates from inbox items and existing memory
2. deduplicate repeated observations
3. classify each item as Observed, Candidate, Operational, LongTerm, or Archived
4. remove or archive expired temporary guidance
5. rewrite relative dates into absolute dates when needed
6. keep temporary operational guidance in ACTIVE.md as Operational
7. keep stable cross-task patterns in LEARNINGS.md as LongTerm
8. keep future capability gaps in FEATURE_REQUESTS.md
9. keep policy-like guidance as proposals unless a human approves a promotion

Review mode:
1. let the main agent build the candidate list first
2. use reviewer-assisted review for promotion, rejection, archive, and conflict decisions
3. promote to LongTerm only when the evidence is stable and the reviewer agrees
4. keep policy-like items proposal-only unless a human explicitly approves them
5. allow a single-agent fast path only for low-risk cleanup such as obvious noise, date normalization, or uncontroversial audit updates
6. retrieve only the relevant global, repo, or thread slice needed for each decision; avoid full-file loading when a targeted read is enough

Hard constraints:
- do not rewrite AGENTS.md
- do not invent learnings with no traceable source
- do not silently delete evidence; archive it

Output a report that includes:
- files read
- files changed and why
- which candidates were reviewed
- whether the main agent and reviewer disagreed
- how disagreements were resolved
- promotions made
- promotions rejected and why
- archive actions
- remaining cleanup
```
