---
name: competitive-intel
description: Models rival capabilities and the moves they are most likely to make next. Use to anticipate competitor behavior and pre-commit your response before you act.
---

# Competitive Intel

## When to use
- You're about to make a move (price, launch, entry) and need to predict how rivals respond.
- An incumbent or insurgent is changing behavior and you need a thesis on what's next.
- The board asks "what will competitors do?" — answer with a reasoned thesis, not a feature table.

## When not to use
- You need a full interactive stress-test of move/counter-move dynamics → use `war-gaming`.
- You need where profit sits across the chain, not rival behavior → use `profit-pool-analysis`.

## Method
1. **Frame structural pressure with Porter's Five Forces.** Rate each force (rivalry, new entrants, substitutes, buyer power, supplier power) High/Med/Low *with the specific reason*. This tells you where the profit pressure comes from before you look at any single rival.
2. **Define the three-ring competitive set.** Ring 1: direct rivals. Ring 2: adjacent players who could cross over. Ring 3: potential entrants (including platform/ecosystem players and your own customers/suppliers integrating). Most strategic surprises come from rings 2 and 3.
3. **Build a force-ranked capability matrix.** Rows = rivals; columns = the 4–6 capabilities that actually decide *this* market (not generic ones). Score each cell and weight columns by how much they drive winning. The weighted score is relative competitive strength.
4. **Write a behavioral thesis per key rival.** One paragraph: their strategy, their economic pressure, their incentives, and what their *last three moves* reveal about how they think. Behavior follows incentives and constraints — predict from those, not from their press releases.
5. **Pre-commit your response logic.** For each key rival's two most-likely moves, define your trigger (the observable signal) and your pre-decided response. Deciding now beats reacting under pressure later.

## Decision rules
- Predict moves from *incentives and constraints*, not stated intentions. Ask "what would I do if I ran their P&L?"
- Weight the capability matrix — an unweighted matrix treats a decisive capability and a trivial one as equal and hides the real gap.
- A rival who is structurally cornered (declining core, activist pressure, cash crunch) is the most dangerous and least predictable — flag them.

## Output format
1. **Five Forces summary** — each force rated H/M/L with the one-line reason and the net "where margin pressure comes from."
2. **Competitive set** — the three rings, named.
3. **Capability matrix** — weighted, force-ranked, with the gaps and your relative position called out.
4. **Behavioral thesis** — one paragraph per key rival.
5. **Move/response table** — rival × likely move × trigger signal × pre-committed response.

## Quality bar
- A *thesis* about behavior, not a feature comparison — predict actions, not specs.
- Capabilities are the ones that decide *this* market and are weighted; generic SWOT-style lists fail.
- Every predicted move is grounded in a named incentive or constraint, not vibes.
- Includes ring-2/ring-3 threats, not just the obvious direct rivals.

## Common failure modes
- A feature/spec table mistaken for competitive analysis.
- Ignoring potential entrants and adjacent threats (the moves that actually blindside you).
- Predicting from what rivals *say* rather than what their economics force them to do.

## Pairs with
Builds on `market-mapping` and `profit-pool-analysis`. Feeds `war-gaming` (play the moves out), `strategic-options` (options must survive likely responses), and `pricing-strategy` (anticipate price retaliation).

## Worked example
Input: a #1 incumbent under margin pressure planning a premium launch. Five Forces: rivalry High (commoditizing core), entrants Med (platform players circling). Capability matrix (weighted to distribution and data) shows the #2 rival weak on premium product but strong on mid-market distribution and structurally cornered by a declining core. Behavioral thesis: facing share loss, #2's cheapest defensive move is a mid-market price cut to protect volume, not a premium counter-launch. Pre-committed response: if #2 cuts list price >8% in mid-market (trigger), we hold premium pricing and redirect promo to defend our mid-tier rather than match — protecting the premium narrative.
