---
name: ai-readiness-assessment
description: Diagnoses whether an organization can actually deliver and scale AI across data, technology, talent, operating model, and governance. Use to find the gaps that will block AI value before you commit.
---

# AI Readiness Assessment

## When to use
- Before committing to an AI program, to know whether the foundations exist to deliver it.
- A pilot succeeded but nothing scaled, and you suspect organizational/data gaps, not model gaps.
- Leadership over-estimates readiness ("our data is fine") and you need an honest baseline.

## When not to use
- You're identifying *what* to build → use `ai-opportunity-mapping`.
- You're designing the target operating model to close the gaps → use `ai-scaling-operating-model`.

## Method
1. **Assess across the readiness dimensions** — each rated against a maturity scale (e.g., 1 = ad hoc, 5 = optimized):
   - **Data**: availability, quality, accessibility, governance, labeling — the most common true blocker.
   - **Technology/platform**: compute, MLOps/LLMOps tooling, model access, integration into workflows.
   - **Talent**: data scientists/ML engineers, AI-literate product and domain people, and leadership fluency.
   - **Operating model**: how AI work is funded, prioritized, and moved from pilot to production; who owns models in production.
   - **Governance & risk**: responsible-AI policy, model risk management, security, regulatory posture (`ai-governance-and-risk`).
   - **Adoption/culture**: will the front line trust and use it; change capacity.
2. **Benchmark against the ambition, not an abstract ideal.** Readiness is relative to the *use cases you intend to run*. A human-in-the-loop drafting tool needs far less maturity than autonomous decisioning. Map required vs current maturity per dimension for the actual roadmap.
3. **Find the binding constraints.** The dimension(s) where the gap most blocks value — usually data quality/accessibility or the pilot-to-production operating model, rarely the model itself.
4. **Distinguish "buy/partner" from "build" gaps.** Some gaps (tooling, models, compute) are quickly bought; others (data foundations, domain talent, trust) take time to build. The mix determines the timeline.
5. **Translate to a closure plan.** For each binding gap: the specific action, owner, and time, sequenced so foundations land before the use cases that need them.

## Decision rules
- Assess readiness *relative to the intended use cases*, not against a generic maturity model — over-building foundations for pilots you'll never run wastes the budget.
- Data and the pilot-to-production operating model are the usual binding constraints; weight them heavily and don't be reassured by "our data is fine" without testing it.
- Separate fast buy/partner gaps from slow build gaps — the slow ones set the realistic timeline.

## Output format
1. **Readiness radar/heatmap** — current maturity per dimension, with the rating rationale.
2. **Required-vs-current** — the gap per dimension against the intended roadmap's ambition.
3. **Binding constraints** — the 1–3 gaps that most block value.
4. **Buy vs build** — which gaps are quick to acquire vs slow to develop.
5. **Closure plan** — action, owner, and timing per binding gap, sequenced ahead of dependent use cases.

## Quality bar
- Maturity rated against the *actual* intended use cases, not an abstract ideal.
- Data and operating-model readiness are tested, not taken on faith.
- Binding constraints are named (not all six dimensions flagged equally).
- Buy-vs-build is explicit, driving a realistic timeline.

## Common failure modes
- "Our data is great" accepted without evidence — then every use case stalls on data.
- Treating readiness as a model/tech question and missing the operating-model and adoption gaps that actually kill scaling.
- A generic maturity score with no link to the use cases or a closure plan.

## Pairs with
Feeds feasibility scoring in `ai-use-case-prioritization` and the foundations in `ai-scaling-operating-model`. Governance dimension expands into `ai-governance-and-risk`; the closure plan feeds `transformation-roadmap`.

## Worked example
Input: a retailer whose two AI pilots never scaled. Readiness ratings: data 2/5 (product data fragmented across 4 systems, no single customer view), platform 3/5 (cloud present, no MLOps), talent 3/5 (data scientists but no ML engineers to productionize), operating model 1/5 (pilots run in a lab, no path or owner for production), governance 2/5. Binding constraints: the pilot-to-production operating model (1/5) and data integration (2/5) — not the models, which worked fine in the lab. Buy vs build: MLOps tooling and ML engineers are buyable in a quarter; the unified data layer and a production ownership model are 9–12 month builds. Closure plan sequences the data layer and a productization squad ahead of any new pilots — explaining why "more pilots" would have failed again.
