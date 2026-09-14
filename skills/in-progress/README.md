# In Progress

Beta. These skills are public on purpose: try them and tell me what breaks. They're excluded from the plugin and the top-level README until they graduate to a stable bucket, they get no docs pages, and they can change or disappear without warning.

The plugin won't give you these. Install one directly:

```bash
npx skills@latest add mattpocock/skills --skill=<name>
```

The three `-pro` skills below are local to this fork and are not on skills.sh, so the command above does not reach them.

- **[loop-me](./loop-me/SKILL.md)**: Grill yourself into implementable workflow specs over multiple sessions, using the current directory as a stateful workspace. User-invoked.
- **[writing-beats](./writing-beats/SKILL.md)**: Shape an article as a journey of beats, choose-your-own-adventure style. Pick a starting beat, write only that beat, then pivot to the next, until the article reaches a natural end.
- **[writing-fragments](./writing-fragments/SKILL.md)**: Grilling session that mines you for fragments (heterogeneous nuggets of writing) and appends them to a single document as raw material for a future article.
- **[writing-shape](./writing-shape/SKILL.md)**: Take a markdown file of raw material and shape it into an article paragraph by paragraph, arguing format choices at each step.
- **[claude-handoff](./claude-handoff/SKILL.md)**: Hand the current conversation off to a fresh background agent that picks up the work immediately, seeded with a handoff summary via `claude --bg`. User-invoked.
- **[setup-ts-deep-modules](./setup-ts-deep-modules/SKILL.md)**: Wire dependency-cruiser into a TypeScript repo so each package is a deep module: implementation hidden in subfolders, reachable only through its entry-point files, tests exercising it through those. User-invoked.
- **[implement-spec](./implement-spec/SKILL.md)**: Implement a whole spec on one branch. Works the tickets as a task graph rather than a list, running implementer subagents across the ready frontier for maximum concurrency, and lands the result as a single PR. User-invoked.
- **[retro](./retro/SKILL.md)**: Suggest improvements to the coding agent's environment (steering files, coding standards, automated checks, tooling) after a session. STUB: design notes only, not functional yet. User-invoked.
- **[grill-me-pro](./grill-me-pro/SKILL.md)**: The `/grill-me` interview with every round asked as option prompts, so you answer by picking options or by typing. User-invoked.
- **[grill-with-docs-pro](./grill-with-docs-pro/SKILL.md)**: The `/grill-with-docs` interview on those same option-prompt rounds, still writing `CONTEXT.md` and ADRs as it goes. User-invoked.
- **[grilling-pro](./grilling-pro/SKILL.md)**: The presentation layer that turns a `grilling` round into harness option prompts. Model-invoked.

## Graduating one of these

A move into `engineering/` or `productivity/` carries the wiring this bucket skips: the `.claude-plugin/plugin.json` entry, the top-level and bucket `README`s, a docs page at `docs/<bucket>/<name>.md`, and a route in `ask-matt` wherever the skill is user-reachable. The `-pro` trio also carries two debts of its own:

- Re-argue the harness tool naming against the 1.2.3 convention that removed Claude Code's tool names from instructions (the reasoning is in [0003-grilling-rounds-as-harness-option-prompts.md](./adr/0003-grilling-rounds-as-harness-option-prompts.md)), then move that ADR to `.agents/adr/`.
- Re-point the skills-manager source with `skills set-source <name> --git-url <repo> --subpath skills/<bucket>/<name>`, since a bucket move breaks the path the library was installed from.
