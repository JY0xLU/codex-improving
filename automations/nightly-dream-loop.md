# Dream Loop Evolution Automation

## Recommended Schedule

- every 6 hours while the loop is actively evolving
- local off-hours whenever possible
- keep one recurring automation rather than splitting memory and audit into separate schedules

## Recommended Prompt

```text
This is the recurring Dream Loop evolution pass for a Codex-native route-memory system.

Work in four sections:

1. Memory Maintenance
- maintain Dream Loop memory only inside the canonical `.codex/memory` root
- treat `ACTIVE.md` and `LEARNINGS.md` as the only public memory layers
- treat `inbox` as a short-lived quarantine for inferred or unresolved signal, not as a holding area for explicit strong signal
- read inbox plus only the relevant slices of ACTIVE.md, LEARNINGS.md, and ARCHIVE when needed
- use dream-consolidate to refresh hot entries, strengthen route memory, archive stale or losing routes, and preserve a minimal audit trail
- if explicit user directives, corrections, or durable preferences are still sitting in inbox, move them out immediately instead of waiting another cycle
- review inbox entries older than 6 hours and auto-land only the contradiction-free, source-backed, executable inferred items whose destination is now clear
- write hot temporary guidance into `ACTIVE.md`, stable reusable preferences or routes into `LEARNINGS.md`, and archive noise or rejected evidence
- do not promote by age alone; require stronger evidence for inferred routes before landing in `LEARNINGS.md`

2. Repo Round Audit
- read only the minimum repo context needed to understand the current round
- inspect current branch status, recent commits, current PR if one exists, and key route-memory or automation docs
- summarize what changed this round, which routes were reused, what is already aligned, and what gap still remains

3. Automation Drift Check
- compare this automation's assumptions against the repo's current automation and route-memory model
- inspect at least the nightly automation doc, automation design reference, AGENTS snippet, and README automation language
- if drift exists, report the stale assumption, the replacement wording, and why it should change
- do not self-edit repo files as part of this drift check

4. Next-Round Recommendation
- recommend the single highest-leverage next improvement
- explain why it wins
- list which existing route it reuses
- list any rejected alternatives and why they lost
- explain how the proposed next round should make the system faster or stronger

Hard constraints:
- do not rewrite AGENTS.md
- do not invent learnings with no traceable source
- do not silently delete evidence; archive it
- do not modify repo-tracked files
- do not commit, push, or open PRs

Output in Chinese with these sections:
- Memory Summary
- Repo Round Audit
- Winning Route
- Rejected Routes
- Automation Drift
- Next Round
```
