---
name: cost-transformation
description: Finds and sequences sustainable cost reduction by activity, driver, and should-cost — not across-the-board cuts. Use to improve margin or fund growth without breaking the business.
---

# Cost Transformation

## When to use
- Margin is below peer and a structural, defensible cost-out is needed (not a panic cut).
- You need to self-fund growth or a transformation by freeing up cost.
- Leadership is reaching for an across-the-board % cut and you want a smarter, targeted alternative.

## When not to use
- The issue is price/revenue realization, not cost → use `pricing-strategy`.
- You're explaining a margin change between periods → use `margin-bridge`.

## Method
1. **Build the cost baseline cleanly.** Cost by category, by activity, and by business unit, mapped to drivers (what makes each cost go up or down). A baseline that's only by GL account hides the levers — cut by *activity and driver*, not by ledger line.
2. **Benchmark and find the gap.** Compare cost ratios (cost as % of revenue, cost per unit/transaction/FTE) to peers and to internal best-in-class. The gap to a credible benchmark sizes the prize; "we feel bloated" doesn't.
3. **Apply the right lens per cost type:**
   - **Zero-based** for discretionary/overhead — justify from zero, not last year ± %.
   - **Should-cost** for procurement/COGS — build what it *ought* to cost from inputs (materials, labor, overhead, margin) and negotiate to it.
   - **Spans-and-layers** for org cost — measure management layers and spans of control vs benchmark; de-layering is often the largest, fastest lever.
   - **Make-vs-buy / footprint** for structural cost — outsource non-differentiating activities, consolidate sites.
4. **Triage savings on size × ease × risk-to-business.** Separate quick wins (fast, low risk) from structural moves (large, slower, harder). Critically, flag cuts that would damage differentiating capabilities or growth — *don't cut muscle*.
5. **Sequence and harden.** Build the initiative list with owners, savings, costs-to-achieve, and timing; hand to `value-realization` so savings are baselined, net, and don't leak back.

## Key formulas
- Cost gap to benchmark = (current cost ratio − benchmark cost ratio) × revenue (or volume).
- Should-cost = Σ (input quantities × should-prices) + reasonable conversion cost + fair margin.
- Span of control = direct reports per manager; layers = levels from CEO to front line (benchmark spans ~6–8, fewer layers is usually better).
- Net savings = gross savings − cost-to-achieve − reinvestment/leakage (track run-rate).

## Decision rules
- Cut by activity and driver, never across-the-board %. A flat cut starves the strong to subsidize the weak and damages capability indiscriminately.
- Protect differentiating capabilities and growth engines explicitly — distinguish "fat" from "muscle" before cutting.
- Bank savings net and run-rate; gross savings that get reinvested or leak back didn't happen (enforce via `value-realization`).

## Output format
1. **Cost baseline** — by category, activity, and driver, mapped to the org.
2. **Benchmark gap** — cost ratios vs peer/best-in-class, sizing the prize.
3. **Lever analysis** — ZBB / should-cost / spans-and-layers / make-vs-buy findings per cost block.
4. **Initiative list** — each: lever | gross saving | cost-to-achieve | risk-to-business | owner | timing.
5. **Sequenced plan** — quick wins → structural, with the protected "do not cut" list called out.

## Quality bar
- Driver-based and benchmarked — the prize is sized against a credible comparator, not a feeling.
- Targeted by activity, with an explicit "do not cut" list protecting differentiating capability.
- Savings are net of cost-to-achieve and tracked run-rate (not gross, not one-time dressed as recurring).
- Each initiative has an owner and a mechanism, not a top-down target handed down.

## Common failure modes
- Across-the-board % cuts that damage capability and quietly reverse within a year.
- Cutting growth/differentiating muscle to hit a short-term number.
- Gross savings claimed, then eaten by reinvestment or leakage with no run-rate tracking.

## Pairs with
Uses `margin-bridge` (where margin went) and `operating-model-design` (spans-and-layers, make-vs-buy). Savings flow into `business-case-builder` / `capital-allocation` (fund growth) and are hardened by `value-realization`; reorg politics handled via `stakeholder-alignment`.

## Worked example
Input: a manufacturer 6 margin points below peer. Baseline by activity + driver, benchmarked: ~3 pts sit in procurement (should-cost shows direct materials 12% above a clean-sheet build), ~2 pts in overhead (zero-based review finds discretionary spend never re-justified), ~1 pt in org (spans-and-layers shows 9 layers vs a 6-layer benchmark and spans of 3.5). Levers: should-cost renegotiation on three categories, ZBB on overhead, de-layering two management levels. Protected: the R&D and key-account teams (differentiating). Triaged: ~2 pts quick win (overhead + procurement quick hits in 2 quarters), ~4 pts structural over 12–18 months. All initiatives owned, net of cost-to-achieve, and tracked run-rate via the value ledger — replacing the proposed flat 5% cut.
