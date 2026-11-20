---
name: presentation-deck-design-system
description: "Master design system, typography matrix, layout patterns, and technical guidelines for designing world-class presentation decks via Figma Plugin API (use_figma) or code. Covers three distinct design archetypes: Professional (MBB / Strategy Consulting / Corporate / Executive), Medium (Editorial / The Ken / Tech Product), and Funky (Poppy Brutalism / Creative / High Energy). Use whenever the user asks to design, style, review, or code presentation slides, pitch decks, or visual artifacts."
---

# Presentation Deck Design System & Universal Figma MCP Skill

A universal, project-agnostic design system and AI skill for creating high-impact presentation decks. This skill allows any AI assistant to immediately understand and execute slides across three distinct visual archetypes: **Professional (MBB / Corporate)**, **Medium (Editorial)**, and **Funky (Poppy Brutalism)**.

---

## 🚨 MANDATORY BAN ON "AI TELLS" & CLICHÉS (STRICT ENFORCEMENT)

Human presentation designers, C-suite executives, and pitch judges immediately spot and reject lazy AI-generated aesthetics. The following elements are **STRICTLY PROHIBITED** across all modes:

1. **NO "AI Blue" / Generic Chatbot Indigo (`#2563EB`, `#3B82F6`):**
   - **Banned:** Generic SaaS blue cards, glowing royal-blue boxes, electric indigo buttons, and standard "Copilot/ChatGPT" corporate blue.
   - **Allowed Instead:** If using cool tones, use either grounded **Midnight Navy (`#0A192F`)** for Professional mode, or hyper-saturated **Electric Cyan (`#00F0FF`)** for Funky mode. Never generic chatbot blue.
2. **NO AI Badges / Sparkles / Pill Outlines:**
   - **Banned:** `✨ AI Insights`, `✦ Generated`, floating pill containers with borders around category kickers, and capsule tags that look like bot UI.
   - **Allowed Instead:** Clean, raw, uppercase monospace text (`JetBrains Mono Bold`) hanging freely without bounding badge boxes.
3. **NO Decorative Gradient Bars / Top Accent Lines:**
   - **Banned:** 2px–4px colored accent lines running across the very top or bottom edge of the slide canvas, glowing neon border trims, or rainbow dividers.
   - **Allowed Instead:** Grounded slide hierarchy where whitespace and bold typography create structure organically.
4. **NO Glassmorphism / Frosted Blur / Glowing Blobs:**
   - **Banned:** Background-blur cards (`backdrop-filter`), glowing neon halos around containers, and generic "neural net / circuit node" vector art.
   - **Allowed Instead:** Solid, confident card fills, tactile editorial borders, or physical-world art textures (torn paper, soft matte splatters at 45%–65% opacity).
5. **NO Fake Quantitative Metrics / Hallucinated Data:**
   - **Banned:** Inventing fake stats like "94.2% operational efficiency gain" or "3.8x faster turnaround" unless explicitly provided in source context.
   - **Allowed Instead:** Concrete qualitative operational mechanisms, structured milestones, verifiable delivery commitments, and realistic baselines.
6. **NO Em-Dashes (`—`) or Double Slashes (`//`):**
   - **Banned:** `// KICKER` or bullet points with `—`.
   - **Allowed Instead:** Use colons (`:`) or pipes (`|`).

---

## 1. Quick Mode Selector

When prompting an AI agent, specify the desired archetype:

```text
"Design this deck in [Professional | Medium | Funky] mode. Ensure zero AI tells."
```

| Mode | Target Audience & Tone | Primary Visual Identifiers | Key Fonts |
|---|---|---|---|
| **1. Professional (MBB / Corporate)** | C-suite, MBB strategy consulting (McKinsey/BCG/Bain), boards, formal enterprise case comps. | Standalone analytical read-aheads, complete-sentence Action Titles, Lead-In Callout boxes, MECE 2–4 column cards, hairline borders (`#E2E8F0`), Harvey Balls, explicit data sources (`#64748B`). Midnight Navy `#0A192F` and Crisp White `#FFFFFF`. | Inter, Plus Jakarta Sans, Merriweather, Georgia |
| **2. Medium (Editorial)** | Investigative journalism, *The Ken* case competitions, tech product deep-dives, strategic narrative pitches. | Warm newspaper off-white `#FDFBF7`, crimson red `#E5252A` accents, charcoal `#1A1A1A` text, bordered workflow cards, dashed wireframe boxes, pill headers, quotation takeaways. | Space Grotesk, Inter Extra Bold, Plus Jakarta Sans, JetBrains Mono |
| **3. Funky (Poppy Brutalism)** | Youth festivals, creative agencies, cultural showcases, dynamic branding, high-energy startup pitches. | Atmospheric tinted canvases (`#F2FAF0`, `#FDF5EE`, etc.), hyper-saturated solid cards (Lime `#A1FF5F`, Cyan `#00F0FF`, Tangerine `#FFA048`), pure black text, background art splatters (45%–65% opacity), anti-whitespace density. | Space Grotesk Bold, Inter Extra Bold, Plus Jakarta Sans Bold, JetBrains Mono Bold |

---

## 2. Benchmark Reference Designs & Live URLs

Refer to these exact benchmarks when designing or reviewing layouts:

1. **Professional / MBB Strategy Consulting (160+ Public McKinsey Decks Analyzed):**
   - **Knowledge Base:** [references/professional-mode.md](file:///C:/Users/Ayushya/presentation-deck-design-system/references/professional-mode.md)
   - **Benchmark Corpus:** [Slideworks 160+ Real McKinsey Presentations Deconstructed](https://slideworks.io/resources/47-real-mckinsey-presentations) (including SAIL Digital Transformation 2025, NYC Waste Containerization 2023, MTA Financial Model 2020, Vancouver COVID Recovery SCR 2020).
   - **URL:** [Draft 1 | MBB Strategy & Governance](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=3-2)
   - **Characteristics:** Standalone analytical briefing books, Barbara Minto's Pyramid Principle (SCQA), complete-sentence Action Titles, Lead-In Callout containers, 20 Core Consulting Archetypes (EBITDA bridge, 2x2 matrix, MACC curve, value chains, Harvey balls), and strict source attribution.

2. **Medium / Editorial (*The Ken* / HAQ Case Competition):**
   - **Characteristics:** Warm newspaper canvas (`#FDFBF7`), signature crimson accents (`#E5252A`), brutalist collegiate display cover ("THE GREAT REWIRING"), clean agent workflow pipelines (8 decisions, step icons, supervisor handoff), dashed wireframe cards for principles, before/after comparison tables ("WITHOUT HAQ" vs "WITH HAQ"), bold closing quotes.

3. **Medium / High-Energy Proposals:**
   - **URL:** [Draft 2 | BITS Pilani High-Energy](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=2-207)
   - **Characteristics:** Clean color-coded vertical tracks, prominent metric counters, structured multi-column proposals.

4. **Funky / Poppy Brutalism (Main Deck):**
   - **URL:** [Draft 3 | Modern Black & Type](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=0-1)
   - **Characteristics:** Hyper-saturated solid card containers, pure black typography (`#000000`), bold lead-ins before colons, atmospheric splatters/swashes at canvas depth, zero dead white space.

---

## 3. Universal Layout Architecture (1440 × 810 px — 16:9)

Every slide adheres to a fixed widescreen 16:9 canvas layout:

```
+-----------------------------------------------------------------------------------------+
| [Tracker Breadcrumb: WORKSTREAM > SUB-THEME]                              Slide [X]     |
| Slide Action Title: Full Grammatical Takeaway Sentence (20px–22px Bold)                 |
| x: 80, y: 44                                                                            |
+-----------------------------------------------------------------------------------------+
| [LEAD-IN CALLOUT CONTAINER: 2-3 Line Synthesized Analytical Takeaway] (y: 105, h: 65px) |
+-----------------------------------------------------------------------------------------+
|   MAIN DATA EXHIBIT ZONE (y: 185, height: 430 px)                                       |
|                                                                                         |
|   Layout Options:                                                                       |
|   • 3-Column Strategy Pillars: 3 cards of ~390px (gap: 20px)                            |
|   • 2x2 Strategic Matrix: 4 quadrants of 610px × 200px                                  |
|   • Value Chain / Pipeline: 5–6 horizontal chevrons with value pool data                |
|   • Data Table / Scorecard: Structured rows with alternating slate fills + Harvey balls  |
|   • EBITDA / MACC Waterfall Bridge: Step-down bar visualization with labeled deltas     |
|                                                                                         |
+-----------------------------------------------------------------------------------------+
|   FOOTNOTES & SOURCES (y: 630, height: 40px)                                            |
|   Source: Official ERP Data / External Benchmark; Methodology: N=2,400                  |
+-----------------------------------------------------------------------------------------+
```

---

## 4. The 3 Design Archetypes: Detailed Specs

### Mode 1: Professional (Corporate / MBB / Strategy Consulting)

- **Canvas Background:** Pure Crisp White (`#FFFFFF`) or Alabaster Slate (`#F8FAFC`).
- **Color Palette:**
  - Primary Dark: Deep Midnight Navy `#0A192F` (`{ r: 0.039, g: 0.098, b: 0.184 }`)
  - Secondary Slate: `#475569` (`{ r: 0.278, g: 0.333, b: 0.412 }`)
  - Accent Red/Blue: Deep Crimson `#991B1B` or Corporate Sapphire `#1E40AF`
  - Neutral Borders: Hairline `#E2E8F0` (`{ r: 0.886, g: 0.910, b: 0.941 }`)
  - Card Fills: `#FFFFFF` with `1px` stroke or subtle lead-in container `#F1F5F9`.
- **Slide Formula (The McKinsey Anatomy):**
  1. *Tracker Breadcrumb:* 10–11px uppercase bold, `#64748B`.
  2. *Action Title:* 18–22px bold `#0A192F`. Full assertion sentence stating the takeaway (never a generic topic label).
  3. *Lead-In Box:* 2–3 sentence executive summary container before exhibits.
  4. *Data Exhibits:* 2-to-4 structured columns with quantitative proof, metric deltas, or Harvey balls (`○`, `◔`, `◑`, `◕`, `●`).
  5. *Footnote / Source:* 9–10px `#64748B` anchoring data sources.
- **Consulting Slide Archetypes:** Executive Summary (SCR), 3-Pillar Strategy, 2x2 Matrix, Value Chain Margin Pools, EBITDA Bridge, MACC Decarbonization Curve, Implementation Roadmap (H1/H2/H3), Capability Scorecard.

### Mode 2: Medium (Editorial / *The Ken* / Investigative Tech)

- **Canvas Background:** Warm Newspaper Off-White (`#FDFBF7` `{ r: 0.992, g: 0.984, b: 0.969 }` or `#F8F6F0`).
- **Color Palette:**
  - Signature Accent: Editorial Crimson `#E5252A` (`{ r: 0.898, g: 0.145, b: 0.165 }`)
  - Text Body: Dark Charcoal `#1A1A1A` (`{ r: 0.102, g: 0.102, b: 0.102 }`)
  - Card Backgrounds: Clean White `#FFFFFF`, Soft Red `#FDF2F2`, Soft Mint `#F0FDF4`.
  - Borders: Crisp Hairline `#E2D9CC` (`{ r: 0.886, g: 0.851, b: 0.800 }`).
- **Cover / Outro Visuals:** Collage aesthetic, torn paper textures, retro/collegiate 3D arched display typography ("THE GREAT REWIRING", "CLAIM CLOSED"), heavy black gothic/grotesque brand title ("HAQ").
- **Inside Slide Modules:**
  - **Category Pill Badges:** Solid red pill (`#E5252A`, white text, `4px` corner radius) e.g. `WHAT CLAIMANTS TOLD US`, `WHERE IT LANDED`.
  - **Agent / Step Cards:** Clean bordered white cards with rounded corners (`12px`–`16px`), icon in top-left, step index (`01 | COMMUNICATION AGENT`), and clear LLM/protocol specifications.
  - **Decision Timelines:** Numbered circles connected by a horizontal path, showing sequential handoffs.
  - **Dashed Wireframe Cards:** 3 bottom cards with dashed borders (`strokeDashes: [4, 4]`) for core design principles.
  - **Bold Takeaway Quotations:** Centered bottom callout wrapped in quotes (`"Independent agents. Shared context. Controlled decisions."`).

### Mode 3: Funky (Poppy Brutalism / High Energy)

- **Canvas Background:** Atmospheric tinted palette with slide-to-slide variance:
  - Pale Mint `#F2FAF0`, Warm Apricot `#FDF5EE`, Ice Sky `#EEF7FA`, Soft Periwinkle `#F4F1FD`, Melon Sand `#FAF5EE`.
- **Color Palette:** Hyper-saturated solid cards:
  - Lime Green: `#A1FF5F` (`{ r: 0.631, g: 1.0, b: 0.373 }`)
  - Electric Cyan: `#00F0FF` (`{ r: 0.0, g: 0.941, b: 1.0 }`)
  - Tangerine Orange: `#FFA048` (`{ r: 1.0, g: 0.627, b: 0.282 }`)
  - Vibrant Coral: `#FF7A59` (`{ r: 1.0, g: 0.478, b: 0.349 }`)
  - Soft Lavender: `#B1A1FF` (`{ r: 0.694, g: 0.631, b: 1.0 }`)
- **Card Styling:** Generous `24px` rounded corners, solid color fill, pure black text (`#000000`).
- **Artistic Depth:** Ink splatters, spray bursts, and brush swashes placed at canvas depth behind cards, dimmed to **45%–65% opacity**.
- **Typography Invariants:**
  - **NO em-dashes (`—`):** Use colons (`:`) or pipes (`|`).
  - **NO double slashes (`//`):** Clean text only.
  - **NO bounding pills around kickers:** Monospace uppercase text hanging freely.
  - **Bold lead-in before colon:** Every bullet point bolded until the colon.
  - **"Filled, Never Cluttered":** Zero empty white space; cards expanded to fill the frame with large typography (`15px`–`16.5px` body, `28px`–`30px` card titles).

---

## 5. Master Typography Matrix (Google Fonts Available in Figma)

| Role | Professional (MBB / Corporate) | Medium / Editorial Mode | Funky / Poppy Brutalism |
|---|---|---|---|
| **Action Title / Main Headline** | `Inter Bold` / `Plus Jakarta Sans Bold` (20px–24px, 2-line assertion) | `Space Grotesk Bold` / `Archivo Bold` (36px–38px) | `Space Grotesk Bold` (38px, line height 44px) |
| **Tracker / Category Kicker** | `Inter Semi Bold` (10px–11px, uppercase, `#64748B`) | `Space Grotesk Bold` / `JetBrains Mono` (11px) | `Space Grotesk Bold` (11px, letterSpacing 1.2px) |
| **Card Title / Column Header** | `Inter Extra Bold` (18px–22px, `#0A192F`) | `Space Grotesk Bold` / `Inter Bold` (26px–28px) | `Inter Extra Bold` / `Space Grotesk` (28px–30px) |
| **Lead-In Callout Text** | `Inter Medium` (14px–15px, `#334155`, line height 22px) | `Plus Jakarta Sans Medium` (15px–16px) | `Plus Jakarta Sans Medium` (16px–17px) |
| **Card Bullets / Explanations** | `Inter Regular` (13px–14px, line height 20px) | `Plus Jakarta Sans Medium` (14.5px–15.5px) | `Plus Jakarta Sans Medium` (15px–16px, bold lead-in) |
| **Metric Headlines / KPIs** | `Inter Extra Bold` (28px–36px) + context label | `Inter Extra Bold` / `Space Grotesk` (32px–36px) | `Inter Extra Bold` (20px–22px in highlight cards) |
| **Footnotes & Sources** | `Inter Regular` (9px–10px, `#64748B`) | `JetBrains Mono Regular` (10px) | `JetBrains Mono Medium` (11px) |
| **Display/Cover** | `Inter Extra Bold` / `Merriweather` | Arched Collegiate / Heavy Gothic Display | Brutalist Massive Space Grotesk Bold |

---

## 6. Technical Figma MCP Rules (`use_figma`)

1. **Preload All Fonts:** Always load fonts before mutating characters:
   ```javascript
   await figma.loadFontAsync({ family: "Space Grotesk", style: "Bold" });
   await figma.loadFontAsync({ family: "Inter", style: "Bold" });
   await figma.loadFontAsync({ family: "Inter", style: "Extra Bold" });
   await figma.loadFontAsync({ family: "Plus Jakarta Sans", style: "Medium" });
   await figma.loadFontAsync({ family: "JetBrains Mono", style: "Bold" });
   ```
2. **Auto-Layout Ordering:** Append node to auto-layout parent **FIRST**, then set `layoutSizingHorizontal = 'FILL'`.
3. **Prevent Text Clipping in Cards:**
   - Card dimensions: `625px` wide (for 2-col) or `390px` wide (for 3-col), `430px`–`450px` high.
   - Safe Card Padding: `paddingTop: 22, paddingBottom: 20, paddingLeft: 24, paddingRight: 24`.
   - Safe Spacing: `itemSpacing: 8` to `10`.
   - Bullet text: `fontSize: 14px`–`15px`, `lineHeight: 20px`–`22px`.
4. **Color Conversion:** Never use `0–255`. Divide RGB values by 255 (e.g. `{ r: 10/255, g: 25/255, b: 47/255 }`).
5. **Output Serialization Guard:** Never return raw node dumps over 48 KB. Return clean structured summaries: `{ status: "success", slideId: slide.id, name: slide.name }`.
6. **Visual Screenshot Check:** Always capture screenshots with `get_screenshot`, download via `curl.exe`, and inspect with `read_file` to confirm layout integrity and zero text clipping.
