---
name: valuation
description: Values a company or asset using DCF, trading comparables, and precedent transactions, triangulated into a defensible range. Use for transactions, fairness checks, or capital decisions.
---

# Valuation

## When to use
- You need to put a defensible number (or range) on a business, asset, or deal.
- An acquisition, divestiture, fundraising, or fairness opinion requires a valuation.
- A board asks "what is this worth?" and you need more than a multiple off the back of an envelope.

## When not to use
- You're evaluating one project's incremental returns → use `business-case-builder`.
- You're sizing merger synergies → use `synergy-valuation` (it sits on top of standalone value).

## Method
1. **Triangulate three methods — never rely on one.**
   - **DCF (intrinsic):** project unlevered free cash flow, discount at WACC, add terminal value, get enterprise value.
   - **Trading comps (market):** apply peer multiples (EV/EBITDA, EV/Revenue, P/E) to the target's metrics.
   - **Precedent transactions (deal):** apply multiples paid in comparable M&A (includes a control premium).
2. **Build the DCF carefully.** Forecast FCF over an explicit horizon (5–10 yrs); FCF = EBIT(1−tax) + D&A − capex − ΔNWC. Terminal value via Gordon growth (FCF×(1+g)/(WACC−g)) or an exit multiple — and cross-check the two. Discount at WACC. Terminal value often drives 60–80% of the answer, so scrutinize g and the exit multiple hardest.
3. **Select comparables honestly.** Truly comparable in business model, growth, margin, and risk — not just the same SIC code. Adjust for size, growth, and margin differences; a faster-growing, higher-margin business deserves a premium multiple.
4. **Bridge enterprise value to equity value.** Equity value = EV − net debt − minority interest − preferred + associates. Per-share = equity value ÷ diluted shares. Getting this bridge wrong is a common, embarrassing error.
5. **Present a range and a football field.** Show the valuation range from each method side by side (the "football field"). Converge on a defensible range, not a single false-precision number, and state what drives the spread.

## Key formulas
- Enterprise Value (DCF) = Σ FCFₜ/(1+WACC)ᵗ + TV/(1+WACC)ⁿ.
- Terminal value (Gordon) = FCFₙ×(1+g) / (WACC − g); (exit multiple) = EBITDAₙ × exit multiple.
- WACC = (E/V)×cost of equity + (D/V)×cost of debt×(1−tax); cost of equity (CAPM) = rf + β×ERP.
- Equity value = EV − net debt − minorities − preferred (+ associates/non-core assets).

## Decision rules
- Triangulate: if DCF and market multiples diverge widely, find out why (different growth/risk view, or a modeling error) — don't just average.
- Sanity-check g: terminal growth above long-run GDP/inflation is almost never defensible. Stress WACC and g; report the sensitivity.
- Use the method that fits: DCF for stable cash generators, revenue multiples for high-growth/pre-profit, precedent transactions for control situations.

## Output format
1. **Valuation summary** — the recommended range and the headline number, answer-first.
2. **Football field** — the range from DCF, trading comps, and precedents, side by side.
3. **DCF detail** — FCF build, WACC, terminal value, and the EV→equity bridge.
4. **Comps detail** — the peer/transaction set, the multiples, and the adjustments made.
5. **Sensitivities** — value vs WACC and g (and key operating drivers); what moves the number most.

## Quality bar
- Three methods triangulated into a range, with the football field shown — not one number from one method.
- WACC, terminal growth, and the comp set are justified, not plugged.
- The EV→equity bridge is explicit and correct.
- Terminal value and its assumptions are stress-tested (they usually dominate the answer).

## Common failure modes
- A single DCF with a hidden hockey-stick and an indefensible terminal growth rate.
- "Comparable" companies that aren't (wrong growth/margin/risk profile).
- Confusing enterprise value with equity value (forgetting the net-debt bridge).
- False precision — quoting "$847M" when the honest answer is "$750–950M."

## Pairs with
Consumes `commercial-due-diligence` (the forecast you value) and `financial-modeling` (the FCF build). Feeds `synergy-valuation` (standalone + synergy = strategic value), `capital-allocation` (buy/build/return decisions), and `decision-memo`.

## Worked example
Input: valuing a mid-market software target. DCF: 7-year FCF build, WACC 11%, terminal growth 3% (below long-run GDP — defensible), EV ≈ $480M; the exit-multiple cross-check (12× terminal EBITDA) lands at $510M, close enough to trust. Trading comps: peers trade 4.5× revenue → $440M, but peers grow slower, so a premium is warranted. Precedents: recent deals at 5.5× revenue (with control premium) → $540M. Football field: $440–540M. EV→equity bridge: less $60M net debt → equity ≈ $380–480M. Sensitivity: value swings ±$90M on WACC ±1pt and g ±1pt — flagged as the key drivers. Recommended range $440–510M, not a single point.
