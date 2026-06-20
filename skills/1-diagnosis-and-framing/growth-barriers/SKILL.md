---
name: growth-barriers
description: Finds the single binding constraint on growth rather than the loudest complaint. Use when growth has slowed or stalled and leadership is debating symptoms.
---

# Growth Barriers

## When to use
- Growth has slowed, stalled, or turned down and the cause is contested.
- Multiple teams each blame a different thing (sales blames product, product blames marketing).
- You need to point scarce resources at the *one* constraint that, if relieved, unlocks the most growth.

## When not to use
- You don't yet have the baseline → run `situation-assessment` first.
- Growth is fine and you're choosing where to expand → use `market-mapping` / `strategic-options`.

## Method
1. **Decompose growth arithmetically.** Revenue growth = New + Expansion − Churn − Contraction (or, for transactional: Volume × Price). Quantify each component's contribution to the delta. The component that swung is where to look — do not theorize before you decompose.
2. **Date the inflection.** Find the month/quarter the curve bent. Overlay what changed then: a launch, a price move, a process change, a competitor move, a macro shift. Correlation in time is the first clue to causation.
3. **Walk the funnel as a waterfall.** Lay out acquisition → activation → conversion → retention → expansion. Compute the step-to-step conversion and the absolute volume lost at each step. The largest *absolute* leak, weighted by how fixable it is, is the candidate constraint.
4. **Read cohort retention curves.** Distinguish structural decay (each new cohort retains worse — a product/onboarding problem) from cyclical decay (all cohorts dipped together — a macro/seasonal problem). Structural is your problem to fix; cyclical usually isn't.
5. **Five-whys to a structural root.** Drive from the symptom to a root cause that is structural (a system/process/incentive), not a person or a one-off. Stop when the next "why" leaves your control.

## Decision rules
- The binding constraint is the one where a fixed unit of effort yields the most growth — relieve it and the *next* constraint becomes binding (theory of constraints). Fixing a non-binding constraint moves nothing.
- Prefer the constraint supported by *both* the arithmetic decomposition and the funnel/cohort evidence. One line of evidence is a hypothesis; two converging is a finding.
- If new-customer acquisition is healthy but NRR < 100%, the constraint is almost always retention/expansion, not top-of-funnel — do not let a loud sales team redirect spend upstream.

## Output format
1. **The binding constraint** — one sentence, named precisely (e.g., "expansion within the post-onboarding cohort," not "retention").
2. **Growth bridge** — waterfall showing how each component moved the number.
3. **Evidence** — the 2–3 analyses that converge on this constraint, each with the number.
4. **Confirm-or-kill** — the single next analysis that would prove or disprove it.
5. **What is *not* the constraint** — explicitly de-prioritize the loud-but-wrong candidates, with the evidence.

## Quality bar
- Name *one* binding constraint, not a list of five "areas of opportunity."
- Quantify: every component of the growth bridge has a number and they reconcile to the total.
- Disconfirm the obvious: explicitly show why the loudest complaint is or isn't the real constraint.

## Common failure modes
- Listing many problems instead of finding the one that binds.
- Confusing a large leak that can't be fixed with the constraint that should be worked.
- Treating cyclical decay as a structural failure (or vice versa).

## Pairs with
Follows `situation-assessment`. Feeds `assumption-audit` (test the causal claim), `initiative-prioritizer` (act on the constraint), and `unit-economics` (if the constraint is economic).

## Worked example
Input: "Why has growth slowed?" Decomposition: New bookings flat YoY, but Expansion revenue fell from +$8M to +$1M and Churn rose — net the swing is entirely retention-side. Inflection dates to the Q2 onboarding redesign. Cohort curves show structural decay: every post-Q2 cohort retains ~15pts worse at month 6. Five-whys lands on a removed onboarding milestone that previously drove second-product adoption. Binding constraint: post-onboarding expansion, not acquisition. Confirm-or-kill: reinstate the milestone for one cohort and measure month-3 attach.
