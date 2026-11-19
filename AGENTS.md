# 12-factor-agents-research — Agent Instructions

> Canonical instructions: AGENTS.md

Local workspace copy of the public `12-factor-agents` research repo. Treat the README and content files as the primary source material and keep local instruction files thin.

## Build & Verify

```bash
make setup
make teardown
```

No dedicated repo-local test or lint target is configured here. Verify documentation-oriented edits manually and avoid committing generated dependencies.

## Working Rules

- Use `README.md` and the `content/` tree as the primary project context instead of reintroducing placeholder persona templates.
- Keep `AGENTS.md` canonical with thin projection pointers (`CLAUDE.md`, `GEMINI.md`, `.clinerules`) and standardized `.codex/config.toml`; keep `.github/copilot-instructions.md` retired.
- Prefer upstream-compatible documentation changes over local workflow scaffolding unless the repo explicitly adopts it.

## Landing

- Land verified changes via `branch -> PR -> claude-harness/bin/hg-land --repo <checkout>` (never `git push origin main` directly; never use `git add -A`).

<!-- BEGIN GENERATED LANDING POLICY -->
Use `hg-land --repo <checkout>` (`--no-verify` while the fleet gate switch
`~/.config/hg/gates-disabled` or `HG_GATES_DISABLED=1` is active; `--local-gate <log>`
under `HG_GATES_DISABLED=0`, or `hg-gate-then-land --require-gate`) to land through a
pull request. Owned by `claude-harness/.agents/policies/landing.md`.

- While fleet gates are disabled (operator 2026-11-08), `hg-land` lands without a
  local gate log; when gated, bind the log to `head=<full SHA>` with final `rc=0`.
- Observe the repository's current remote requirements. Required checks and
  branch protections remain binding; hosted CI is not assumed required everywhere.
- Never bypass a failed gate, force-push, or replace unrelated work. Do not use
  direct pushes to main as a substitute for the configured landing route.
- Optoinvest repositories remain local-only: no remote publication.
- Prove landing with the tool receipt and exact remote main SHA. Source updates
  and runtime/deployment verification are separate claims.
<!-- END GENERATED LANDING POLICY -->
