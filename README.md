# Presentation Deck Design System & Agent Skill

A comprehensive, production-grade design system and universal skill for creating high-stakes presentation decks across three distinct archetypes: **Professional (MBB / Corporate)**, **Medium (Editorial / The Ken)**, and **Funky (Poppy Brutalism)**.

Designed for automated design agents using the Figma MCP / Plugin API or code-first generation.

---

## 🎨 The 3 Visual Modes

| Mode | Visual Identity | Primary Use Case | Reference Benchmark |
|---|---|---|---|
| **Professional** | Crisp light slate/white, deep midnight navy, subtle crimson/blue, dense structured data tables, hairline borders. | C-suite reviews, corporate governance, MBB strategy decks, formal investment pitches. | [Draft 1 | MBB Strategy](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=3-2) |
| **Medium (Editorial)** | Warm newspaper off-white (`#FDFBF7`), crimson red accents (`#E5252A`), 8-stage decision timelines, pill tags, dashed wireframe principle boxes, takeaway quotes. | Investigative journalism, case competitions, tech product deep-dives (*The Ken* style). | *HAQ: The Great Rewiring* Case Competition Deck |
| **Funky (Poppy Brutalism)** | Atmospheric tinted canvases, hyper-saturated solid cards (Lime, Cyan, Tangerine, Coral, Lavender), pure black text, 45%–65% opacity art splatters, bold lead-ins before colons. | Youth festivals, creative agencies, cultural showcases, high-energy startup presentations. | [Draft 3 | Modern Black & Type](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=0-1) |

---

## 📂 Repository Structure

```
presentation-deck-design-system/
├── SKILL.md                          # Antigravity & AI Agent Skill definition (YAML frontmatter + master instructions)
├── README.md                         # Documentation & Quickstart
└── references/
    ├── typography-and-fonts.md       # Full Google Fonts matrix, pairings, styles, and sizes across all 3 modes
    ├── professional-mode.md          # Complete blueprint & components for MBB / Corporate decks
    ├── medium-editorial-mode.md      # Complete blueprint & components for The Ken / Editorial decks
    ├── funky-poppy-mode.md           # Complete blueprint & components for Poppy Brutalism decks
    └── figma-mcp-guide.md            # Technical guide, gotcha prevention, and production code recipes for use_figma
```

---

## 🚀 How to Use with an AI Assistant

### Option A: As an Antigravity Skill
Place this folder in your skills directory or add `SKILL.md` to your agent workspace. The agent will automatically recognize `presentation-deck-design-system`.

### Option B: Prompting in Any AI Tool (Claude, Cursor, ChatGPT, Gemini)
Provide `SKILL.md` or invoke the design mode directly:
> *"Design this presentation using the **presentation-deck-design-system** in **[Professional | Medium | Funky]** mode."*

---

## 🔗 Live Reference Decks

- **Draft 3 (Funky / Poppy Brutalism):** [Figma File](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=0-1)
- **Draft 2 (Medium / High-Energy Proposals):** [Figma File](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=2-207)
- **Draft 1 (Professional / MBB Strategy):** [Figma File](https://figma.com/design/u8OBskjwy3EWUDawNM68Ja/Untitled?node-id=3-2)
- **The Ken / HAQ Deck:** Editorial Brutalist case competition presentation with multi-agent workflow architecture.
