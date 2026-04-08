# LEARNINGS

Long-term learning projection. Entries here should already be stable enough for future minimal retrieval.

## [LRN-20260408-001] narrow-first validation
**Logged**: 2026-04-08T09:30:00+08:00
**State**: LongTerm
**Scope**: repo
**Task Type**: frontend-validation
**Repeat Count**: 4
**Score**: 0.86
**Reviewer Verdict**: promote
**Source IDs**: OBS-20260406-002, OBS-20260407-001, OBS-20260408-001

### Summary
Run the narrowest relevant test target before broad lint or full-suite validation.

### Why It Generalizes
This pattern repeatedly reduces wasted time across similar repo tasks by catching local breakage before broader checks.

### Actionable Rule
When the changed area is clear, validate with the narrowest relevant target first and widen only after it passes.
