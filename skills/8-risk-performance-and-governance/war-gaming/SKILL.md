---
name: war-gaming
description: Stress-tests a strategy against realistic, reacting opposition before launch. Use when a move will provoke competitors, regulators, or customers and you need to see their countermoves.
---

# War Gaming

## When to use
- You're about to make a visible move (price, launch, entry, M&A) that rivals will react to.
- The base case assumes competitors stand still — and you know they won't.
- A board wants confidence the plan survives contact with a reacting market, not a static spreadsheet.

## When not to use
- The uncertainty is long-horizon and exogenous (macro, tech, regulation), not adversarial → use `scenario-planning`.
- You're testing internal assumptions, not external reactions → use `assumption-audit`.

## Method
1. **Design the scenario and the question.** State the move under test and the single question the game must answer ("does our launch hold margin if the #2 retaliates?"). A game with no decision question is theater.
2. **Cast the roles.** Blue (you), Red (each key rival, played to *their* incentives — not as you'd act), Yellow (customers, channel, regulators), White/Control (referee who adjudicates outcomes and enforces realism). Brief each Red team to maximize *their* P&L, not to lose gracefully.
3. **Play three turns, forcing second- and third-order effects.** Turn 1: your move and immediate reactions. Turn 2: their counter and your counter-counter. Turn 3: the new equilibrium. After each turn, Control updates the market state. The insight usually appears in turn 2–3, not turn 1.
4. **Register failure modes.** Capture every way the strategy broke and the specific competitor/customer action that broke it.
5. **Pre-commit triggers and responses.** For each serious failure mode, define the observable trigger and your pre-decided response *now*, while calm — so you react in days, not quarters, when it happens for real.

## Decision rules
- Play Red to its own incentives and constraints, not as a punching bag. The whole value is in an honest adversary.
- If the strategy survives only when competitors behave irrationally or passively, it has failed the test — redesign it.
- Pre-commit responses before launch; the cost of deciding under live pressure (slow, emotional, public) is what war-gaming exists to avoid.

## Output format
1. **Scenario & question** — the move and the decision the game resolves.
2. **Actors** — Red/Yellow players and the incentives each is played to.
3. **Turn-by-turn play** — the move/counter sequence over three turns with the market state after each.
4. **Failure modes** — where and how the strategy broke, and what broke it.
5. **Trigger–response table** — failure mode → observable trigger → pre-committed response.

## Quality bar
- Red is played to *its* incentives, hard — not as a strawman that conveniently loses.
- The game runs to second/third-order effects; a single-turn "they react, we win" is not a war game.
- Output is a pre-committed trigger–response table, not just "risks to watch."
- Names the specific actions that break the plan, not generic "competitive risk."

## Common failure modes
- Red plays soft, so Blue always wins (confirmation theater).
- Stopping at turn 1, missing the counter-counter where strategies actually unravel.
- Producing a list of worries instead of pre-committed responses.

## Pairs with
Stress-tests the output of `strategic-options` and `pricing-strategy`, using `competitive-intel` (rival incentives) as the Red brief. Surfaced failure modes feed `risk-mitigation`; triggers feed `kpi-architect` as leading indicators.

## Worked example
Input: an aggressive premium launch into an incumbent-held segment. Red (the #2, played to defend volume) doesn't counter-launch — too slow — but in turn 2 cuts mid-market price 10% to starve our funnel and bundles a free tier. Yellow (channel) demands higher margins to carry a new SKU, squeezing our economics. By turn 3 our launch holds premium share but the base-case volume assumption breaks: blended CAC rises 40%. Failure mode registered. Trigger: #2 list cut >8% in mid-market or channel margin demand >X. Pre-committed response: don't match price; redirect launch spend to defend the mid-tier and accelerate the bundled-value message — decided now, not in the crisis.
