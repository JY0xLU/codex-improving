# Scope Model

## v1 Default

MVP v1 assumes a global-first layout:

- global rule entry: `~/.codex/AGENTS.md`
- global memory directory: `~/.codex/memory/`

This keeps the first version simple and easy to explain.

## Why Not More In v1

Repo-local memory and custom profile switching are valuable, but they add policy complexity:

- merge strategy between scopes
- conflict resolution
- promotion target selection
- cross-repo contamination risk

Those concerns are deferred to later versions.

## Future Scope Roadmap

### v2: Global + Repo-Local

- `~/.codex/memory/` for personal cross-project patterns
- `<repo>/.codex/memory/` for project-specific learnings

### v3: Custom Profiles

- support alternative `CODEX_HOME`
- document portable profile setups for shared or sandboxed environments
