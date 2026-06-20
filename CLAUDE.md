# CLAUDE.md — Slideware

Project memory for Claude when working in this repository.

## What this project is

**Slideware** is a pack of Claude **skills** that encode MBB-grade (McKinsey/BCG/Bain) strategy,
corporate-finance, and AI-strategy methods, plus two guides that turn analysis into executive-ready
output. The long-term vision: pair this analytical "brain" with a slide-generation engine so an
approved storyline can be rendered into a board-ready deck. The presentation engine is **not yet
built** — its design is being planned separately.

This repo is **content, not code**: Markdown skill definitions and guides. There is no build, no
tests, no runtime. "Correctness" here means sound method, math that ties out, and prose that meets
the quality standard below.

## Repository structure

```
README.md            Banner, framing, full skill index (keep in sync with skills/)
WORKFLOW.md          Engagement playbook + the quality standard (Part 4) + quality gates
DESIGN-GUIDE.md      Exhibit catalog (how to represent information) + tuning by context
CLAUDE.md            This file
skills/
  1-diagnosis-and-framing/
  2-market-and-competitive-intelligence/
  3-strategic-choice/
  4-corporate-finance-and-valuation/
  5-corporate-strategy-and-portfolio/
  6-mergers-and-acquisitions/
  7-operating-model-and-execution/
  8-risk-performance-and-governance/
  9-alignment-and-communication/
  10-ai-strategy/
      <skill-name>/SKILL.md     One skill = one folder = one SKILL.md
```

42 skills across 10 numbered category folders. The numbering encodes the engagement arc
(frame → analyze → choose → build → govern → communicate; 10 = AI strategy lane).

## Conventions for editing or adding a skill

**Frontmatter `name:` MUST equal the skill's folder name.** (CI of the human kind — always verify.)

Every `SKILL.md` follows this section structure — match it exactly for consistency:

```
---
name: <kebab-case, == folder name>
description: <one sentence: what it does + when to use it; trigger-rich for skill selection>
---

# Title

## When to use            (3-4 concrete triggers)
## When not to use         (point to the sibling skill that fits instead)
## Method                  (numbered; real mechanics, not topic labels)
## Key formulas / decision rules   (where quantitative)
## Output format           (the actual artifact template)
## Quality bar             (what separates this from generic output)
## Common failure modes
## Pairs with              (how it chains to other skills, by name)
## Worked example          (concrete, with numbers)
```

When adding a skill: create `skills/<category>/<name>/SKILL.md`, then **update README.md** (the
category table count, the numbered skill list, and the "how skills fit together" map).

## Non-negotiables (the house style)

- **The math must tie out.** Any formula stated must be correct; any worked example must compute.
  Bridges reconcile to zero residual, models balance, NPV/IRR/LTV/elasticity formulas are standard
  and right. If you change a finance/quant skill, re-verify the worked example by hand.
  (Reference: `margin-bridge` uses the price@Q₁ / volume@prior-margin convention so it reconciles
  exactly — do not reintroduce a price@Q₀ convention without adding the interaction term.)
- **Answer-first, MECE, hypothesis-driven, exposed logic, honest ranges, "so what" on everything.**
  These are the design principles in the README and the seven tests in WORKFLOW.md Part 4.
- **Quality language is implicit.** Describe the standard ("filler," "generic," "weak output,"
  "hollow content") — do **not** use the literal phrase "AI slop" / "slop" in skills or guides.
  The discipline stays; the label doesn't.
- **No filler.** No throat-clearing, no empty intensifiers ("robust," "world-class," "holistic"),
  no verb-free arguments, no bullet sprawl. Every line is an assertion with a point of view.
- **Cross-references use plain skill names** in backticks (e.g., `market-mapping`) inside skills;
  README/guides use Markdown links with the full nested path.

## Things to check before committing

- Frontmatter `name:` matches every folder.
- README links all resolve (42 SKILL.md links + 10 folder links).
- The anchor `WORKFLOW.md#part-4--the-quality-standard` is referenced consistently.
- No literal "slop" appears (note: "**Slope** chart" in DESIGN-GUIDE.md is a legitimate term).
- Any edited finance/quant worked example still computes correctly.

## Slide-generation engine (planned, not built)

A separate skill (`presentation-image-generator` per the source spec) will render an approved
storyline into slides. It is **design-stage only** — do not assume it exists when chaining skills.
The intended hand-off: analysis skills → `narrative-builder` (storyline) → slide engine.
