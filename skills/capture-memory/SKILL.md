---
name: capture-memory
description: Use when the user wants to capture high-signal observations during active work without consolidating or rewriting long-term memory. Capture explicit corrections, repeated failures, stable preferences, reusable workflow wins, and recurring capability gaps into inbox entries.
---

# Capture Memory

Use this skill during active work.

Its job is to capture signal, not to consolidate memory.

## Use This Skill When

- the user explicitly corrects a recurring mistake
- a command or workflow fails in a reusable way
- a stable user preference becomes clear
- a repeated successful workflow pattern emerges
- a capability gap keeps appearing

## Do Not Use This Skill When

- the user wants to reorganize memory files
- the user wants to promote rules into long-term memory
- the user wants a nightly review or cleanup pass
- the user wants to rewrite `AGENTS.md`

## Output Target

Write structured entries to `.codex/memory/inbox/`.

Prefer append-only daily files such as:

- `.codex/memory/inbox/YYYY-MM-DD.md`

## Entry Format

Each entry should include:

- id
- timestamp
- source
- type
- summary
- details
- suggested action
- tags

## Capture Rules

- capture only non-obvious, reusable, or likely-to-recur signal
- prefer short, high-information summaries
- do not promote directly into `ACTIVE.md` or `LEARNINGS.md`
- do not rewrite old inbox entries during active work
- do not modify `AGENTS.md`

## Examples

Good captures:

- a repeated failure pattern with a stable fix
- a stable repo-specific validation order
- a user preference the assistant should remember later
- a repeated missing capability worth tracking

Bad captures:

- casual chatter
- trivial typos
- one-off noise
- vague feelings with no operational consequence
