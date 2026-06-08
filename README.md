# skills

[![CI](https://github.com/barlevalon/skills/actions/workflows/ci.yml/badge.svg)](https://github.com/barlevalon/skills/actions/workflows/ci.yml)
[![npm](https://img.shields.io/npm/v/%40barlevalon%2Fskills.svg)](https://www.npmjs.com/package/@barlevalon/skills)

Portable `SKILL.md` workflows for AI-assisted engineering: planning, debugging, TDD, review, documentation, handoff, and release prep.

These skills are plain Markdown instructions. Use them with any agent harness, editor, or chat workflow that can load files, install packages, or accept custom instructions. The npm packages include Pi metadata, but the skills are not Pi-only.

## Start here

| If you want to... | Read this |
|---|---|
| Install or load the skills | [Setup guide](docs/setup.md) |
| Decide which skill to use | [Workflow guide](docs/workflow.md) |
| Look up every skill quickly | [Usage reference](docs/usage.md) |
| Browse all documentation | [Docs index](docs/README.md) |
| Release or maintain this package | [Maintainer release process](docs/release.md) |

## Quick start

1. Install the bundle.

   ```bash
   npm install @barlevalon/skills
   ```

2. Use the skills.

   Tools with npm skill-package support can load the bundle by package name:

   ```text
   @barlevalon/skills
   ```

   Tools that work from files can use the installed `SKILL.md` files under:

   ```text
   node_modules/@barlevalon/skills/skills/
   ```

3. Ask for the workflow by name:

   ```text
   Use TDD to implement this change.
   ```

   ```text
   Diagnose this failure before fixing it.
   ```

   ```text
   Prepare the next release and recommend the SemVer bump.
   ```

See [Setup guide](docs/setup.md) for single-skill installs, Pi, Git checkout, copy/paste, and editor-rule options.

## Workflow map

| Situation | Skills to reach for |
|---|---|
| New feature, fuzzy idea | `write-a-prd`, `grill-with-docs`, `prd-to-plan`, `prototype` |
| Bug or regression | `diagnose`, then `tdd` |
| Behavior change | `tdd` |
| Architecture feels tangled | `improve-codebase-architecture`, `zoom-out` |
| Strict review | `thermo-nuclear-code-quality-review` |
| Visual explanation or plan review | `plannotator-visual-explainer`, `plannotator-setup-goal`, `plannotator-compound` |
| Docs work | `documentation-system` |
| Release prep | `release-prep` |
| Commit message or concise communication | `caveman-commit`, `caveman`, `caveman-help` |
| Session handoff | `handoff` |
| Find more capabilities | `find-skills` |

## Skills

### Communication

- [`caveman`](skills/communication/caveman/SKILL.md) — concise communication mode.
- [`caveman-commit`](skills/communication/caveman-commit/SKILL.md) — compact, release-aware commit messages.
- [`caveman-help`](skills/communication/caveman-help/SKILL.md) — quick reference for caveman modes.

### Discovery

- [`find-skills`](skills/discovery/find-skills/SKILL.md) — find installable skills for a task.

### Documentation

- [`documentation-system`](skills/documentation/documentation-system/SKILL.md) — write, classify, audit, and restructure docs using the Divio model.

### Engineering

- [`diagnose`](skills/engineering/diagnose/SKILL.md) — disciplined bug/performance diagnosis loop.
- [`grill-with-docs`](skills/engineering/grill-with-docs/SKILL.md) — stress-test a plan against domain docs and ADRs.
- [`improve-codebase-architecture`](skills/engineering/improve-codebase-architecture/SKILL.md) — find deeper modules and better seams.
- [`prd-to-plan`](skills/engineering/prd-to-plan/SKILL.md) — turn a PRD into tracer-bullet implementation phases.
- [`prototype`](skills/engineering/prototype/SKILL.md) — build a throwaway prototype to test a design.
- [`tdd`](skills/engineering/tdd/SKILL.md) — red/green/refactor implementation loop.
- [`worktrunk`](skills/engineering/worktrunk/SKILL.md) — branch and worktree workflow using Worktrunk.
- [`write-a-prd`](skills/engineering/write-a-prd/SKILL.md) — interview, explore, and write a PRD.
- [`zoom-out`](skills/engineering/zoom-out/SKILL.md) — ask for broader context before changing code.

### Evaluation

- [`thermo-nuclear-code-quality-review`](skills/evaluation/thermo-nuclear-code-quality-review/SKILL.md) — strict maintainability review.

### Handoff

- [`handoff`](skills/handoff/handoff/SKILL.md) — compact a session for another agent.

### Release

- [`release-prep`](skills/release/release-prep/SKILL.md) — plan and validate a release without pushing/publishing by accident.

### Review

- [`plannotator-compound`](skills/review/plannotator-compound/SKILL.md) — analyze rejected planning feedback and improve future prompts.
- [`plannotator-setup-goal`](skills/review/plannotator-setup-goal/SKILL.md) — turn an objective into a reviewed goal package.
- [`plannotator-visual-explainer`](skills/review/plannotator-visual-explainer/SKILL.md) — create self-contained HTML visual explanations.

## Package layout

```text
skills/
  <category>/
    <skill>/
      SKILL.md
      package.json
      README.md
      LICENSE
```

New skills should use `skills/<category>/<skill>/SKILL.md`, include a local `package.json`, and keep skill names globally unique. Skill packages version independently from the root bundle.

## Credits

- `caveman`, `caveman-commit`, `caveman-help`: based on `JuliusBrussee/caveman` by Julius Brussee.
- `diagnose`, `grill-with-docs`, `handoff`, `improve-codebase-architecture`, `prd-to-plan`, `prototype`, `write-a-prd`, `zoom-out`: based on `mattpocock/skills` by Matt Pocock.
- `find-skills`: based on `vercel-labs/skills` by Vercel.
- `worktrunk`: based on `max-sixty/worktrunk` by Maximilian Roos.
- `thermo-nuclear-code-quality-review`: based on `cursor/plugins` by Cursor.
- `plannotator-*`: based on `backnotprop/plannotator` by backnotprop.

## Validate

```bash
npm ci
npm run ci
```

## License

MIT
