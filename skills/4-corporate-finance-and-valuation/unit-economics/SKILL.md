---
name: unit-economics
description: Establishes whether the business makes money on a single unit/customer — contribution margin, CAC, LTV, payback, and the path to profitability. Use to test commercial viability and scalability.
---

# Unit Economics

## When to use
- You need to know if the business makes money on *one* customer/unit before scaling it.
- Growth is fast but profitability is elusive, or burn is high and you need to find why.
- A go-to-market, pricing, or fundraising decision hinges on whether the model actually scales.

## When not to use
- You're valuing the whole company → use `valuation`.
- You're explaining a period-over-period margin change → use `margin-bridge`.

## Method
1. **Define the unit.** A customer, an account, an order, a ride, a subscription — the smallest thing that repeats. Get this right; the wrong unit produces nonsense.
2. **Build the contribution margin per unit.** Revenue per unit − variable/direct costs (COGS, payment fees, support, fulfilment) = contribution margin. This is what's left to cover fixed costs and CAC. A negative contribution margin means scaling *loses* money faster — stop and fix the model.
3. **Compute CAC and CAC payback.** Fully-loaded customer acquisition cost (all S&M ÷ new customers), and payback = CAC ÷ monthly contribution per customer. Payback tells you how long capital is tied up before a customer turns cash-positive.
4. **Compute LTV and LTV/CAC.** LTV = contribution margin per period × average customer lifetime (or contribution ÷ churn rate for recurring). LTV/CAC measures whether acquisition creates value. Use *contribution-margin-based* LTV, not revenue-based (revenue LTV flatters everything).
5. **Find the path to profitability.** Identify the levers (raise price, cut CAC, improve retention, raise contribution margin) and the scale at which fixed costs are covered. Show what has to change for the unit to fund the company.

## Key formulas
- Contribution margin = revenue per unit − variable cost per unit (also as a %).
- CAC = total fully-loaded S&M ÷ new customers acquired in the period.
- CAC payback (months) = CAC ÷ monthly contribution margin per customer.
- LTV (recurring) = (ARPU × gross/contribution margin %) ÷ churn rate; or contribution per period × average lifetime.
- LTV/CAC ratio; target ≥ 3:1 with CAC payback < 12 months (healthy SaaS rule of thumb).

## Decision rules
- Use *contribution-margin* LTV, never revenue LTV — the latter hides the cost of serving.
- LTV/CAC ≥ 3 with payback < 12 months ≈ healthy and scalable; LTV/CAC < 1 means every new customer destroys value — don't scale it.
- Watch the churn assumption in LTV: small churn changes swing LTV massively (LTV ∝ 1/churn). Use observed cohort churn, not hope.

## Output format
1. **Unit definition** — what one unit is.
2. **Contribution economics** — revenue, variable cost, and contribution margin per unit (and %).
3. **Acquisition economics** — CAC and CAC payback.
4. **Lifetime value** — LTV (contribution-based), churn assumption, and LTV/CAC.
5. **Path to profitability** — the binding lever(s) and the scale/changes needed to cover fixed cost.

## Quality bar
- LTV is contribution-margin-based with a real (cohort-observed) churn rate, not revenue-based with a guessed lifetime.
- CAC is fully loaded (all S&M, not just paid media).
- The verdict is explicit: does this scale or not, and what has to change.
- The fragile assumptions (churn, payback) are flagged with their sensitivity.

## Common failure modes
- Revenue-based LTV that ignores cost-to-serve and flatters the model.
- Under-counted CAC (paid media only, ignoring sales salaries and overhead).
- An optimistic churn/lifetime assumption that inflates LTV beyond reality.
- Celebrating top-line growth on negative contribution margin ("we lose a bit on each one but make it up on volume").

## Pairs with
Underpins `go-to-market` (motion viability), `pricing-strategy` (margin floor), and `business-case-builder` (the per-unit drivers). Feeds `growth-barriers` (if the constraint is economic) and `customer-segmentation` (economics by segment).

## Worked example
Input: a subscription business burning cash despite 80% YoY growth. Unit = a paying customer. Contribution: $1,200 ARPU × 72% contribution margin = $864/yr ($72/mo). CAC fully loaded = $1,150 (founders had been counting only $600 of paid media). Payback = $1,150 ÷ $72 ≈ 16 months — too long, capital tied up. LTV: monthly churn 3% → ~33-month lifetime → contribution LTV ≈ $2,400; LTV/CAC ≈ 2.1 (below the 3 threshold). Verdict: marginal, not yet scalable. Binding levers: cut blended CAC (over-reliant on expensive paid) and reduce early churn (cohort data shows month-1–3 churn drives the bulk). Fixing churn to 2% lifts LTV to ~$3,600 and LTV/CAC to 3.1 — the unlock, not more ad spend.
