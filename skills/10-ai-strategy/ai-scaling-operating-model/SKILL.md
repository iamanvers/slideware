---
name: ai-scaling-operating-model
description: Designs how AI moves from successful pilots to scaled production value — the operating model, MLOps/LLMOps, ownership, adoption, and reuse. Use to cross the pilot-to-production chasm.
---

# AI Scaling & Operating Model

## When to use
- Pilots work but value isn't scaling — the classic "pilot purgatory" where nothing reaches production at scale.
- You need to decide how AI is organized, owned, and run as a capability, not a series of experiments.
- Multiple use cases are coming and you need reusable foundations, not bespoke one-offs each time.

## When not to use
- You're designing a single pilot → use `ai-poc-design`.
- You're diagnosing whether foundations exist at all → use `ai-readiness-assessment`.

## Method
1. **Choose the AI operating model.** Centralized (a central AI team — control and depth, but a bottleneck), federated/hub-and-spoke (central platform + capability, embedded squads in the business — usually best for scale), or fully embedded (speed, but duplication and weak governance). Match to ambition and maturity; most scaling orgs land on hub-and-spoke.
2. **Stand up the platform and MLOps/LLMOps.** The reusable foundation: data/feature access, model registry, deployment pipelines (CI/CD for models), monitoring (drift, quality, cost), evaluation harnesses, prompt/version management, and guardrail/safety layers. This is what turns each new use case from a project into a configuration.
3. **Fix production ownership and the run model.** Name who owns each model *in production* (not the data scientist who built it): monitoring, retraining triggers, incident response, and the SLA. Models degrade — drift, data changes, prompt regressions — so productionizing without an owner guarantees silent failure.
4. **Engineer adoption and trust.** The hardest part is human, not technical. Workflow integration (AI in the tool people already use, not a separate app), human-in-the-loop design, transparency/explainability for users, training, and incentives. Measure adoption as a first-class metric — an unused model creates zero value.
5. **Build for reuse and governance at scale.** A use-case intake and stage-gate process, shared components, and embedded responsible-AI/model-risk checks (`ai-governance-and-risk`) so each use case doesn't reinvent controls. Govern the portfolio's value with `value-realization`.

## Decision rules
- Productionizing means assigning an *owner and a monitoring/retraining loop* — a model with no production owner will silently degrade and erode trust.
- Adoption is the binding constraint on value far more often than model quality — design the workflow and trust, and measure usage as a core KPI.
- Build shared platform/MLOps once; bespoke pipelines per use case is the most common reason AI cost balloons and scaling stalls.

## Output format
1. **Operating model** — central/federated/embedded choice, with roles and the rationale.
2. **Platform & MLOps blueprint** — the reusable components (registry, pipelines, monitoring, eval, guardrails).
3. **Production ownership model** — who owns each model live; monitoring, retraining, incident response, SLAs.
4. **Adoption plan** — workflow integration, human-in-the-loop, training, incentives, the adoption metric.
5. **Reuse & governance** — intake/stage-gate, shared components, embedded responsible-AI checks.

## Quality bar
- Every production model has a named owner and a monitoring/retraining loop.
- Shared platform/MLOps is built once and reused — not bespoke per use case.
- Adoption is designed and measured, not assumed; AI lives inside existing workflows.
- Governance is embedded in the operating model, not bolted on per project.

## Common failure modes
- Pilot purgatory: endless experiments, nothing owned or monitored in production.
- "Throw it over the wall" — data scientists build, no one owns the model live, it degrades silently.
- A great model nobody uses because it sits in a separate tool outside the workflow.
- Reinventing pipelines and controls for every use case, so cost scales linearly and value doesn't.

## Pairs with
Builds on `ai-readiness-assessment` (the gaps to close) and `operating-model-design` (decision rights, structure). Consumes graduated pilots from `ai-poc-design`; embeds `ai-governance-and-risk`; tracks portfolio value with `value-realization` and `kpi-architect`; sequences via `transformation-roadmap`.

## Worked example
Input: a bank with 8 successful pilots, 1 in production. Diagnosis: every pilot was bespoke, none had a production owner, and models that did ship drifted unmonitored. Operating model chosen: hub-and-spoke — a central platform/MLOps team owns the shared foundation; embedded squads in lending, fraud, and service own use cases. Platform blueprint: model registry, standardized deployment pipeline, drift+cost monitoring, an evaluation harness, and a guardrail layer (PII, toxicity, policy). Production ownership: each model gets a named squad owner with a monitoring dashboard, retraining triggers, and an incident runbook. Adoption: AI embedded in the existing loan-origination and case tools, with adoption tracked weekly. Result design: the next use case ships as a configuration on the platform in weeks, with controls inherited — converting pilots into a scaling capability.
