# Typography & Fonts Reference Catalog
> Comprehensive font breakdown, pairing matrix, styles, and usage rules across the three deck archetypes.

All recommended fonts are freely available via **Google Fonts** and pre-installed or supported within Figma.

---

## 1. Archetype Typography Matrix

| Category | Professional (Corporate/MBB) | Medium (Editorial / The Ken) | Funky (Poppy Brutalism) |
|---|---|---|---|
| **Primary Vibe** | Rigorous, authoritative, precise, institutional. | Analytical, narrative, intellectual, clean, investigative. | Vibrant, rebellious, punchy, high-energy, cultural. |
| **Headline Font** | **Inter** (Bold / Extra Bold)<br>or **Plus Jakarta Sans** (Bold) | **Space Grotesk** (Bold)<br>or **Archivo** (Bold / Black)<br>or **Syne** (Bold) | **Space Grotesk** (Bold)<br>or **Inter** (Extra Bold) |
| **Cover Display Font** | **Inter Extra Bold**<br>or **Merriweather** (Black) | **Arched Collegiate 3D Display**<br>+ Heavy Grotesque Gothic | **Massive Brutalist Space Grotesk**<br>(48px–72px uppercase) |
| **Body & Bullets** | **Inter** (Regular / Medium)<br>or **Roboto** (Regular) | **Plus Jakarta Sans** (Medium)<br>or **Inter** (Medium) | **Plus Jakarta Sans** (Medium)<br>+ **Bold lead-ins** before colon |
| **Kickers & Tags** | **Inter** (Semi Bold, uppercase)<br>or **Plus Jakarta Sans** (Semi Bold) | **JetBrains Mono** (Bold)<br>or Solid Crimson Pill Badges | **JetBrains Mono** (Bold)<br>(raw uppercase text, no pills) |
| **Data & Stats** | **Inter Extra Bold** (32px–40px)<br>or **JetBrains Mono** (Bold) | **Space Grotesk Bold** (32px–36px)<br>or **Inter Extra Bold** (32px) | **Inter Extra Bold** (21px–30px)<br>on solid color backgrounds |

---

## 2. Mode 1: Professional (Corporate / MBB) Typography

### Recommended Font Pairings:
1. **Modern Clean (Default):**
   - Headings: `Inter Bold` / `Extra Bold`
   - Body & Tables: `Inter Regular` (14px, line height 20px)
   - Numbers & Metrics: `Inter Extra Bold` (32px–40px)
   - Labels / Metadata: `Inter Semi Bold` (11px, uppercase, letterSpacing 1.0px)
2. **Executive Serif Hybrid:**
   - Headings: `Merriweather Bold` (or `Georgia`)
   - Body: `Plus Jakarta Sans Regular` / `Medium`
   - Data & Metrics: `Inter Extra Bold`

### Typography Rules:
- Line lengths should not exceed 75 characters.
- Maintain high contrast: pure black `#0A192F` or `#1E293B` on `#FFFFFF` / `#F8FAFC`.
- Bullet points must be concise, starting with an action verb or structured bold topic.

---

## 3. Mode 2: Medium (Editorial / The Ken / Investigative Tech)

Based on the investigative editorial style seen in *The Ken* and top-tier case competition decks (e.g. *HAQ: The Great Rewiring*):

### Recommended Font Pairings:
1. **The Ken Editorial Standard:**
   - Title / Section Headers: `Space Grotesk Bold` (36px–38px, line height 42px–44px)
   - Step & Agent Titles: `Inter Extra Bold` (20px–24px) or `Space Grotesk Bold`
   - Body Copy: `Plus Jakarta Sans Medium` (14px–15px, line height 21px–22px)
   - Pill Badges: `Inter Bold` / `Plus Jakarta Sans Bold` (11px–12px, white on `#E5252A` crimson)
   - Code / Process Metadata: `JetBrains Mono Medium` (11px–12px)
   - Bottom Quotes: `Inter Semi Bold` / `Plus Jakarta Sans Medium` (18px–20px, italicized or quoted)

### Typography Rules:
- Cover slide utilizes bold expressive collage typography (e.g. arched collegiate 3D display for the theme title, paired with clean brutalist sans for the brand name).
- Inside slides maintain structured newspaper-like discipline: red accents highlight transitions, clean pill badges introduce evidence, and numbered steps (`01 \| INTAKE`, `02 \| SUPERVISOR`) organize multi-agent workflows.

---

## 4. Mode 3: Funky (Poppy Brutalism)

Based on modern youth festival pitch decks and high-impact visual presentations:

### Recommended Font Pairings:
1. **Poppy High-Contrast (Main System):**
   - Slide Header Title: `Space Grotesk Bold` (38px, line height 44px, pure black `#000000`)
   - Slide Category Kicker: `Space Grotesk Bold` (11px, letterSpacing 1.2px, 50% opacity black)
   - Card Main Title: `Inter Extra Bold` (28px–30px, line height 34px–36px)
   - Card Subtitle: `Plus Jakarta Sans Medium` (15.5px–17px, line height 21.5px–23px)
   - Card Bullets: `Plus Jakarta Sans Medium` (15px–16px, line height 21px–23px)
   - Card Bullet Lead-Ins: `Plus Jakarta Sans Bold` (before colon)
   - Card Hanging Kicker: `JetBrains Mono Bold` (12.5px–13px, uppercase, letterSpacing 0.8px, 65% opacity black)
   - Highlight Stat Titles: `Inter Extra Bold` (20px–22px, line height 25px–27px)

### Typography Invariants:
- **NO Em-Dashes (`—`):** Never use em-dashes. Use colons (`:`) or vertical pipes (`|`).
- **NO Double Slashes (`//`):** Prefixing kickers with `//` looks cluttered and dated.
- **NO Pill Bounding Boxes:** Kickers must hang as pure uppercase monospace text.
- **Always Bold Before Colon:** Make every bullet point scannable by applying bold styling from character 0 to `indexOf(':')`.
