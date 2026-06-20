---
name: problem-structuring
description: Turns a fuzzy question into a hypothesis-driven, MECE issue tree and a prioritized workplan. Use right after framing to structure the problem before any analysis begins.
---

# Problem Structuring

## When to use
- The question is agreed but the path to answer it isn't — you need to decompose it before analyzing.
- A team is about to "go gather data" without a hypothesis (the surest route to boiling the ocean).
- You need a workplan that says exactly which analyses to run, in what order, to resolve the decision.

## When not to use
- You don't yet have the factual baseline or the right question → run `situation-assessment` first.
- The problem is already structured and you're choosing among options → use `strategic-options`.

## Method
1. **State the core question as a single, decision-oriented problem statement.** Specific, measurable, and bounded ("How can we restore EBIT margin from 9% to 14% within 18 months without losing share?"), not "improve profitability."
2. **Build a MECE issue tree.** Decompose the question into sub-questions that are mutually exclusive and collectively exhaustive. Choose the decomposition logic that fits: a **lever/driver tree** (math: margin = revenue − cost, decomposed down), a **conceptual framework** (e.g., 3Cs, value chain), or a **hypothesis tree**. Each branch should be a question that, if answered, helps answer its parent.
3. **Attach a hypothesis to each branch (hypothesis-driven).** Don't gather data neutrally; state what you *believe* the answer is, then design analysis to confirm or kill it. This is the single biggest accelerator of an engagement.
4. **Prioritize branches by impact × ease.** Not every branch deserves equal effort. Identify the load-bearing branches (where the answer most likely lives and most moves the decision) and de-prioritize the rest.
5. **Write the workplan.** For each priority branch: the hypothesis, the analysis that would confirm/kill it, the data needed, the source, the owner, and the end date. This is the "ghost deck" / analysis plan that drives the whole engagement.

## Decision rules
- MECE is the discipline: no overlaps (or you double-count effort) and no gaps (or you miss the answer). Test every level.
- Be hypothesis-led, not data-led. Data-gathering without a hypothesis expands infinitely; a hypothesis tells you exactly what data ends the question.
- Prioritize ruthlessly. The 80/20 branch — the one analysis that resolves most of the uncertainty — runs first.

## Output format
1. **Problem statement** — one decision-oriented sentence with the target and constraint.
2. **Issue tree** — the MECE decomposition (state which logic: driver / framework / hypothesis).
3. **Hypotheses** — the believed answer on each priority branch.
4. **Prioritization** — which branches are load-bearing (impact × ease) and which are parked.
5. **Workplan** — per priority branch: hypothesis | analysis | data & source | owner | due date.

## Quality bar
- The tree is genuinely MECE — checked for overlaps and gaps, not just drawn.
- Every priority branch carries a falsifiable hypothesis and the specific analysis that resolves it.
- The workplan names analyses and data, not vague "research workstreams."
- Prioritized — it's obvious which one analysis to run first and why.

## Common failure modes
- A topic tree (lists of areas) instead of a question tree with hypotheses.
- Non-MECE branches that overlap (wasted effort) or leave gaps (missed answer).
- "Go collect all the data" with no hypothesis, leading to boiling the ocean.

## Pairs with
Follows `situation-assessment` (the framed question). Directs which analysis skills to invoke — `market-mapping`, `profit-pool-analysis`, `unit-economics`, `cost-transformation`, etc. — and in what order. The synthesized answer feeds `narrative-builder` and `decision-memo`.

## Worked example
Input: "How do we restore EBIT margin from 9% to 14% in 18 months?" Driver tree: margin gap = revenue levers (price, mix, volume) + cost levers (COGS, opex, footprint). MECE decomposition isolates four branches. Hypotheses: (1) *price realization* leaks 4 pts via uncontrolled discounting [likely large — run first]; (2) overhead is 2 pts above peer benchmark; (3) mix is fine; (4) COGS is at benchmark. Prioritization: branches 1 and 2 are load-bearing (~5 of the 5-pt gap); 3 and 4 parked. Workplan: branch 1 → price-waterfall analysis (pull discount-approval and invoice data, FP&A owns, 2 weeks); branch 2 → spans-and-layers + opex benchmark (HR + finance data, 3 weeks). The engagement now has a spine before anyone touches a spreadsheet.
