---
name: ask-matt-pro
description: Ask which skill or flow fits your situation, answered with the option-prompt routes.
disable-model-invocation: true
---

Answer from the `ask-matt` skill's `SKILL.md` map unchanged, with one substitution: wherever it names a skill that has a `-pro` twin, name the twin instead.

| `ask-matt` names | Answer with |
| --- | --- |
| `/grill-with-docs` | `/grill-with-docs-pro` |
| `/grill-me` | `/grill-me-pro` |
| `/grilling` | `/grilling-pro` |
| `/wayfinder` | `/wayfinder-pro` |
| `/triage` | `/triage-pro` |
| `/improve-codebase-architecture` | `/improve-codebase-architecture-pro` |

Every other route, the phase boundary, and the stop-and-recommend behaviour stay exactly as `ask-matt` has them.