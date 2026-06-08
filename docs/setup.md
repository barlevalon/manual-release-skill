# Setup

These skills are plain Markdown files. The easiest setup is to clone the repo and let your agent read the skill you want.

## 1. Clone the repo

```bash
git clone https://github.com/barlevalon/skills.git
```

## 2. Give your agent the right file or folder

Use the whole bundle:

```text
skills/
```

Use one skill:

```text
skills/engineering/tdd/SKILL.md
skills/release/release-prep/SKILL.md
skills/documentation/documentation-system/SKILL.md
```

If a skill links to helper files, give the agent the whole skill folder.

## 3. Ask for the workflow

```text
Use TDD to implement this change.
```

```text
Diagnose this bug before fixing it.
```

```text
Prepare a release plan.
```

## opencode

opencode reads project instructions from `AGENTS.md`.

In the project where you use opencode, add a short skills block to `AGENTS.md`:

```md
## Agent skills

Use workflow skills from `/path/to/barlevalon/skills`.

When I ask for a named workflow, read the matching `SKILL.md` before acting.
Examples:
- TDD: `/path/to/barlevalon/skills/skills/engineering/tdd/SKILL.md`
- Diagnose: `/path/to/barlevalon/skills/skills/engineering/diagnose/SKILL.md`
- Release prep: `/path/to/barlevalon/skills/skills/release/release-prep/SKILL.md`

If a skill links to helper files, read those from the same skill folder too.
```

Then run opencode in your project and ask normally:

```text
Use TDD to implement this change.
```

Tip: if you do not have `AGENTS.md` yet, run `/init` in opencode first, then add the block above.

## VS Code with AI extensions

Clone this repo next to your project, then make it visible to your AI extension.

Best option: add both folders to one VS Code workspace:

1. Open your project in VS Code.
2. Use **File → Add Folder to Workspace...**.
3. Add the cloned `skills` repo folder.
4. Ask your extension to use a skill file.

Example prompts:

```text
Use the TDD workflow from skills/engineering/tdd/SKILL.md to implement this change.
```

```text
Read skills/release/release-prep/SKILL.md and prepare a release plan.
```

```text
Use skills/documentation/documentation-system/SKILL.md to clean up these docs.
```

If your extension supports custom instructions, add something like this to its project instructions:

```md
Use workflow skills from the `skills` workspace folder. When I ask for a named workflow, read the matching `SKILL.md` before acting. If the skill links to helper files, read those too.
```

## npm package

The bundle is also on npm:

```bash
npm install @barlevalon/skills
```

Use npm when your agent has first-class support for npm skill packages. In that case, load:

```text
@barlevalon/skills
```

Single-skill packages are also available:

```text
@barlevalon/tdd-skill
@barlevalon/release-prep-skill
```

## Pi

Pi users can install from npm:

```bash
pi install npm:@barlevalon/skills
```

Or run from a checkout:

```bash
pi -e .
```

## Updating

If you cloned the repo:

```bash
git pull
```

If you installed from npm:

```bash
npm update @barlevalon/skills
```
