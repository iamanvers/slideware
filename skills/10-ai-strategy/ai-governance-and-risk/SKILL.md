---
name: ai-governance-and-risk
description: Builds a proportionate responsible-AI and model-risk framework — risk tiering, controls across the lifecycle, and oversight — without strangling delivery. Use to govern AI safely and credibly.
---

# AI Governance & Risk

## When to use
- AI use cases are scaling and the board/regulator wants assurance they're safe, fair, and compliant.
- You need a responsible-AI framework that manages real risk without becoming a bureaucracy that kills delivery.
- A high-stakes or regulated AI use case (credit, hiring, health, autonomous decisioning) needs controls before launch.

## When not to use
- You're stress-testing a strategy's business assumptions → use `assumption-audit` / `risk-mitigation`.
- You're designing the delivery operating model broadly → use `ai-scaling-operating-model` (governance embeds into it).

## Method
1. **Tier use cases by risk — and govern proportionately.** Classify by impact and autonomy: low (internal, human-in-the-loop, low stakes) → light-touch; high (affects customers' rights/safety/money, autonomous, regulated) → full controls and sign-off. Proportionality is the whole game: uniform heavy governance kills low-risk velocity; uniform light governance lets a high-risk model through. Align tiers to frameworks like the EU AI Act risk classes and NIST AI RMF.
2. **Map the risk taxonomy per use case.** Performance (accuracy, robustness, drift), fairness/bias, transparency/explainability, privacy/data protection, security (prompt injection, data leakage, adversarial), safety/harm, hallucination/factuality (for GenAI), IP/copyright, third-party/model-provider dependency, and regulatory/compliance.
3. **Define controls across the AI lifecycle.** Data (provenance, consent, bias checks), development (documentation, evaluation, fairness testing), deployment (human-in-the-loop where stakes warrant, guardrails, red-teaming), and monitoring (drift, bias, incident detection). Controls scale with the risk tier.
4. **Assign accountability and oversight.** Clear roles (model owner, risk/compliance, an AI governance forum), a model inventory/registry as the system of record, approval gates by tier, and an incident-response and escalation path. "Responsible AI" with no named owner is a poster, not a control.
5. **Make it auditable and adaptive.** Documentation (model cards, decision logs, data lineage) sufficient for audit/regulator, and a review cadence — because models, data, threats, and regulation all change.

## Decision rules
- Govern *proportionately to risk tier* — the framework's credibility depends on not treating an internal summarizer like an autonomous credit decision.
- High-stakes/regulated use cases require human-in-the-loop, explainability, and bias testing as launch gates — not retrofits.
- Every model in production needs a named accountable owner and a place in the model inventory; ungoverned shadow AI is the real exposure.

## Output format
1. **Risk-tiering scheme** — the classification and what governance each tier triggers (mapped to EU AI Act / NIST RMF where relevant).
2. **Risk taxonomy** — the risks assessed per use case, with severity.
3. **Lifecycle controls** — data / development / deployment / monitoring controls by tier.
4. **Accountability & oversight** — roles, the governance forum, model inventory, approval gates, incident response.
5. **Audit & review** — required documentation (model cards, logs, lineage) and the review cadence.

## Quality bar
- Governance is proportionate to risk tier — light-touch for low-risk, full controls for high — not uniform.
- Controls span the whole lifecycle (data → dev → deploy → monitor), not just a pre-launch checklist.
- Every production model has a named owner and a registry entry; shadow AI is addressed.
- Documentation is genuinely audit/regulator-ready, and the framework is reviewed as conditions change.

## Common failure modes
- Bureaucracy that treats every use case as high-risk, so teams route around governance entirely.
- A one-time pre-launch checklist with no ongoing monitoring for drift, bias, or new threats.
- "Responsible AI principles" with no owners, gates, or inventory — aspiration without control.
- Ignoring GenAI-specific risks (hallucination, prompt injection, data leakage, IP) in a framework built for classical ML.

## Pairs with
Embeds into `ai-scaling-operating-model` (controls live in the operating model) and informs feasibility in `ai-use-case-prioritization` (high-risk = lower near-term feasibility). Uses `risk-mitigation` discipline (owners, leading indicators); guardrails are gates in `ai-poc-design`.

## Worked example
Input: a lender scaling AI across marketing, service, and credit. Risk tiering: a marketing-copy generator = low (internal, reviewed) → light-touch; a service chatbot = medium (customer-facing, bounded) → guardrails + monitoring; an AI credit-decisioning model = high (regulated, affects access to credit) → full controls. For credit: bias testing across protected classes, explainability/adverse-action reasons, human review of declines, model documentation, and regulator-ready lineage — all as launch gates. A model inventory becomes the system of record; an AI governance forum approves high-tier launches. The marketing generator ships in days under light-touch rules, while the credit model passes full review — proportionality keeps both velocity and safety, and surfaces two "shadow" models already running ungoverned in service.
