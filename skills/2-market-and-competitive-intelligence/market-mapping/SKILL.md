---
name: market-mapping
description: Sizes the market and finds where attractive, under-served space sits. Use to size a market, segment demand, and locate white space for a where-to-play decision.
---

# Market Mapping

## When to use
- You need a defensible market size (for a board, an investment case, or entry decision).
- You're deciding *where to play* and need to see where attractive, under-served demand sits.
- A category is shifting and you need to see where the growth is moving.

## When not to use
- You need to group *your existing customers* for targeting → use `customer-segmentation`.
- You need to know where *profit* sits in the chain, not where demand sits → use `profit-pool-analysis`.

## Method
1. **Size TAM / SAM / SOM two ways and triangulate.**
   - *Top-down:* TAM = population of buyers × spend per buyer (or industry revenue × relevant share). Source each factor.
   - *Bottom-up:* SOM = (reachable accounts × win rate × ACV) built from your actual funnel/capacity.
   - The two methods should land within ~20–30% of each other. A large gap means a wrong assumption — find and reconcile it; don't average blindly.
2. **Segment demand by jobs-to-be-done,** not demographics alone. Two buyers in the same industry hiring the product for different jobs are different segments.
3. **Plot demand strength × supply quality** on a 2×2. High demand / weak existing supply = white space. This is where attractive, under-served space lives.
4. **Decompose growth by segment.** Split market growth into volume, price/mix, and substitution. Find where the *market itself* is moving, not just where it's big today — size attracts competition; growth + white space is where to win.
5. **Rank where-to-play options** on attractiveness (size × growth × margin) and your right-to-win (relative capability, access, cost position).

## Key formulas
- TAM (top-down) = # potential buyers × annual spend per buyer.
- SAM = TAM × (% reachable given geography/segment/regulation).
- SOM (bottom-up) = target accounts × realistic win rate × average contract value.
- Growth decomposition: ΔRevenue = ΔVolume + ΔPrice/Mix + ΔSubstitution.

## Decision rules
- Trust the *bottom-up* number for planning and capital; use top-down only as a sanity ceiling.
- State every estimate as a range with its key swing assumption, not a false-precision point ("$1.2B" hides more than "$0.9–1.4B, swinging on adoption rate").
- A big market that is shrinking or fully served beats a smaller market that is growing with white space — rank on *growth × white space*, not absolute size.

## Output format
1. **Market map** — segments laid out with size, growth, and current supply intensity.
2. **Triangulated size** — TAM/SAM/SOM as ranges, top-down vs bottom-up shown side by side with the reconciliation.
3. **White-space view** — the demand×supply 2×2 with the gaps marked.
4. **Growth decomposition** — where the market is moving and why.
5. **Ranked where-to-play options** — 2–3 beachheads, each with the size, the gap, and the right-to-win.

## Quality bar
- Every number is sourced and built from named factors — no unsourced "$X billion market" figures.
- Two independent methods that reconcile; show the build, not just the total.
- Ranges with swing assumptions, never false-precision point estimates.
- White space is *evidenced* (a real demand×supply gap), not asserted.

## Common failure modes
- Top-down only, anchored to an analyst headline number nobody can defend.
- Sizing the whole market when only the reachable slice (SOM) matters for the decision.
- Confusing a big market with an *attractive* one (ignoring growth, margin, and competition).

## Pairs with
Feeds `customer-segmentation` (sharpen the chosen segment), `competitive-intel` (who already occupies the white space), `go-to-market` (how to enter the beachhead), and `business-case-builder` (the SOM becomes the revenue ramp).

## Worked example
Input: a SaaS firm eyeing an adjacent category. Top-down: 40k mid-market firms × $30k average spend = $1.2B TAM. Bottom-up: 6k reachable accounts × 18% win rate × $28k ACV ≈ $30M SOM over the planning horizon; the methods reconcile once geography filters SAM to ~$420M. Demand×supply 2×2 shows the mid-market segment under-served by incumbents focused upmarket. Growth decomposition: the segment is growing 14%/yr, driven by substitution away from spreadsheets. Recommended beachhead: mid-market ops teams, where right-to-win is highest given existing product fit.
