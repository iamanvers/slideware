---
name: financial-modeling
description: Builds an integrated, driver-based three-statement financial model (P&L, balance sheet, cash flow) that ties out and flexes. Use to project financials, test scenarios, or underpin a valuation.
---

# Financial Modeling

## When to use
- You need a projection that links income statement, balance sheet, and cash flow and stays consistent.
- A valuation, fundraise, budget, or strategic plan needs a model others can audit and flex.
- You need to test scenarios/sensitivities on a coherent set of financials, not a single tab of numbers.

## When not to use
- You only need one project's incremental NPV → use `business-case-builder`.
- You only need per-unit economics → use `unit-economics`.

## Method
1. **Architect for clarity: inputs → calculations → outputs.** Separate assumption cells (one color), calculation cells, and output cells. Never hard-code a number inside a formula. A model others can't audit is a liability, not an asset.
2. **Build the P&L driver-based.** Revenue from real drivers (volume × price, or customers × ARPU with a retention/cohort build), not a blanket growth %. COGS and opex from their own drivers (headcount, unit cost). Down to EBITDA, EBIT, net income.
3. **Build the balance sheet and working-capital engine.** Working capital from days ratios (DSO, DIO, DPO), capex and the PP&E/depreciation roll-forward, debt schedule with interest. The balance sheet must *balance* every period — that's the integrity check.
4. **Build the cash flow statement and link the three.** Cash flow from operations (net income + D&A − ΔNWC), investing (capex), financing (debt/equity). Ending cash flows to the balance sheet; retained earnings flows from net income. The three statements must articulate — change one input and all three move consistently.
5. **Add scenarios, sensitivities, and checks.** A scenario switch (base/upside/downside), sensitivity tables on the key drivers, and explicit error checks (balance sheet balances, cash ties, no circularity breaks). Build the checks *in*, don't eyeball.

## Key formulas / integrity checks
- FCF = EBIT(1−tax) + D&A − capex − ΔNWC.
- ΔNWC from days: receivables = DSO/365×revenue; inventory = DIO/365×COGS; payables = DPO/365×COGS.
- Balance check: Assets = Liabilities + Equity, every period (build the row; it must be zero).
- Cash check: cash-flow-statement ending cash = balance-sheet cash; retained earnings_t = RE_{t−1} + net income − dividends.

## Decision rules
- Driver-based, never hard-coded growth. If a reviewer can't change an assumption and see the model respond correctly, it's not finished.
- The balance sheet balancing is non-negotiable — an unbalanced model is wrong somewhere, full stop.
- Keep terminal/forecast assumptions defensible and visible; don't bury a hockey stick in a hidden cell.

## Output format
1. **Assumptions sheet** — every driver, sourced, in one place, scenario-switchable.
2. **Three statements** — P&L, balance sheet, cash flow, fully linked.
3. **Supporting schedules** — working capital, debt, capex/depreciation.
4. **Outputs** — FCF, key ratios/margins, the metrics the decision needs.
5. **Scenarios, sensitivities & checks** — the switch, sensitivity tables, and the integrity-check row.

## Quality bar
- Inputs/calcs/outputs are separated; no hard-codes inside formulas.
- The three statements are genuinely linked and the balance sheet balances every period (check row shown).
- Driver-based throughout; assumptions are visible and sourced.
- Scenario/sensitivity capability is built in, with error checks, not bolted on.

## Common failure modes
- A "model" that's really a P&L with no balance sheet or cash flow (so it can't catch its own errors).
- Hard-coded numbers buried in formulas that no one can find or flex.
- An unbalanced balance sheet "plugged" to balance, hiding a real error.
- Untraceable circular references that silently break the answer.

## Pairs with
Feeds `valuation` (the FCF stream), `business-case-builder` and `capital-allocation` (the financial base case), and `scenario-planning`/`financial-modeling` scenarios. Driver assumptions come from `market-mapping`, `pricing-strategy`, `unit-economics`, and `cost-transformation`; outputs are stress-tested by `assumption-audit`.

## Worked example
Input: a 5-year plan for a growth company to support a fundraise. Architecture: a single colored assumptions tab feeds three linked statements. Revenue built from a cohort engine (new customers × ARPU × retention curve), not a flat growth rate. Working capital driven by DSO 45 / DIO 30 / DPO 60; capex on a PP&E roll-forward; a debt schedule with interest feeding the P&L. The balance-check row sits at zero every period; ending cash ties to the cash-flow statement. A scenario switch flips base/upside/downside, and a sensitivity table shows FCF vs churn and ARPU. The model outputs the FCF stream that `valuation` then discounts — auditable, balanced, and flexible, so the investor's analyst can stress it without it breaking.
