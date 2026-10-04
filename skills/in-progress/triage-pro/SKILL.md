---
name: triage-pro
description: Move issues through a state machine of triage roles, with the grill step run on option-prompt rounds.
disable-model-invocation: true
---

Follow the `triage` skill's `SKILL.md` unchanged, with one substitution: wherever it calls the Skill tool with "grilling", call it with "grilling-pro" instead, and wherever it names `/grill-me` or `/grill-with-docs`, name `/grill-me-pro` or `/grill-with-docs-pro` instead.

Everything else stays as `triage` has it: the roles, the labels, the agent brief, and the triage notes.