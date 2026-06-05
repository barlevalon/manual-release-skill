# pi-manual-release

A small [Pi](https://pi.dev/) / Agent Skills package for AI-assisted manual software releases.

It helps agents prepare releases from repository evidence instead of blindly deriving release meaning from commit-message automation.

## What it does

- Discovers local release tooling and policy first
- Inspects tags, commits, PRs, changelogs, workflows, and package manifests
- Recommends SemVer bumps with evidence
- Drafts user/operator-facing changelogs and release notes
- Produces GO / CONDITIONAL / NO-GO release readiness gates
- Requires explicit approval before tag, push, publish, deploy, or release mutation
- Helps create project-local release policy docs

## What it does not do

- It does not auto-publish packages
- It does not assume Conventional Commits are authoritative
- It does not tag, push, deploy, or publish without explicit approval
- It does not replace deterministic CI artifact builders such as GoReleaser

## Install

From npm, after publish:

```bash
pi install npm:pi-manual-release
```

From GitHub:

```bash
pi install git:github.com/barlevalon/pi-manual-release@v0.1.0
```

Try from a local checkout:

```bash
pi -e ./pi-manual-release
```

## Use

Ask Pi something like:

```text
Prepare a release.
```

```text
Draft release notes since the last tag.
```

```text
Recommend the next version and explain the evidence.
```

```text
Create a project-local release policy.
```

The skill loads as `manual-release`.

## Design stance

- Commit logs are for contributors.
- Changelogs and release notes are for users and operators.
- AI may draft and classify; humans approve release meaning.
- CI should build/publish deterministic artifacts when possible.
- Release actions that mutate remote state need explicit approval.

## Package layout

```text
skills/manual-release/SKILL.md
```

The package declares the skill through `package.json`:

```json
{
  "pi": {
    "skills": ["./skills"]
  }
}
```

## License

MIT
