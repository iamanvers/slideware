# The Design Reference Guide — Representing Information for Executive Decisions

Analysis is only half the job. The other half is **representation**: choosing the form that makes
the insight land with a specific audience in the time you have. This guide is the reference for
*how to show what you know* — which exhibit fits which message, what each form communicates (and
secretly implies), and how to tune everything to your context.

Use it alongside [WORKFLOW.md](WORKFLOW.md). Where the workflow governs *what you conclude*, this
governs *how you present it*.

---

## Part 1 — First principles

1. **The message picks the exhibit, never the reverse.** Decide the one sentence the exhibit must
   prove ("the action title"), *then* choose the form that proves it fastest. If you can't write the
   takeaway sentence, you're not ready to draw anything.

2. **One exhibit, one message.** If a chart makes two points, it makes neither. Split it.

3. **The title carries the insight.** Every exhibit gets an **action title** — the takeaway as a
   full sentence ("Expansion revenue, not acquisition, drove the decline"), not a topic label
   ("Revenue by source"). A reader who reads only your titles should get the whole argument.

4. **Data-ink discipline.** Every pixel earns its place. Strip gridlines, 3-D effects, redundant
   legends, decorative color. Clutter signals you don't know what matters.

5. **Color is meaning, not decoration.** Default to greyscale + **one** accent color for the point
   you're making. Color = "look here." If everything is colored, nothing is emphasized.

6. **Show uncertainty honestly.** Ranges, error bands, and "estimate" flags build trust; false
   precision destroys it. A confident single number you can't defend is worse than an honest range.

7. **Match encoding to how people read it.** Position and length are read most accurately; angle and
   area less so; color hue and saturation least. Encode the most important variable in the most
   accurately-read channel. (This is why bars usually beat pies and why a ranked dot plot beats a
   rainbow heat map for precise comparison.)

---

## Part 2 — The exhibit catalog

Organized by the **job** the exhibit does. For each job: the standard forms, the lesser-used
specialist forms, what each communicates, and the trap. The two signature consulting exhibits —
the **waterfall** and the **2×2 / strategy matrix** — and the qualitative encodings (**Harvey
balls**, RAG) and flow forms (**Sankey**) all live here.

### A. Comparison & ranking — "X is bigger/smaller/better than Y"
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Bar (horizontal)** | Comparing one metric across categories | "These are bigger than those" | Unsorted bars; truncated axis that exaggerates |
| **Grouped/clustered bar** | Same metric across categories × a second dimension | "The pattern differs by group" | More than ~3 groups becomes unreadable |
| **Dot / lollipop plot** | Ranking many items compactly | "Here's the order" | — (cleaner than bars for long lists) |
| **Dumbbell / connected dot** | Gap between two points per item (current vs target, year-on-year) | "Here's the gap, item by item" | Unlabeled endpoints |
| **Bullet chart** | Actual vs target with qualitative bands | "Ahead/behind the goal" | Overuse where a number + delta suffices |
| **Pareto chart** | Ranked bars + cumulative line | "A few categories drive most of it (80/20)" | Omitting the cumulative line (the whole point) |
| **Radar / spider chart** | One or two items across 5–8 dimensions | "Profile shape / strengths and gaps" | Comparing >2 items; implying area means something |
| **Slope chart** | Two-period change across many items | "Who rose, who fell, who crossed" | Too many crossing lines |

### B. Composition — "what it's made of / how the mix shifts"
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **100% stacked bar** | Mix/share across a few groups or over time | "The composition differs / is shifting" | >5 segments; ordering segments inconsistently |
| **Stacked bar (absolute)** | Total *and* its parts | "Both the size and the split" | Hard to compare inner segments — only the bottom one shares a baseline |
| **Pie / donut** | A single part-to-whole with 2–3 slices | "This dominates" | More than ~3 slices; comparing across multiple pies (use 100% bars) |
| **Treemap** | Hierarchical part-to-whole, many items | "Relative size within a hierarchy" | Precise comparison (area is read poorly) |
| **Sunburst** | Multi-level hierarchy composition | "Nested shares" | Depth beyond 2–3 rings |
| **Marimekko / Mekko (variable-width stacked)** | Two dimensions at once — e.g. segment size (width) × share (height) | "Where the big, winnable pockets are" | Reading precise values; overcrowding |
| **Waterfall / bridge** | How you got from A to B (decomposition) | "Exactly what added and subtracted" | Not reconciling to endpoints (residual must ≈ 0) |
| **Icon array / pictograph** | Proportion for a lay audience (e.g. "23 of 100 customers churn") | "This share, made tangible" | Using for precise multi-category data |

> **The waterfall is the signature decomposition exhibit.** Use it for margin bridges, growth
> bridges, EBITDA→FCF walks, value-creation bridges, and budget variances. It turns "margin fell
> 4 points" into "here are the five forces that moved it, and which one to act on." See `margin-bridge`.

### C. Trend over time — "the trajectory / the inflection"
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Line chart** | A metric over time | "The trajectory / where it bent" | Spaghetti (5+ lines) — highlight one, grey the rest; label directly |
| **Indexed / rebased line (=100)** | Comparing growth of series with different scales | "This grew faster than that" | Hiding the absolute size that also matters |
| **Area / stacked area** | A total over time and its composition | "The whole and its parts grew/shrank" | Many bands obscure the lower series |
| **Cohort / retention curve** | Retention or ramp by start group | "Structural vs cyclical change" | Too many cohorts; no benchmark curve |
| **Fan chart (projection bands)** | A forecast with widening uncertainty | "Our confidence narrows the further out we look" | A single forecast line implying false certainty |
| **Bump chart** | Rank changes over time | "Who overtook whom" | Many items crossing |
| **Sparkline** | Trend inline in a table/dashboard | "Direction at a glance" | Using where exact values matter |
| **Candlestick / OHLC** | Price ranges over time (finance) | "Volatility and range, not just close" | Non-finance audiences |
| **Step chart** | Values that change in discrete jumps (price tiers, rates) | "It holds, then steps" | Smoothing into a line (misleads) |

### D. Relationship & correlation — "these things move together"
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Scatter plot** | Relationship between two variables across many items | "They co-vary / here are the outliers" | Implying causation from correlation |
| **Bubble chart** | Three variables — two axes + magnitude | "Big things in the sweet spot" | Bubble *diameter* vs *area* confusion (scale by area) |
| **Connected scatter** | Two variables tracked over time | "The path the relationship took" | Unlabeled time direction |
| **Heat map** | A grid where the high/low pattern matters | "The hot spots" | Rainbow palettes — use single-hue intensity |
| **Correlation matrix** | Pairwise relationships among many variables | "What relates to what" | Over-interpreting weak correlations |
| **Network / node-link diagram** | Connections among entities (org, supply, influence) | "Who connects to whom; the hubs" | Hairballs — filter to the meaningful links |
| **Chord diagram** | Flows/relationships among a fixed set (trade, migration between segments) | "Bilateral flows in a closed system" | Too many nodes; prefer a Sankey for directional flow |

### E. Distribution & sensitivity — "the spread / what moves the answer"
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Histogram** | Distribution of one variable | "Where values cluster; the shape" | Misleading bin widths |
| **Box-and-whisker** | Distribution summary across groups | "Median, spread, and outliers compared" | Lay audiences who don't read quartiles |
| **Violin / beeswarm** | Full distribution shape across groups | "The actual density, not just quartiles" | Overkill for executive audiences |
| **Tornado diagram** | Sensitivity — which driver swings the result most | "Attack this driver first" | Inconsistent flex ranges across drivers (see `business-case-builder`) |
| **2-variable sensitivity table** | Output across two key inputs | "The combinations that make or break it" | Too fine a grid; no shading of the breakeven zone |
| **Spider/radar (risk)** | Multi-dimension risk or capability profile | "Where exposure concentrates" | Comparing too many entities |

### F. Flow & process — "how things move through a system"
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Sankey diagram** | Flows where volume splits/merges (revenue → segments → margin; headcount moves; energy/material flow; budget allocation) | "Where the volume goes and where it leaks; widths = magnitude" | Too many strands; use when *quantity flowing* is the point |
| **Funnel chart** | Sequential conversion with drop-off | "Where we lose the most in the journey" | Implying equal stage difficulty; ignoring absolute volumes |
| **Flow / process diagram** | Steps and decision points | "How it works end to end" | Excess detail that hides the breaking step |
| **Swimlane diagram** | Process across owners/functions | "Who does what and where it hands off" | No hand-off failure points marked |
| **Value-stream map** | Process with time/cost/waste per step | "Where the delay and waste sit" | Mapping the whole plant when one flow matters |
| **Customer journey map** | Stages of customer experience with pain points | "Where the experience breaks" | Generic stages with no evidence |

> **Use a Sankey when the *quantity flowing and splitting* is the message** — e.g., "$100M revenue
> flows in, but 40% leaks out as discounts and cost-to-serve before it reaches operating profit."
> A waterfall decomposes a single number; a Sankey shows volume routing through a system.

### G. Hierarchy & structure — "how it's organized / the logic tree"
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Issue / hypothesis tree** | MECE decomposition of a problem | "The structure of the question" | Topic lists masquerading as a logic tree (see `problem-structuring`) |
| **Decision tree** | Sequential choices with probabilities/payoffs | "The expected-value path" | Unstated probabilities |
| **Org chart** | Reporting structure | "Who reports to whom" | Confusing it with decision rights |
| **RACI / RAPID matrix** | Decision rights / accountability | "Exactly one owner per decision" | Multiple deciders — defeats the purpose (see `operating-model-design`) |
| **Tree / dendrogram** | Nested grouping (segmentation, taxonomy) | "How things cluster" | Over-deep trees |
| **Mind map** | Early-stage idea structuring (working, not final) | "The space of considerations" | Shipping it as a finished exhibit |

### H. Geospatial — "where, on a map"
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Choropleth (shaded regions)** | A rate/metric by geography | "Regional concentration" | Shading by raw count (population bias) — use rates |
| **Symbol / bubble map** | Magnitude by location | "Where the big nodes are" | Overlapping bubbles in dense areas |
| **Flow map** | Movement between locations | "Trade/migration/supply routes" | Too many arrows |
| **Cartogram** | Resizing geography by a metric | "Economic size, not land size" | Unfamiliar shapes confuse audiences |

### I. Time & project — "the plan, sequenced"
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Gantt chart** | Tasks over time with dependencies | "Sequence and overlap" | Dates with no owners or exit criteria |
| **Roadmap with stage gates** | Phased program with go/no-go gates | "Phases, owners, and what unlocks the next" | Calendar phases instead of exit-criteria phases (see `transformation-roadmap`) |
| **Milestone timeline** | Key dates only | "The handful of moments that matter" | Clutter of minor tasks |
| **Swimlane roadmap** | Workstreams × time | "Parallel tracks and their owners" | Exceeding real capacity |

### J. Qualitative & rating encodings — "judgment at a glance"
These compress expert judgment into a scannable grid. They are the visual language of consulting
scorecards and comparison tables.
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Harvey balls** (○ ◔ ◑ ◕ ●) | Ordinal rating (0–4) across options × criteria | "Relative strength per cell, comparable down columns" | Using for precise data; no legend; inconsistent direction (full = good) |
| **Traffic-light / RAG** | Status or risk level (Red/Amber/Green) | "What needs attention now" | No defined thresholds behind the colors; red/green only (colorblind) |
| **Stoplight table** | Many items × dimensions, RAG-shaded | "The pattern of strong/weak across a portfolio" | Subjective colors with no rubric |
| **Check / cross matrix (✓/✗)** | Binary feature/criterion presence | "Has it or not" | Hiding nuance that needs a Harvey ball |
| **+/− or High/Med/Low table** | Qualitative scoring across options | "Directional comparison" | No weighting when criteria differ in importance |
| **Heat-shaded table** | Numbers + background intensity | "The numbers *and* the pattern" | Shading drowning the figures |

> **Harvey balls** are the right tool for an option-comparison scorecard (`strategic-options`,
> vendor selection, `commercial-due-diligence`): rows = options, columns = weighted criteria, each
> cell a filled fraction. The eye scans a column to see who wins on each criterion — far faster than
> reading numbers, while still ordinal and honest. Always include a legend and keep "more filled = better."

### K. Strategic frameworks — named exhibit templates
These are pre-structured exhibits that carry an embedded analytical logic. Reach for them when the
*framework itself* is the message; don't force-fit one where a plain chart is clearer.
| Framework | Use it for | Communicates | Trap |
|---|---|---|---|
| **Generic 2×2 matrix** | Positioning on two decisive, independent dimensions | "Strategic posture by quadrant" | Axes chosen to flatter a pre-baked answer; dots placed by vibe |
| **BCG growth–share matrix** | Portfolio of businesses: market growth × relative share (Stars / Cash Cows / Question Marks / Dogs) | "Which units to fund, milk, fix, or exit; cash flows across the portfolio" | Treating it as gospel; relative-share axis misdefined; ignoring synergies between units |
| **GE–McKinsey nine-box** | Portfolio on market attractiveness × competitive strength (richer than BCG) | "Graded invest/hold/harvest posture per unit" | Unscored, subjective placements (see `portfolio-review`) |
| **Ansoff matrix** | Growth options: existing/new product × existing/new market | "The four growth vectors and their risk" | Listing without assessing right-to-win |
| **Three Horizons** | Balancing core, adjacent, and transformational bets | "Are we investing across time horizons?" | Using as a timeline rather than a risk/maturity frame (see `strategic-options`) |
| **Porter's Five Forces** | Industry structure / profit pressure | "Where margin pressure comes from" | A static list with no H/M/L rating or "so what" (see `competitive-intel`) |
| **Value chain** | Activities from input to customer | "Where cost and value are added" | No link to profit pools or differentiation |
| **Profit-pool chart** | Value-chain stage (width = revenue) × margin (height) | "Where the money actually sits and is migrating" | Sizing revenue and calling it profit (see `profit-pool-analysis`) |
| **SWOT / TOWS** | Quick internal/external scan | "The strategic situation in four cells" | A dumping ground with no prioritization or resulting action |
| **Strategy canvas / value curve** (Blue Ocean) | Your offer vs rivals across buyer factors | "Where we differ / where to break the trade-off" | Cherry-picked factors |
| **Perceptual / positioning map** | Brand/product position on two buyer attributes | "White space in customers' minds" | Axes that aren't the buyer's real decision criteria |
| **McKinsey 7S** | Organizational alignment diagnostic | "Where structure, systems, and culture misalign" | Description with no change implication |
| **S-curve / experience curve** | Adoption or cost-vs-cumulative-volume dynamics | "Where we are on the maturity/cost trajectory" | Assuming the curve continues without evidence |
| **Kano model** | Feature classification (basic/performance/delight) | "What merely satisfies vs what delights" | Static treatment (delighters become basics over time) |

### L. Finance-specific exhibits
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Football field** | Valuation range across methods (DCF, comps, precedents) | "The defensible range and where methods agree/diverge" | A single point estimate (see `valuation`) |
| **Value-creation bridge** | Walk from entry to exit value (PE) or plan vs actual | "What created the value — multiple, growth, or deleveraging" | Not reconciling to the endpoints |
| **EBITDA→FCF / earnings bridge** | Walk between financial line items | "What sits between the two numbers" | Skipping reconciliation |
| **Sources & uses table** | Deal funding structure | "Where the money comes from and goes" | Not balancing |
| **Debt maturity ladder** | Debt due by year | "Refinancing walls and timing risk" | Ignoring covenants |
| **Returns sensitivity (IRR grid)** | IRR/NPV across two assumptions | "How fragile the return is" | No breakeven zone highlighted |

### M. Tables & single numbers
| Form | Use it for | Communicates | Trap |
|---|---|---|---|
| **Data table** | Precise values readers will look up | "The exact figures" | A table where a chart would reveal the shape faster |
| **Weighted scorecard table** | Options × weighted criteria with scores | "The transparent basis for the choice" | Weights set after scoring; no rationale per cell |
| **Comparison matrix** | Options/vendors × attributes (often Harvey balls) | "The full side-by-side" | Unweighted criteria of unequal importance |
| **Single big stat / KPI callout** | The one number that anchors a decision | "This is the number that matters" | Decorating a weak number; no source/basis |

---

## Part 3 — Message → exhibit quick map

| If your message is… | Reach for… |
|---|---|
| "X is bigger/smaller than Y" | Ranked horizontal bar / dot plot |
| "A few drivers cause most of it" | Pareto chart |
| "Here's the gap per item" | Dumbbell / bullet chart |
| "The mix is shifting" | 100% stacked bar; Marimekko for size × share |
| "Here's how we got from A to B" | **Waterfall / bridge** |
| "Where the volume flows and leaks" | **Sankey diagram** |
| "Where we lose people in the journey" | Funnel chart |
| "Here's the trend / the inflection" | Line (highlight one series) |
| "This grew faster than that" | Indexed line |
| "Structural vs cyclical change" | Cohort / retention curves |
| "The forecast, with honest uncertainty" | Fan chart |
| "Where the attractive, winnable pockets are" | Marimekko or bubble 2×2 |
| "Strategic posture / where each thing sits" | **2×2 / GE-McKinsey / BCG matrix** |
| "Which units to fund, milk, or exit" | **BCG growth–share** or GE nine-box |
| "The four growth vectors" | Ansoff matrix |
| "Where industry margin pressure comes from" | Porter's Five Forces |
| "Where value/cost/profit sits in the chain" | Value chain + profit-pool chart |
| "These two variables relate" | Scatter (+ bubble for a 3rd) |
| "Which assumption swings the result" | Tornado diagram |
| "How the units compare across criteria" | **Harvey-ball scorecard** |
| "What needs attention now" | RAG / stoplight table |
| "Who decides" | RACI / RAPID matrix |
| "The structure of the problem" | Issue / hypothesis tree |
| "The plan, sequenced and owned" | Roadmap with stage gates |
| "The defensible valuation range" | Football field |
| "What created the value" | Value-creation bridge |
| "Where the risks/hot spots are" | Heat map / risk matrix |
| "Regional concentration" | Choropleth map |
| "The one number that decides this" | Single big stat |
| "Full multi-attribute comparison" | Scorecard table (Harvey balls, weighted) |

---

## Part 4 — Tuning representation to your context

Same analysis, different audience → different representation. Read the room and adjust on these dials.

### By audience
- **Board / CEO / investment committee.** Answer-first, one exhibit per point, action titles, the
  decision and the ask up front. They want the "so what" and the risk, not the method. Depth lives in
  an appendix. One killer 2×2, waterfall, or football field beats ten charts. Time budget: assume you
  get half of what you're promised (see `narrative-builder`'s four lengths).
- **CFO / finance.** Show the build. Driver-based tables, reconciliations, sensitivities (tornado,
  IRR grids), sources. They will probe the model — expose the logic and assumptions explicitly.
- **Operators / functional leaders.** Concrete, near-term, owned. Roadmaps, RACI, the first 90 days,
  metrics they control. Less 2×2, more "who does what by when."
- **Technical / analytical teams.** Methodology, data lineage, distributions, confidence intervals,
  edge cases. Here the detail *is* the credibility — box plots and histograms are welcome.
- **External / public / regulatory.** Conservative claims, sourced, defensible. Strip anything you
  can't stand behind; prefer simple bars and clearly-labeled ranges over clever forms.

### By decision stakes & reversibility
- **Big, irreversible decision (M&A, major capex):** more rigor visible — football fields, scenario
  ranges, tornado sensitivities, downside cases. Show you've earned the conviction.
- **Small, reversible decision:** a single stat and a recommendation. Don't over-produce; matching
  exhibit weight to decision weight is itself a signal of judgment.

### By medium
- **Live presentation:** one message per slide, build complexity progressively, the title tells the
  story if the projector dies. Anticipate the hostile question per exhibit. Avoid dense small-multiples.
- **Read-ahead / memo:** denser is fine, but stay answer-first (BLUF); the reader has no narrator.
- **Dashboard:** hierarchy (north star → drivers → health), RAG thresholds = action, sparklines for
  trend, not a wall of equal-weight tiles (see `kpi-architect`).
- **Spreadsheet model:** inputs/calcs/outputs separated, colored assumption cells, built-in checks
  (see `financial-modeling`).

### By time available
- **30 seconds:** the headline number + the recommendation. One exhibit, maybe none.
- **2 minutes:** SCQA + the governing thought + one proof exhibit.
- **10–60 minutes:** the full Pyramid with one exhibit per supporting argument, backup in appendix.

### By data maturity
- **Rich data:** precise charts, real numbers, tight ranges, distributions where they matter.
- **Thin / early data:** show ranges and assumptions transparently, label exhibits "illustrative,"
  use Harvey balls / RAG for honest qualitative judgment, and present the *structure* of the answer
  with the workplan to fill it. Never dress an illustrative number as a finding — that one move
  undoes all the credibility the rest of the work earns (see [WORKFLOW.md](WORKFLOW.md#part-4--the-quality-standard)).

### By cultural / accessibility constraints
- **Colorblind-safe:** never rely on red/green alone — add shape, label, or position. RAG should
  carry text or icons, not just fill.
- **Print / grayscale:** test that the accent still reads when color is stripped.
- **Numerate vs lay audiences:** box plots and violins for the former; icon arrays and simple bars
  for the latter.

---

## Part 5 — Anatomy of an executive exhibit

Every chart that reaches an executive should have:

1. **Action title** (top) — the takeaway as a sentence with a verb.
2. **The exhibit** — the single cleanest form that proves the title (Part 2).
3. **A callout** — the one data point/zone that matters, in the accent color, annotated.
4. **Source line** (bottom) — data source and period, so it's auditable. "Source: client P&L FY22–24; team analysis."
5. **Units & basis** — currency, real vs nominal, gross vs net, time period. Ambiguity here is a credibility leak.

```
┌────────────────────────────────────────────────────────────┐
│ Mix shift to the low-margin channel drove 2.6pts of the     │ ← action title (the message)
│ 4pt EBIT margin decline — not discounting                   │
│                                                              │
│   16% ──┐                                                    │
│         │ −0.5  +0.3                                         │
│         price  vol  ┌──────┐ −2.6        ┌── 12%            │ ← waterfall (the form)
│                     │ MIX  │ ████  −1.4  │                  │
│                     └──────┘ cost  ┌─────┘                  │ ← accent on MIX (the callout)
│                                                              │
│ Source: client P&L FY23–24; team analysis. EBIT margin, %.  │ ← source + basis
└────────────────────────────────────────────────────────────┘
```

---

## Part 6 — The exhibit quality checklist

Before any exhibit ships:

- [ ] **Action title** states the takeaway as a sentence (not a topic label).
- [ ] **One message** — the exhibit proves exactly one thing.
- [ ] **Right form** — it's the fastest form to prove that message (Parts 2–3), not the default chart.
- [ ] **Right encoding** — the key variable is in the most accurately-read channel (position/length first).
- [ ] **Ranked / ordered** — categories sorted by value unless they have natural order.
- [ ] **Honest axes** — no truncated/exaggerated scales; ranges or bands shown where uncertain.
- [ ] **Color = emphasis** — greyscale + one accent on the point; colorblind-safe; not a rainbow.
- [ ] **Data-ink clean** — no 3-D, no chartjunk, no redundant legend.
- [ ] **Sourced** — data source, period, units, and basis (gross/net, real/nominal) are stated.
- [ ] **So-what present** — a reader gets the decision implication without you narrating.
- [ ] **Tuned** — depth, density, and form match *this* audience, stakes, medium, and time.
- [ ] **Consistent** — numbers match every other artifact in the pack (see WORKFLOW Part 3).

If an exhibit fails any box, it isn't done. The fix is almost always to **sharpen the message**,
not to add more decoration.
