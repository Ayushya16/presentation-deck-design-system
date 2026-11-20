# Mode 3: Funky (Poppy Brutalism / High Energy)
> Detailed specification based on the *Modern Black & Type / Poppy Brutalism* pitch deck system.

---

## 1. Visual Identity & Tone

- **Audience:** Cultural fest committees, creative agencies, youth demographics, high-energy startup demo days.
- **Tone:** Unapologetic, vibrant, visually dense, confident, ultra-high contrast.
- **Atmosphere:** Warm, pale tinted slide canvases (`#F2FAF0`, `#FDF5EE`, `#EEF7FA`, `#F4F1FD`, `#FAF5EE`) paired with hyper-saturated poppy cards and soft background art splatters.

---

## 2. Color Palette

```typescript
export const FUNKY_POPPY_COLORS = {
  // Atmospheric Slide Canvases
  canvasMint: '#F2FAF0',       // Pale Sage / Mint
  canvasPeach: '#FDF5EE',      // Warm Apricot
  canvasSky: '#EEF7FA',        // Ice Sky
  canvasLilac: '#F4F1FD',      // Soft Periwinkle
  canvasSand: '#FAF5EE',       // Melon Sand

  // Hyper-Saturated Poppy Cards
  cardLime: '#A1FF5F',         // Neon Lime Green
  cardCyan: '#00F0FF',         // Electric Cyan
  cardTangerine: '#FFA048',    // Saturated Tangerine
  cardCoral: '#FF7A59',        // Punchy Coral
  cardLavender: '#B1A1FF',     // Rich Lavender

  // Foreground
  text: '#000000',             // Pure High-Contrast Black
  kickerMuted: 'rgba(0,0,0,0.65)',
  headerKicker: 'rgba(0,0,0,0.50)',
};
```

Figma 0–1 Color Math:
- Lime `#A1FF5F`: `{ r: 0.631, g: 1.0, b: 0.373 }`
- Cyan `#00F0FF`: `{ r: 0.0, g: 0.941, b: 1.0 }`
- Tangerine `#FFA048`: `{ r: 1.0, g: 0.627, b: 0.282 }`
- Coral `#FF7A59`: `{ r: 1.0, g: 0.478, b: 0.349 }`
- Lavender `#B1A1FF`: `{ r: 0.694, g: 0.631, b: 1.0 }`

---

## 3. Structural Layout Patterns

### A. The 2-Card Wide Power Split
- Left Card: `width: 625px`, `height: 450px`, `x: 80`, `y: 125`.
- Right Card: `width: 625px`, `height: 450px`, `x: 735`, `y: 125`.
- Inside each card:
  - Raw Hanging Kicker: `JetBrains Mono Bold`, `12.5px`–`13px`, uppercase.
  - Card Title: `Inter Extra Bold`, `28px`–`30px`, line height `34px`–`36px`.
  - Subtitle: `Plus Jakarta Sans Medium`, `15.5px`–`16px`.
  - 4 Dense Bullets: `Plus Jakarta Sans Medium`, `15px`, line height `21px`, with **bold lead-in before colon**.

### B. The 3-Column Stepped Pipeline
- 3 cards side-by-side (`width: ~405px`, `height: 450px`, `gap: 20px`).
- Card 1 (Coral): The Critical Problem / Bottleneck.
- Card 2 (Lime Hero): The Core System / Solution.
- Card 3 (Cyan): The Scaling / Tracking Layer.

### C. The Bottom 3-Card Highlight Strip
- 3 cards across `y: 595`, `height: 165px`:
  - Card 1: `x: 80, width: 400`
  - Card 2: `x: 500, width: 410`
  - Card 3: `x: 930, width: 430`
- Top Kicker: `JetBrains Mono Bold`, `12px`.
- Core Metric Title: `Inter Extra Bold`, `20px`–`22px`.
- 2-Line Summary Description: `Plus Jakarta Sans Medium`, `14px`–`14.5px`.

---

## 4. Strict Formatting Invariants
- **ZERO Em-Dashes (`—`):** Never use em-dashes. Use colons (`:`) or pipes (`|`).
- **ZERO Double Slashes (`//`):** Prefixing kickers with `//` is banned.
- **ZERO Pill/Badge Outlines on Kickers:** Monospace uppercase text must hang freely.
- **Bold Lead-In Before Colon:** Ensure character 0 to `indexOf(':')` is bolded.
- **Splatters at 45%–65% Opacity:** Never 100% opacity, which competes with text.
- **Zero Empty Space ("Filled, Never Cluttered"):** Scale text and cards to fill the slide frame completely.
