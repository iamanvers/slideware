---
name: risk-mitigation
description: Builds a board-ready risk view with owners, mitigations, and leading indicators — not a generic risk list. Use to govern the risks a specific strategy or program actually carries.
---

# Risk & Mitigation

## When to use
- A strategy/program is approved and the board wants to know what could derail it and who owns it.
- You have a pile of generic risks and need the few that are real, ranked, owned, and monitored.
- You need early-warning indicators that fire *before* a risk materializes, not a post-mortem.

## When not to use
- You're stress-testing assumptions pre-decision → use `assumption-audit`.
- You're modeling adversary reactions → use `war-gaming` (its failure modes feed this).

## Method
1. **Scope the register to *this* strategy.** Derive risks from the strategy's own assumptions, dependencies, and the failure modes surfaced by `assumption-audit` and `war-gaming`. Generic enterprise-risk lists (cyber, macro, talent) only belong here if *this* strategy is specifically exposed.
2. **Score likelihood × impact and rank.** Use a consistent scale (e.g., 1–5 each); severity = likelihood × impact. Plot on a heat map. Add **velocity** (how fast it hits) and **detectability** for the top risks — a fast, undetectable risk is worse than a severe but slow, visible one.
3. **Assign one owner and a specific response per top risk.** Classify each: Avoid (change the plan), Reduce (mitigate), Transfer (insure/contract), or Accept (with a reserve). Vague "monitor closely" is not a response.
4. **Define leading indicators.** For each top risk, the observable metric that moves *before* the risk lands, with a threshold that triggers the contingency. This converts risk management from reactive to anticipatory.
5. **Set contingencies and reserves.** For the top risks, the pre-planned fallback and any budget/time reserve held against it.

## Key lenses
- Severity = likelihood × impact; rank by severity, break ties by velocity ÷ detectability.
- Residual risk = inherent risk after the mitigation is applied — manage and report *residual*, not inherent.
- Risk appetite: state the threshold above which a risk must be escalated to the board.

## Decision rules
- Rank and work the top 5–10. A register of 60 risks nobody acts on is a compliance artifact, not risk management.
- Every top risk has exactly one accountable owner and a leading indicator with a threshold. No owner or no indicator = not managed.
- Report residual risk after mitigation; an impressive list of mitigations means nothing if residual is still red.

## Output format
1. **Risk register** — scoped to the strategy: risk | likelihood | impact | severity | velocity | owner.
2. **Heat map** — top risks plotted on likelihood × impact.
3. **Response plan** — per top risk: Avoid/Reduce/Transfer/Accept, the specific action, residual risk after it.
4. **Leading indicators** — the early-warning metric and trigger threshold per top risk.
5. **Contingencies & reserves** — pre-planned fallbacks and any reserve held.

## Quality bar
- Risks specific to *this* strategy, not a boilerplate enterprise list.
- Leading indicators with thresholds — the difference between anticipation and hindsight.
- One owner per top risk; responses are specific actions, not "monitor."
- Residual (post-mitigation) risk is shown, not just inherent risk.

## Common failure modes
- A generic 50-risk register that applies to any company and drives no action.
- "Mitigation: monitor closely" — a non-response.
- Lagging indicators (the risk has already happened) instead of leading ones.

## Pairs with
Consumes failure modes from `assumption-audit` and `war-gaming`. Leading indicators feed `kpi-architect`; reserves and gates feed `value-realization` and `transformation-roadmap`; top risks go into the `decision-memo`.

## Worked example
Input: a strategy dependent on a single contract manufacturer. Register (scoped): single-source disruption ranks #1 — likelihood Med, impact High, velocity fast, detectability low → top severity. Response: Reduce + Transfer — qualify a second source within 6 months and add a contractual capacity guarantee with penalties. Residual after mitigation: Med→Low. Leading indicator: supplier on-time-delivery dropping below 95% or lead times extending >10% (trigger to activate the second source). Contingency: 6 weeks of safety stock on the two highest-volume SKUs. This single owned, monitored risk replaces a 40-line generic register.
