# skills

[![CI](https://github.com/barlevalon/skills/actions/workflows/ci.yml/badge.svg)](https://github.com/barlevalon/skills/actions/workflows/ci.yml)
[![npm](https://img.shields.io/npm/v/%40barlevalon%2Fskills.svg)](https://www.npmjs.com/package/@barlevalon/skills)

A public bundle of `SKILL.md` workflows for AI-assisted engineering.

Use it when you want an agent to follow a better process for planning, debugging, TDD, review, documentation, handoff, or release prep.

## Quick start

Clone the repo:

```bash
git clone https://github.com/barlevalon/skills.git
```

Point your agent at the repo, the `skills/` directory, or one skill file:

```text
skills/
skills/engineering/tdd/SKILL.md
skills/release/release-prep/SKILL.md
```

Then ask naturally:

```text
Use TDD to implement this change.
```

```text
Diagnose this failure before fixing it.
```

```text
Prepare the next release.
```

If your agent supports npm skill packages, you can also use:

```text
@barlevalon/skills
```

## What should I use?

| Work | Skill |
|---|---|
| Shape a feature | `write-a-prd`, `prd-to-plan`, `grill-with-docs` |
| Debug a hard failure | `diagnose` |
| Build test-first | `tdd` |
| Try an idea quickly | `prototype` |
| Improve architecture | `improve-codebase-architecture` |
| Review code harshly | `thermo-nuclear-code-quality-review` |
| Write or clean up docs | `documentation-system` |
| Prepare a release | `release-prep` |
| Write a commit message | `caveman-commit` |
| Hand off work | `handoff` |
| Make a visual explanation | `plannotator-visual-explainer` |

See [docs/workflow.md](docs/workflow.md) for the fuller map.

## Docs

- [Setup](docs/setup.md) — includes opencode and VS Code examples
- [Workflow map](docs/workflow.md)
- [Skill reference](docs/usage.md)
- [All docs](docs/README.md)
- [Maintainer release process](docs/release.md)

## Skills

### Communication

- [`caveman`](skills/communication/caveman/SKILL.md) — concise communication mode.
- [`caveman-commit`](skills/communication/caveman-commit/SKILL.md) — compact, release-aware commit messages.
- [`caveman-help`](skills/communication/caveman-help/SKILL.md) — quick reference for caveman modes.

### Discovery

- [`find-skills`](skills/discovery/find-skills/SKILL.md) — find installable skills for a task.

### Documentation

- [`documentation-system`](skills/documentation/documentation-system/SKILL.md) — write, classify, audit, and restructure docs.

### Engineering

- [`diagnose`](skills/engineering/diagnose/SKILL.md) — disciplined diagnosis loop.
- [`grill-with-docs`](skills/engineering/grill-with-docs/SKILL.md) — stress-test a plan against domain docs and ADRs.
- [`improve-codebase-architecture`](skills/engineering/improve-codebase-architecture/SKILL.md) — find deeper modules and better seams.
- [`prd-to-plan`](skills/engineering/prd-to-plan/SKILL.md) — turn a PRD into implementation phases.
- [`prototype`](skills/engineering/prototype/SKILL.md) — build a throwaway prototype.
- [`tdd`](skills/engineering/tdd/SKILL.md) — red/green/refactor implementation loop.
- [`worktrunk`](skills/engineering/worktrunk/SKILL.md) — branch and worktree workflow.
- [`write-a-prd`](skills/engineering/write-a-prd/SKILL.md) — interview, explore, and write a PRD.
- [`zoom-out`](skills/engineering/zoom-out/SKILL.md) — ask for broader context.

### Evaluation

- [`thermo-nuclear-code-quality-review`](skills/evaluation/thermo-nuclear-code-quality-review/SKILL.md) — strict maintainability review.

### Handoff

- [`handoff`](skills/handoff/handoff/SKILL.md) — compact a session for another agent.

### Release

- [`release-prep`](skills/release/release-prep/SKILL.md) — plan and validate a release.

### Review

- [`plannotator-compound`](skills/review/plannotator-compound/SKILL.md) — analyze rejected planning feedback.
- [`plannotator-setup-goal`](skills/review/plannotator-setup-goal/SKILL.md) — turn an objective into a reviewed goal package.
- [`plannotator-visual-explainer`](skills/review/plannotator-visual-explainer/SKILL.md) — create HTML visual explanations.

## Credits

- `caveman`, `caveman-commit`, `caveman-help`: based on `JuliusBrussee/caveman` by Julius Brussee.
- `diagnose`, `grill-with-docs`, `handoff`, `improve-codebase-architecture`, `prd-to-plan`, `prototype`, `write-a-prd`, `zoom-out`: based on `mattpocock/skills` by Matt Pocock.
- `find-skills`: based on `vercel-labs/skills` by Vercel.
- `worktrunk`: based on `max-sixty/worktrunk` by Maximilian Roos.
- `thermo-nuclear-code-quality-review`: based on `cursor/plugins` by Cursor.
- `plannotator-*`: based on `backnotprop/plannotator` by backnotprop.

## License

MIT
