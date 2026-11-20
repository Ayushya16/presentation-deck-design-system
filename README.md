# Presentation Deck Design System & Agent Skill
> Universal, production-grade design system and agent skill for generating high-stakes presentation decks across three distinct archetypes: **Professional (MBB / Strategy Consulting / Corporate)**, **Medium (Editorial / The Ken)**, and **Funky (Poppy Brutalism)**.
> Engineered for automated AI design agents utilizing the Figma MCP / Plugin API (`use_figma`) or code-first SVG/HTML slide generation.

---

## 🎨 The 3 Visual Modes

| Mode | Visual Identity & Tone | Primary Use Cases | Canonical References |
|---|---|---|---|
| **Professional (MBB / Corporate)** | Standalone analytical briefing books, complete-sentence Action Titles, Lead-In Callout containers, 2-to-4 column MECE cards, hairline dividers (`#E2E8F0`), Harvey balls, explicit data attribution. Crisp light slate `#F8FAFC` canvas, deep midnight navy `#0A192F`. | C-suite reviews, corporate governance, MBB strategy decks (McKinsey/BCG/Bain), investment pitches, formal case competitions. | [160+ Public McKinsey Decks Deconstructed](https://slideworks.io/resources/47-real-mckinsey-presentations) & [Figma Draft 1](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=3-2) |
| **Medium (Editorial)** | Warm newspaper off-white (`#FDFBF7`), editorial crimson red accents (`#E5252A`), 8-stage decision timelines, pill tags, dashed wireframe principle boxes, bold takeaway quotes. | Investigative journalism, case competitions, tech product deep-dives (*The Ken* style). | *HAQ: The Great Rewiring* Case Competition Deck & [Figma Draft 2](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=2-207) |
| **Funky (Poppy Brutalism)** | Atmospheric tinted canvases (`#F2FAF0`, `#FDF5EE`), hyper-saturated solid cards (Lime, Cyan, Tangerine, Coral, Lavender), pure black text, 45%–65% opacity art splatters, bold lead-ins before colons. | Youth festivals, creative agencies, cultural showcases, high-energy startup presentations. | [Figma Draft 3](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=0-1) |

---

## 🚨 Mandatory Ban on "AI Tells"

Human designers and executives immediately reject generic AI slides. This skill strictly prohibits:
- ❌ **NO AI Blue (`#2563EB`, `#3B82F6`) or generic purple gradients.**
- ❌ **NO Top decorative colored lines or gradient border strips.**
- ❌ **NO AI sparkle badges, `✨ AI Insights`, or floating capsule pill tags.**
- ❌ **NO Glassmorphism or generic glowing blur blobs.**
- ❌ **NO Markdown em-dashes (`—`) or double slashes (`//`) in copy.**
- ❌ **NO Fabricated or hallucinated metrics without context.**

---

## 📂 Repository Structure

```
presentation-deck-design-system/
├── SKILL.md                          # Universal Agent Skill definition (YAML frontmatter + system rules)
├── README.md                         # Architecture overview & quickstart
└── references/
    ├── professional-mode.md          # Complete MBB consulting blueprint: Pyramid Principle, Action Titles, 20 Slide Archetypes, Slideworks McKinsey Corpus
    ├── medium-editorial-mode.md      # The Ken / Editorial blueprint: Multi-agent pipelines, brutalist covers, wireframes
    ├── funky-poppy-mode.md           # Poppy Brutalism blueprint: Saturated cards, splatter depth, anti-whitespace rules
    ├── typography-and-fonts.md       # Master typography matrix, Google Fonts pairings, line heights, and hierarchy
    └── figma-mcp-guide.md            # Technical use_figma execution guide, auto-layout recipes, and clipping prevention
```

---

## 🚀 How to Use with an AI Assistant

### As an Antigravity Skill
Place this repository in your local skills directory (`.gemini/skills/` or active workspace). The agent will automatically trigger the skill whenever slide design or deck review is requested.

### In Any AI Tool (Claude, Cursor, ChatGPT, Gemini)
Provide `SKILL.md` or invoke the design mode directly:
> *"Design this presentation using the **presentation-deck-design-system** in **[Professional | Medium | Funky]** mode. Ensure zero AI tells."*

---

## 🔗 Live Reference Decks & Resources

- **McKinsey & MBB Corpus:** [Slideworks 160+ Real McKinsey Presentations Deconstructed](https://slideworks.io/resources/47-real-mckinsey-presentations)
- **Draft 1 (Professional / MBB Strategy):** [Figma File](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=3-2)
- **Draft 2 (Medium / High-Energy Proposals):** [Figma File](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=2-207)
- **Draft 3 (Funky / Poppy Brutalism):** [Figma File](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=0-1)
- **The Ken / HAQ Deck:** Editorial Brutalist case competition presentation with multi-agent workflow architecture.
