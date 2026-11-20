# Mode 1: Professional (Corporate / MBB / Case Competition)
> Detailed specification for designing formal corporate, strategy consulting (McKinsey/BCG/Bain), and executive pitch decks.

---

## 1. Visual Identity & Tone

- **Audience:** C-suite executives, investment committees, formal judging panels.
- **Tone:** Authoritative, quantitative, disciplined, rigorous, structured.
- **Atmosphere:** Clean white or light slate canvas (`#FFFFFF` or `#F8FAFC`). No playful decorative splatters or noisy gradients.

---

## 2. Color Palette

```typescript
export const PROFESSIONAL_COLORS = {
  canvas: '#F8FAFC',          // Clean light slate/alabaster
  cardBg: '#FFFFFF',          // Pure white card containers
  cardStroke: '#E2E8F0',      // Subtle hairline border
  textPrimary: '#0A192F',     // Deep midnight navy
  textSecondary: '#475569',   // Refined slate
  accentPrimary: '#1E40AF',   // Deep sapphire blue
  accentAlert: '#991B1B',     // Formal crimson
  accentSuccess: '#166534',   // Deep forest green
};
```

Figma 0–1 Color Math:
- Deep Navy `#0A192F`: `{ r: 0.039, g: 0.098, b: 0.184 }`
- Hairline Border `#E2E8F0`: `{ r: 0.886, g: 0.910, b: 0.941 }`
- Slate Secondary `#475569`: `{ r: 0.278, g: 0.333, b: 0.412 }`

---

## 3. Structural Layout Patterns

### A. The 3-Pillar Strategic Recommendation
- 3 cards side-by-side (`width: ~410px`, `height: 450px`, `gap: 20px`).
- Top banner with pillar number (`01`, `02`, `03`) and theme name.
- 3 structured bullet points with quantitative impact estimates.
- Bottom KPI block with hairline border showing ROI / cost reduction.

### B. The 2x2 Strategic Matrix / MECE Split
- 4 quadrant cards (`width: 625px`, `height: 215px`).
- Clear axes headers (e.g. Feasibility vs. Business Impact).

### C. The Executive Data Table
- Structured horizontal rows with alternating subtle fills (`#FFFFFF` and `#F8FAFC`).
- Hairline horizontal dividers (`#E2E8F0`).
- Strict column alignment (Left-aligned text, Right-aligned numbers).

---

## 4. Key Rules & Anti-Patterns
- **Avoid:** Empty visual space that gives no information; over-saturated neon fills; playful cartoon illustrations.
- **Prefer:** Hard numbers (CAGR %, basis point improvements, payback periods); clear source citations in the bottom footer (10px, `#64748B`); structured action titles stating the slide's takeaway.
