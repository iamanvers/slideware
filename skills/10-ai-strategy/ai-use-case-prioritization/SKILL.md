---
name: ai-use-case-prioritization
description: Ranks and sequences a portfolio of AI use cases on value and feasibility, balancing quick wins against foundational and transformational bets. Use to decide which AI initiatives to fund first.
---

# AI Use-Case Prioritization

## When to use
- You have a list of candidate AI use cases (e.g., from `ai-opportunity-mapping`) and limited money, talent, and attention.
- Everyone wants their use case funded and you need a defensible, value-based sequence.
- You need a portfolio that delivers early proof while building toward the big prizes.

## When not to use
- You don't yet have a candidate set → run `ai-opportunity-mapping` first.
- You're prioritizing general (non-AI) initiatives → use `initiative-prioritizer`.

## Method
1. **Score value rigorously.** Quantify each use case's annual value via its mechanism (`ai-value-case`): cost saved, revenue gained, risk reduced. Use a consistent basis across all use cases or the ranking is noise.
2. **Score feasibility on AI-specific dimensions.** Not just generic "effort." AI feasibility = **data availability/quality** + **technical maturity of the archetype** (a forecasting model is more proven than an autonomous agent) + **integration/workflow change required** + **talent/tooling on hand** + **acceptable error tolerance** (high-stakes, low-tolerance use cases are harder to ship).
3. **Plot value × feasibility; bubble = cost or strategic importance.** Quadrants: quick wins (high/high — do now to build credibility), big bets (high value / lower feasibility — invest to enable), fill-ins (low value / easy — only if near-free), money pits (low/low — kill).
4. **Layer in foundations and dependencies.** Some low-standalone-value use cases build the data/platform that unlocks several others — sequence those early as enablers even if their direct score is modest (theory of constraints applies to the AI roadmap too).
5. **Sequence as a wave plan.** Wave 1: 2–3 quick wins that prove value and earn trust. Wave 2: foundation + first big bet. Wave 3: scale and transformational bets. Write the explicit kill list with reasons.

## Decision rules
- Weight **error tolerance and reversibility**: ship low-stakes, human-in-the-loop use cases first; defer autonomous/high-stakes ones until trust and guardrails exist.
- Sequence for *proof then scale* — an early, visible win unlocks budget and adoption far beyond its own value.
- Fund enablers (data/platform) ahead of the use cases that depend on them, even when their standalone score is unexciting.

## Output format
1. **Scoring table** — value ($) and feasibility (with the AI-specific sub-scores) per use case, on one basis.
2. **Value × feasibility matrix** — use cases placed; quadrants labeled.
3. **Dependency/foundation overlay** — what enables what.
4. **Wave plan** — Wave 1 quick wins → Wave 2 foundation + first big bet → Wave 3 scale, with the rationale.
5. **Kill list** — use cases cut now, with reasons.

## Quality bar
- Value scored on a consistent, quantified basis — not gut feel.
- Feasibility uses AI-specific dimensions (data, archetype maturity, error tolerance), not generic effort.
- The sequence funds enablers and early proof first, not just the highest raw scores.
- An explicit kill list exists — a real choice was made.

## Common failure modes
- "Pilot everything" — no cutline, so attention and credibility scatter and nothing scales.
- Ignoring data readiness, so a top-ranked use case stalls for months on data.
- Leading with a high-stakes autonomous use case that fails publicly and poisons appetite for the rest.
- Scoring value inconsistently (rigorous NPV for some, hand-waving for others).

## Pairs with
Consumes `ai-opportunity-mapping` (the register) and `ai-value-case` (the value scores), checks against `ai-readiness-assessment` (feasibility reality). Feeds `ai-poc-design` (design the Wave 1 pilots) and `transformation-roadmap` (the wave plan).

## Worked example
Input: 14 insurer use cases. Scored on common value basis and AI-specific feasibility. Claims-note drafting lands as a Wave-1 quick win — high value, mature generation tech, human-in-the-loop (low error stakes), data on hand. Autonomous claims settlement scores high value but low feasibility (high stakes, low error tolerance, regulatory) → deferred to Wave 3 with guardrails. The unified claims-data layer scores modest standalone value but enables 6 use cases → sequenced as the Wave-2 keystone. Wave plan: W1 = note drafting + fraud flag (prove value in 2 quarters); W2 = data layer + demand forecasting; W3 = agentic intake + assisted settlement. Five low/low use cases killed with reasons.
