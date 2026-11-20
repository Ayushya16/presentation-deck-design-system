# Mode 2: Medium (Editorial / The Ken / Investigative Tech)
> Detailed specification based on *The Ken* case competition slides, investigative journalism, and product architecture narratives (e.g. *HAQ: The Great Rewiring*).

---

## 1. Visual Identity & Tone

- **Audience:** Product leaders, case competition judges, tech founders, investigative readers.
- **Tone:** Sharp, analytical, evidence-backed, narrative-driven, visually engaging without being cartoonish.
- **Atmosphere:** Warm, tactile newspaper off-white (`#FDFBF7` or `#F8F6F0`) reminiscent of high-end business periodicals (*Financial Times*, *The Ken*).

---

## 2. Color Palette

```typescript
export const EDITORIAL_COLORS = {
  canvas: '#FDFBF7',          // Warm newspaper off-white
  canvasTinted: '#F8F6F0',    // Alternative paper shade
  textPrimary: '#1A1A1A',     // Deep editorial charcoal
  textSecondary: '#4A4A4A',   // Medium charcoal
  accentCrimson: '#E5252A',   // Signature editorial red
  cardBg: '#FFFFFF',          // Clean white surface
  cardBorder: '#E2D9CC',      // Warm paper-toned hairline border
  pillBg: '#E5252A',          // Solid crimson tag background
  pillText: '#FFFFFF',        // Pure white on crimson
  accentMint: '#F0FDF4',      // Soft green success/intake background
  accentRose: '#FEF2F2',      // Soft red exception/break background
  accentBeige: '#FBF9F5',     // Soft muted card background
};
```

Figma 0–1 Color Math:
- Canvas `#FDFBF7`: `{ r: 0.992, g: 0.984, b: 0.969 }`
- Crimson `#E5252A`: `{ r: 0.898, g: 0.145, b: 0.165 }`
- Charcoal `#1A1A1A`: `{ r: 0.102, g: 0.102, b: 0.102 }`
- Border `#E2D9CC`: `{ r: 0.886, g: 0.851, b: 0.800 }`

---

## 3. Structural Layout Patterns

### A. The Agent / Specialist Grid (Multi-Agent Workflow)
- **Grid:** 2 rows of 4 cards (8 stages total), each card `~300px` wide, `~200px` high.
- **Card Anatomy:**
  - Corner step index: `01 | COMMUNICATION AGENT` (in `JetBrains Mono` or `Inter Semi Bold`, colored `#E5252A`).
  - Small icon in top left (chat, shield, scale, document, checkmark).
  - Body explaining: Model used, role, input/output handoff, and confidence thresholds.
  - Color-coded borders: Thin green border for intake/closure, thin red/gray border for middle review agents.

### B. The 8-Stage Decision Timeline ("One Claim, Eight Decisions")
- Horizontal progression track (`y: 180` to `240`):
  - Numbered red circles (`18px × 18px`) connected by a horizontal connector line.
  - Step card above/below each point (`Incident Captured`, `Case Created`, `Facts Extracted`, `Policy Tested`, `Signals Assessed`, `Settlement Assembled`, `Money Reconciled`, `Case Resolved`).
- Followed by 3 category blocks below:
  - `WHAT MOVES THROUGH THE SYSTEM` (Evidence, Claim State, Decision Trace).
  - `WHEN THE CASE LEAVES THE AI` (Voice, Payments, Logistics).
  - `THE HANDOFF` (Agent completes -> Supervisor routes -> Case ends).
  - Accent Takeaway Box: Crimson solid block with bold quote: *"The intelligence is not in one answer. It is in how evidence accumulates across the claim."*

### C. The "With vs. Without" Transformation Table
- 3-column table comparing moments:
  - Column 1: `MOMENT` (Filing, Understanding cover, Evidence, Settlement, Exceptions).
  - Column 2: `WITHOUT PRODUCT` (Pain points, delays, fragmented docs).
  - Column 3: `WITH PRODUCT` (Instant structure, automated checks, verified handoffs).
  - Right-hand side panel: 3 cards showing `WHAT THIS CHANGES` (For Claimant, For Insurer, For System).
  - Bottom Big Number Row: `8/8 Stages carried`, `100% Traceable`, `< 0.5 Confidence trigger`.

### D. The Dashed Wireframe Principle Cards
- 3 cards at the bottom with dashed borders (`dashPattern: [4, 4]`, stroke `#E5252A` or `#E2D9CC`).
- Headings: `HUB / ORCHESTRATION`, `GOVERNANCE / AUTONOMY`, `THE DESIGN PRINCIPLE`.
- Gives an architectural, blueprint-like credibility to system design slides.

### E. The Editorial Cover & Outro Slides
- **Background:** Collage / torn paper edge textures.
- **Typography:**
  - Theme Headline: Arched / curved 3D retro collegiate serif (e.g. *"THE GREAT REWIRING"* or *"CLAIM CLOSED"*).
  - Product Name: Massive brutalist sans-serif (*"HAQ"*).
  - Mission Statement: Punchy all-caps subtitle (*"BECAUSE SMALL CLAIMS DESERVE A FAIR FIGHT"*).
  - Team Box: Clean rounded hairline card with names.

---

## 4. Key Rules & Anti-Patterns
- **Do:** Use solid red pill labels (`WHAT CLAIMANTS TOLD US`, `WHERE IT LANDED`, `WHAT COULD KILL IT`) to create immediate visual anchors.
- **Do:** Frame takeaways as memorable philosophical maxims in quotation marks at the bottom of the slide.
- **Don't:** Use random neon colors (lime, purple, cyan); keep strictly to the newspaper palette: warm paper, crimson red, charcoal, subtle mint/rose status tints.
