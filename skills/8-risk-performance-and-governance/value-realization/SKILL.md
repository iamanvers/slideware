---
name: value-realization
description: Makes sure the value a strategy or business case promised is actually captured — via a value ledger, stage gates, and governance. Use after approval to prevent benefit leakage.
---

# Value Realization

## When to use
- A business case was approved and now someone has to prove the promised value actually lands.
- A cost or growth program is underway and benefits keep slipping into "next year."
- The board wants assurance that funding the next phase is justified by realized — not projected — value.

## When not to use
- You're building the case/economics in the first place → use `business-case-builder`.
- You're designing the metric system broadly → use `kpi-architect`.

## Method
1. **Build a value ledger.** Every promised benefit as a line: the benefit, its size ($), the owner, the baseline it's measured against, the mechanism (how it's actually realized), and the date it should land. Sum must reconcile to the approved business case — gaps mean phantom benefits.
2. **Define measurement and baselines rigorously.** For each benefit, the exact metric, the pre-program baseline, and how you'll isolate the program's effect from market noise (control group, run-rate vs one-time, gross vs net of cost-to-achieve). Unbaselined benefits are unfalsifiable.
3. **Set stage gates.** Tie release of the next phase's funding/scope to *proven* value from the prior phase. Gate criteria are pre-committed and measurable. This converts a hopeful program into a self-correcting one.
4. **Govern with a cadence.** A regular review (monthly/quarterly) that marks each ledger line green/amber/red on realized-vs-plan, reallocates from stalled lines, and escalates leakage. Owners report realized, not forecast.
5. **Track leakage and re-forecast honestly.** When a benefit erodes, log why (over-optimistic baseline, slower adoption, offsetting cost) and adjust — protecting the credibility of the remaining ledger.

## Key lenses
- Realization rate = realized benefit ÷ promised benefit; track per line and in aggregate.
- Net benefit = gross benefit − cost-to-achieve − offsetting leakage (e.g., cost savings eaten by reinvestment).
- Run-rate vs one-time: separate recurring annualized benefits from one-off gains; boards care about run-rate.

## Decision rules
- Gate funding on realized value, not status updates. "On track" with no measured benefit is a red flag.
- Measure net of cost-to-achieve and offsetting leakage — gross savings that get spent elsewhere aren't savings.
- Reallocate from stalled lines rather than waiting; a benefit 6 months late rarely recovers without intervention.

## Output format
1. **Value ledger** — benefit | size | owner | baseline | mechanism | due date | status, reconciled to the case.
2. **Measurement plan** — metric, baseline, and effect-isolation method per benefit.
3. **Stage gates** — phase → gate criteria → funding/scope released on proof.
4. **Governance model** — review cadence, RAG rules, reallocation and escalation triggers.
5. **Realization dashboard** — realized vs promised (rate), run-rate vs one-time, leakage log.

## Quality bar
- The ledger reconciles to the approved business case — no benefits that nobody owns.
- Benefits are baselined and net of cost-to-achieve; effect isolated from market noise.
- Funding is gated on *realized* value; gates are pre-committed and measurable.
- Leakage is tracked and re-forecast honestly, not buried.

## Common failure modes
- A tracker of activities ("workshops held") instead of realized financial benefit.
- Gross benefits with no baseline, so realization can never be proven or disproven.
- Phantom synergies/savings that quietly get reinvested and never reach the P&L.

## Pairs with
Consumes the benefits from `business-case-builder` / `synergy-valuation` and the metrics from `kpi-architect`. Stage gates align with `transformation-roadmap` phases; stalled-line reallocation feeds `initiative-prioritizer` / `capital-allocation`.

## Worked example
Input: an approved $40M cost-out program. Ledger: 14 benefit lines, each with an owner, a pre-program baseline, the realization mechanism, and a due date, summing exactly to $40M (net of $6M cost-to-achieve). Measurement isolates run-rate savings from one-time and nets out reinvestment. Stage gate: Phase 2 funding ($15M) releases only when Phase 1 has booked ≥$10M of *realized, run-rate* savings verified by finance. At the Q2 review three lines are amber (procurement savings eaten by volume reinvestment) — flagged, re-forecast down $3M, and offset by accelerating a green line. Realization rate reported at 78% with the leakage explained.
