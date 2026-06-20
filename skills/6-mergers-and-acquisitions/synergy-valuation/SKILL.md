---
name: synergy-valuation
description: Sizes, risk-adjusts, and times the cost and revenue synergies in a merger or acquisition, net of costs-to-achieve. Use to justify a strategic premium and to build the integration value plan.
---

# Synergy Valuation

## When to use
- A strategic buyer needs to justify a premium over standalone value with credible synergies.
- An integration team needs a bottom-up, owned synergy target — not a banker's headline number.
- The board asks "is the premium worth it?" and "how much of the synergy is real and when does it land?"

## When not to use
- You're validating the target's standalone forecast → use `commercial-due-diligence`.
- You're valuing the standalone business → use `valuation`.

## Method
1. **Separate cost synergies from revenue synergies — and trust them differently.** Cost synergies (overhead consolidation, procurement scale, facility/footprint, systems) are more controllable and credible. Revenue synergies (cross-sell, pricing, new markets) are real but slower, riskier, and routinely overstated — discount them harder.
2. **Build bottom-up, not top-down.** Estimate each synergy from a specific mechanism with an owner ("consolidate two ERP instances → $X", "combined procurement on category Y → Z% of $W spend"). A "5% of combined cost" top-down number is a red flag.
3. **Net out costs-to-achieve and dis-synergies.** Subtract one-time integration costs (severance, systems, advisory) and recurring dis-synergies (customer attrition from overlap, talent flight, distraction). Report **net** synergy, not gross.
4. **Risk-adjust and phase.** Apply a probability/realization factor by type (cost high, revenue low) and a ramp curve — synergies land over 1–3 years, not on day one. Compute the NPV of the phased, risk-adjusted, net synergy stream.
5. **Tie to the premium and to value-realization.** Compare synergy NPV to the premium paid: how much synergy must be captured just to break even on the premium? Hand the phased targets to `value-realization` with owners and gates.

## Key formulas
- Net synergy = gross cost synergies + gross revenue synergies − costs-to-achieve − dis-synergies.
- Risk-adjusted synergy = Σ (synergy_i × realization probability_i), phased over the ramp.
- Synergy NPV = Σ risk-adjusted net synergyₜ / (1+r)ᵗ − one-time costs.
- Break-even capture = premium paid ÷ gross synergy NPV (what % of synergies must land just to justify the premium).

## Decision rules
- Discount revenue synergies hard (often 25–50% realization in year 1) and phase them late; over-crediting revenue synergies is the #1 cause of value-destroying deals.
- Always report net of costs-to-achieve and dis-synergies — gross synergy numbers are marketing.
- If break-even capture exceeds ~70–80% of credible synergies, the premium is too high — the deal has no margin of safety.

## Output format
1. **Synergy register** — each synergy: type (cost/revenue) | mechanism | gross size | owner | ramp.
2. **Costs-to-achieve & dis-synergies** — one-time and recurring offsets.
3. **Risk-adjusted, phased view** — realization factors and the year-by-year net synergy curve.
4. **Synergy NPV vs premium** — the value created vs paid, and the break-even capture %.
5. **Realization plan** — owners, milestones, and gates handed to `value-realization`.

## Quality bar
- Bottom-up, mechanism-by-mechanism, with owners — not a % of combined cost.
- Cost and revenue synergies separated and risk-adjusted differently.
- Net of costs-to-achieve and dis-synergies; phased, not day-one.
- Explicitly compared to the premium with a break-even capture figure.

## Common failure modes
- Top-down synergy percentages with no mechanism or owner.
- Crediting full revenue synergies immediately (the classic deal-killer).
- Ignoring costs-to-achieve and integration dis-synergies, overstating net value.
- No link to the premium, so "$200M of synergies" sounds great but doesn't justify the price.

## Pairs with
Follows `commercial-due-diligence` and `valuation` (standalone value + synergies = strategic value). Hands the realization plan to `value-realization` and the integration sequence to `transformation-roadmap`; risks go to `risk-mitigation`.

## Worked example
Input: a $1.2B acquisition at a $300M premium. Bottom-up register: $180M gross cost synergies (overlapping G&A, procurement, two data centers — each owned), $120M gross revenue synergies (cross-sell). Costs-to-achieve: $90M one-time. Risk-adjustment: cost synergies at 85% realization phased over 2 years; revenue synergies at 35% year-1 ramping to 60%, phased over 3 years. Risk-adjusted net synergy NPV ≈ $310M. Break-even capture = $300M premium ÷ ~$430M gross synergy NPV ≈ 70% — thin margin of safety, driven by the soft revenue synergies. Recommendation: the deal works on cost synergies alone if revenue synergies are treated as upside, not underwriting — and the IC should not pay up for the cross-sell.
