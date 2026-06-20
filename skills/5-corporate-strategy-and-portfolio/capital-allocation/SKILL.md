---
name: capital-allocation
description: Decides how a company deploys cash across reinvestment, M&A, debt paydown, and returns to shareholders to maximize long-run value per share. Use for corporate-level capital strategy.
---

# Capital Allocation

## When to use
- A company generates cash and must decide where it goes: organic investment, M&A, debt, dividends, or buybacks.
- The CFO/board wants a disciplined framework instead of funding-by-inertia or empire-building.
- Returns on invested capital are mediocre and you suspect capital is being deployed badly.

## When not to use
- You're reallocating across existing business units → use `portfolio-review` (a key input here).
- You're ranking discrete projects in one budget → use `initiative-prioritizer`.

## Method
1. **Establish the cash available and the cost of capital.** Operating cash flow + balance-sheet capacity (prudent leverage headroom), and the WACC / hurdle rate every use of capital must clear.
2. **Lay out the full menu of uses with their returns.** (1) Reinvest organically (high-ROIC growth/maintenance capex), (2) M&A, (3) pay down debt, (4) dividends, (5) buybacks. Estimate the value created per dollar for each — every use competes against the others and against the hurdle rate.
3. **Rank by value creation, not habit.** Fund uses where ROIC > WACC and the marginal return is highest first. Reinvestment only beats returning cash if it earns above the hurdle; otherwise returning capital *is* the value-maximizing choice.
4. **Apply the discipline tests.** Buybacks create value only below intrinsic value (`valuation`) — buying back overvalued stock destroys it. M&A must clear the hurdle after a realistic premium and synergies (`synergy-valuation`). Maintain balance-sheet resilience and strategic optionality (don't over-distribute and starve the future).
5. **Set the policy and the reallocation.** A through-cycle framework: target leverage, dividend policy, the reinvestment bar, and the M&A criteria — plus this period's explicit allocation. State what gets funded, what gets returned, and why.

## Key formulas / lenses
- Economic profit = (ROIC − WACC) × invested capital; deploy capital where this is most positive.
- Reinvestment test: marginal project ROIC > WACC, else return the cash.
- Buyback test: create value only if price < intrinsic value per share; accretion to EPS alone is not value creation.
- Total shareholder return drivers = profit growth + cash returned (dividends + buybacks) + multiple re-rating.

## Decision rules
- Capital is fungible and every use competes — rank organic, M&A, debt, dividends, and buybacks on the *same* value-per-dollar yardstick.
- Don't reinvest below the hurdle to chase growth; disciplined return of capital beats value-destroying growth (the empire-building trap).
- Buy back stock only below intrinsic value; never on "we have spare cash" or to manage EPS optics.

## Output format
1. **Capital available** — operating cash + balance-sheet capacity; the hurdle rate.
2. **Menu of uses** — each use with its expected value-per-dollar / ROIC vs WACC.
3. **Ranked allocation** — what gets funded first and why, on a single yardstick.
4. **Discipline checks** — buyback (vs intrinsic value), M&A (post-premium return), resilience/optionality.
5. **Policy & this-period allocation** — leverage target, payout policy, reinvestment bar, and the explicit deployment.

## Quality bar
- All uses compared on one value-creation yardstick — not "we always reinvest" or "we always pay a dividend."
- Buybacks tested against intrinsic value; M&A tested after a realistic premium.
- Balance-sheet resilience and optionality preserved, not distributed away.
- Output is an explicit allocation, not a generic "balanced approach."

## Common failure modes
- Empire-building: reinvesting/acquiring below the hurdle to grow the company rather than value per share.
- Buybacks at any price to flatter EPS, destroying value.
- Funding by inertia (last year's split) with no return comparison.
- Over-distributing and leaving no resilience or strategic optionality.

## Pairs with
Sits above `portfolio-review` (where reinvestment goes), `valuation` (intrinsic value for buybacks and M&A), `synergy-valuation` (M&A returns), and `initiative-prioritizer` (organic project ranking). The decision lands in a `decision-memo` for the board.

## Worked example
Input: a mature company generating $500M annual free cash, WACC 9%, trading below most analysts' intrinsic value. Menu: organic reinvestment opportunities earn ~7% ROIC at the margin (below hurdle — limited high-return projects); a bolt-on acquisition clears 12% post-premium; debt is already conservative; the stock trades ~15% below a triangulated intrinsic value. Ranked allocation: fund only the organic projects above 9% (~$120M), do the accretive bolt-on (~$150M), and return the rest via buyback *because* the stock is below intrinsic value (~$200M), holding $30M for resilience. The framework explicitly rejects pouring the full $500M into sub-hurdle organic growth just to "keep investing."
