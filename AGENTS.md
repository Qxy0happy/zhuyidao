# zhuyidao — Personal Workspace

Not a code project. This repo stores agent skills and collected reference articles.

## Structure

- `.agents/skills/` — installed skills. Each subdirectory is one skill (contains `SKILL.md`).
- `skills-lock.json` — tracks installed skills and their versions.
- Article directories — self-contained reference material with images/ and a `.md` file.

## Skills

The only installed skill is `skill-creator` (at `.agents/skills/skill-creator/`). Its `SKILL.md` has the exact commands for creating, editing, benchmarking, and validating skills.

- To create a new skill, follow the workflow in `.agents/skills/skill-creator/SKILL.md`.
- New skills go into `.agents/skills/<name>/` with `SKILL.md` as the entrypoint.

## Key facts

- No `opencode.json` — global config applies.
- No build, test, lint, or typecheck commands exist.
- No package manager, no language runtime is assumed.
- The repo is not a git repo — no VCS workflows apply.
