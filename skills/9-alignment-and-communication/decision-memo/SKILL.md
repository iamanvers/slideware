---
name: decision-memo
description: Turns the analysis into a one-page decision document an executive can act on — answer-first, with options, rationale, risks, and the specific ask. Use to produce the written artifact that drives a decision.
---

# Decision Memo

## When to use
- An executive or board needs a clear, written recommendation they can approve.
- The analysis is done and must be compressed into one page that drives a decision, not a discussion.
- You need a durable artifact of record (what was decided, why, and what was asked).

## When not to use
- You need the full presentation/story across lengths → use `narrative-builder`.
- The recommendation isn't decided yet → finish `strategic-options`.

## Method
1. **State the decision question precisely at the top.** One sentence, framed as a decision ("Should we exit X and redeploy to Y?"), with the date and the decision-maker named.
2. **Give the recommendation first (answer-first / BLUF).** The recommendation in 1–2 sentences before any rationale. An executive should be able to read the first three lines and know what you're asking and why.
3. **Lay out the options and criteria considered.** A compact table: the options (including base case), the decision criteria, and how each option scored — so the reader sees the choice was real, not a foregone conclusion.
4. **Give the rationale, the economics, and the risks.** The 3 reasons (Pyramid-style), the headline economics (NPV/IRR/payback or the key number), the top 2–3 risks with mitigations, and what would have to be true.
5. **Close with the specific ask, owners, and next steps.** Exactly what decision/approval is being requested (the dollar amount, the go-ahead), who owns what next, and by when. A memo that doesn't name the ask isn't a decision memo.

## Decision rules
- One page. If it spills over, the thinking isn't sharp enough yet — compress, don't append.
- The ask must be specific and bounded: "approve $12M and the Q3 start," not "support the direction."
- Show the options and criteria even briefly — a recommendation with no visible alternatives reads as advocacy and invites suspicion.

## Output format (the one page)
1. **Title / decision question** — one line; decision-maker and date.
2. **Recommendation (BLUF)** — 1–2 sentences, answer-first.
3. **Options & criteria** — compact scored table including the base case.
4. **Rationale & economics** — 3 reasons + the headline numbers.
5. **Risks & what-would-have-to-be-true** — top 2–3 with mitigations.
6. **The ask & next steps** — the specific approval requested, owners, dates.

## Quality bar
- Answer-first; the ask is unmissable and specific (amount, date, decision).
- Fits one page; every sentence earns its place — no filler, no restating the obvious.
- Options and criteria are visible so the recommendation is auditable, not asserted.
- Risks are named honestly, including the one the reader will worry about most.

## Common failure modes
- Burying the recommendation on page 3 under context.
- A vague ask ("seeking alignment") that lets everyone nod and decide nothing.
- Hiding the inconvenient risk, which destroys credibility when it surfaces.
- Sprawling to five pages because the argument was never distilled.

## Pairs with
The terminal artifact for most engagements: consumes `strategic-options` (options/criteria), `business-case-builder` (economics), `risk-mitigation` (risks), and `narrative-builder` (the framing). Pre-wire it with `stakeholder-alignment` before circulating.

## Worked example
Input: a build-vs-buy decision for a data platform. Title: "Decision: build in-house or acquire DataCo — for CTO approval, by June 30." BLUF: "Recommend acquiring DataCo for $18M; it reaches capability 14 months faster and is NPV-positive by $6M versus building." Options table: Build / Buy / Partner / Base case, scored on time-to-capability, cost, risk, fit. Rationale: speed-to-market, scarce talent we can't hire fast enough, lower execution risk; NPV +$6M, payback 3.1 yrs. Risks: integration (mitigation: 90-day plan + retention packages), overpayment (mitigation: earn-out). Ask: "Approve $18M acquisition and a Q3 close; CTO sponsors, Corp Dev leads diligence." One page.
