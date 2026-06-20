---
name: ai-value-case
description: Quantifies the value and full cost of an AI initiative — benefit mechanism, build/run economics including inference cost, and risk-adjusted ROI. Use to justify and compare AI investments honestly.
---

# AI Value Case

## When to use
- An AI use case needs a credible value/ROI number to be funded or prioritized.
- Leadership is excited by AI but hasn't costed the full build-and-run economics (including inference at scale).
- You need to compare AI initiatives — or AI vs a non-AI alternative — on the same economic basis.

## When not to use
- It's a large, multi-driver capital decision better served by the general engine → use `business-case-builder` (this is its AI-specialized cousin and feeds it).
- You're tracking value after launch → use `value-realization`.

## Method
1. **Quantify the benefit by mechanism.** Tie value to a concrete chain: e.g., (volume × time saved per task × loaded cost) for efficiency; (incremental conversion × margin) for revenue; (loss events avoided × cost per event) for risk. State the baseline and the *attributable* AI uplift — not the gross process value.
2. **Cost the full build economics.** Model development (data prep — often the biggest line — engineering, model selection/fine-tuning, evaluation), integration into the workflow, and change management/adoption. Data and integration usually dwarf the modeling.
3. **Cost the run economics — and don't skip inference.** Ongoing **inference/API cost** (per-call cost × volume — this scales with usage and can quietly exceed the benefit), plus hosting/compute, monitoring/LLMOps, model refresh/retraining, and human-in-the-loop review labor. Many AI cases look great until inference cost at full volume is added.
4. **Risk-adjust.** Apply a realization probability reflecting model performance uncertainty, adoption risk, and data risk. Phase the benefit on an adoption ramp — value lands as usage grows, not on day one.
5. **Compute risk-adjusted ROI and compare to the alternative.** Net value = risk-adjusted phased benefit − build − run. Always compare to the realistic non-AI alternative (process redesign, outsourcing, status quo) — AI must beat the next-best option, not just be positive.

## Key formulas
- Efficiency benefit = tasks/yr × time saved per task × fully-loaded hourly cost × adoption rate.
- Inference cost = calls/yr × cost per call (tokens × price); stress this at *full* production volume.
- Net annual value = risk-adjusted benefit − (amortized build) − annual run cost (incl. inference + human review).
- ROI / payback as in `business-case-builder`; risk-adjusted benefit = benefit × realization probability, phased on the adoption curve.
- Value per call = (benefit per use) − (inference + review cost per use); must be positive at scale.

## Decision rules
- Always include inference cost at full volume and human-in-the-loop review labor — the two lines most often omitted that flip an AI case from positive to negative.
- Count only *attributable, adoption-weighted* benefit, net of the baseline — not the whole process's value.
- AI must beat the realistic alternative; a positive ROI that's worse than a simple process fix is still a no.

## Output format
1. **Benefit model** — mechanism, baseline, attributable uplift, adoption ramp.
2. **Build cost** — data, engineering, integration, change management.
3. **Run cost** — inference/API at full volume, hosting, monitoring, retraining, human review.
4. **Risk-adjusted ROI** — net value, payback, with the realization probability stated.
5. **Vs alternative** — AI net value compared to the next-best non-AI option.

## Quality bar
- Inference cost at full production volume and ongoing human-review labor are both modeled.
- Benefit is attributable, net of baseline, and weighted by a realistic adoption ramp.
- Risk-adjusted, not gross; realization probability is explicit.
- Compared to the realistic non-AI alternative, not just to zero.

## Common failure modes
- Omitting inference cost — the case looks great in the pilot and loses money at scale.
- Claiming the gross process value as AI benefit (ignoring baseline and partial automation).
- Ignoring the human-in-the-loop review cost that most production AI still requires.
- Day-one full benefit with no adoption ramp.

## Pairs with
The AI-specialized input to `business-case-builder` and `ai-use-case-prioritization`. Uses `unit-economics` discipline (value per call) and `sensitivity-analysis` (flex adoption and inference cost). Tracked post-launch by `value-realization`.

## Worked example
Input: the claims-note-drafting use case. Benefit: 500k claims/yr × 12 min saved × $0.80/min loaded cost × 70% adoption = ~$3.4M/yr attributable (net of the portion adjusters still edit). Build: $0.9M (mostly data access + integration; modeling is small). Run: inference = 500k × $0.12/note = $60k/yr, plus monitoring and a 10% human-QA review sample ≈ $0.4M/yr. Risk-adjust benefit at 75% realization and phase over an 18-month adoption ramp. Risk-adjusted net value ≈ +$1.8M/yr at steady state; payback <2 years. Vs alternative (a macro/template tool) which would capture ~30% of the benefit at 10% of the cost — so the AI case must justify the incremental spend, which it does on the residual $2M+ of value the template can't reach. Inference cost is trivial here, but the human-QA line is material — and was nearly omitted.
