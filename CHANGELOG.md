# Changelog

All notable changes to `Codex Native Dream Loop` will be documented in this file.

## 2026-04-09

### Changed
- Reframed the project around a v2 memory-priority architecture focused on self-improvement and memory optimization.
- Compressed the core model into four parts: Policy, Memory Scopes, Improvement Loop, and Audit.
- Tightened retrieval guidance so the system prefers minimal, scope-aware lookups over broad rereads.

### Skills
- Updated `capture-memory` to record lightweight, scoped events without promoting or consolidating memory during active work.
- Updated `dream-consolidate` to handle candidate generation, reviewer-assisted promotion and rejection, audit-first updates, and nightly consolidation.
- Kept policy-like changes proposal-only and reserved human approval for top-level policy updates.

### Templates
- Updated the global `AGENTS.md` snippet to use `global`, `repo`, and `thread` scopes with minimal retrieval guidance.
- Reworked memory templates so `ACTIVE.md` acts as the Operational projection and `LEARNINGS.md` acts as the LongTerm projection.
- Strengthened audit template fields around source trace, reviewer verdict, final decision, and rollback clues.

### References and Examples
- Updated the reference docs to match the v2 memory-priority model, including scope, promotion, automation, prompt-eval, and audit guidance.
- Refreshed the minimal example to show Observed, Operational, LongTerm, and audit-style nightly reporting in practice.
