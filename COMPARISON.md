# Comparison

## Previous Skill vs Dream Loop MVP

### Previous `self-improving-for-codex`

Strengths:

- clear mental model
- lightweight
- easy to install
- good first-generation structure

Limitations:

- capture and consolidation are blended together
- auditability is weak
- mostly global-first
- not yet shaped as a governed pipeline

### `codex-improving`

Strengths:

- separates daytime capture from nighttime consolidation
- introduces audit and archive expectations
- uses memory layers intentionally
- aligns more directly with Codex-native execution primitives

Tradeoffs:

- more moving pieces
- requires discipline around promotion rules
- needs a stronger README and examples to stay approachable

## Design Shift

The old model is:

- one skill
- one memory system
- one refinement loop

The new model is:

- one execution substrate
- one raw capture stream
- one governed consolidation pass
- one auditable promotion path

## What Stays The Same

- `AGENTS.md` remains the stable entry point
- memory should be externalized, not hidden in transient context
- top-level rules should stay short and durable

## What Changes

- raw observations first land in `inbox/`
- `ACTIVE.md` becomes explicitly temporary and current
- `LEARNINGS.md` becomes the main durable output
- `FEATURE_REQUESTS.md` becomes the bridge toward future capabilities
- `AGENTS.md` remains human-owned
