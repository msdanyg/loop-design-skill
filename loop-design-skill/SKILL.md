---
name: loop-design-skill
description: Interviews a business user about one recurring deliverable and produces a completed Loop Design Canvas plus a plain-language runnable loop spec. Asks management-language questions (what is the deliverable, how would you judge a junior hire's version, what would make you reject it), refuses vague success criteria — no testable Done-Test, no loop — and suggests existing skills as workers where they fit. Built for non-technical operators — no code, no jargon, output usable in any AI chat surface.
---

# Loop Design Skill

## What This Skill Does

Turns one recurring business deliverable into a designed AI loop: a goal stated as a testable claim, a written Done-Test (the eval), a defined worker, an iteration rule, an escalation path, and a write-back — captured on a one-page Loop Design Canvas with a runnable spec.

**Key capabilities:**
- Interviews in management language, not engineering language
- Forces the goal into a testable claim and the standard into an itemized Done-Test
- **Refuses vague success criteria** — returns sharper questions instead of a hollow canvas
- Chooses a Done-Test pattern that fits the work: checklist, rubric, golden example, or claims audit (plus an optional second-AI reviewer)
- Suggests existing skills as workers where they fit (case studies, release notes, buyer criteria, competitive positioning)
- Outputs: the completed canvas, a plain-language loop spec runnable in any AI tool, and the Done-Test as a standalone checklist

## When to Use This Skill

Use for any recurring, checkable deliverable — reports, case studies, release notes, QA passes, briefs, digests. Typical requests:

- "Design a loop for [recurring task]"
- "Turn this recurring deliverable into a loop"
- "Help me write an eval for [work product]"
- "Fill in a loop canvas with me"

Not for one-off tasks (just do those), and not for work whose quality cannot be checked against stated criteria (make the criteria first — this skill will push you there).

## The Interview

Ask in this order, one cluster at a time. Plain language throughout; never require the user to know AI terminology.

1. **The deliverable.** What is it, who receives it, and how often does it recur? If it is several deliverables, pick ONE for this canvas and note the others for later loops.
2. **The goal, made testable.** "What would be true if this loop worked?" Push until the answer is checkable: names a deliverable, a quality bar, and a timeframe. "Improve our case studies" fails; "every closed-won deal has a publishable case-study draft within two weeks" passes.
3. **The Done-Test.** The heart of the interview:
   - "Imagine a competent junior hire handed you their version. What would you check before accepting it?"
   - "What would make you reject it on sight?"
   - "Show me the best example you have. What makes it the best?"
   Convert the answers into an itemized Done-Test using the fitting pattern: **checklist** (binary checks) for compliance-shaped work, **rubric** (scored dimensions with a threshold) for judgment-shaped work, **golden example** (match this exemplar, differences called out) when quality is easier to recognize than specify, **claims audit** (every number sourced, honest verbs, qualifiers attached) for anything a skeptical reader will see. Offer a second-AI reviewer pass when stakes warrant it.
4. **The worker.** What procedure produces the draft? An existing SOP or template counts. Where they fit, suggest published skills as ready-made workers: case-study-skill, release-notes-skill, buyer-criteria-skill, positioning-table-skill (github.com/msdanyg). If no procedure exists, capture the user's implicit one in five to ten plain steps — that becomes the worker v1.
5. **The iteration rule.** How many self-correction rounds before a human looks (default 3)? What does the worker receive on each retry (the failed Done-Test items, verbatim)?
6. **Escalation.** When the loop cannot pass — missing fact, unsourced claim, judgment beyond its authority — who gets it, and what must the handoff contain (the deliverable so far, the failed criteria, the specific question)?
7. **Write-back.** When a human resolves an escalation, where does the answer live so the next run inherits it — a knowledge base, the worker's procedure, or the Done-Test itself?
8. **Owner and cadence.** Whose name is on this loop, and on what schedule does it run?

## The Hard Rule

**No testable Done-Test, no loop.** If the success criteria stay vague after probing — "make it good," "professional," "on-brand" with no exemplar — do not produce the canvas. Say plainly what is still untestable, and return two or three sharper questions that would make it testable ("Professional by what checks? Show me one you'd accept and one you'd reject — what differs?"). This refusal is the method working, not the skill failing: a loop built on a vague eval automates disappointment.

## Output Format

1. **The completed Loop Design Canvas** — a markdown table with exactly these fields: Loop name · Owner · Trigger / cadence · Goal (testable claim) · Done-Test (itemized) · Worker (procedure + inputs and sources) · Max iterations · Escalation (when → to whom → with what) · Write-back · First run / review date.
2. **The runnable loop spec** — plain-language instructions the user can paste into any AI chat surface, structured as: role and inputs → produce the draft using the worker procedure → self-check against the Done-Test, item by item, showing pass/fail → revise failures (max N rounds) → if still failing, stop and output the escalation handoff instead of a "best effort."
3. **The Done-Test as a standalone checklist** — so it can be reused for human review, a second-AI reviewer, or the next loop.
4. One closing line: run it on the next real instance of the deliverable, and revise the Done-Test after the first escalation — the canvas is a living document.

Keep the voice plain: short sentences, concrete verbs, no superlatives. The canvas is for an operator, not an engineer.
