---
name: assumption-audit
description: Surfaces the unstated beliefs a strategy rests on and stress-tests the ones that matter. Use before committing to a plan, or when a recommendation feels fragile or too confident.
---

# Assumption Audit

## When to use
- A strategy or business case is about to be approved and you want to know where it breaks.
- The logic feels too clean, or the upside depends on a few heroic numbers.
- A board/investment committee will ask "what would have to be true?" — answer it first.

## When not to use
- You're testing against a live adversary's reactions → use `war-gaming`.
- You're exploring long-horizon external uncertainty with multiple futures → use `scenario-planning`.

## Method
1. **Build the assumption register.** List every belief the plan needs to be true: market (size, growth, willingness to pay), competitive (rivals won't respond), execution (we can build/hire/ship on time), financial (margins, attach, ramp), behavioral (customers/channel will switch). Force out the *implicit* ones — the dangerous assumptions are the ones nobody wrote down.
2. **Map importance × confidence.** Plot each assumption on *how much the case depends on it* (importance) vs *how sure we are it's true* (confidence). The **high-importance / low-confidence** quadrant is where the strategy is actually fragile — everything else is noise or already safe.
3. **Grade the evidence A–F.** A = hard data, directly observed; C = analogy/benchmark; F = assertion/hope. Grade is independent of how much you *like* the assumption.
4. **Design kill-shot tests.** For each fragile assumption, design the cheapest test that could *disprove* it (not confirm it). Define the pass/fail threshold *before* running it. Order tests by (information value ÷ cost).
5. **Write a pre-mortem.** Assume it's 18 months later and the strategy failed. Narrate the most likely failure story in two paragraphs. The fragile assumptions usually appear as the villain — confirming the register.

## Decision rules
- Rank fragility by **importance × (1 − confidence)**. Work the top 2–3; ignore the rest.
- An assumption graded D or F that sits in the high-importance quadrant is a *gate*: the decision should be conditional on testing it, not made before.
- Test to *falsify*. A test designed to confirm proves nothing; design the experiment that would make you abandon the plan.

## Output format
1. **Assumption register** — table: assumption | importance (H/M/L) | confidence (H/M/L) | evidence grade (A–F) | source.
2. **Fragility map** — the importance×confidence 2×2 with assumptions placed; the danger quadrant called out.
3. **Top 2–3 load-bearing assumptions** — the ones the whole case rests on.
4. **Test plan** — for each fragile assumption: the kill-shot test, the pre-set pass/fail threshold, the cost, and the time to result.
5. **Pre-mortem** — the two-paragraph failure narrative.

## Quality bar
- Surface the *unstated* assumptions — a register that only restates what's already in the deck adds nothing.
- Tests must be falsifiable with a pre-committed threshold. "Do more research" is not a test.
- Grade honestly: the most-loved assumption is often the worst-evidenced.

## Common failure modes
- Listing 30 assumptions and stress-testing none (no prioritization).
- Designing confirmation-seeking tests instead of disconfirming ones.
- Grading on conviction rather than evidence.

## Pairs with
Stress-tests the output of `strategic-options`, `business-case-builder`, `market-mapping`, and `commercial-due-diligence`. The fragile assumptions become risks in `risk-mitigation` and gates in `value-realization`.

## Worked example
Input: a market-entry plan projecting break-even in year 2. Register surfaces an unstated belief: "we acquire customers through partner channels at $400 CAC." It sits high-importance / low-confidence and grades D — based on one analog deal, not our own data. The whole case's break-even date depends on it. Kill-shot test: run a 6-week paid pilot with two partners; fail threshold = blended CAC > $700. Pre-mortem: "We launched assuming partner economics that never materialized; CAC ran 2× and we burned the runway before the channel matured." Decision reframed as conditional on the pilot.
