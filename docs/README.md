# /brainstorm

A Claude [Agent Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) built on theater improv, not a business-brainstorm template.

A "Yes, and..." idea engine (based on theater improv) that builds toward a business goal, red-teams itself before you see a draft, and never praises you, pitches you, or sounds like AI. 

**[See the full writeup and demo →](https://YOUR-USERNAME.github.io/brainstorm/)**

## Install

1. Download [`brainstorm.skill`](./brainstorm.skill) (or clone this repo and zip the `brainstorm/` folder yourself — it's just a folder with one `SKILL.md` file inside).
2. In Claude: **Settings → Capabilities/Features → Skills** → upload the file.
3. Make sure **Code Execution and File Creation** is enabled (Claude will tell you if it isn't).
4. Toggle the skill on.
5. Type `/brainstorm <your goal>` in any chat.

If you don't give it an explicit goal, it infers one from context and states its assumption in one line before starting.

## What makes it different from "just ask Claude to brainstorm"

- 🟥 **Always "Yes, and..."** Based on 40 years of theater, improv, and Executive Coaching, everything is "Yes, and..." so ideas flow from one to the next, and you never get a boring, safe, unrelated list.
- 🟧 **Synthetic ADHD behavior.** Ideas are deliberately borrowed from other industries, so it feels like a true brainstorming session with the smartest entrepreneurs in the world.
- 🟨 **Built-in Red Team.** Claude is quietly doing full opposition research behind the scenes, so you only see fresh ideas with problems already solved.
- 🟩 **Weird by design.** The first idea is grounded in reality, the next few get strange, and then everything wraps up in the best buildable version of your goal.
- 🟦 **Spontaneous, related ideas.** Each call returns 5-6 spontaneous ideas, each building on the last, with a short analysis at the end.
- 🟪 **Doesn't sound like AI.** No intros, no summaries, no praise. No "Would you like me to..." next steps. This Skill optimizes for success, not engagement.

## Repo layout

```
brainstorm/
└── SKILL.md          ← the whole skill; a single plain-text file, no dependencies
brainstorm.skill       ← the same folder, pre-zipped, ready to upload
docs/
└── index.html         ← this repo's GitHub Pages landing page
```

## Extending it

The current skill is intentionally a single file — the fastest path from idea to something usable. A more elaborate version could add:

- `references/` — worked examples for weirdness calibration, a bank of cross-domain analogies, common red-team objection patterns
- `scripts/` — a script that scores which generated ideas have real mechanism/distribution logic behind them, versus novelty alone
- `agents/` — a red-team subagent that only ever sees the idea (not the reasoning behind it), for genuinely adversarial critique instead of the same voice softening its own idea — useful in environments that support subagents (Claude Code, Cowork)
- `assets/` — an output template to keep formatting consistent across models

None of that is required to use the skill as-is.

## License

MIT — see [LICENSE](./LICENSE). Fork it, rename it, break it, ship it.
