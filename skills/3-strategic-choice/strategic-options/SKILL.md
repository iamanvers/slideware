---
name: strategic-options
description: Generates a real option set and reasons to a recommendation instead of advocating one answer. Use when a direction must be chosen and you want genuine alternatives evaluated honestly.
---

# Strategic Options

## When to use
- A direction must be chosen and you want real alternatives, not one favored answer with strawmen around it.
- Leadership is anchored on a single path and you need to widen the choice set before committing.
- A decision is reversible-once and expensive — it deserves an explicit, scored comparison.

## When not to use
- The options are already chosen and you're sequencing them → use `initiative-prioritizer`.
- You only need the economics of one path → use `business-case-builder`.

## Method
1. **Generate options across horizons (the 3 Horizons).** H1: optimize/defend the core. H2: expand into adjacencies. H3: transformational bets. Force at least one genuine option per horizon plus the **"do nothing / base case"** — without a base case you can't tell if any option actually beats inertia. Each option must be a *coherent, mutually-exclusive* strategy, not a feature.
2. **Define weighted decision criteria up front.** Typically value (NPV/upside), feasibility (capability, capital, time), risk (downside, reversibility), strategic fit. Set the weights *before* scoring so the answer isn't reverse-engineered.
3. **Score honestly and show trade-offs.** Score each option on each criterion (e.g., 1–5) with a one-line rationale per cell. Show where each option is genuinely worse — an option with no weaknesses was not scored honestly.
4. **Reason to a recommendation.** Recommend the highest weighted-score option, but explicitly name the **conditions under which a different option wins** (e.g., "if capital is constrained, option B dominates"). State the no-regret moves common to all live options that you can start now.
5. **Define the trigger to revisit.** What signal would change the recommendation? Pre-name it.

## Decision rules
- Always include a base case and at least three live options; two options is usually a false binary.
- Set criteria weights before scoring. If the recommendation flips under reasonable re-weighting, say so — that's a finding, not a flaw.
- Separate *reversible* from *irreversible* options: reversible bets need less certainty to start; irreversible ones need a higher bar and more `assumption-audit`.

## Output format
1. **Option set** — 3–4 mutually-exclusive strategies + the base case, each described in 2–3 sentences.
2. **Weighted criteria scorecard** — options × criteria, weights shown, with per-cell rationale.
3. **Trade-off narrative** — what you gain and give up with each.
4. **Conditional recommendation** — the pick, plus the explicit conditions under which another option wins.
5. **No-regret moves + revisit trigger** — what to start now regardless, and what signal forces a rethink.

## Quality bar
- Options are real and mutually exclusive — no strawmen built to lose.
- Weights are set before scoring and shown; the math is transparent.
- The recommendation is *conditional* and names what would change it — not a one-eyed advocacy piece.
- Includes the base case so "is this better than doing nothing?" is answered.

## Common failure modes
- One real option dressed up with two obvious losers.
- Reverse-engineering weights to justify a pre-decided answer.
- Scoring with no rationale, so the scorecard is unfalsifiable.

## Pairs with
Built on `situation-assessment`/`problem-structuring`. Each option's economics go through `business-case-builder`; the recommended option is stress-tested by `assumption-audit` and `war-gaming`, then turned into a plan by `transformation-roadmap`.

## Worked example
Input: a declining core business. Options: (Base) run the core for cash; (A/H1) cost-out and defend the core; (B/H2) expand into an adjacent segment leveraging the existing channel; (C/H3) acquire into a new category. Criteria weighted value 35 / feasibility 25 / risk 25 / fit 15. B scores highest on the weighted card. Recommendation: pursue B — *unless* the next financing round slips, in which case A (cash-generative, low capital) dominates. No-regret move startable now: stand up the adjacent-segment pilot, which serves B and informs C. Revisit trigger: core decline steeper than −12%/yr forces a return to the harvest case.
