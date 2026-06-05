# Usage

This package ships portable Agent Skills for AI-assisted engineering workflows.

## Included skills

- `caveman-commit` — release-aware terse commit messages.
- `grill-with-docs` — stress-test plans against project language and documentation.
- `tdd` — red-green-refactor implementation workflow.
- `release-prep` — evidence-backed release preparation and approval-gated publishing plans.

## Install

This package uses the portable Agent Skills layout:

```text
skills/<category>/<skill>/SKILL.md
```

Use whichever install path your agent harness supports.

### Generic

Clone the repository and add `skills/` or a specific skill directory to your agent's skill paths.

```bash
git clone https://github.com/barlevalon/skills.git
```

### npm packages

Install all skills:

```text
@barlevalon/skills
```

Install only one skill:

```text
@barlevalon/tdd-skill
@barlevalon/release-prep-skill
```

### Pi

```bash
pi install npm:@barlevalon/skills
pi install npm:@barlevalon/tdd-skill
pi install git:github.com/barlevalon/skills
pi install /path/to/skills
pi install /path/to/skills/skills/engineering/tdd
```

## Example prompts

```text
Write a commit message for the staged changes.
```

```text
Use TDD to implement this bug fix.
```

```text
Grill this plan against the domain docs before we build it.
```

```text
Prepare the next release and recommend the SemVer bump.
```
