---
name: wayfinder-pro
description: Plan a huge chunk of work as a shared map of decision tickets, with every grilling run on option-prompt rounds.
disable-model-invocation: true
---

Follow the `wayfinder` skill's `SKILL.md` unchanged, with one substitution: wherever it calls the Skill tool with "grilling", call it with "grilling-pro" instead, and wherever it names `/grill-me` or `/grill-with-docs`, name `/grill-me-pro` or `/grill-with-docs-pro` instead.

Everything else stays as `wayfinder` has it: the map, the decision tickets, the frontier, the blocking edges, and the `wayfinder:grilling` ticket label (a label rather than a skill call, so it keeps its name).