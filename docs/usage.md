# Usage reference

This is the quick lookup page. For a guided decision tree, read [workflow.md](workflow.md). For installation and editor setup, read [setup.md](setup.md).

## Install

Install the full bundle:

```bash
npm install @barlevalon/skills
```

Install one skill package:

```bash
npm install @barlevalon/tdd-skill
```

## Loading model

Tools with npm skill-package support can load the bundle by package name:

```text
@barlevalon/skills
```

For file-based tools, a skill in a repo checkout lives at:

```text
skills/<category>/<skill>/SKILL.md
```

After installing the full npm bundle, the same skill is available under:

```text
node_modules/@barlevalon/skills/skills/<category>/<skill>/SKILL.md
```

After installing a single-skill npm package, it is available under:

```text
node_modules/@barlevalon/<skill-name>-skill/SKILL.md
```

Some skills also include supporting files in the same directory. If a `SKILL.md` links to local references or scripts, load the whole skill directory when your tool supports it.

## Package names

| Scope | Package |
|---|---|
| Full bundle | `@barlevalon/skills` |
| One skill | `@barlevalon/<skill-name>-skill` |

Examples:

```text
@barlevalon/tdd-skill
@barlevalon/release-prep-skill
@barlevalon/plannotator-visual-explainer-skill
```

Pi users can install npm packages with `pi install npm:<package>`. Other harnesses should use their own npm/package or file-loading mechanism.

## Skill quick reference

| Need | Skill |
|---|---|
| Concise communication | `caveman` |
| Commit message | `caveman-commit` |
| Caveman mode help | `caveman-help` |
| Find more skills | `find-skills` |
| Documentation audit/write/restructure | `documentation-system` |
| Diagnose a bug or regression | `diagnose` |
| Stress-test a plan against docs/ADRs | `grill-with-docs` |
| Find architecture deepening opportunities | `improve-codebase-architecture` |
| Turn a PRD into implementation phases | `prd-to-plan` |
| Explore design with a throwaway prototype | `prototype` |
| Implement behavior test-first | `tdd` |
| Manage worktrees/branches with Worktrunk | `worktrunk` |
| Write a PRD | `write-a-prd` |
| Ask for broader context | `zoom-out` |
| Strict maintainability review | `thermo-nuclear-code-quality-review` |
| Compact a session for handoff | `handoff` |
| Prepare a release | `release-prep` |
| Analyze denied/rejected planning patterns | `plannotator-compound` |
| Create a reviewed goal package | `plannotator-setup-goal` |
| Create an HTML visual explanation | `plannotator-visual-explainer` |

## Example prompts

```text
Use TDD to implement this bug fix.
```

```text
Diagnose this failure before fixing it.
```

```text
Grill this plan against the domain docs before we build it.
```

```text
Run a strict code-quality review.
```

```text
Create a visual explainer for this architecture change.
```

```text
Prepare the next release and recommend the SemVer bump.
```

```text
Write a commit message for the staged changes.
```
