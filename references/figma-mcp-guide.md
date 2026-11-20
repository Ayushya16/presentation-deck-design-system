# Figma MCP & Plugin API Developer Guide
> Technical reference, production recipes, and gotcha preventions for building presentation slides via `use_figma`.

---

## 1. Golden Rules of `use_figma`

1. **Preload Fonts Before Any Mutation:**
   Figma throws `Cannot write to node with unloaded font` if you modify text characters or font styles without loading the exact font family and style first:
   ```javascript
   await figma.loadFontAsync({ family: "Space Grotesk", style: "Bold" });
   await figma.loadFontAsync({ family: "Inter", style: "Extra Bold" });
   await figma.loadFontAsync({ family: "Plus Jakarta Sans", style: "Bold" });
   await figma.loadFontAsync({ family: "Plus Jakarta Sans", style: "Medium" });
   await figma.loadFontAsync({ family: "JetBrains Mono", style: "Bold" });
   ```
   *Tip:* If modifying an existing node, read its font via `getStyledTextSegments(['fontName'])` and preload all detected fonts.

2. **Auto-Layout Child Sizing Ordering:**
   `layoutSizingHorizontal = 'FILL'` throws an error if set before the node is appended to an auto-layout parent:
   ```javascript
   // WRONG
   text.layoutSizingHorizontal = 'FILL';
   parent.appendChild(text);

   // CORRECT
   parent.appendChild(text);
   text.layoutSizingHorizontal = 'FILL';
   ```

3. **Wrapping Text Nodes:**
   Wrapping text inside auto-layout containers requires `textAutoResize = 'HEIGHT'` and an explicit width or parent `FILL`:
   ```javascript
   text.textAutoResize = 'HEIGHT';
   parent.appendChild(text);
   text.layoutSizingHorizontal = 'FILL';
   ```

4. **Card Padding & Text-Clipping Math:**
   To guarantee zero text clipping inside a `625px × 450px` card holding 4 bullet points:
   ```javascript
   card.paddingTop = 22;
   card.paddingBottom = 20;
   card.paddingLeft = 32;
   card.paddingRight = 32;
   card.itemSpacing = 8; // or 9
   
   // Bullet Typography
   bullet.fontSize = 15;
   bullet.lineHeight = { unit: "PIXELS", value: 21 };
   ```

5. **Color Math (0.0 to 1.0 Floats):**
   Figma Plugin API colors are normalized between `0.0` and `1.0`. Divide RGB values by 255:
   ```javascript
   function hexToFigmaColor(hex) {
     const c = hex.replace('#', '');
     return {
       r: parseInt(c.substring(0, 2), 16) / 255,
       g: parseInt(c.substring(2, 4), 16) / 255,
       b: parseInt(c.substring(4, 6), 16) / 255
     };
   }
   ```

6. **Serialization Budget Guard (< 48 KB):**
   Figma MCP has a strict 48,000-byte return limit. Never return raw node dumps (`slide.children` or deep trees). Return lightweight status summaries:
   ```javascript
   return {
     status: "success",
     slideId: slide.id,
     name: slide.name,
     x: slide.x,
     y: slide.y
   };
   ```

7. **Verification Protocol:**
   Always take a visual screenshot after composition:
   ```javascript
   // Capture via get_screenshot MCP tool
   // Download via: curl.exe -f -L -o screen.png "<image_url>"
   // View via: read_file Path: "screen.png"
   ```

---

## 2. Reusable Component Recipes

### A. Slide Header Builder
```javascript
function createSlideHeader(slide, categoryStr, titleStr) {
  const header = figma.createAutoLayout('VERTICAL');
  header.name = "Slide Header";
  header.x = 80;
  header.y = 44;
  header.itemSpacing = 4;
  header.fills = [];

  const category = figma.createText();
  category.characters = categoryStr;
  category.fontName = { family: "Space Grotesk", style: "Bold" };
  category.fontSize = 11;
  category.letterSpacing = { unit: "PIXELS", value: 1.2 };
  category.fills = [{ type: 'SOLID', color: { r: 0, g: 0, b: 0 }, opacity: 0.5 }];
  header.appendChild(category);

  const title = figma.createText();
  title.characters = titleStr;
  title.fontName = { family: "Space Grotesk", style: "Bold" };
  title.fontSize = 38;
  title.lineHeight = { unit: "PIXELS", value: 44 };
  title.fills = [{ type: 'SOLID', color: { r: 0, g: 0, b: 0 } }];
  header.appendChild(title);

  slide.appendChild(header);
  return header;
}
```

### B. Bullet Formatter with Bold Lead-In
```javascript
function createBoldBullet(text, boldFont, regularFont, size = 15, lineH = 21) {
  const t = figma.createText();
  t.characters = text;
  t.fontName = regularFont;
  t.fontSize = size;
  t.lineHeight = { unit: "PIXELS", value: lineH };
  t.fills = [{ type: 'SOLID', color: { r: 0, g: 0, b: 0 } }];

  const colonIdx = text.indexOf(':');
  if (colonIdx !== -1) {
    t.setRangeFontName(0, colonIdx + 1, boldFont);
  }
  return t;
}
```

### C. Bottom Highlight Card Builder
```javascript
function createHighlight(name, kickerText, titleText, descText, x, width, color) {
  const hl = figma.createAutoLayout('VERTICAL');
  hl.name = name;
  hl.x = x;
  hl.y = 595;
  hl.resize(width, 165);
  hl.cornerRadius = 20;
  hl.paddingLeft = 24;
  hl.paddingRight = 24;
  hl.paddingTop = 20;
  hl.paddingBottom = 20;
  hl.itemSpacing = 6;
  hl.fills = [{ type: 'SOLID', color: color }];

  const k = figma.createText();
  k.characters = kickerText;
  k.fontName = { family: "JetBrains Mono", style: "Bold" };
  k.fontSize = 12.5;
  k.fills = [{ type: 'SOLID', color: { r: 0, g: 0, b: 0 }, opacity: 0.65 }];
  hl.appendChild(k);

  const ti = figma.createText();
  ti.characters = titleText;
  ti.fontName = { family: "Inter", style: "Extra Bold" };
  ti.fontSize = 21;
  ti.lineHeight = { unit: "PIXELS", value: 26 };
  ti.fills = [{ type: 'SOLID', color: { r: 0, g: 0, b: 0 } }];
  hl.appendChild(ti);

  const d = figma.createText();
  d.characters = descText;
  d.fontName = { family: "Plus Jakarta Sans", style: "Medium" };
  d.fontSize = 14.5;
  d.lineHeight = { unit: "PIXELS", value: 20.5 };
  d.fills = [{ type: 'SOLID', color: { r: 0, g: 0, b: 0 } }];
  hl.appendChild(d);
  d.layoutSizingHorizontal = 'FILL';

  return hl;
}
```
