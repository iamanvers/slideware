---
name: margin-bridge
description: Explains a change in profit or margin between two periods (or vs plan/peer) by decomposing it into price, volume, mix, cost, and FX drivers. Use to answer "why did margin move?"
---

# Margin Bridge

## When to use
- Profit or margin moved between periods (or vs budget, or vs a peer) and leadership wants to know *why*.
- A P&L variance is being blamed on the wrong thing and you need the real decomposition.
- You need a waterfall that walks from last year's profit to this year's, driver by driver.

## When not to use
- You're hunting for cost-reduction opportunities going forward → use `cost-transformation`.
- You're testing per-unit profitability → use `unit-economics`.

## Method
1. **Define the two anchors and the metric.** From-period and to-period (or actual vs plan, or you vs peer), and exactly what's being bridged (gross margin %, EBIT $, contribution). Be precise — bridging the wrong metric explains the wrong thing.
2. **Decompose into clean, non-overlapping effects.** The standard set: **price** (Δ price × volume), **volume** (Δ units × prior margin), **mix** (shift toward higher/lower-margin products/customers/channels), **cost/input** (Δ unit cost × volume), and **FX / other**. Each effect must be isolated so they sum exactly to the total change (MECE — no double-counting).
3. **Compute each effect with a reconciling convention.** The clean choice that ties out exactly: measure **volume at the prior unit margin** and **price and cost at the current volume (Q₁)**. This leaves no residual (proof below). If you instead measure price at prior volume (Q₀), you must add a separate **price×volume interaction** bar — otherwise the bridge won't sum to the total. Never silently drop the interaction term.
4. **Build the waterfall.** Start bar = prior profit/margin, one bar per driver (up/down), end bar = current. The visual instantly shows which driver dominated and which offset which.
5. **Read the "so what."** Distinguish drivers within management's control (price, mix, cost discipline) from those outside (FX, input inflation), and name the action implied — e.g., "the margin fall is mix, not price erosion, so the fix is portfolio steering, not a price increase."

## Key formulas (the convention that reconciles exactly)
- **Volume effect** = (Q₁ − Q₀) × (P₀ − C₀)  [ΔUnits at the *prior* unit margin].
- **Price effect** = (P₁ − P₀) × Q₁  [ΔPrice at *current* volume].
- **Cost/input effect** = −(C₁ − C₀) × Q₁  [ΔUnit cost at *current* volume; negative if costs rose].
- **Mix effect** is a refinement *inside* the volume effect for a multi-product book: split it into pure volume (ΔtotalQ × average prior margin) + mix (Σ share-shiftᵢ × Q₁ × (marginᵢ,₀ − avg margin₀)).
- **Reconciliation (exact):** volume + price + cost = ΔProfit, because
  Q₁(P₁−C₁) − Q₀(P₀−C₀) = (Q₁−Q₀)(P₀−C₀) + (P₁−P₀)Q₁ − (C₁−C₀)Q₁. The three terms sum to the total with **zero residual** — verify this identity holds in your build. (Using Q₀ for price instead introduces a −(Q₁−Q₀)(P₁−P₀) interaction term that must be shown as its own bar.)

## Decision rules
- Effects must reconcile to the total with no unexplained residual; a bridge that doesn't add up is wrong somewhere.
- Separate mix from price — they're constantly confused, and the remedy is opposite (mix → portfolio steering; price → pricing action). This distinction is the whole value of the analysis.
- Flag controllable vs uncontrollable drivers so management acts on what it can actually move.

## Output format
1. **Anchors & metric** — the two periods/benchmarks and exactly what's bridged.
2. **Driver decomposition** — price / volume / mix / cost / FX-other, each quantified.
3. **Waterfall** — prior → drivers → current, reconciled (residual shown ≈ 0).
4. **Controllable vs not** — which drivers management owns.
5. **So-what** — what actually moved margin and the action it implies.

## Quality bar
- The bridge reconciles exactly — effects sum to the total change, residual ≈ 0.
- Price and mix are cleanly separated, not lumped together.
- Controllable vs uncontrollable drivers are distinguished.
- Ends in the action implied, not just a decomposition.

## Common failure modes
- Lumping mix into "price," leading to a pricing action when the real issue was a portfolio shift.
- A bridge that doesn't reconcile (an unexplained residual nobody chases down).
- Inconsistent conventions across drivers, so the effects double-count or miss.
- Stopping at the numbers without naming the controllable lever.

## Pairs with
Feeds `cost-transformation` (where cost-driven erosion is), `pricing-strategy` (if price/mix is the issue), and `growth-barriers`/`situation-assessment` (diagnosing performance). The waterfall is a core `design-guide` exhibit; results land in `decision-memo`.

## Worked example
Input: EBIT margin fell from 16% to 12% YoY and the CEO assumed "we discounted too hard." Bridge (reconciled to the full 4-pt drop): price −0.5 pt (modest, not the culprit), volume +0.3 pt, **mix −2.6 pts** (rapid growth in a low-margin channel diluted the average), input cost −1.4 pts (raw-material inflation), FX +0.2 pt. So-what: the margin fall is overwhelmingly **mix and input cost**, not price/discounting. Controllable lever is portfolio steering (reweight toward the high-margin channel) plus should-cost work on inputs — *not* a price increase, which would have attacked a driver that barely moved. The CEO's instinct was wrong, and the bridge proved it in one waterfall.
