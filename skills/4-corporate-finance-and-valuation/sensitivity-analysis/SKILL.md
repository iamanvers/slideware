---
name: sensitivity-analysis
description: Tests how an output moves as inputs change — one-way and two-way tables, tornado, break-even, scenario, and Monte Carlo. Use to find what drives a result and how fragile it is.
---

# Sensitivity Analysis

## When to use
- A model gives one number and you need to know how much to trust it and what it hinges on.
- A decision-maker asks "what if we're wrong about X?" or "what has to be true for this to work?"
- You must separate the few inputs that swing the answer from the many that don't.

## When not to use
- The uncertainty is structural and long-horizon (different worlds, not different numbers) → use `scenario-planning`.
- You're testing beliefs/logic rather than numerical inputs → use `assumption-audit`.

## Method
1. **Identify candidate drivers.** List every input the output depends on. Don't pre-judge — the surprising driver is often the point.
2. **Run one-way sensitivities.** Flex each input across a *plausible* range (e.g., ±1 std dev, or a defensible high/low), holding others at base. Record the output range each produces. Use a consistent range logic so drivers are comparable.
3. **Rank with a tornado.** Sort drivers by the width of the output swing they cause; chart widest-at-top. The top 2–3 bars are where the answer is actually decided — and where due diligence and risk effort should go.
4. **Run two-way tables on the top drivers.** A grid of the output across the two most important inputs simultaneously shows their interaction and the **break-even frontier** (where the output crosses the decision threshold — e.g., NPV = 0, IRR = hurdle). Shade the zone that fails.
5. **Add scenarios and (where warranted) Monte Carlo.** Combine adverse inputs into a coherent downside case (and favorable into upside). For genuinely probabilistic problems, assign input distributions and simulate to get an output distribution — report P10/P50/P90, not a single point.

## Key concepts / formulas
- **One-way sensitivity** isolates ∂Output/∂Input by flexing one input at a time.
- **Tornado**: rank drivers by |Output(high) − Output(low)|; the order is the priority list.
- **Break-even (goal seek)**: solve the input value where Output = threshold (e.g., the attach rate where NPV = 0).
- **Elasticity of the output to an input** = (%ΔOutput) ÷ (%ΔInput) — a unit-free comparator across drivers of different scales.
- **Monte Carlo**: sample each input from its distribution, recompute the output N times → empirical distribution; read percentiles and P(Output < threshold).

## Decision rules
- Use *plausible, comparable* ranges. A tornado where each driver is flexed by a different, arbitrary amount is misleading — normalize the ranges (e.g., each to its own realistic uncertainty).
- One-at-a-time sensitivity misses interactions; always pair the top drivers in a two-way table or scenario, because the worst outcomes come from drivers moving *together*.
- Report the break-even on the key driver as a sentence the decision-maker can hold: "this holds as long as attach stays above 18%."

## Output format
1. **Driver list** — inputs tested and the range used for each (with the range rationale).
2. **Tornado chart** — drivers ranked by output swing; the top 2–3 highlighted.
3. **Two-way table(s)** — output across the top two drivers, with the break-even frontier and failure zone shaded.
4. **Break-even thresholds** — the goal-seek value on each key driver, stated plainly.
5. **Downside/upside (and Monte Carlo if used)** — combined scenarios; P10/P50/P90 if simulated.

## Quality bar
- Ranges are plausible and comparable across drivers, with the rationale stated.
- The tornado ranks drivers so attention goes to the 2–3 that matter.
- Interactions are tested (two-way / scenario), not just one-at-a-time.
- Break-even thresholds are surfaced as plain decision sentences, not buried in a grid.

## Common failure modes
- Arbitrary, inconsistent flex ranges that make the tornado meaningless.
- Only one-at-a-time analysis, hiding the compound downside where drivers move together.
- A wall of numbers with no break-even and no "so what."
- Monte Carlo theater — precise-looking distributions built on guessed input distributions.

## Pairs with
Stress-tests `business-case-builder`, `valuation`, `lbo-modeling`, `financial-modeling`, and `synergy-valuation`. The swing drivers become the assumptions for `assumption-audit` and the leading indicators for `risk-mitigation`; the break-even sentence goes into the `decision-memo`.

## Worked example
Input: a new-product business case with base-case NPV +$9.4M. One-way sensitivities (each flexed across its realistic range): attach rate ±6pts swings NPV by ±$11M; ARPU ±10% by ±$5M; ramp speed by ±$3M; discount rate ±1pt by ±$2M. Tornado puts **attach rate** on top by a wide margin. Two-way table of NPV across attach × ARPU shows the break-even frontier: NPV turns negative below an 18% attach rate at base ARPU. Goal-seek confirms break-even attach = 17.6%. Downside case (attach 15%, ARPU −10%, slow ramp together) = −$4M. Decision sentence for the memo: "Value-creating only if attach holds above ~18%; below that the case destroys value, so fund a pilot to prove attach before committing capital."
