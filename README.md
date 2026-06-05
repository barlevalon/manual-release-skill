# skills

[![CI](https://github.com/barlevalon/skills/actions/workflows/ci.yml/badge.svg)](https://github.com/barlevalon/skills/actions/workflows/ci.yml)
[![npm](https://img.shields.io/npm/v/%40barlevalon%2Fskills.svg)](https://www.npmjs.com/package/@barlevalon/skills)

Portable Agent Skills for AI-assisted engineering workflows.

This repo is a skills monorepo. It contains original skills plus locally customized forks of upstream skills whose licenses permit redistribution. Verbatim upstream skills and stale local copies are intentionally excluded.

## Skills

### Communication

- [`caveman-commit`](skills/communication/caveman-commit/SKILL.md) — release-aware terse commit message generator.

### Engineering

- [`grill-with-docs`](skills/engineering/grill-with-docs/SKILL.md) — stress-test plans against project language and docs.
- [`tdd`](skills/engineering/tdd/SKILL.md) — red-green-refactor workflow guidance.

### Release

- [`release-prep`](skills/release/release-prep/SKILL.md) — evidence-backed release preparation, changelog drafting, SemVer recommendation, and approval-gated publishing plans.

## Install

### npm

Install all skills:

```bash
pi install npm:@barlevalon/skills
```

Install one skill:

```bash
pi install npm:@barlevalon/tdd-skill
pi install npm:@barlevalon/release-prep-skill
```

Packages declare Pi compatibility through `package.json`:

```json
{
  "pi": {
    "skills": ["./skills/*/*/SKILL.md"]
  }
}
```

### Git

```bash
git clone https://github.com/barlevalon/skills.git
```

Then point your agent harness at the package root, `skills/`, or a specific skill directory such as `skills/engineering/tdd`.

### Local checkout

```bash
pi -e .
pi -e ./skills/engineering/tdd
```

## Layout

```text
skills/
  <category>/
    <skill>/
      SKILL.md
      package.json
      README.md
      LICENSE
```

New skills should use `skills/<category>/<skill>/SKILL.md`, include a local `package.json`, and keep skill names globally unique.

## Attribution and licensing

Each skill directory includes its own `LICENSE` and README attribution. Customized forks currently included:

- `caveman-commit`: derived from `JuliusBrussee/caveman` under MIT.
- `grill-with-docs`, `tdd`: derived from `mattpocock/skills` under MIT.

## Validation

```bash
npm ci
npm run ci
```

## Documentation

- [Usage](docs/usage.md)
- [Maintainer release process](docs/release.md)
- [Changelog](CHANGELOG.md)

## License

MIT, except where individual skill directories declare a different license.
