---
name: pricing-analytics
description: The quantitative mechanics of setting price — elasticity, conjoint, Van Westendorp, optimal-price math, discount break-even, and the realization waterfall. Use to actually set numbers, not just pricing strategy.
---

# Pricing Analytics

## When to use
- The pricing *strategy* is set and now you need the actual numbers — the price points, the elasticity, the discount rules.
- You need to estimate willingness to pay or price response from data (survey or transactional).
- Someone proposes a discount or price increase and you need the break-even volume math before they pull the trigger.

## When not to use
- You're still deciding the pricing model, structure, and where value sits → use `pricing-strategy` (this executes it).
- You're explaining a past margin move → use `margin-bridge`.

## Method
1. **Estimate demand response (elasticity).** From transactional history (regress quantity on price, controlling for seasonality/promo/competition) or experiments (A/B price tests). Price elasticity ε = %ΔQ ÷ %ΔP. |ε| < 1 = inelastic (you're likely under-priced); |ε| > 1 = elastic (price cuts may pay, increases may not).
2. **Measure willingness to pay.**
   - **Van Westendorp** (survey): ask the four price questions (too cheap / cheap / expensive / too expensive); the intersections give the optimal price point (OPP), indifference price (IPP), and the acceptable range (PMC–PME).
   - **Conjoint / discrete choice**: derive part-worth utilities, then WTP for a feature = (its utility) ÷ (the price coefficient). Best when buyers trade off features and price.
   - **Gabor-Granger** for a single product's demand curve at tested price points.
3. **Solve for the profit-maximizing price.** For constant elasticity, the optimal markup follows the **Lerner index**: (P − MC) ÷ P = 1 ÷ |ε|, i.e., P* = MC × |ε| ÷ (|ε| − 1) (valid for |ε| > 1). Walk the price–profit curve (margin per unit × volume at each price) and find the peak; don't trust a single formula blindly.
4. **Compute discount/price-change break-evens.** Before any move, the volume change required to hold contribution: **break-even %ΔQ = −%ΔP ÷ (CM% + %ΔP)** (CM% = contribution margin). This says how much volume a price cut must *gain* (or an increase can afford to *lose*) to be neutral.
5. **Quantify price realization (the waterfall).** Decompose list → invoice → pocket price across every leakage (off-invoice discounts, rebates, terms, freight) and size each. Recovering pocket-price leakage is usually faster and lower-risk than a list change.

## Key formulas
- Elasticity: ε = %ΔQ ÷ %ΔP.
- Optimal price (constant elasticity): P* = MC × |ε| ÷ (|ε| − 1); equivalently (P−MC)/P = 1/|ε|.
- Discount break-even volume: %ΔQ needed = −%ΔP ÷ (CM% + %ΔP). *(e.g., a 10% price cut at 40% CM needs +33% volume: −(−10%)/(40%−10%) = 10/30.)*
- Price-increase break-even: tolerable volume loss = %ΔP ÷ (CM% + %ΔP).
- Conjoint WTP for a feature = feature utility ÷ |price coefficient|.
- Pocket price = list − off-invoice discounts − rebates − terms/financing − freight.

## Decision rules
- Inelastic demand (|ε| < 1) is a near-certain signal of under-pricing — test an increase before assuming the market won't bear it.
- Never approve a discount without its break-even volume; high-margin products almost never recover the volume a discount requires.
- Prefer recovering pocket-price leakage over cutting list — it lifts realized price without a public price change customers can anchor to.

## Output format
1. **Demand response** — estimated elasticity by segment/product, with method and confidence.
2. **WTP evidence** — Van Westendorp / conjoint / Gabor-Granger output and the implied price band.
3. **Optimal price** — the profit-max point(s) from the price–profit curve, with the markup logic.
4. **Break-even table** — required volume change for the proposed price moves.
5. **Realization waterfall** — list→pocket with each leakage sized and the recovery opportunity.

## Quality bar
- Elasticity/WTP estimated from real data or experiments, with the method and its confidence stated — not asserted.
- The optimal price comes from the price–profit curve, not a single formula taken on faith.
- Every proposed price move carries its break-even volume.
- The realization waterfall quantifies each leakage, not just "we discount too much."

## Common failure modes
- Cost-plus pricing that ignores elasticity and WTP entirely.
- Approving discounts without break-even math, destroying contribution to "win" volume that never covers it.
- Confusing stated WTP (surveys) with revealed WTP (behavior) — triangulate, and weight behavior.
- A single blended elasticity hiding very different segment responses.

## Pairs with
Executes `pricing-strategy` and uses `customer-segmentation` (WTP per segment) and `unit-economics` (the margin floor). Break-evens feed `business-case-builder`; competitive price response is tested in `competitive-intel`/`war-gaming`; the waterfall is a `decision-memo` exhibit.

## Worked example
Input: a B2B product, list $1,000, 40% contribution margin, sales pushing a 10% discount to hit quota. Transactional regression gives segment elasticity: enterprise |ε| = 0.6 (inelastic), SMB |ε| = 1.8 (elastic). Discount break-even: a 10% cut needs +33% volume (10 ÷ (40−10)) just to stay neutral — implausible in enterprise, so the discount destroys contribution there. Optimal-price check on SMB (|ε|=1.8): P* = MC × 1.8/0.8; with MC $600 → ~$1,350 indicated, suggesting SMB is *under*-priced, not over-priced. Realization waterfall shows pocket price 41% below list once rebates and terms are counted. Recommendation: hold enterprise price (kill the blanket discount), test a price increase in inelastic enterprise, and recover the off-invoice leakage before touching list anywhere.
