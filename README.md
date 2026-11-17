# Apple

**Start with the experience. Work backward to the technology.**

An agent skill for designing useful, intuitive product experiences with deliberate subtraction, clear feedback, and thoughtful recovery.

## What it does

- Defines the value moment and the shortest realistic path to it.
- Identifies unnecessary complexity before specifying the implementation.
- Works backward from the experience to the technical requirements.
- Reviews actual behavior, including loading, empty, partial, and error states.

A design lens rather than a visual component library. It does not require a particular aesthetic, framework, or brand.

## Install

This repository contains a portable, instruction-only agent skill. No API key,
MCP server, executable script, or companion skill is required. Tools are useful
when your task needs current information or inspection of an existing project.

1. Download this repository with **Code → Download ZIP**, or clone it:

   ```bash
   git clone https://github.com/jwexler10/apple-skill.git
   ```

2. For a Codex project, copy the entire `skills/apple` folder into the target
   project's `.agents/skills/` directory. The result should be:

   ```text
   your-project/
     .agents/
       skills/
         apple/
           SKILL.md
   ```

   Keep any supporting files inside that folder when copying. For user-wide local
   Codex discovery, use `~/.agents/skills/apple/` instead. Choose one scope to avoid
   installing duplicate copies.

3. In Codex, invoke the skill with `$apple` followed by your task, or let the
   agent select it when your task matches the description. If it does not appear,
   restart Codex. See the [official skills guide](https://learn.chatgpt.com/docs/build-skills).

For another agent that supports `SKILL.md`, use that agent's documented skills
directory. You can also explicitly ask an agent to read and apply
[`skills/apple/SKILL.md`](skills/apple/SKILL.md). Discovery and invocation syntax
depend on the host.

## Try it

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

- [`skills/apple/SKILL.md`](skills/apple/SKILL.md): the complete skill.
- [`LICENSE`](LICENSE): MIT license for these instructions and documentation.

Copyright © 2026 Jason Wexler.
