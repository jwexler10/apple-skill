# Apple

**Start with the experience. Work backward to the technology.**

An agent skill for designing useful, intuitive product experiences with deliberate subtraction, clear feedback, and thoughtful recovery.

## Install in one command

```bash
npx skills add jwexler10/apple-skill
```

Choose Claude Code, Cursor, Codex, or another supported agent in the installer.
Requires [Node.js](https://nodejs.org/) 22.20 or later. Installs to the current project
by default; add `--global` for a user-wide installation. See the
[skills CLI](https://github.com/vercel-labs/skills) for supported agents and options.

For a noninteractive installation to Claude Code, Cursor, and Codex together:

```bash
npx skills add jwexler10/apple-skill --skill apple --agent claude-code cursor codex --yes
```

Prefer a graphical install? Use the Claude marketplace option below.

## What it does

- Defines the value moment and the shortest realistic path to it.
- Identifies unnecessary complexity before specifying the implementation.
- Works backward from the experience to the technical requirements.
- Reviews actual behavior, including loading, empty, partial, and error states.

A design lens rather than a visual component library. It does not require a particular aesthetic, framework, or brand.

## Before vs. after

**Example request:** “Design a document upload screen for people using our product for the first time.”

| Aspect | Without the skill: illustrative pitfall | With Apple: intended behavior |
|---|---|---|
| Starting point | Starts with a file picker and a list of supported formats. | Starts with the useful outcome and the shortest path a new user takes to reach it. |
| Controls | Exposes every available processing option. | Chooses a sensible default and keeps controls that meet a real user need. |
| Review | Shows only a polished success screen. | Checks progress, partial results, empty states, failure, and recovery as part of the design. |

These are illustrative comparisons, not recorded model outputs or benchmark results.
Actual results depend on the model, the prompt, and the evidence you provide.

## Install as a Claude plugin

This repository is both a standalone skill and a single-plugin marketplace. The
plugin and the skills CLI install the same `SKILL.md`; choose one route per host
to avoid duplicate installations.

### Claude and Cowork: no terminal

1. Open **Plugins** (or **Customize → Plugins**, depending on your version).
2. Choose **Add → Add marketplace → Add from a repository**.
3. Enter `jwexler10/apple-skill` or `https://github.com/jwexler10/apple-skill`.
4. Select **Apple** and add the plugin. Find its skill through `/` or the
   skill picker; when namespaced commands are shown, use `/apple:apple`.

Availability and organization controls depend on your Claude plan and account.
See [Anthropic's plugin installation guide](https://support.claude.com/en/articles/13837440-use-plugins-in-claude).

### Claude Code: marketplace commands

Run these inside Claude Code:

```text
/plugin marketplace add jwexler10/apple-skill
/plugin install apple@jwexler10-apple
```

Then invoke `/apple:apple` followed by your task. The marketplace is defined in
[`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json), and the plugin
in [`.claude-plugin/plugin.json`](.claude-plugin/plugin.json).

### Manual installation

Download the repository using **Code → Download ZIP**, or clone it:

```bash
git clone https://github.com/jwexler10/apple-skill.git
```

Copy the entire `skills/apple` folder, including any supporting files, into the
appropriate directory in your target project:

| Agent | Project skill directory | Invocation |
|---|---|---|
| Claude Code, direct skill | `.claude/skills/apple/` | `/apple` |
| Codex | `.agents/skills/apple/` | `$apple` |
| Cursor | `.cursor/skills/apple/` | Ask the agent to use Apple. |

Each destination must contain `SKILL.md` directly. Other hosts may use different
discovery or invocation rules; follow their documentation. See the
[Codex skills guide](https://learn.chatgpt.com/docs/build-skills).

This is an instruction-only skill: no API key, MCP server, companion skill, or
executable script is required. Tools are useful when your actual task needs live
information or inspection of an existing project.

## Try it

The prompts below use Codex's `$apple` syntax. In Claude Code, use `/apple` for a
direct skills installation or `/apple:apple` for a marketplace plugin. In Cursor,
ask the agent to use Apple and give it the same task.


```text
$apple Design a first-run experience for a household budgeting app. Start with what a new user should accomplish and feel.
```

```text
$apple Review this file-upload flow. Can users tell what happened, recover from failure, and see what to do next?
```

```text
$apple We can expose twelve configuration options. Help us choose a useful default and decide which controls earn their place.
```

Expect a clear experience promise, a practical interaction flow, deliberate omissions, and the evidence needed to judge whether the design works.

## Adapt it

Supply your actual objective, constraints, evidence, and priorities. Edit the skill
to fit your workflow. It assumes no particular product, repository structure,
technology stack, or internal decision log. Applying a thinking skill does not
itself authorize changes, purchases, deployments, or other external actions.

This independent project is not affiliated with or endorsed by Apple Inc. The name describes the design lens; it does not package Apple software or branding assets.

## Repository contents

- [`.claude-plugin/plugin.json`](.claude-plugin/plugin.json): Claude plugin metadata.
- [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json): installable marketplace catalog.
- [`skills/apple/SKILL.md`](skills/apple/SKILL.md): the complete skill.
- [`LICENSE`](LICENSE): MIT license for these instructions and documentation.

Copyright © 2026 Jason Wexler.
