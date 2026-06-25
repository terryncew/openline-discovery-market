# OpenLine · Discovery Market

**A market that funds discovery — not prediction.**

Turn raw ideas into structured, testable **Opportunity Packs** with pre-registered falsifiers. Run the cheapest credible witnesses first. Emit auditable receipts.

No wallets. No logins. Just proof discipline.

---

## What is Discovery Market?

OpenLine Discovery Market is a browser demo of the OpenLine discovery loop:

1. **Pack** — Generate a falsifiable Opportunity Pack: claim, measurable KPI, and cheapest disproof.
2. **Falsifier** — Register what would kill the idea before investing heavily.
3. **Witnesses** — Run dual-witness tests: hard binary checks plus soft advisory signals, cheapest first.
4. **Receipt** — Emit a portable, machine-readable `openline.science.v1` receipt.

The core inversion is simple:

> Before asking “How do we make this work?”, ask “What would prove this does not work?”

That one move lowers confirmation bias, raises the cost of cheap talk, and makes results easier to verify.

---

## Live demo

[terryncew.github.io/openline-discovery-market](https://terryncew.github.io/openline-discovery-market/)

The demo is fully static and runs in the browser.

---

## Quick start

```bash
git clone https://github.com/terryncew/openline-discovery-market.git
cd openline-discovery-market
```

Then open `index.html` in your browser, or use the deployed GitHub Pages demo.

No build step required.

---

## How it works

### 1. Choose a domain

Examples include:

- AI Governance
- Climate & Carbon
- Cost & Productivity
- Privacy & Freedom
- Research & Science
- Public Accountability

### 2. Select or describe a project

Use a preloaded template or describe a custom idea in plain English.

### 3. Set context

Choose the runner and time window.

Examples:

- solo
- team
- lab
- 1 hour
- day
- weekend

### 4. Generate the pack

The app produces:

- a claim
- a falsifier
- witness tests
- a testability score
- ready-to-use artifacts

### 5. Optional AI customization

Describe your idea and have an AI assistant generate a tailored claim, falsifier, and witness plan.

---

## Output artifacts

Discovery Market can produce three useful artifacts:

### Human-readable issue body

A plain-language Opportunity Pack that can be pasted into GitHub Issues, Linear, Notion, or any project tracker.

### YAML spec

A structured `openline.science.v1` artifact designed for version control, CI workflows, and downstream automation.

### Testability score

A 0–100 score based on witness strength, cheat risk, setup burden, and time window.

A score of **85 or higher** means the idea is probably ready to test this week.

---

## OpenLine ecosystem

This repo is the idea-intake and discovery-market layer of the OpenLine stack.

| Repo | Purpose |
| --- | --- |
| `openline-core` | Typed claim/evidence graphs and portable receipt primitives |
| `COLE` | Coherence dashboard for stress, drift, UCR, and guard policy |
| `openline-hub` | Viewer and live proof wallet |
| `openline-discovery-market` | Opportunity Packs, falsifiers, witness ordering, and science receipts |

Principle:

> Receipts, not rhetoric. Proof moves; data does not.

---

## Philosophy

Most plans optimize for looking successful.

Discovery Market optimizes for being wrong as fast and cheaply as possible, then learning from it.

High-risk ideas get stricter falsifiers and better witness ordering. The market rewards real signal, not narrative.

An idea should earn more confidence only after it survives contact with reality.

---

## Example Opportunity Pack

```yaml
schema: openline.science.v1
type: opportunity_pack
title: Reduce AI support escalation cost
claim: >
  A retrieval-first support agent can reduce human escalation rate by 15%
  without increasing customer complaint rate.
kpi:
  name: escalation_rate
  target: -15%
falsifier: >
  FAIL if complaint rate rises by 5% or more, or if escalation rate falls
  by less than 5% after the pilot window.
witnesses:
  - type: hard
    name: escalation_delta
    check: compare pilot escalation rate against baseline
  - type: hard
    name: complaint_delta
    check: compare complaint rate against baseline
  - type: soft
    name: support_reviewer
    check: human review of 20 randomly sampled cases
receipt:
  emit: true
  format: openline.science.v1
```

---

## Contributing

Pull requests are welcome, especially for:

- new domains
- preloaded project templates
- stronger numeric falsifiers
- better witness simulations
- cleaner UI flows
- receipt export improvements

Falsifiers must be specific and measurable.

Good:

> FAIL if latency rises above 500ms for more than 5% of requests.

Weak:

> FAIL if performance is bad.

---

## Roadmap

- More domain templates
- Stronger falsifier generation
- Exportable `openline.science.v1` receipts
- Better witness simulation
- GitHub Issue export
- Receipt lineage view
- Optional AI-assisted pack generation
- Integration with broader OpenLine receipt tooling

---

## License

Apache 2.0

---

**OpenLine · receipts, not rhetoric.**
