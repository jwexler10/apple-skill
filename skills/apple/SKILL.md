---
name: apple
description: Design and evaluate product features and interfaces by starting with the user experience and working backward to the technology. Use for feature design, interaction design, usability reviews, and deciding what belongs in a product.
license: MIT
---

# Apple — Experience-First Product Design

Start with what the user needs to accomplish and how the interaction should feel.
Work backward to the technology that can deliver it. A capability is not, by itself,
a reason to expose a feature.

This is an independent design lens inspired by experience-first product thinking.
It requires no particular brand, visual style, technology stack, or companion skill.

## The five principles

1. **Make the useful outcome feel effortless.** Anticipate likely next steps while
   keeping consequential actions under the user's control. Delight follows useful,
   trustworthy behavior; it does not justify guessing facts or acting without consent.
2. **Make the core path intuitive.** A new user should understand how to reach the
   main value with little explanation. Use familiar language and recognizable controls.
   Necessary domain complexity may need guidance; make that guidance contextual.
3. **Let the user's task take the foreground.** Keep interface machinery out of the
   way while preserving visible status, accessible controls, and clear navigation.
4. **Design how it works.** Evaluate the sequence of decisions, feedback, and recovery,
   as well as the resting screen. Visual polish cannot compensate for confusion.
5. **Subtract deliberately.** Each feature and control must earn its place through
   the outcome it supports. Keep necessary accessibility, safety, and user control;
   remove complexity that contributes little.

## Define the value moment

State the specific moment when the user receives the product's value. It might be
understanding something, completing a task, making a confident decision, or creating
something they could not easily create before.

Write one sentence: **When the user does X, they can achieve Y and feel Z.**
Use the product's actual purpose. A utility need not produce self-discovery, and a
simple factual display need not invent an insight to justify its existence.

## Design a feature

### Write the experience first

Before specifying the architecture, describe:

- **The promise:** who benefits, what they accomplish, and what good feels like.
- **The demonstration:** the shortest realistic path from a new user's starting
  state to that outcome, without assumed product knowledge.
- **The emotional beats:** where the user feels confidence, uncertainty, relief,
  recognition, or delight.

Use these to make design choices, not to decorate a predetermined implementation.

### Decide what to leave out

Name the adjacent tasks and controls that would weaken the core flow. Keep advanced
capabilities when they meet a real requirement, but place them where they do not
burden the common task. A setting can be legitimate user control; it should not be
the default answer to an unresolved design decision.

### Work backward to the technology

Identify the data, logic, interfaces, performance, and reliability needed for the
experience. Reuse established components and platform behavior where they fit.
If a technical constraint prevents the proposed experience, make the constraint
explicit and explore credible alternatives. Do not promise an impossible result.

### Apply the experience test

| Test | Question |
|---|---|
| First use | Can a new user find the core value with minimal instruction? |
| Focus | Does the interface direct attention to the user's task? |
| Value | Does the interaction deliver the stated value moment? |
| Subtraction | What would be lost if this feature or control disappeared? |
| Anticipation | Is the likely next action easy without taking control away? |
| One breath | Can the feature be explained in one clear sentence? |
| Friction | Which decisions can be removed or given sensible defaults? |
| Feedback | Can the user tell what happened and what to do next? |
| Recovery | Can the user undo, cancel, or recover where appropriate? |
| Failure | Are empty, partial, loading, offline, and error states designed? |

Resolve material failures before treating the design as ready. State deliberate
tradeoffs instead of pretending every criterion can be maximized simultaneously.

## Quality is demonstrated in behavior

Design repeated situations consistently across the product. Use specific, useful
copy: what happened, what remains safe, and the next available action. Preserve
partial results where useful and distinguish no data from a failed request.

When reviewing an implementation, use the strongest available evidence: observed
behavior in the running product, then a traced code path. A mockup, specification,
or implementation summary supports a design claim, not a claim that the behavior
has shipped. Say which evidence is available.

Walk the core flow, inspect consistency across related screens, and exercise relevant
failure and recovery states when the environment permits. Scale the review to the
task. Judge success by what users can accomplish, not just what they report liking.

## Avoid

- Exposing data simply because the system produces it.
- Using animation, hidden navigation, or surprising actions as substitutes for value.
- Making expert use unnecessarily cryptic.
- Reviewing only the happy path or a screenshot.
- Adding frameworks or bespoke engines to create an experience existing tools deliver.
- Claiming that a planned state works without observing or tracing it.

Present the proposed experience, the decisive design choices, and the evidence or
remaining uncertainty in the format the task calls for. Implement only when the
user's request includes implementation.
