# Mode 1: Professional (Corporate / MBB / Strategy Consulting)
> Authoritative specification for designing C-suite corporate deliverables, strategy consulting presentations (McKinsey, BCG, Bain), investment banking pitchbooks, and executive decision decks.
> Synthesized from ex-MBB partner methodologies and the empirical deconstruction of 160+ public McKinsey client decks (Slideworks consulting corpus).

---

## 1. Visual Identity & Foundational Philosophy

### The "Standalone Deliverable" Philosophy
Real MBB presentations are **not** oral slideshow props with 3 bullet points meant for a speaker to talk over. In tier-1 strategy consulting, slide decks are **dense, self-contained analytical briefing documents** (often termed "deckuments" or "pre-reads"). They are built to be read, annotated, and debated by C-suite executives, boards of directors, and government ministers with zero voiceover.

Every slide must function as an independent analytical unit:
1. **The Action Title** states the strategic conclusion upfront.
2. **The Lead-In Box** synthesizes the core argument and empirical proof points.
3. **The Data Exhibits** provide the quantitative/structural evidence.
4. **The Footnote / Source** anchors the data in reality.

---

## 2. Barbara Minto's Pyramid Principle & SCQA Storylining

Every consulting engagement and presentation is governed by the **Pyramid Principle**:
- **Answer First (Top-Down Communication):** State the overarching recommendation or finding on Slide 1 and at the top of every slide. Never build suspense or bury the conclusion at the end.
- **MECE Structuring (Mutually Exclusive, Collectively Exhaustive):** Every breakdown—market segments, operational levers, financial impacts—must divide the problem space without overlaps or omissions.
- **SCQA Narrative Arc:**
  - **Situation (S):** The undisputed current context (e.g., *"Client X is the #2 player in European industrial logistics"*).
  - **Complication (C):** The friction or disruption (e.g., *"Rising fuel costs and new decarbonization mandates will erode EBITDA by 320 bps by 2027"*).
  - **Question (Q):** The implied executive question (e.g., *"How can Client X protect margins while electrifying 40% of the fleet?"*).
  - **Answer / Resolution (A):** The core recommendation (e.g., *"Implement a 3-pillar transformation capturing $180M in recurring savings"*).

---

## 3. The Anatomy of a McKinsey Slide

Every professional consulting slide follows a strict 5-layer hierarchy:

```
+--------------------------------------------------------------------------------------------------+
| TRACKER BREADCRUMB: REVENUE ACCELERATION > COMMERCIAL PRICING LEVERS                 Slide 14   |
+--------------------------------------------------------------------------------------------------+
| ACTION TITLE: Optimizing value-based pricing and renegotiating legacy contracts will capture     |
| $45M in run-rate EBITDA over the next 18 months                                                  |
+--------------------------------------------------------------------------------------------------+
| LEAD-IN / CALLOUT BOX (Light Slate #F1F5F9 or Hairline Box):                                     |
| While volume growth has plateaued at 2.1% CAGR, significant price dispersion exists across tiers;|
| closing the bottom-quartile discount gap unlocks immediate margin without risking tier-1 churn.  |
+--------------------------------------------------------------------------------------------------+
| EXHIBIT 1: Current Margin Spread        | EXHIBIT 2: Three Price Levers  | EXHIBIT 3: EBITDA Bridge|
| (Column: 390px)                         | (Column: 390px)                | (Column: 390px)         |
| - Top-quartile realized margin: 28%     | 1. Dynamic Surcharge Model     | Base 2025: $120M        |
| - Bottom-quartile margin: 11%           | 2. Renegotiate Tier-3 Contracts| + Discount Cap: +$22M   |
| - Spread variance: 1,700 bps            | 3. Indexation to Input Costs   | + Surcharges: +$23M     |
| [Structured bar chart or clean table]   | [Structured 3-row card block]  | Target 2026: $165M      |
+--------------------------------------------------------------------------------------------------+
| FOOTNOTE / SOURCE: Source: Company ERP Data (FY2023-FY2025); McKinsey Commercial Practice Benchmark|
+--------------------------------------------------------------------------------------------------+
```

### Layer Rules:
1. **Tracker / Kicker Breadcrumb:** Top-left, 10–11px uppercase bold, `#64748B`. Tells the executive exactly which workstream or pyramid branch this slide belongs to.
2. **Action Title:** 18–22px bold, `#0A192F`, max 2 lines. Must be a complete, grammatically sound sentence that states an analytical assertion.
   - *Prohibited:* "Market Overview", "Financial Results", "Key Recommendations".
   - *Mandatory:* "European retail footfall dropped 14% post-2020, accelerating the transition to high-density urban micro-fulfillment."
3. **Lead-In Callout Box:** Full-width or top-aligned card (`#F8FAFC` or `#FFFFFF` with `#E2E8F0` border). Summarizes the 2–3 key insights so a board member can scan the takeaway in 5 seconds.
4. **Data Exhibits (2 to 4 Columns):** Structured cards, tables, or charts with hairline dividing rules (`#E2E8F0`).
5. **Footnotes & Source Citations:** Bottom-left, 9–10px, `#64748B`. Explicitly states datasets, time periods, and assumptions.

---

## 4. Color Palette & Anti-AI Rules

```typescript
export const PROFESSIONAL_COLORS = {
  canvas: '#F8FAFC',          // Crisp light slate / off-white background
  cardBg: '#FFFFFF',          // Pure white card container
  cardStroke: '#E2E8F0',      // 1px hairline border
  leadInBg: '#F1F5F9',        // Lead-in callout background
  textPrimary: '#0A192F',     // Deep midnight navy (high contrast, authoritative)
  textSecondary: '#475569',   // Refined slate for descriptions and labels
  textMuted: '#94A3B8',       // Subtle grey for metadata and trackers
  accentPrimary: '#1E40AF',   // Deep corporate sapphire (NOT generic electric AI blue)
  accentAlert: '#991B1B',     // Formal crimson for risk, deficit, or hurdles
  accentSuccess: '#166534',   // Forest green for growth, synergy, or upside
  tableAltRow: '#F8FAFC',     // Alternating row background for data tables
};
```

### Strict Anti-AI Design Invariants:
- **NO Generic AI Blue (`#2563EB`, `#3B82F6`):** Use deep navy `#0A192F` or deep sapphire `#1E40AF`.
- **NO Top Colored Border Lines:** Never put a 2px–4px blue or gradient line across the top edge of slides.
- **NO Sparkle / Capsule Badges:** Never add `✦ AI Powered` or rounded capsule pill tags that look like SaaS marketing widgets.
- **NO Markdown Em-Dashes (`—`) or Programmer Double-Slashes (`//`):** Use clean colons, commas, or parentheses in copy.
- **NO Fabricated Numbers:** Every metric must have realistic units (`bps`, `CAGR %`, `$M`, `FTEs`, `payback months`).

---

## 5. The 20 Core Consulting Slide Archetypes

Analysis of 160+ McKinsey, BCG, and Bain presentations proves that 80%+ of all strategy decks rely on these 20 standardized slide archetypes:

### 1. Executive Summary / SCR Dashboard
- **Purpose:** Provide the entire engagement's findings on a single slide for the board.
- **Layout:** 3 wide horizontal cards or 3 vertical columns representing Situation, Complication, and Resolution, each with 2–3 quantified bullet points and an impact callout.

### 2. Market Sizing & Growth Waterfall (TAM / SAM / SOM)
- **Purpose:** Break down total addressable market to actionable revenue opportunity.
- **Layout:** Step-down waterfall or 3 concentric analytical cards with explicit CAGR drivers and segment filters.

### 3. Competitive 2x2 Positioning Matrix
- **Purpose:** Map players across two strategic dimensions (e.g., Market Reach vs. Digital Maturity).
- **Layout:** 4 quadrants with clear threshold axes, labeled competitor bubbles (sized by revenue), and an executive callout box highlighting the "Winning Zone".

### 4. Value Chain & Margin Pool Breakdown
- **Purpose:** Illustrate where value and profit margin are concentrated across the industry.
- **Layout:** 5–6 connected horizontal chevron stages (e.g., Raw Materials -> Processing -> Logistics -> Retail -> Aftermarket) with margin % and value capture tags below each step.

### 5. Initiative Prioritization Matrix (Impact vs. Feasibility)
- **Purpose:** Prioritize a portfolio of 15–30 strategic initiatives into quick wins vs. long-term bets.
- **Layout:** 2x2 grid (Y: Financial Impact, X: Implementation Feasibility) with quadrants: Quick Wins, Strategic Imperatives, Fill-Ins, and Deprioritize.

### 6. EBITDA / Cost-Reduction Bridge (Waterfall)
- **Purpose:** Quantify the exact journey from current EBITDA to target EBITDA.
- **Layout:** Horizontal waterfall chart: Base Revenue -> Volume Effects -> Price Optimization -> COGS Rationalization -> SG&A Reduction -> Target EBITDA.

### 7. Strategic Roadmap & Implementation Gantt
- **Purpose:** Sequence workstreams and milestones across time horizons.
- **Layout:** 3 Horizon columns (H1: Immediate 0–6 mo, H2: Medium 6–18 mo, H3: Long-term 18–36 mo) mapped across 3–4 functional workstreams.

### 8. Capability Maturity Model & Benchmarking Scorecard
- **Purpose:** Assess organizational capability across 5–8 functional dimensions.
- **Layout:** Matrix table with dimensions (Strategy, Tech, Talent, Governance) on the left, maturity stages (1 to 5) across columns, and Harvey balls (`○`, `◔`, `◑`, `◕`, `●`) indicating current vs. target state.

### 9. Marginal Abatement Cost Curve (MACC) / Cost Curve
- **Purpose:** Rank decarbonization or cost-reduction levers by economic efficiency.
- **Layout:** Step chart where column width represents total volume impact (e.g., tons CO2 or hours saved) and column height represents cost/benefit per unit.

### 10. Value Creation Levers / 3-Pillar Strategy
- **Purpose:** Standard high-level strategic recommendation architecture.
- **Layout:** 3 balanced vertical columns (`01`, `02`, `03`), each with an anchor theme, 3 action items, risk mitigation note, and bottom KPI box.

### 11. Decision Tree & Governance Escalation Matrix
- **Purpose:** Provide a logical protocol for organizational decision-making.
- **Layout:** Horizontal branching nodes from core trigger question to binary decision criteria to designated ownership body (Executive Committee, SteerCo, Unit Lead).

### 12. Customer Journey & Touchpoint Friction Map
- **Purpose:** Diagnose churn and drop-off across the customer lifecycle.
- **Layout:** Horizontal stage flow (Discover, Evaluate, Purchase, Onboard, Renew) with satisfaction scores, identified friction bottlenecks, and digital intervention levers.

### 13. Target Operating Model & Organizational Architecture
- **Purpose:** Outline structural organizational redesign.
- **Layout:** 3-tier horizontal architecture (Corporate Governance & Strategy -> Business Unit Execution -> Shared Services & Centers of Excellence).

### 14. Financial Sensitivity & Scenario Analysis
- **Purpose:** Model downside, base, and upside financial trajectories.
- **Layout:** 3 scenario cards (Conservative / Base / Aggressive) with transparent macro assumptions (oil price, GDP growth, interest rates) and projected financial outcomes.

### 15. Risk Assessment & Heatmap
- **Purpose:** Evaluate and mitigate operational, regulatory, or strategic risks.
- **Layout:** 3x3 or 5x5 matrix (Likelihood vs. Severity) with numbered risk dots and an accompanying mitigation table.

### 16. Procurement / Strategic Sourcing Lever Tree
- **Purpose:** Break down spend reduction opportunities across direct and indirect spend.
- **Layout:** Hierarchical tree decomposing total spend into Commercial Levers (supplier consolidation, rate card harmonization) and Demand Levers (spec reduction, consumption policies).

### 17. Digital & Technology Architecture Stack
- **Purpose:** Present IT modernization and digital transformation roadmap.
- **Layout:** Layered architectural stack (Front-End Engagement -> API / Middleware Layer -> Core Systems / ERP -> Cloud Infrastructure & Data Foundation).

### 18. Pilot / Case Study Deep-Dive Readout
- **Purpose:** Prove feasibility through empirical results from a pilot or single business unit.
- **Layout:** 3 structured containers: Context & Baseline, Actions Taken, and Quantified Results (e.g., +14% throughput, -22% scrap rate).

### 19. Chapter Breaker / Executive Teaser Slide
- **Purpose:** Transition between major deck sections while reinforcing the storyline.
- **Layout:** Dark navy or light slate background, large section number (`02`), bold chapter title, and a 2-sentence executive summary previewing the upcoming analysis.

### 20. Consolidated Recommendation & Governance Scorecard
- **Purpose:** Final wrap-up slide assigning ownership, capital, and timelines to every initiative.
- **Layout:** High-density structured table with columns: Workstream, Strategic Initiative, Executive Sponsor, Capex/Opex, Target Completion, and 12-Month Target KPI.

---

## 6. Micro-Components & Data Visualizers

MBB slides rely on specific visual micro-components that signal precision and executive polish:

### A. Harvey Balls (Qualitative Scoring)
Used extensively in benchmarking, maturity models, and feasibility scoring:
- `○` Empty (0% - Not Started / Poor)
- `◔` Quarter (25% - Initial Development)
- `◑` Half (50% - Moderate / In Progress)
- `◕` Three-Quarters (75% - Advanced)
- `●` Full (100% - Fully Mature / Best-in-Class)

### B. KPI Metrics with Contextual Deltas
Never present a standalone number without baseline and context:
```
+------------------------------------------------------+
| $42.8M                +14.2% YoY                     |
| Net Run-Rate Savings  Baseline: $37.5M (FY24 Actual) |
+------------------------------------------------------+
```

### C. Chevron Process Flow
Used for sequence, workflows, and value chains:
- Clean 1px outlined or subtle solid filled chevrons with step numbers (`STEP 01`).
- Never use heavy cartoon arrows; use crisp geometric chevrons with 8px horizontal spacing.

### D. Executive Callout Bento Containers
- Background: `#F1F5F9` (Slate 100) or pure white with `#E2E8F0` border.
- Border radius: 6px–8px (tight, formal; never pill-rounded 24px).
- Internal padding: 16px–20px.

---

## 7. Real Public McKinsey Case Study Decks for Reference

When designing corporate and consulting decks, refer to these canonical real-world public McKinsey decks cataloged on Slideworks:

1. **SAIL Digital Transformation (2025):** 115-page roadmap illustrating digital initiatives, target architecture, and clear multi-year workstream governance.
2. **The Future of Trash: Waste Containerization in NYC (2023):** 95-page operational study demonstrating detailed cost-benefit trade-offs, logistics models, and implementation hurdles.
3. **MTA COVID-19 Financial Impact Assessment (2020):** 38-page financial forecast modeling revenue shortfalls, cost elasticity, and federal funding gaps.
4. **City of Vancouver COVID-19 Business Recovery (2020):** 26-page masterclass in applying Barbara Minto's SCR (Situation-Complication-Resolution) framework.
5. **Chilean Green Hydrogen Pathway (2020):** 65-page industrial strategy featuring levelized cost curves, export economics, and infrastructure roadmaps.
6. **NC Department of Transportation Review (2019):** 24-page board-level diagnostic on cash reserve variances and operational governance.
7. **University of Arizona Strategic Plan (2018):** 25-page presentation of a 5-pillar institutional strategy with quantified initiative scorecards.
8. **Lebanon Economic Vision (2018):** 1,200+ page comprehensive economic masterplan covering macro diagnostics, sector deep-dives, and detailed one-pager executive summaries.
9. **UK Electricity Efficiency Potential (DECC / 2012):** 129-page report with textbook McKinsey cost curves, efficiency barriers, and prioritization matrices.
10. **USPS Future Business Model (2010):** 39-page strategy document dissecting structural mail volume decline and retail network optimization.

---

## 8. Summary Checklist for Professional Consulting Slides

Before exporting or approving a slide in Professional Mode, verify:
- [ ] Is the title a complete, bold **action title** stating the analytical conclusion?
- [ ] Is there a **tracker breadcrumb** indicating the workstream at the top?
- [ ] Does the slide contain a **lead-in callout box** summarizing the key data?
- [ ] Are all columns and cards structured using clean hairlines (`#E2E8F0`) with 16px–24px gaps?
- [ ] Are all metrics accompanied by units, baselines, and timeframes?
- [ ] Are data sources and methodologies explicitly cited in the bottom footer?
- [ ] Are all generic AI design tropes (electric blue fills, top colored bars, sparkle tags, em-dashes) completely absent?
