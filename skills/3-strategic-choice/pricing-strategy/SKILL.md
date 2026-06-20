---
name: pricing-strategy
description: Diagnoses pricing power and produces a concrete pricing action plan. Use when discounting is heavy, monetization is unclear, or value and price have drifted apart.
---

# Pricing Strategy

## When to use
- Discounting is heavy or inconsistent and margin is leaking.
- You're launching/repricing and need a structure (tiers, fences, metric) not just a number.
- You suspect you're leaving money on the table or under-pricing relative to value delivered.

## When not to use
- The question is unit profitability and contribution, not list/realized price → use `unit-economics`.
- You need full demand sizing and white space → use `market-mapping`.

## Method
1. **Anchor to value, not cost.** Estimate the economic value to the customer (EVC): the next-best alternative's price + the quantified value of your differentiation (time saved, risk reduced, revenue gained). Cost sets your floor; value sets the ceiling; competition sets the reference point. Price lives between floor and ceiling — never cost-plus by default.
2. **Estimate willingness to pay by segment.** Use Van Westendorp (too cheap / cheap / expensive / too expensive) or conjoint/menu tests where data allows; otherwise infer WTP from win/loss, discount-approval data, and historical price-change response. Different segments have different WTP — one price for all leaves money on the table.
3. **Model price–volume sensitivity.** Estimate elasticity from history or tests. Profit-max price balances margin per unit against volume lost. Walk the curve, don't guess the peak.
4. **Diagnose the leak.** Build a **price waterfall**: list price → invoice price (off-invoice discounts) → pocket price (rebates, terms, freight, payment) → pocket margin. The gap between list and pocket is where realized price is lost; quantify each leak.
5. **Translate into a pricing action plan:** the structure (tiers/packaging), the value metric you charge on, fences (what separates tiers/segments), and discount discipline (floors, approval thresholds, escalation rules).

## Key formulas
- EVC = next-best-alternative price + value of differentiation − cost of switching to you.
- Pocket price = list − off-invoice discounts − rebates − terms/financing − freight.
- Pocket margin = pocket price − cost-to-serve.
- Profit-max condition: margin × volume is maximized where marginal revenue = marginal cost; near it, %Δvolume from a price move should be smaller than %Δprice × (price ÷ margin) to be accretive.

## Decision rules
- Charge on the value metric that scales with the value the customer gets (seats, usage, outcomes) — the wrong metric caps your upside no matter the number.
- For a high-margin product, holding price and losing some volume usually beats discounting to hold volume — check the break-even volume change before any discount.
- Fix the pocket-price leak before touching list price; recovering 2 pts of leakage often beats a list increase customers will fight.

## Output format
1. **Pricing diagnosis** — where value, WTP, and current price diverge; the price waterfall with leaks sized.
2. **Segment WTP view** — value and willingness to pay by segment.
3. **Recommended structure** — value metric, tiers/packaging, fences.
4. **Discount discipline** — floors, approval thresholds, and the governance to hold them.
5. **Sequenced action plan** — quick wins (leak recovery) → structural reprice → migration plan for existing customers.

## Quality bar
- Value-based, not cost-plus; EVC is actually estimated.
- A real price waterfall with each leak quantified — not just "we discount too much."
- Segment-level WTP, not one blended number.
- Discount discipline is specific (floors, thresholds, owners), not "be more disciplined."

## Common failure modes
- Cost-plus pricing that ignores value and leaves the ceiling untouched.
- Cutting list price when the leak is in pocket (rebates/terms), so the cut compounds the loss.
- One price for all segments, capping upside on high-WTP buyers.

## Pairs with
Builds on `customer-segmentation` (WTP per segment) and `unit-economics` (margin floor). Feeds `business-case-builder` (price as a driver), `competitive-intel` (anticipate price retaliation), and `value-realization`.

## Worked example
Input: an enterprise software firm discounting 35% on average to close deals. Price waterfall shows list → pocket erosion of 41% once multi-year rebates and payment terms are counted — far worse than the visible 35%. Segment WTP: enterprise buyers value the compliance module at ~3× what they pay; SMB is genuinely price-sensitive. Diagnosis: under-priced on enterprise value, over-discounted via off-invoice terms. Plan: (1) recover leakage with a rebate cap and a 28% list-discount floor requiring VP approval; (2) move to value tiers with compliance fenced into the top tier; (3) migrate existing enterprise accounts at renewal. Modeled margin recovery ≈ 6–9 pts without raising list.
