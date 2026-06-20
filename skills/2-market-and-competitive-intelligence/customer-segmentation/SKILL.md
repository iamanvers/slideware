---
name: customer-segmentation
description: Produces decision-useful segments instead of generic personas. Use to group customers in a way that changes where you play, what you build, and how you sell.
---

# Customer Segmentation

## When to use
- You need to focus product, pricing, or go-to-market on the segments that matter.
- Your current "segments" are demographic labels that don't predict behavior or value.
- You're choosing a wedge/beachhead and need to know which customers to win first.

## When not to use
- You're sizing the whole external market → use `market-mapping`.
- You need to translate segments into a sales motion and channels → use `go-to-market`.

## Method
1. **Segment on needs and behavior (jobs-to-be-done),** not just firmographics/demographics. The test of a good segmentation axis: it *predicts* different buying behavior, willingness to pay, or cost-to-serve. If two segments behave identically, the cut is cosmetic.
2. **Enforce MECE.** Every customer lands in exactly one segment (mutually exclusive) and the segments cover the whole base (collectively exhaustive). Check for orphans and overlaps explicitly.
3. **Score each segment on two axes:** *attractiveness* (size × growth × willingness-to-pay × retention) and *right-to-win* (product fit, cost-to-serve, access, switching cost you can create). 
4. **Profile the chosen segments** so they're operational: the job they hire you for, the trigger to buy, who decides, the buying process, what they'll pay, and what it costs to serve them.
5. **Name the wedge.** Pick the one or two segments to build the strategy around and state explicitly which segments you are *choosing not to serve well*.

## Decision rules
- A segment is only real if it changes a decision (what you build, price, or how you sell). If acting on it would change nothing, merge or drop it.
- Prioritize high-attractiveness × high-right-to-win. A huge segment you can't win is a trap; a smaller one you dominate is a beachhead.
- Cost-to-serve belongs in attractiveness — a high-revenue, high-WTP segment that is expensive to serve may be less attractive than a quiet, sticky one.

## Output format
1. **Segmentation scheme** — the axis/axes used and *why they predict behavior*, with the MECE check stated.
2. **Segment profiles** — for each: size, growth, the job-to-be-done, WTP, cost-to-serve, retention, right-to-win.
3. **Attractiveness × right-to-win 2×2** — segments placed.
4. **Priorities** — the 1–2 wedge segments, and the explicit "not now / not us" segments.
5. **So-what** — what each priority implies for product, pricing, and go-to-market.

## Quality bar
- Needs/behavior-based axes that *predict* something — not "SMB / Mid / Enterprise" relabeled.
- MECE is checked, not assumed.
- Every segment has a WTP and a cost-to-serve, not just a size.
- The output names who you will *not* serve — a segmentation with no de-prioritization made no choice.

## Common failure modes
- Personas with names and stock photos that don't change any decision.
- Demographic/firmographic cuts that don't predict behavior or value.
- Too many segments (8+) so none gets real focus, or overlapping segments that violate MECE.

## Pairs with
Builds on `market-mapping`. Feeds `pricing-strategy` (price to segment WTP), `go-to-market` (motion per segment), `value-realization`, and `kpi-architect` (segment-level metrics).

## Worked example
Input: a broad SMB software base treated as one undifferentiated group. Re-cut by job-to-be-done reveals four segments; the sharpest split is "compliance-driven" buyers (buy to pass an audit, high WTP, low price sensitivity, sticky) vs "efficiency-driven" buyers (buy to save time, price-sensitive, churn-prone). They behave oppositely on price and retention — a real cut. On the 2×2, compliance-driven is high-attractiveness (high WTP, high retention) and high-right-to-win (existing audit features). Chosen wedge: compliance-driven mid-market; efficiency-driven micro-SMB explicitly de-prioritized as a low-margin, high-churn trap.
