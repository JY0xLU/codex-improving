# LEARNINGS

## [LRN-20260408-001] narrow-first validation
**Logged**: 2026-04-08T09:30:00+08:00
**Priority**: medium
**Status**: promoted
**Source IDs**: INBOX-20260406-002, INBOX-20260407-001, INBOX-20260408-001

### Summary
Run the narrowest relevant test target before broad lint or full-suite validation.

### Why It Generalizes
This pattern reduces wasted time across UI and service tasks by catching local breakage early.

### Actionable Rule
When the changed area is clear, validate with the narrowest relevant target first and widen only after it passes.
