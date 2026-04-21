# founder-mode

**Turn Brian Chesky's founder mode philosophy into an AI-powered operating system.**

A Claude Code plugin that extends your AI assistant from coding tool to AI co-founder. 12 slash commands that encode the operating system behind Airbnb's pandemic-era transformation — grounded in 6 primary sources from Chesky, Paul Graham, and YC.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code Plugin](https://img.shields.io/badge/Claude%20Code-Plugin-orange)](https://claude.ai/code)

---

## Why this exists

Every founder gets the same advice as they scale: "Hire great people and get out of their way."

Brian Chesky followed that advice. Airbnb drifted into divisional structure, politics, bureaucracy, and slow execution. Then the pandemic forced him to make five years of decisions in three months. He pulled decision-making back in, eliminated management layers, restructured to functional teams, and started personally reviewing every major product decision.

The result? Airbnb's best era.

Paul Graham named it **founder mode** — the opposite of the "hire and delegate" playbook. It's not micromanagement. It's knowing whether people are doing a good job, because you're close enough to the work to have that judgment.

founder-mode encodes this entire operating system into slash commands you can use in Claude Code. Not generic advice. Structured frameworks built from Chesky's specific practices, with scoring, diagnostics, and actionable next steps.

> "You can't delegate understanding." — Charles Eames, cited by Brian Chesky

---

## The 12 Commands

### Core Operating System

| Command | What it does |
|---------|-------------|
| `/founder-mode:founder-audit` | Diagnose where you sit on the founder mode ↔ manager mode spectrum. Scores 7 dimensions, identifies drift, recommends specific interventions. |
| `/founder-mode:org-health` | Detect the division → politics → bureaucracy → complacency arc. Places your org on Chesky's failure trajectory and tells you what to fix. |
| `/founder-mode:hiring-scorecard` | Score an executive hire using the "guilty until proven innocent" framework. Builder vs. manager classification, red flag detection, and a tailored reference check script. |
| `/founder-mode:review-cadence` | Design your CEO operating rhythm — what to review, how often, in what format. Based on Chesky's tiered review system with green/yellow/red scoring. |

### Strategic Tools

| Command | What it does |
|---------|-------------|
| `/founder-mode:add-a-zero` | Force 10x thinking on any goal. Breaks out of incremental thinking by surfacing which constraints need to break for 10x — then uses that insight to find the real 2x move. |
| `/founder-mode:launch-story` | Build the product narrative BEFORE building the product. Story-first design based on Chesky's "the story will often dictate the product." |
| `/founder-mode:delegation-scorer` | Score whether a delegation decision is healthy (amplifying) or harmful (abdicating). Prevents the "hire and disappear" trap that kills founder-led companies. |
| `/founder-mode:bureaucracy-detector` | Score any process for bureaucrat-mode creep. 12 anti-patterns from Paul Graham + Chesky's war on fake work. Includes the "just stop doing it" test. |

### Advanced

| Command | What it does |
|---------|-------------|
| `/founder-mode:skip-level-planner` | Design your skip-level strategy using Chesky's concentric circle model. Who to meet, how often, what to listen for, and how to handle manager relationships. |
| `/founder-mode:founder-quiz` | 15-question behavioral self-assessment. Reveals your actual operating mode — not what you think, but what you do. Tracks drift over time. |
| `/founder-mode:decision-check` | Determine if a decision requires founder-level involvement (institutional memory, permission, craft judgment) or can be safely delegated. |
| `/founder-mode:crisis-catalyst` | Reframe a crisis as a forcing function for decisions that were previously politically blocked. Based on Chesky's pandemic transformation. |

Every command returns:
- **Structured analysis** with scoring and diagnosis
- **Specific next steps** grounded in Chesky's actual practices
- **Pressure-test questions** to challenge your assumptions
- **Honest assessment** — including when founder mode might be the wrong call

---

## Install

### Claude Code

```bash
claude plugin install founder-mode
```

### Test locally (development)

```bash
git clone https://github.com/sohaibt/founder-mode.git
claude --plugin-dir ./founder-mode
```

Then try:

```
/founder-mode:founder-audit I'm CEO of a 45-person SaaS company. I used to review every feature but now I have a VP Product and VP Engineering who run their teams independently. I feel disconnected from what we're shipping.
```

---

## Example: Founder Mode Audit

**Ask:**

> /founder-mode:founder-audit I run a 60-person fintech startup. I have 6 direct reports. I do weekly 1:1s but rarely see the actual product work until it ships. My VP Product handles all roadmap decisions. I feel like I'm managing a company, not building one.

**What you get:**

A 7-dimension score (Product Involvement, Organizational Depth, Decision Velocity, Hiring Rigor, Org Structure, Narrative Ownership, Operating Cadence), a spectrum diagnosis (founder mode → manager mode → bureaucrat mode), the critical question ("Is this founder mode, or inability to delegate?"), and 3 specific interventions with first-step actions for this week.

---

## Example: Hiring Scorecard

**Ask:**

> /founder-mode:hiring-scorecard We're considering a VP Engineering from Google. 12 years experience, managed teams of 50+. Strong resume but in the interview he talked mostly about process and stakeholder management. I'm not sure he's a builder.

**What you get:**

Builder vs. Manager classification, a guilty-until-proven-innocent scorecard across 5 dimensions, red flag analysis, a customized 7-question reference check script using Chesky's techniques, and a closing strategy (talk them OUT of the job to test intrinsic motivation).

---

## The Research Behind It

This plugin is grounded in 6 primary sources, not generic startup advice:

1. **Brian Chesky's new playbook** — Lenny's Podcast deep dive on Airbnb's operating system
2. **Founder Mode & The Art of Hiring** — Chesky on executive hiring, reference checks, and the "guilty until proven innocent" framework
3. **Founder Mode (YC Talk)** — Chesky at Y Combinator on the concentric circle model, skip levels, and the pandemic transformation
4. **Paul Graham's "Founder Mode" essay** — The original essay that named the concept
5. **"We need to talk about founder mode"** — Critical analysis of when founder mode works and when it breaks
6. **Brian Chesky on Founder Mode** — On passion, permission, and institutional memory

Every recommendation in the plugin traces back to a specific practice, quote, or principle from these sources.

---

## What's coming next

- More frameworks grounded in primary source research
- Community-contributed slash commands
- Integration with strategy-mcp for connected strategy + execution

---

## Contributing

Contributions welcome. Some ways to help:

- **Add a new command** — open an issue with the framework and what it should do
- **Improve existing commands** — sharper analysis, better questions, deeper Chesky references
- **Add research sources** — transcripts, articles, or talks that surface new founder mode practices
- **Report bad advice** — if a command gives shallow or wrong analysis, that's a bug

---

## License

MIT — use it however you want.

---

## Built by

[Sohaib Thiab](https://sohaibthiab.me) — Former CPO, now building AI products in public.

- [strategy-mcp](https://github.com/sohaibt/strategy-mcp) — 12 product strategy frameworks as MCP tools
- [Mastering Product HQ](https://masteringproducthq.com) — Weekly writing on product leadership

**Want connected strategy execution?** [GetVelocity.ai](https://getvelocity.ai) takes founder mode principles further — connecting your OKRs to Jira, Linear, and ClickUp with AI-powered monitoring and real-time velocity tracking.

---

> "Leadership is presence, not absence." — Brian Chesky
