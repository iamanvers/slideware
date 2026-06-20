---
name: ai-opportunity-mapping
description: Maps where AI can create value across a business by decomposing the value chain into candidate use cases tied to real problems and economics. Use to build the AI opportunity portfolio before prioritizing.
---

# AI Opportunity Mapping

## When to use
- Leadership wants an AI strategy but the conversation is a list of buzzwords, not business problems.
- You need a structured, exhaustive view of where AI could create value before deciding where to invest.
- A "we need AI" mandate exists and you must convert it into concrete, owned use cases.

## When not to use
- You already have a candidate list and need to rank/sequence it → use `ai-use-case-prioritization`.
- The question is whether the org *can* deliver AI at all → use `ai-readiness-assessment`.

## Method
1. **Start from problems and the value chain, not the technology.** Decompose the business into its value-chain stages or core processes (`profit-pool-analysis` / `operating-model-design` help). For each, ask "where is there toil, judgment-at-scale, prediction, generation, or matching that AI is good at?" AI follows a business problem, never the reverse.
2. **Classify each candidate by AI archetype.** What *kind* of AI it is determines feasibility and risk: prediction/forecasting (classical ML), classification/extraction, generation (LLM content/code), conversation/agents, recommendation/matching, optimization, computer vision. Naming the archetype anchors the later effort and risk estimate.
3. **Frame each as a use case, not a capability.** "Reduce claims-handling time by drafting adjuster notes from the case file" (a use case) beats "use GenAI in claims" (a capability). Each gets a problem, a user, the AI archetype, the data it needs, and the value mechanism.
4. **Locate value type.** Tag each as cost-reduction (efficiency/automation), revenue (growth, conversion, pricing), risk (fraud, compliance, quality), or experience (CX, employee enablement). A portfolio skewed entirely to "efficiency pilots" usually signals unambitious framing.
5. **Map the portfolio.** Lay use cases on the value chain so leadership sees coverage, clusters, and white space — and which shared data/platform foundations multiple use cases depend on.

## Decision rules
- Anchor every use case to a measurable business problem and a value mechanism; "explore AI for X" is not a use case.
- Prefer use cases that share data/platform foundations — clustered use cases compound; scattered one-offs don't.
- Don't let the loudest/shiniest use case (usually a chatbot) crowd out higher-value, less visible ones (forecasting, extraction, decision support).

## Output format
1. **Value-chain map** with candidate use cases placed per stage/process.
2. **Use-case register** — for each: problem | user | AI archetype | data needed | value type | rough value mechanism.
3. **Value-type mix** — the cost / revenue / risk / experience balance of the portfolio.
4. **Foundation map** — the shared data/platform capabilities multiple use cases depend on.
5. **So-what** — where the concentration and white space are, feeding prioritization.

## Quality bar
- Use cases are problem-anchored with a named value mechanism — not technology looking for a use.
- Each is tagged with its AI archetype (which governs feasibility/risk downstream).
- The portfolio spans value types, not just efficiency pilots.
- Shared foundations are identified so the roadmap can build them once.

## Common failure modes
- A list of technologies ("LLMs," "computer vision") instead of business use cases.
- Chatbot tunnel vision — defaulting to conversational AI and missing higher-value prediction/extraction.
- Ignoring data dependencies, so "great" use cases turn out to be undeliverable.

## Pairs with
Uses `profit-pool-analysis`/`operating-model-design` to decompose the business. Feeds `ai-use-case-prioritization` (rank the register) and `ai-readiness-assessment` (can we deliver these?). Foundations feed `ai-scaling-operating-model`.

## Worked example
Input: an insurer with a vague "use AI" board mandate. Value-chain decomposition surfaces 14 candidates across underwriting, claims, distribution, and service. Classified by archetype: claims-note drafting (generation), fraud detection (classification), demand/loss forecasting (prediction), and an agent for first-notice-of-loss intake (conversation). Value-type mix is healthy — not all efficiency: fraud is risk, dynamic pricing is revenue. Foundation map shows 6 of 14 use cases depend on a unified claims-data layer — making that the keystone investment rather than any single model. The shiny "customer chatbot" ranks mid-pack, not top, once value mechanisms are made explicit.
