---
name: transformation-roadmap
description: Turns a prioritized plan into a phased roadmap with owners, milestones, and a concrete first-90-days. Use to convert strategy and initiatives into sequenced, accountable execution.
---

# Transformation Roadmap

## When to use
- The strategy and the priority initiatives are set, and now they must become a sequenced, owned plan.
- A program needs phases with exit criteria, not a Gantt chart of wishful dates.
- Leadership needs to see momentum start now — a concrete first 90 days, not a year-out vision.

## When not to use
- You still need to choose/cut initiatives → use `initiative-prioritizer` first.
- You need the metrics system to track it → use `kpi-architect`; benefit tracking → `value-realization`.

## Method
1. **Define phases by objective and exit criteria, not by calendar.** Each phase has a single objective and a measurable exit criterion ("Phase 1 complete when X is true"). Phases are typically Stabilize → Build → Scale, but name them to the work. A phase that ends "when the quarter ends" isn't a phase.
2. **Place initiatives into phases** respecting dependencies and real capacity (from `initiative-prioritizer`). Front-load enablers and quick wins that fund/credibilize later phases.
3. **Assign a single accountable owner and a milestone per workstream.** Named person, not a committee or a function. Each workstream gets a few hard milestones with dates and a definition of done.
4. **Detail the first 90 days concretely.** Week-by-week (or at least by 30/60/90): what ships, who owns it, what early win proves the program works. The first 90 days build the credibility that funds the rest.
5. **Wire in governance and risk.** A steering cadence, a decision/escalation path, the top risks with owners, and the leading indicators that show whether the roadmap is on track.

## Decision rules
- Sequence for momentum: deliver a visible, credible win inside 90 days even if it isn't the biggest prize — early proof unlocks belief, budget, and political capital.
- Exit criteria gate phase transitions; don't start Phase 2 because the calendar says so if Phase 1's criterion isn't met.
- One accountable owner per workstream. Shared accountability is no accountability.

## Output format
1. **Phase plan** — phases with objective, exit criterion, and the initiatives in each.
2. **Workstream owners & milestones** — table: workstream | accountable owner | key milestones (dated) | definition of done.
3. **First-90-days plan** — 30/60/90 (or weekly) with the early win called out.
4. **Governance** — steering cadence, decision rights, escalation path.
5. **Risk & leading indicators** — top risks with owners and the early-warning metrics.

## Quality bar
- Phases gated by exit criteria, not dates on a Gantt chart.
- Every workstream has one named accountable owner.
- A concrete, credible first-90-days with a real early win — not "kick off and align."
- Dependencies and capacity respected, so the plan is executable, not aspirational.

## Common failure modes
- A Gantt chart of dates with no exit criteria and no owners.
- A first 90 days full of "workshops" and "alignment" but no shipped outcome.
- Over-stuffed parallel workstreams that exceed real capacity and all slip together.

## Pairs with
Consumes `initiative-prioritizer` (the sequenced few) and `operating-model-design` (owners and decision rights). Pairs with `kpi-architect` (track progress), `value-realization` (track benefits), `risk-mitigation`, and `stakeholder-alignment` (sustain sponsorship).

## Worked example
Input: 4 funded initiatives for an ops turnaround. Phases: Stabilize (exit: defect rate < 2% and cash runway > 9 months), Build (exit: new ops model live in 2 of 4 regions), Scale (exit: model in all regions, target margin hit). Workstreams each get one accountable owner and dated milestones. First 90 days, week by week: weeks 1–4 stand up the daily ops huddle and fix the top defect driver (the early, visible win); weeks 5–8 pilot the new model in one region; weeks 9–12 lock the metrics and prove the margin delta. Governance: biweekly steering, GM decides scope trade-offs. Top risk: regional GM resistance — owned by the COO with stakeholder pre-wiring.
