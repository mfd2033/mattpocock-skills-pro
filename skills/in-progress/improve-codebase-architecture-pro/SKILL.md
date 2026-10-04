---
name: improve-codebase-architecture-pro
description: Scan a codebase for deepening opportunities, then grill through the candidate you pick on option-prompt rounds.
disable-model-invocation: true
---

Follow the `improve-codebase-architecture` skill's `SKILL.md` unchanged, with one substitution: wherever it calls the Skill tool with "grilling", call it with "grilling-pro" instead, and wherever it names `/grill-me` or `/grill-with-docs`, name `/grill-me-pro` or `/grill-with-docs-pro` instead.

Everything else stays as it is there, the HTML report and the candidate cards included, and its `domain-modeling` and `codebase-design` calls keep their names.