---
name: grilling-pro
description: Present a grilling round as harness option prompts, so the human answers by picking or typing. Reached by grill-me-pro and grill-with-docs-pro, or use it when the user asks to be grilled with clickable options.
---

Call the Skill tool with "grilling". Wherever `grilling` says to emit a round, emit it the way below instead: the round arrives in the prompt tool, not in the chat. Where the two disagree about how a round reaches the human, this skill wins.

## A round is a prompt, not a paragraph

Ask the round with your harness's structured-choice prompt tool: the one that takes a question body and a short list of options, and returns the human's pick. On CodeBuddy that tool is `ask_followup_question`; on Claude Code, `AskUserQuestion`. A round typed out as text has failed this skill.

- **One call takes at most 4 questions, and at most 4 options per question.** A round carries the whole frontier, so a round of five or more questions runs as consecutive calls with continuous numbering. The round is the run of calls, not one call.
- **Consecutive calls go one per turn.** Never put two calls in the same message: the tool reports the second as displayed, but its answers never come back, so the round silently reads as finished with questions unanswered. Send the next call only once the previous call's answers have arrived, and re-ask any question you never got an answer to rather than assuming it.
- **The calls are the round.** Ask the questions once, in the tool. Do not also print the numbered text round.
- **Each question keeps its full body**: the title, the alternatives, any prose the decision needs, and a closing `➡️` line naming your recommended option, worded in the session's language.
- **Two to four short options** per question: the tool takes at most four. Turn multi-select on only where the decision genuinely admits several answers at once; a decision with one right answer stays single-select.
- **A decision with more than four real alternatives is a question doing two jobs.** Split it. If it genuinely will not split, put that one question to the human in the text round and keep the rest of the round in the tool, rather than dropping alternatives to fit.
- **Typing stays open.** A typed answer overrides the picks, so never present the options as the only way through.
- **Wait for the answers before the next round.** The frontier does not move until the human answers, exactly as `grilling` requires.

Where the harness offers no such tool, fall back to `grilling`'s text round: ask it in full and carry on. Never invent a tool, and never record an answer the human did not give.
