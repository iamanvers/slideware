---
name: kpi-architect
description: Designs a metrics system that links daily work to strategic outcomes, with thresholds and gaming-resistance. Use when metrics are noisy, lagging, performative, or disconnected from strategy.
---

# KPI Architect

## When to use
- Dashboards are crowded with metrics nobody acts on, or metrics that lag too late to steer by.
- A strategy/program needs a measurement system that connects frontline activity to the outcome.
- Targets exist but are gamed, or "engagement"-style metrics that sound good and mean nothing.

## When not to use
- You're tracking *financial benefits* of a specific case → use `value-realization`.
- You need early-warning indicators for *risks* specifically → use `risk-mitigation`.

## Method
1. **Define one north-star metric** the strategy ultimately moves — the single number that, if it goes up, means the strategy is working (e.g., net revenue retention, activated accounts, contribution per customer). Not revenue-for-its-own-sake; the metric that captures *value delivered*.
2. **Decompose it into a MECE KPI tree** down to operational drivers each team can influence. North star = f(driver₁, driver₂, …); each driver = f(sub-drivers). The tree shows how a frontline action propagates to the strategic outcome — and where to intervene.
3. **Set three layers: outcome, driver, health.** Outcome metrics (lagging, what we're trying to achieve), driver metrics (leading, what we do to get there), and health/guardrail metrics (what must *not* break while we push — quality, attrition, unit economics). Every push metric needs a paired guardrail.
4. **Set action thresholds, not just targets.** For each metric: the target, and the threshold that triggers a specific action (red/amber/green with a defined response). A metric with no action threshold is a number, not a control.
5. **Stress-test each metric for proxy failure (gaming).** Ask "how would a rational person hit this number without delivering the intent?" Pair it with a guardrail that closes the loophole (Goodhart's law: a measure that becomes a target stops measuring).

## Decision rules
- One north star per strategy. Competing north stars produce conflicting local optimization.
- Every leading/driver metric must plausibly *cause* the outcome — correlation isn't enough. If you can't draw the causal arrow, it's a vanity metric.
- Every push metric is paired with a guardrail. Optimizing speed without a quality guardrail just breaks quality.

## Output format
1. **North-star metric** — the one number, with why it captures value delivered.
2. **KPI tree** — MECE decomposition from north star to operational drivers.
3. **Three-layer metric set** — outcome / driver / health, with owner and cadence for each.
4. **Thresholds & actions** — target + red/amber/green trigger and the response per metric.
5. **Proxy-failure notes** — how each key metric could be gamed and the guardrail that prevents it.

## Quality bar
- One north star, decomposed through a causal MECE tree to actions teams can take.
- Every metric carries an action threshold — measurement that drives decisions, not dashboards.
- Gaming/proxy-failure is explicitly addressed with paired guardrails.
- Leading drivers, not just lagging outcomes — you can steer before it's too late.

## Common failure modes
- A 40-metric dashboard with no hierarchy, no thresholds, and no actions.
- Vanity/vague metrics ("engagement," "synergy") that don't decompose to anything actionable.
- Push metrics with no guardrails, so teams optimize the number and break the intent.

## Pairs with
Built from the strategy via `operating-model-design` (who owns what) and `transformation-roadmap` (what we're executing). Leading indicators from `risk-mitigation` and `war-gaming` slot in as health metrics; outcome metrics feed `value-realization`.

## Worked example
Input: vague "improve engagement" goals across a B2B product. North star reframed to **activated accounts** (accounts reaching the value milestone that predicts retention). KPI tree: activated accounts = signups × onboarding completion × milestone reach; each branch owned by a team. Three layers: outcome = activated accounts and NRR; drivers = onboarding completion rate, time-to-first-value; health = support load and seat-level churn (guardrails). Thresholds: onboarding completion < 60% (red) triggers an onboarding sprint. Proxy-failure check: "activation" could be gamed by auto-completing steps — guardrail = milestone must be a real usage event, cross-checked against 30-day retention.
