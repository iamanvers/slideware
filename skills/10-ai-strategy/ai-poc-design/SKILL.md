---
name: ai-poc-design
description: Designs an AI proof-of-concept or pilot as a falsifiable test with pre-committed success criteria, scope, data plan, and an explicit path to production. Use to plan a PoC that proves value, not a demo.
---

# AI PoC Design

## When to use
- A prioritized AI use case needs a pilot to prove it works and creates value before scaling.
- Past "PoCs" were impressive demos that never converted to production and you want one that does.
- You need to de-risk the riskiest assumption of an AI use case cheaply before committing real capital.

## When not to use
- You're choosing *which* use cases to pilot → use `ai-use-case-prioritization`.
- The PoC has proven out and you're scaling it → use `ai-scaling-operating-model`.

## Method
1. **State the hypothesis as a falsifiable claim.** "An LLM can draft adjuster notes that are accepted with minor edits ≥80% of the time, cutting handling time ≥30%." A PoC that can't fail proves nothing — define what failure looks like up front.
2. **Pre-commit success criteria on two axes.** **Technical** (model quality: accuracy/precision-recall, factuality/hallucination rate, latency, cost-per-call) *and* **business** (the value metric: time saved, conversion lift, error reduction — measured against a baseline). Set the numeric pass/fail thresholds *before* building. Business criteria are what matter; a technically impressive model that doesn't move the business metric is a fail.
3. **Scope tight, with production in mind.** Narrow to one workflow, one user group, a bounded dataset — small enough to run in weeks, real enough that success implies production value. Decide the **path-to-production gate** now: what would have to be true (integration, guardrails, scale economics) to graduate this, so you don't build a dead-end demo.
4. **Plan data and evaluation.** The data to use, how it's accessed/governed, and — critically — a **held-out evaluation set with a human-graded rubric** (and a baseline: current process or a simple benchmark). For generative use cases, define how you measure quality and catch hallucination/harm.
5. **Run human-in-the-loop and instrument value.** Keep a human in the loop for the pilot; measure not just model metrics but the realized business delta vs baseline, plus adoption (did users actually use it?) and the unit economics at pilot scale (inference cost vs value).

## Decision rules
- The business success metric, measured against a baseline, decides the PoC — not the demo's wow factor or raw model accuracy.
- Define the path-to-production gate before building; a PoC with no graduation criteria is theater that will never scale.
- Time-box it (typically 4–12 weeks). If it can't show signal in that window at tight scope, that itself is a finding.

## Output format
1. **Hypothesis** — the falsifiable claim, with what failure looks like.
2. **Success criteria** — technical *and* business thresholds, pre-committed, vs a named baseline.
3. **Scope** — workflow, users, dataset, timeline, team.
4. **Data & evaluation plan** — data access/governance, held-out eval set, human-graded rubric, baseline.
5. **Path-to-production gate** — what graduation requires (integration, guardrails, scale economics, adoption).

## Quality bar
- A falsifiable hypothesis with pre-committed numeric thresholds on both technical and business axes.
- Value measured against an explicit baseline, with a held-out evaluation set — not vibes on a demo.
- The path-to-production gate is defined before building.
- Pilot unit economics (inference cost vs value) and adoption are instrumented, not just accuracy.

## Common failure modes
- Demo-driven development: an impressive prototype with no baseline, no value measurement, no production path.
- Success criteria set after seeing results (unfalsifiable).
- Measuring model accuracy but never the business metric or adoption.
- Ignoring inference cost, so a "successful" pilot is uneconomic at production scale.

## Pairs with
Consumes a Wave-1 use case from `ai-use-case-prioritization` and its `ai-value-case`. Borrows the falsification discipline of `assumption-audit` and the metric design of `kpi-architect`. A graduated PoC feeds `ai-scaling-operating-model`; guardrails come from `ai-governance-and-risk`.

## Worked example
Input: the claims-note-drafting use case. Hypothesis: "An LLM drafting notes from the case file will be accepted with only minor edits ≥80% of the time and cut average handling time ≥30%, at <$0.15 per note." Success criteria pre-committed: technical — hallucination rate <2% on a 200-case human-graded held-out set, p95 latency <5s; business — ≥30% handling-time reduction vs the current baseline measured on a matched cohort, ≥70% adjuster adoption. Scope: one claim type, 20 adjusters, 8 weeks, human-in-the-loop. Eval: 200 held-out cases graded against a rubric; baseline = current handling time. Path-to-production gate defined now: integration with the claims system, a PII-redaction guardrail, and inference cost <$0.15/note at full volume. The pilot is built to graduate, not to impress.
