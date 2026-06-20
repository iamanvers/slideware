---
name: initiative-prioritizer
description: Reduces a long initiative list to the few that matter, sequences them, and writes an explicit kill list. Use when too many projects compete for limited capital and attention.
---

# Initiative Prioritizer

## When to use
- The initiative list is long, everything is "a priority," and capacity is overcommitted.
- You need to defend *why* some things are funded and others are explicitly stopped.
- Several business cases exist and must be ranked and sequenced under a real budget/capacity limit.

## When not to use
- The choices are mutually-exclusive strategic directions, not stackable projects → use `strategic-options`.
- You need to allocate across business units, not projects → use `portfolio-review` / `capital-allocation`.

## Method
1. **Score impact × feasibility; size capital as bubble area.** Impact = value created (NPV, or a consistent proxy). Feasibility = capability + readiness + time-to-value + dependency risk. Use the *same* yardstick across all initiatives or the ranking is meaningless. For lightweight scoring use **ICE** (Impact × Confidence × Ease) or **RICE** (Reach × Impact × Confidence ÷ Effort).
2. **Model real capacity.** Count the binding constraint — usually scarce people (engineers, a key team) or cash, not slots. How many can *actually* run in parallel given that constraint? This number is almost always smaller than the wish list.
3. **Sequence for dependencies and cash flow.** Order by dependency (enablers first), early cash/proof (fund later phases from early wins), and risk (run cheap disconfirming bets before expensive commitments). Highest-score-first is wrong if it ignores dependencies and cash.
4. **Write an explicit kill list.** Name every initiative cut and the *reason* (low impact, no capacity, dependency not ready, fails strategy fit). The kill list is the real output — a prioritization that funds everything prioritized nothing.
5. **Define a stage-gate for the survivors.** What proof releases the next tranche of funding/effort.

## Key formulas
- RICE score = (Reach × Impact × Confidence) ÷ Effort.
- ICE score = Impact × Confidence × Ease.
- Capital productivity = expected value ÷ resource consumed; rank ties by this.

## Decision rules
- Fund the few, not the many. If "everything is a priority," nothing is — force a hard cutline at real capacity.
- Score everything on one consistent scale; mixing NPV for some and gut-feel for others corrupts the rank.
- Sequence beats rank: a lower-scored enabler that unblocks three high-value initiatives goes first.

## Output format
1. **Prioritization view** — impact × feasibility chart, bubble = capital, all initiatives placed.
2. **The funded few** — 3–5 initiatives that make the cutline, with their scores.
3. **Sequenced roadmap** — order with dependencies and cash flow shown, and the cutline at real capacity.
4. **Kill list** — every cut initiative with its one-line reason.
5. **Stage-gates** — the proof that releases the next phase for the funded few.

## Quality bar
- One consistent scoring scale across all initiatives.
- A real capacity constraint enforced, producing a hard cutline — not a ranked list of all 14 "priorities."
- An explicit kill list with reasons — the test that a real choice was made.
- Sequencing reflects dependencies and cash, not just raw score.

## Common failure modes
- Ranking everything and funding everything anyway (no cutline).
- Inconsistent scoring (rigorous NPV next to wishful guesses).
- Ignoring dependencies, so a funded initiative stalls waiting on an unfunded enabler.

## Pairs with
Consumes `business-case-builder` outputs (impact scores). Feeds `transformation-roadmap` (turn the sequence into phases/owners) and `value-realization` (track the funded few). Sits under `portfolio-review`/`capital-allocation` at the corporate level.

## Worked example
Input: 14 initiatives, all "must-do," against a real constraint of one platform team and a fixed capex envelope. Consistent RICE scoring plus capacity modeling shows only 4 can run in parallel this year. Sequencing surfaces a low-scored data-migration enabler that three high-value initiatives depend on — it goes first despite a modest standalone score. Result: 4 funded and sequenced (enabler → two high-value builds → one quick cash win to self-fund phase 2); 10 killed, each with a one-line reason (6 low-impact, 3 no-capacity, 1 fails strategy fit). Stage-gate: phase-2 funding released only on the quick win hitting its target.
