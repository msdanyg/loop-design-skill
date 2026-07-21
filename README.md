# Loop Design Skill

A Claude skill that turns any **recurring business deliverable into a designed AI loop** — by interviewing you in management language and producing a completed **Loop Design Canvas** plus a plain-language, runnable loop spec. It asks the questions a good operator asks ("How would you judge a junior hire's version? What would make you reject it?") and it **refuses vague success criteria**: no testable definition of done, no loop.

Companion to the loop-design method at [cmoconfessions.com/loops](https://www.cmoconfessions.com/loops), from the practice behind [Kill the Battle Card](https://www.cmoconfessions.com/method) and [the PMM Skill Stack](https://www.cmoconfessions.com/skills).

## What it does

- **Interviews, not configures** — management questions in plain language; no AI jargon required
- **Forces testable goals** — "improve our case studies" becomes "every closed-won deal has a publishable draft within two weeks"
- **Builds your Done-Test (the eval)** — choosing the pattern that fits: checklist, rubric, golden example, or claims audit, with an optional second-AI reviewer
- **Refuses vague criteria** — "make it professional" gets you sharper questions back, not a hollow canvas; a loop built on a vague eval automates disappointment
- **Defines the full loop** — worker, iteration rule, escalation path, write-back, owner, and cadence
- **Outputs three artifacts** — the completed canvas (markdown), a runnable loop spec you can paste into any AI tool your company uses, and the Done-Test as a standalone checklist

## When it triggers

Phrases like:

- "Design a loop for [recurring task]"
- "Turn this recurring deliverable into a loop"
- "Help me write an eval for [work product]"
- "Fill in a loop canvas with me"

## Installation

### Option A — Claude.ai (no command line — where most operators work)

1. Download [`loop-design-skill.skill`](./loop-design-skill.skill) from this repo (top level, one click).
2. In claude.ai, open **Settings → Capabilities**, find **Skills**, and upload the file.
3. Done — next time you ask to design a loop, the skill runs.

### Option B — Claude Code (if you work in the terminal)

Copy the skill folder into your Claude skills directory:

```bash
# Personal (all projects)
cp -r loop-design-skill ~/.claude/skills/

# Or project-scoped
cp -r loop-design-skill /path/to/project/.claude/skills/
```

Restart Claude Code (or start a new session) and the skill will be available.

## Usage

> Design a loop for our weekly campaign QA. It goes to the CMO every Friday.

The skill interviews you, then returns the canvas, the runnable spec, and the checklist. See [`examples/`](./examples) for a worked interview (invented, illustrative data) — including the moment the skill refuses a vague criterion and sharpens it.

## The blank canvas

Prefer paper first? The one-page Loop Design Canvas is a free PDF: [cmoconfessions.com/loops](https://www.cmoconfessions.com/loops).

## Repository contents

- [`loop-design-skill/SKILL.md`](./loop-design-skill/SKILL.md) — the skill
- [`examples/`](./examples) — worked example (illustrative, invented data)
- [`loop-design-skill.skill`](./loop-design-skill.skill) — packaged for upload

## Part of a series

Prompt → skill → loop. The method: [Stop Prompting. Start Managing.](https://www.cmoconfessions.com/loops) · The tools: [the PMM Skill Stack](https://www.cmoconfessions.com/skills) · Built by [Daniel Glickman](https://www.cmoconfessions.com) — product marketing and AI leader.
