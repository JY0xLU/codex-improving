---
name: capture-memory
description: Use when active work produces a discrete event worth recording. Capture lightweight observations into inbox entries without consolidating or promoting long-term memory.
---

# Capture Memory

Use this skill during active work.

Its job is to capture one event at a time, not to consolidate memory.

## Use This Skill When

- the user explicitly corrects a mistake
- a command or workflow fails in a reusable way
- a stable preference becomes clear
- a repeatable workflow win appears
- a capability gap keeps showing up
- a task outcome, blocker, or decision should be remembered later

## Do Not Use This Skill When

- the user wants to reorganize memory files
- the user wants to promote rules into long-term memory
- the user wants a nightly review or cleanup pass
- the user wants to rewrite `AGENTS.md`

## Output Target

Write structured entries to the active inbox, usually `D:\CodexData\.codex\memory\inbox\`.

Prefer append-only daily files such as:

- `D:\CodexData\.codex\memory\inbox\YYYY-MM-DD.md`

## Entry Format

Each entry should include:

- id
- timestamp
- scope
- source
- type
- summary
- details
- suggested action
- tags

## Capture Rules

- capture only non-obvious, reusable, or likely-to-recur signal
- prefer short, high-information summaries
- record the narrowest useful scope: `global`, `repo`, or `thread`
- keep the entry event-oriented and lightweight
- do not promote directly into `ACTIVE.md` or `LEARNINGS.md`
- do not rewrite old inbox entries during active work
- do not modify `AGENTS.md`

## Examples

Good captures:

- a repeated failure pattern with a stable fix
- a stable repo-specific validation order
- a user preference the assistant should remember later
- a repeated missing capability worth tracking
- a scoped observation tied to a specific thread or repo task

Bad captures:

- casual chatter
- trivial typos
- one-off noise
- vague feelings with no operational consequence
