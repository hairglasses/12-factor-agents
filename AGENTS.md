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
- Keep `AGENTS.md` canonical; keep `CLAUDE.md` and `GEMINI.md` as thin compatibility mirrors.
- Prefer upstream-compatible documentation changes over local workflow scaffolding unless the repo explicitly adopts it.