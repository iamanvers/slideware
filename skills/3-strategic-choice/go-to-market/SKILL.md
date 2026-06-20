---
name: go-to-market
description: Designs how to reach, win, and keep customers in a chosen segment — motion, channels, coverage, and economics. Use to turn a where-to-play choice into a how-to-win commercial engine.
---

# Go-to-Market

## When to use
- You've chosen a segment/market and need the commercial model to win it (motion, channels, coverage, pricing-to-sell).
- A product is built but not selling efficiently — CAC is too high or the motion doesn't fit the buyer.
- You're entering a new segment/geography and need an entry plan, not just a sales target.

## When not to use
- You're still choosing the segment → use `customer-segmentation` / `market-mapping`.
- The question is the price level/structure itself → use `pricing-strategy`.

## Method
1. **Anchor on the buyer and the buying process.** For the target segment (from `customer-segmentation`): the job-to-be-done, who decides, the buying committee, the trigger to buy, and the decision journey. The motion must fit how the customer actually buys — not how you prefer to sell.
2. **Choose the sales motion to fit deal economics.** Match motion to ACV and complexity: product-led/self-serve (low ACV, simple), inside sales (mid ACV), field/enterprise sales (high ACV, complex committee), or channel/partner-led (reach/scale). The wrong motion for the price point destroys unit economics (e.g., field sales on a $5k product).
3. **Design channels and coverage.** Direct vs partner vs marketplace; territory/account coverage model; the routes that reach the buyer at acceptable cost. Map the full funnel: demand gen → qualification → conversion → onboarding → expansion.
4. **Validate the economics.** Check CAC, CAC payback, and LTV/CAC for the motion (`unit-economics`). A motion that doesn't pay back within the segment's tolerance isn't viable, however well it sells.
5. **Build the entry/scale plan.** Beachhead first (concentrate to win a reference base), then expand; the enablement, content, and metrics to run it; and the 90-day proof. Sequence for proof-then-scale, not land-everywhere-at-once.

## Key formulas
- CAC = fully-loaded sales & marketing spend ÷ new customers acquired.
- CAC payback = CAC ÷ (monthly gross margin per customer), in months.
- LTV/CAC = (ARPU × gross margin × average lifetime) ÷ CAC; target ≥ 3:1, payback < 12 months for healthy SaaS.
- Magic number / sales efficiency = net new ARR ÷ prior-period S&M spend.

## Decision rules
- Fit the motion to the deal size: the cost of the sales motion must be a small fraction of the lifetime gross margin it generates.
- Win a beachhead before expanding — concentrated reference customers in one segment beat thin presence across five.
- If CAC payback exceeds the segment's tolerance, fix the motion/channel before scaling spend; scaling a broken motion just loses money faster.

## Output format
1. **Buyer & buying process** — decision-maker, committee, trigger, journey for the target segment.
2. **Sales motion** — the chosen motion and why it fits the deal economics.
3. **Channel & coverage model** — direct/partner/marketplace, territory/account coverage, the funnel.
4. **GTM economics** — CAC, payback, LTV/CAC by motion, with the viability check.
5. **Entry/scale plan** — beachhead → expansion sequence, enablement, metrics, 90-day proof.

## Quality bar
- The motion is matched to deal economics and the buyer's actual process — not a generic "build a sales team."
- Unit economics (CAC payback, LTV/CAC) validate the model, with real numbers.
- A beachhead-first sequence, not a simultaneous everywhere launch.
- Channel choice is justified by reach-at-cost, not by what's fashionable.

## Common failure modes
- Mismatched motion (expensive field sales on a low-ACV product, or self-serve on a complex enterprise sale).
- Scaling spend before the motion's payback is proven.
- Designing the sale around the seller's preference instead of the buyer's journey.

## Pairs with
Follows `customer-segmentation`, `market-mapping`, and `pricing-strategy`. Relies on `unit-economics` (the viability math). Feeds `business-case-builder` (the revenue ramp), `kpi-architect` (funnel metrics), and `transformation-roadmap` (the rollout).

## Worked example
Input: a $15k-ACV B2B product currently sold by an expensive field team with 14-month CAC payback. Buyer analysis: a 3-person committee (ops lead decides, IT and finance influence), triggered by a compliance deadline. Mismatch found: field sales is too costly for a $15k deal. Redesigned motion: inside sales + product-led trial for qualification, partners for reach into regulated verticals. Reworked economics: CAC drops, payback to ~8 months, LTV/CAC to 3.4:1. Plan: beachhead in one regulated vertical to build references (90-day proof = 10 reference logos), then expand to adjacent verticals via the partner channel. Field sales reserved only for the rare 6-figure expansion.
