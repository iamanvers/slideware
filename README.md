```
  ____  _ _     _
 / ___|| (_) __| | _____      ____ _ _ __ ___
 \___ \| | |/ _` |/ _ \ \ /\ / / _` | '__/ _ \
  ___) | | | (_| |  __/\ V  V / (_| | | |  __/
 |____/|_|_|\__,_|\___| \_/\_/ \__,_|_|  \___|

 ✻ Slideware — the strategy, finance & AI thinking layer for Claude
   42 skills · 10 domains · workflow + design guides
```

> **Slideware is the thinking layer for executive strategy, finance, and AI work — it gets the
> content and the reasoning right. It is not a slide generator (yet).**
> A comprehensive pack of **42 standalone Claude skills** plus two guides that encode the methods,
> frameworks, and quantitative rigor of top-tier strategy firms (McKinsey, BCG, Bain) and corporate
> strategy / PE / IB / AI-transformation teams.

## What Slideware is (and isn't)

Most "AI slide" tools generate pretty templates with hollow content. Slideware deliberately does the
opposite half first — the half that is hard and that actually matters:

- **It does:** structure the problem, run the analysis, make the math tie out, and tell you exactly
  how to represent each finding ([DESIGN-GUIDE.md](DESIGN-GUIDE.md)) and how to assemble it into a
  decision-grade executive narrative ([WORKFLOW.md](WORKFLOW.md)).
- **It does not (yet):** generate, render, or export slides — there is no slide engine wired in. The
  name signals where this is headed; **today it is the content-and-guidance brain** that feeds a deck
  you build (or that a future rendering layer will produce).

A slide-rendering layer is being scoped as a future addition. Until it ships, use Slideware as the
analytical and design-direction layer — the substance and the storyline — not a deck builder.

> **Read these two guides first — they are what make output MBB-grade, not just a list of frameworks:**
> - **[WORKFLOW.md](WORKFLOW.md)** — how to chain the skills into a full engagement and hold every output to an executive quality standard.
> - **[DESIGN-GUIDE.md](DESIGN-GUIDE.md)** — how to represent each kind of information, what each exhibit communicates, and how to tune it to your audience and context.

## How the pack is organized

The 42 skills live in **10 category folders** under [`skills/`](skills/), ordered along a typical
engagement arc (frame → analyze → choose → build → govern → communicate), with AI strategy as a
dedicated tenth domain:

| # | Category folder | Covers |
|---|---|---|
| 1 | [`1-diagnosis-and-framing/`](skills/1-diagnosis-and-framing/) | Framing the real problem and finding the binding constraint |
| 2 | [`2-market-and-competitive-intelligence/`](skills/2-market-and-competitive-intelligence/) | Market sizing, competitors, customers, profit pools |
| 3 | [`3-strategic-choice/`](skills/3-strategic-choice/) | Options, scenarios, go-to-market, pricing strategy & analytics |
| 4 | [`4-corporate-finance-and-valuation/`](skills/4-corporate-finance-and-valuation/) | Valuation, modeling, business cases, unit economics, sensitivity |
| 5 | [`5-corporate-strategy-and-portfolio/`](skills/5-corporate-strategy-and-portfolio/) | Capital allocation and portfolio reallocation |
| 6 | [`6-mergers-and-acquisitions/`](skills/6-mergers-and-acquisitions/) | Commercial due diligence, synergies, LBO modeling |
| 7 | [`7-operating-model-and-execution/`](skills/7-operating-model-and-execution/) | Operating model, cost, prioritization, roadmap |
| 8 | [`8-risk-performance-and-governance/`](skills/8-risk-performance-and-governance/) | War-gaming, risk, KPIs, value capture |
| 9 | [`9-alignment-and-communication/`](skills/9-alignment-and-communication/) | Stakeholders, narrative, the decision memo |
| 10 | [`10-ai-strategy/`](skills/10-ai-strategy/) | AI opportunity → PoC → value → scaling → governance |

## What's inside (42 skills)

### 1. Diagnosis & Framing
1. **[problem-structuring](skills/1-diagnosis-and-framing/problem-structuring/SKILL.md)** — Turns a fuzzy question into a hypothesis-driven, MECE issue tree and a prioritized workplan.
2. **[situation-assessment](skills/1-diagnosis-and-framing/situation-assessment/SKILL.md)** — A fact-based picture of where the business really is and the real question to answer.
3. **[growth-barriers](skills/1-diagnosis-and-framing/growth-barriers/SKILL.md)** — Finds the single binding constraint on growth, not the loudest complaint.
4. **[assumption-audit](skills/1-diagnosis-and-framing/assumption-audit/SKILL.md)** — Surfaces the unstated beliefs a strategy rests on and stress-tests the load-bearing ones.

### 2. Market & Competitive Intelligence
5. **[market-mapping](skills/2-market-and-competitive-intelligence/market-mapping/SKILL.md)** — Sizes the market (TAM/SAM/SOM, triangulated) and finds attractive white space.
6. **[competitive-intel](skills/2-market-and-competitive-intelligence/competitive-intel/SKILL.md)** — Models rival capabilities and the moves they're most likely to make next.
7. **[customer-segmentation](skills/2-market-and-competitive-intelligence/customer-segmentation/SKILL.md)** — Decision-useful, needs-based segments instead of generic personas.
8. **[profit-pool-analysis](skills/2-market-and-competitive-intelligence/profit-pool-analysis/SKILL.md)** — Maps where the money actually sits along the value chain and where it's migrating.

### 3. Strategic Choice
9. **[strategic-options](skills/3-strategic-choice/strategic-options/SKILL.md)** — Generates a real option set and reasons to a conditional recommendation.
10. **[scenario-planning](skills/3-strategic-choice/scenario-planning/SKILL.md)** — Builds distinct, plausible futures and derives robust + contingent strategy under deep uncertainty.
11. **[go-to-market](skills/3-strategic-choice/go-to-market/SKILL.md)** — Designs the motion, channels, coverage, and economics to win a chosen segment.
12. **[pricing-strategy](skills/3-strategic-choice/pricing-strategy/SKILL.md)** — Diagnoses pricing power and produces a value-based pricing plan.
13. **[pricing-analytics](skills/3-strategic-choice/pricing-analytics/SKILL.md)** — The quantitative mechanics of setting price — elasticity, conjoint, optimal-price math, discount break-evens.

### 4. Corporate Finance & Valuation
14. **[valuation](skills/4-corporate-finance-and-valuation/valuation/SKILL.md)** — Values a company/asset via DCF, comps, and precedents, triangulated into a defensible range.
15. **[financial-modeling](skills/4-corporate-finance-and-valuation/financial-modeling/SKILL.md)** — Builds an integrated, driver-based three-statement model that ties out and flexes.
16. **[business-case-builder](skills/4-corporate-finance-and-valuation/business-case-builder/SKILL.md)** — Builds the economics of a decision (NPV/IRR/payback) with the logic exposed.
17. **[unit-economics](skills/4-corporate-finance-and-valuation/unit-economics/SKILL.md)** — Tests whether the business makes money per unit/customer (contribution, CAC, LTV, payback).
18. **[margin-bridge](skills/4-corporate-finance-and-valuation/margin-bridge/SKILL.md)** — Explains a profit/margin change by decomposing price, volume, mix, cost, and FX (reconciling exactly).
19. **[sensitivity-analysis](skills/4-corporate-finance-and-valuation/sensitivity-analysis/SKILL.md)** — Tests what drives a result and how fragile it is — tornado, two-way tables, break-even, Monte Carlo.

### 5. Corporate Strategy & Portfolio
20. **[capital-allocation](skills/5-corporate-strategy-and-portfolio/capital-allocation/SKILL.md)** — Deploys cash across reinvestment, M&A, debt, and shareholder returns to maximize value per share.
21. **[portfolio-review](skills/5-corporate-strategy-and-portfolio/portfolio-review/SKILL.md)** — Reallocates capital and attention across businesses on evidence, not inertia.

### 6. Mergers & Acquisitions
22. **[commercial-due-diligence](skills/6-mergers-and-acquisitions/commercial-due-diligence/SKILL.md)** — Validates whether a target's market, position, and forecast justify the deal.
23. **[synergy-valuation](skills/6-mergers-and-acquisitions/synergy-valuation/SKILL.md)** — Sizes, risk-adjusts, and times merger synergies net of costs-to-achieve.
24. **[lbo-modeling](skills/6-mergers-and-acquisitions/lbo-modeling/SKILL.md)** — Models a leveraged buyout — entry, debt, cash sweep, exit, IRR/MOIC, and a value-creation bridge.

### 7. Operating Model & Execution
25. **[operating-model-design](skills/7-operating-model-and-execution/operating-model-design/SKILL.md)** — Turns strategy into capabilities, structure, processes, and decision rights.
26. **[cost-transformation](skills/7-operating-model-and-execution/cost-transformation/SKILL.md)** — Finds sustainable cost-out by activity, driver, and should-cost — not across-the-board cuts.
27. **[initiative-prioritizer](skills/7-operating-model-and-execution/initiative-prioritizer/SKILL.md)** — Reduces a long initiative list to the few that matter, sequenced, with a kill list.
28. **[transformation-roadmap](skills/7-operating-model-and-execution/transformation-roadmap/SKILL.md)** — Turns the plan into a phased roadmap with owners and a concrete first 90 days.

### 8. Risk, Performance & Value Governance
29. **[war-gaming](skills/8-risk-performance-and-governance/war-gaming/SKILL.md)** — Stress-tests a strategy against realistic, reacting opposition.
30. **[risk-mitigation](skills/8-risk-performance-and-governance/risk-mitigation/SKILL.md)** — A board-ready risk view with owners, mitigations, and leading indicators.
31. **[kpi-architect](skills/8-risk-performance-and-governance/kpi-architect/SKILL.md)** — A metrics system that links daily work to strategic outcomes and resists gaming.
32. **[value-realization](skills/8-risk-performance-and-governance/value-realization/SKILL.md)** — Ensures promised value is actually captured via a value ledger and stage gates.

### 9. Alignment & Executive Communication
33. **[stakeholder-alignment](skills/9-alignment-and-communication/stakeholder-alignment/SKILL.md)** — Maps who must say yes and pre-wires the decision before the meeting.
34. **[narrative-builder](skills/9-alignment-and-communication/narrative-builder/SKILL.md)** — Structures the recommendation (Pyramid + SCQA) so it lands fast and survives scrutiny.
35. **[decision-memo](skills/9-alignment-and-communication/decision-memo/SKILL.md)** — Compresses the analysis into a one-page, answer-first decision document.

### 10. AI Strategy
36. **[ai-opportunity-mapping](skills/10-ai-strategy/ai-opportunity-mapping/SKILL.md)** — Maps where AI can create value across the business as problem-anchored use cases.
37. **[ai-use-case-prioritization](skills/10-ai-strategy/ai-use-case-prioritization/SKILL.md)** — Ranks and sequences AI use cases on value and AI-specific feasibility into a wave plan.
38. **[ai-readiness-assessment](skills/10-ai-strategy/ai-readiness-assessment/SKILL.md)** — Diagnoses whether the org can deliver and scale AI (data, tech, talent, operating model, governance).
39. **[ai-poc-design](skills/10-ai-strategy/ai-poc-design/SKILL.md)** — Designs an AI PoC as a falsifiable test with pre-committed success criteria and a path to production.
40. **[ai-value-case](skills/10-ai-strategy/ai-value-case/SKILL.md)** — Quantifies AI value and full cost (incl. inference) into a risk-adjusted ROI.
41. **[ai-scaling-operating-model](skills/10-ai-strategy/ai-scaling-operating-model/SKILL.md)** — Crosses the pilot-to-production chasm — operating model, MLOps, ownership, adoption.
42. **[ai-governance-and-risk](skills/10-ai-strategy/ai-governance-and-risk/SKILL.md)** — A proportionate responsible-AI and model-risk framework that doesn't strangle delivery.

## How the skills fit together

A typical engagement flows down the categories and back up to communication:

```
FRAME            problem-structuring → situation-assessment → growth-barriers
   ↓
ANALYZE          market-mapping · competitive-intel · customer-segmentation · profit-pool-analysis
                 valuation · financial-modeling · unit-economics · margin-bridge · sensitivity-analysis
   ↓
CHOOSE           strategic-options · scenario-planning · pricing-strategy/analytics · go-to-market
                 portfolio-review · capital-allocation · commercial-due-diligence · synergy-valuation · lbo-modeling
   ↓             (stress-test: assumption-audit · war-gaming)
BUILD            operating-model-design · cost-transformation · initiative-prioritizer · transformation-roadmap
   ↓
GOVERN           risk-mitigation · kpi-architect · value-realization
   ↓
COMMUNICATE      stakeholder-alignment · narrative-builder · decision-memo

AI LANE          ai-opportunity-mapping → ai-use-case-prioritization → ai-readiness-assessment
                 → ai-poc-design → ai-value-case → ai-scaling-operating-model → ai-governance-and-risk
```

See **[WORKFLOW.md](WORKFLOW.md)** for the full engagement playbook and skill chains for common situations (turnaround, growth strategy, M&A, cost program, market entry, AI transformation, board review).

## Install
1. Clone or unzip this pack.
2. Add the `skills/` tree to a Claude Project as Project Knowledge, **or** copy the skill folders into `~/.claude/skills/` (skill discovery recurses into subfolders, so the category folders can be kept as-is; or flatten them if you prefer). Each skill is a folder containing a single `SKILL.md`.
3. In a conversation, name the skill — e.g., *"Use the market-mapping skill,"* or describe the task and let Claude select it. Claude runs the method with the framework already loaded.

Keep the whole set for a full strategy + finance + AI toolkit, or pull out just the category folders you need.

## Design principles
- **Answer-first.** Lead with the recommendation; the build supports it.
- **MECE & hypothesis-driven.** Structure before analysis; test beliefs, don't gather data aimlessly.
- **Exposed logic.** Driver-based models and sourced claims a reviewer can challenge — never a black box.
- **The math ties out.** Bridges reconcile, models balance, formulas are stated and correct.
- **Honest ranges over false precision.** "$440–510M, swinging on WACC," not "$847M."
- **So-what on everything.** Every exhibit and finding states the decision it informs.
- **Earn every page.** No filler, no hedging, no generic management-speak(faff), see the quality standard in [WORKFLOW.md](WORKFLOW.md#part-4--the-quality-standard).
