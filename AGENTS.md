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

- Land verified changes via feature branch and Pull Request with passing CI checks; never push directly to main or stage with git add -A.
