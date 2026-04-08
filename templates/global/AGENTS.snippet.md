## Dream Loop

Use the global memory directory at `~/.codex/memory/`.

Scope model:
- global: shared memory across workspaces
- repo: repo-specific memory
- thread: current conversation memory
Keep the system at these three scopes. Avoid adding task/session files unless a human explicitly approves a new pattern.

Before starting any task:
1. Determine the narrowest relevant scope: `global`, `repo`, or `thread`
2. Retrieve only the relevant slices from `~/.codex/memory/ACTIVE.md` and `~/.codex/memory/LEARNINGS.md`
3. Apply only that minimal memory context before analyzing the request

During active work:
1. Capture high-signal observations into `~/.codex/memory/inbox/`
2. Keep raw Observed items short and source-backed
3. Do not rewrite long-term memory while solving the current task

Memory policy:
1. Policy is human-approved only
2. If a rule seems like policy, propose it for human review; do not auto-write it

Off-hours and maintenance:
1. Prefer subagent review for promotion, rejection, archive, and conflict decisions
2. Keep low-risk cleanup on a single-agent fast path when no judgment call is needed

Promotion rules:
1. Promote temporary but high-frequency guidance into `~/.codex/memory/ACTIVE.md`
2. Promote stable cross-task patterns into `~/.codex/memory/LEARNINGS.md`
3. Track future capability gaps in `~/.codex/memory/FEATURE_REQUESTS.md`
4. Preserve `~/.codex/memory/AUDIT_LOG.md` and `~/.codex/memory/ARCHIVE/` for traceability

Behavior expectations:
- Prefer short, auditable memory entries over long narratives
- Keep temporary rules out of long-term memory unless they recur
- Preserve enough raw evidence to explain promotions later
- Keep `capture-memory` lightweight; reserve subagent-heavy work for Dream Loop review and audit decisions
