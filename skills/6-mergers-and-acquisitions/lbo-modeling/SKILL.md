---
name: lbo-modeling
description: Models a leveraged buyout — entry, debt structure, cash sweep, exit, and returns (IRR/MOIC) with a value-creation bridge. Use to test what a sponsor can pay and where returns come from.
---

# LBO Modeling

## When to use
- A private-equity sponsor needs to know the IRR/MOIC a target can deliver and the maximum price they can pay.
- You're testing how much leverage a business can carry and still de-risk through the hold.
- The investment committee asks "where do the returns actually come from — growth, multiple, or deleveraging?"

## When not to use
- You're valuing the business on intrinsic/strategic grounds → use `valuation`.
- You need the full operating three-statement projection → use `financial-modeling` (the LBO sits on top of it).
- You're sizing a strategic buyer's merger benefits → use `synergy-valuation`.

## Method
1. **Set the entry.** Entry EV = entry EBITDA × entry multiple. Build **Sources & Uses**: Uses = purchase EV + transaction fees + minimum cash; Sources = new debt (turns of EBITDA the lenders allow) + sponsor equity (the plug). Sponsor equity is what must earn the return.
2. **Structure the debt.** Layer the facilities (revolver, TLB/term loan, senior/sub notes) with their rates and amortization. Track the blended interest cost and any covenants (e.g., max net debt/EBITDA). Over-levering juices IRR but raises default risk — model both.
3. **Project the cash flow and sweep the debt.** From the operating model, compute free cash flow available for debt paydown = EBITDA − cash interest − cash taxes − capex − ΔNWC − mandatory amortization. Apply the **cash sweep**: excess FCF pays down debt, which lowers interest next period (the deleveraging flywheel). Roll the debt schedule year by year.
4. **Set the exit.** Exit EV = exit-year EBITDA × exit multiple (be conservative — assume flat-to-lower vs entry unless you can defend expansion). Exit equity = exit EV − exit net debt.
5. **Compute returns and attribute them.** MOIC = exit equity ÷ entry equity; IRR from the equity cash flows. Then build the **value-creation bridge**: EBITDA growth, multiple change, and debt paydown should sum to the equity value created — this tells you whether the deal is an operating story or a financial-engineering story.

## Key formulas
- Entry EV = entry EBITDA × entry multiple; Sponsor equity = EV + fees + min cash − total debt raised.
- FCF for debt paydown = EBITDA − cash interest − cash taxes − capex − ΔNWC − mandatory amortization.
- Exit equity = (exit EBITDA × exit multiple) − exit net debt.
- **MOIC** = exit equity ÷ entry equity. **IRR** ≈ MOIC^(1/years) − 1 (with no interim distributions; otherwise solve NPV=0 on the dated equity flows).
- Value-creation bridge: ΔEquity = **EBITDA growth** (ΔEBITDA × entry multiple) + **multiple expansion** ((exit − entry multiple) × exit EBITDA) + **deleveraging** (entry net debt − exit net debt). These three sum to the equity value created.

## Decision rules
- Returns from deleveraging and multiple expansion are lower-quality than returns from EBITDA growth — a deal that only works on multiple expansion is a bet on the market, not the business.
- Solve for the **maximum entry multiple** that still clears the sponsor's hurdle (typically ~20–25% IRR / ~2.5–3.0× MOIC over ~5 years) — that's the disciplined bid ceiling.
- Stress the exit multiple down; if the deal only works assuming you sell higher than you bought, it's fragile (always pair with `sensitivity-analysis`).

## Output format
1. **Sources & Uses** — entry EV, fees, debt by tranche, sponsor equity.
2. **Debt schedule** — balances, interest, amortization, and the cash sweep year by year.
3. **Returns** — IRR and MOIC at the base case, plus the max-price-to-hurdle.
4. **Value-creation bridge** — EBITDA growth vs multiple vs deleveraging (reconciled to ΔEquity).
5. **Sensitivities** — IRR/MOIC across entry multiple, exit multiple, leverage, and EBITDA growth.

## Quality bar
- Sources & Uses balances; the debt schedule and cash sweep tie to the operating model.
- The value-creation bridge reconciles exactly to the change in equity value.
- Returns are shown against a stated hurdle, with the max disciplined bid solved for.
- Exit multiple is conservative and stress-tested — no return that depends on selling higher than you bought.

## Common failure modes
- Assuming generous multiple expansion to make the deal work (a market bet dressed as an operating thesis).
- Over-levering to hit IRR while ignoring covenant/default risk under a downside case.
- A returns number with no attribution, so no one knows if value came from the business or the balance sheet.
- Forgetting fees, minimum cash, or NWC swings in Sources & Uses.

## Pairs with
Sits on a `financial-modeling` operating projection; uses `commercial-due-diligence` (is the growth real?) and `valuation` (intrinsic cross-check). Always run with `sensitivity-analysis`; the thesis is stress-tested by `assumption-audit` and lands in a `decision-memo` for the IC.

## Worked example
Input: target with $100M EBITDA, bought at 10.0× ($1,000M EV), 5.0× net leverage ($500M debt), $30M fees + min cash → sponsor equity ≈ $530M. Hold 5 years; EBITDA grows to $150M (8.5%/yr); cash sweep pays net debt down from $500M to $200M. Exit conservatively at 10.0× (no expansion) → exit EV $1,500M − $200M net debt = $1,300M exit equity. MOIC = 1,300 ÷ 530 ≈ 2.45×; IRR ≈ 2.45^(1/5) − 1 ≈ 19.6%. Value-creation bridge (on the EV-basis entry equity of EV − net debt = $500M): EBITDA growth (+$50M × 10× = $500M), multiple expansion ($0, held flat), deleveraging (+$300M) → +$800M equity created, reconciling the $500M EV-basis equity to the $1,300M exit equity. (The $30M of fees + min cash is why the sponsor actually wrote $530M, which is the base for MOIC and slightly dilutes it.) Read: this is an operating + deleveraging story, not a multiple bet — the higher-quality kind. To clear a 25% IRR hurdle, the model shows the entry multiple would need to fall below ~8.7×.
