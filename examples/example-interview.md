# Example — a worked interview

> **Illustrative — all data below is invented.** No real company or team is described. Abridged: repetitive turns trimmed, the decisive moments kept.

**User:** Design a loop for our weekly campaign QA. It goes to the CMO every Friday.

**Skill:** Good candidate — recurring and checkable. Three questions to start:
1. What exactly does the CMO receive — a document, a dashboard walkthrough, an email?
2. What would be true if this loop worked? Give me something checkable, with a quality bar and a timeframe.
3. Who assembles it today, and how long does it take them?

**User:** A two-page summary of all active campaigns — spend, results, what changed, what needs a decision. Maya writes it Thursdays, takes her about four hours. If it worked… the CMO gets an accurate summary every Friday without Maya losing her Thursday.

**Skill:** Goal, made testable: **"Every Friday by 9am, the CMO receives a two-page campaign summary covering all active campaigns, with every figure traceable to the source dashboard, and no more than 30 minutes of Maya's review time."** Accept, or adjust the bar.

**User:** Accept.

**Skill:** Now the Done-Test — the standard the draft must pass before Maya sees it. Imagine a competent junior hire handed you their version of this summary. What would you check before accepting it?

**User:** That it covers everything, the numbers are right, and it looks professional.

**Skill:** Two of those I can work with; one I cannot.
- "Covers everything" → testable: *every campaign active in the ad platforms this week appears; any campaign present last week but missing this week is explicitly listed as ended.*
- "Numbers are right" → testable: *every figure carries its source (platform + report + date); any figure that cannot be traced is flagged, not stated.*
- **"Looks professional" is not testable yet.** I will not put it on the canvas as written — a vague criterion automates disappointment. Two questions to sharpen it: Show me one past summary you considered excellent and one that missed the mark — what differs? And are there fixed structural rules (length, section order, chart style) the CMO expects?

**User:** Fair. The good one led with the three decisions she needed to make. The weak one was a data dump. Structure: max two pages, decisions-needed section first, then per-campaign one-liners, then spend table.

**Skill:** That is a golden example plus a checklist. Done-Test, itemized:

1. Decisions-needed section appears first and contains every item requiring CMO action, each with a one-line recommendation — [checklist]
2. Every active campaign appears; ended campaigns listed as ended — [checklist]
3. Every figure carries source + date; untraceable figures are flagged in a "verify" list, never stated as fact — [claims audit]
4. Max two pages; section order: decisions → campaign one-liners → spend table — [checklist]
5. Reads like the 2026-03-06 exemplar, not a data dump: each one-liner states what changed and why it matters, not just numbers — [golden example]

**[Interview continues: worker = Maya's implicit procedure captured as 8 steps; iteration = 3 rounds, failed items fed back verbatim; escalation = untraceable figures and any new campaign missing goals go to Maya with the specific gap; write-back = resolved answers land in the campaign-tracker notes; owner = Maya; cadence = Thursday 3pm.]**

## Final output (abridged)

| Field | Entry |
|---|---|
| **Loop name** | Friday campaign summary |
| **Owner** | Maya (marketing ops) |
| **Trigger / cadence** | Thursdays 3pm, weekly |
| **Goal** | CMO receives the two-page summary Friday 9am; every figure traceable; ≤30 min of Maya's review |
| **Done-Test** | The five itemized checks above |
| **Worker** | The 8-step assembly procedure (sources: ad platforms, campaign tracker, spend sheet) |
| **Max iterations** | 3 |
| **Escalation** | Untraceable figures or goal-less campaigns → Maya, with the specific gap and the draft so far |
| **Write-back** | Resolutions recorded in campaign-tracker notes |
| **First run / review** | Next Thursday; revise Done-Test after first escalation |

Plus the runnable spec (paste-ready instructions implementing the above) and the five-item Done-Test as a standalone checklist for Maya's 30-minute review.
