---
name: business-case-builder
description: Builds the economics behind a decision with the logic exposed — NPV, IRR, payback, sensitivities, and what would have to be true. Use when an investment or initiative needs a defensible case.
---

# Business Case Builder

## When to use
- A specific investment, initiative, or project needs a go/no-go economic case.
- The board/investment committee will ask "what are the returns and what could break them?"
- You need to compare an initiative against a credible base case (do-nothing).

## When not to use
- You're valuing a whole company or asset for a transaction → use `valuation`.
- You need the full integrated three-statement model → use `financial-modeling`.

## Method
1. **Build it driver-based.** Make every line a function of explicit drivers (volume × price − unit cost; headcount × productivity; adoption curve × ARPU). No hard-coded "revenue grows 20%" — expose the driver so reviewers can challenge the assumption, not the output.
2. **Define the base case (counterfactual).** Model what happens if you *don't* do this. The case must measure the *incremental* effect vs the base case, not the absolute future — a common and fatal error.
3. **Compute the returns and show the build.** NPV (discount incremental free cash flows at WACC/hurdle rate), IRR, and payback period. Show the cash-flow timeline, not just the summary numbers.
4. **Run sensitivities and a tornado.** Flex the 2–3 drivers that move the result most, one at a time, across a plausible range. Rank them (tornado chart). Add a downside and upside scenario combining adverse/favorable drivers.
5. **State what would have to be true.** Translate the swing drivers into break-even thresholds ("holds only above X% attach"), name the key risks, and give the decision logic in one line.

## Key formulas
- FCF = EBIT × (1 − tax) + D&A − capex − Δnet working capital. Use *incremental* FCF (with-case minus base-case).
- NPV = Σ FCFₜ / (1 + r)ᵗ − initial investment, where r = hurdle rate / WACC.
- IRR = the rate r at which NPV = 0; accept if IRR > hurdle rate.
- Payback = time for cumulative FCF to turn positive (use discounted payback for a truer read).

## Decision rules
- Discount at the hurdle rate the capital provider actually requires; a case that's positive at 8% but negative at the real 15% hurdle is a no.
- A positive NPV that depends entirely on a terminal/year-5 hockey stick is a red flag — weight near-term, evidenced cash over distant hope.
- Decide on *incremental* NPV vs the base case and on payback against the company's risk tolerance, not on absolute revenue.

## Output format
1. **Decision and recommendation** — go/no-go in one line, up top.
2. **Driver tree** — the assumptions, each sourced or tagged, with the base case stated.
3. **Returns** — NPV, IRR, payback, with the cash-flow timeline visible.
4. **Sensitivity/tornado** — the drivers that swing it, ranked, with break-even thresholds.
5. **Risks + what-would-have-to-be-true** — the conditions for the case to hold and what kills it.

## Quality bar
- Driver-based and transparent — a reviewer can change one assumption and watch the answer move.
- Incremental vs an explicit base case, not absolute.
- Sensitivities on the *real* swing drivers, with break-even thresholds named.
- No unexplained hockey stick; near-term cash is evidenced.

## Common failure modes
- Hard-coded growth rates that can't be challenged.
- Modeling the absolute future instead of the incremental effect vs doing nothing.
- A single point-estimate NPV with no sensitivity, hiding how fragile it is.
- Burying a positive answer that depends entirely on year-5 assumptions.

## Pairs with
Consumes `market-mapping` (the revenue ramp), `pricing-strategy` and `unit-economics` (price/margin drivers), `cost-transformation` (cost drivers). Output is stress-tested by `assumption-audit` and tracked by `value-realization`; multiple cases feed `initiative-prioritizer` and `capital-allocation`.

## Worked example
Input: a new product line, $12M upfront, 5-year horizon, 14% hurdle. Driver tree: addressable accounts × attach rate × ARPU − unit cost − go-to-market. Base case = no launch (channel capacity goes to the core). Incremental NPV = +$9.4M, IRR 22%, discounted payback 3.4 years. Tornado: attach rate dominates, then ARPU, then ramp speed. Break-even: the case is NPV-positive only above an 18% attach rate; below that it destroys value. What-would-have-to-be-true: 18%+ attach within 9 months — flagged as a D-grade assumption and handed to `assumption-audit` for a pilot test before full funding.
