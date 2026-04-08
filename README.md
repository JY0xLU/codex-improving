# Codex Improving

[中文](README.zh-CN.md) | English

`codex-improving` is a Codex-native Dream Loop for self-improvement and memory optimization.

It keeps the original loop:

- daytime captures signal
- nighttime consolidates memory

It also keeps the original building blocks:

- `AGENTS.md`
- skills
- automations
- worktrees
- sandbox and permissions
- subagents

The v2 emphasis is simple:

- improve the agent
- keep memory lightweight and searchable
- preserve auditability and rollback paths
- avoid broad rereads when a narrow lookup is enough

## Architecture

### 1. Policy

Human-approved rules only.

- `AGENTS.md` stays the human-facing policy entrypoint
- never auto-edit policy
- if a rule belongs in Policy, propose it for review

### 2. Memory Scopes

Only three scopes are used: global, repo, and thread.

- `global` holds cross-project patterns
- `repo` holds project-specific memory
- `thread` holds short-lived session context
- `ACTIVE.md` is the operational projection
- `LEARNINGS.md` is the long-term projection
- retrieval should be minimal: read only the slices needed for the task, not the full memory set

### 3. Improvement Loop

Use `capture-memory` during active work and `dream-consolidate` off-hours.

- capture raw signal into `inbox/`
- consolidate nightly
- deduplicate, expire, rewrite, and promote only when evidence is repeated and actionable
- an agent reviewer may auto-review and promote clear cases into long-term memory, but not into Policy
- keep nightly consolidation as a regular habit, not an ad hoc cleanup

### 4. Audit

Every memory change should be explainable and recoverable.

- preserve source ids
- record what was read, changed, promoted, rejected, archived, and rolled back
- prefer reports that support rollback and follow-up review
- keep low-risk cleanup fast, but never at the expense of traceability

## What This Repository Includes

This repository ships a minimal Dream Loop:

- `skills/capture-memory/`
  - a daytime capture skill
  - records structured observations into `inbox/`
- `skills/dream-consolidate/`
  - a nighttime consolidation skill
  - deduplicates, expires, rewrites, promotes, and reports memory changes
- `templates/`
  - starter `AGENTS.md` snippet
  - starter memory files
- `examples/`
  - a minimal global-memory example
- `automations/`
  - a recommended nightly automation prompt and schedule

## Core Rules

- Daytime capture writes only to `.codex/memory/inbox/`
- Nighttime consolidation may rewrite memory files under `.codex/memory/`
- `AGENTS.md` must not be auto-modified
- Every promotion, merge, archive, and rejection should be auditable
- `ACTIVE.md` may contain temporary guidance, but every temporary item should include an expiry condition
- `capture-memory` should stay lightweight; subagent-heavy work belongs in Dream Loop review and audit passes

## Subagent Bias

This repo prefers subagent-assisted review for Dream Loop maintenance:

- `capture-memory` remains a lightweight single-agent workflow
- `dream-consolidate` should prefer at least one subagent for promotion, rejection, archive, and conflict review
- low-risk cleanup may still use a single-agent fast path
- if the main agent and reviewer disagree, the final report should record the disagreement and the resolution

## Repo Layout

```text
codex-improving/
├── README.md
├── README.zh-CN.md
├── references/
├── templates/
├── examples/
├── automations/
└── skills/
    ├── capture-memory/
    └── dream-consolidate/
```

## Quick Start

1. Copy `skills/capture-memory/` and `skills/dream-consolidate/` into `$CODEX_HOME/skills/` or `~/.codex/skills/` so Codex can discover them.
2. Copy the templates under `templates/global/` into your global Codex home as a starting point.
3. Add the `AGENTS.md` snippet to your global or project entrypoint.
4. Use `capture-memory` during active work.
5. Run `dream-consolidate` on a nightly automation.
6. Prefer subagent cross-review for important nightly promotion or rejection decisions.
7. Review the generated audit report before trusting promoted rules.
