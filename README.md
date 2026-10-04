# Mosaic Field — Generative Art

> A seed-based generative system for thresholded tile compositions.  
> A reproducible catalogue of computational textile compositions.

---

## What is this?

**Mosaic Field** is a generative design system that lays an 80 × 80 grid across the canvas and fills it with a mathematical field — circular waves, checkerboard noise, organic blobs, concentric rings, random dots, or swirls. Each value is compared to a threshold curve that varies with distance from the centre, and the cell is set on or off accordingly. What survives the threshold becomes a tile: a square, a circle, or a rotated square, chosen once per composition.

Every artwork in this catalogue is defined by a single numeric seed. The same seed always produces the identical composition — making each piece **traceable, reproducible, and licensable** across textile, print, and apparel applications.

Named for the ancient surface made of many small pieces, each placed by hand within a larger geometry — **Mosaic Field** translates that logic into code.

---

## Live

🌐 **[View the catalogue →](https://reyrove.github.io/Mosaic-Field-Generative-Art/)**

---

## The System

The generator combines three layers:

| Layer | Description |
|-------|-------------|
| **Field** | An 80 × 80 grid, filled with one of six mathematical patterns. |
| **Threshold** | A distance-varying curve that masks the field into a shape rather than a rectangle. |
| **Tiles** | Surviving cells, drawn as squares, circles, or rotated squares, with per-cell colour variation. |

All three layers are driven by the same seed, ensuring deterministic output.

### Parameters

- **Pattern type** — one of six: circular waves, checker noise, organic blobs, concentric rings, random dots, swirl
- **Grid size** — fixed at 80 × 80
- **Shape** — squares, circles, or rotated tiles, chosen per seed
- **Colour set** — 2 to 5 hues spaced around a base drawn opposite the background
- **Final effect** — glow dots, connecting lines, or cross patterns

---

## Structure

```
Mosaic-Field-Generative-Art/
├── index.html          ← Full catalogue (single-file)
├── images/
│   ├── fav.svg
│   ├── tote.png
│   ├── tee.png
│   └── cushion.png
└── README.md
```

The entire project is contained in a single `index.html` — no build step, no framework. Open it in any modern browser.

---

## Features

- **Seed-based generation** — every composition is deterministic and reproducible
- **Six pattern types** — circular waves, checker noise, organic blobs, concentric rings, random dots, swirl
- **Three tile shapes** — squares, circles, rotated tiles
- **Three final effects** — glow dots, connecting lines, cross patterns
- **Live catalogue** — cover, plate, surfaces, process, archive, commission sections
- **Multiple surfaces** — print, scarf, textile, wallpaper — all rendered from the same seed
- **Archive of 8 seeds** — click any plate to load it into the main view
- **PNG export** — download any composition directly from the browser
- **Keyboard shortcuts** — `R` for new seed, `S` to save
- **Legal modal** — licensing, terms, and credits built in
- **Responsive** — works on desktop, tablet, and mobile
- **Mobile-first navbar** — horizontally scrollable with fade hint

---

## Usage

### Generate a new composition

Click **New Seed** or press `R`.

### Download the current composition

Click **Download** or press `S`.

### Load a seed from the archive

Click any plate in the **Archive** section.

---

## Colour System

Each seed draws a coherent colour set rather than a fixed palette:

1. A **background hue** is drawn from the full 360° range, with low saturation (15–30%) and low brightness (10–20%).
2. A **base hue** is placed opposite the background — 180° away, jittered ±30°.
3. **Two to five hues** are spaced evenly around the base, each jittered ±20°, with saturation 60–90% and brightness 60–90%.

The result reads as luminous marks above a deep, coloured ground — the tiles feel lit rather than painted.

The **final effect** adds one of three luminous overlays at low opacity: glow dots (bright halos around some tiles), connecting lines (short strokes between adjacent tiles), or cross patterns (small crosses centred on some tiles).

---

## Technical Notes

- p5.js 1.9.0 (CDN) for canvas rendering
- Custom seeded random generator for deterministic output
- HSB colour mode, per-instance
- Background wash applied at 15% alpha over the base fill
- Final effect applied at 5–25% alpha, chosen per seed
- Rectangular surfaces tile the square composition to fill aspect ratio
- Threshold curve varies with distance from canvas centre, masking the field into a soft-edged shape

---

## About

**Mosaic Field** is a project by [Reyhaneh Daneshdoost](https://reyrove.github.io/) — an Iranian-born artist working at the intersection of classical textile logic and generative systems.

The work begins with a simple observation: the woven surface — repetitive, mathematically structured, infinitely variable — has always been a form of computation, long before computers.

**Mosaic Field** is an attempt to render that logic visible.

> *A wave crosses a grid, crosses a threshold, and becomes a field of tiles.*

---

## Licensing

All compositions are seed-documented and available for licensing across textile, surface, and apparel applications.

For commercial use, custom editions, or exclusive rights:

📧 **reyhanehdaneshdoost@gmail.com**

See the **Licensing** section in the live catalogue for details.

---

## Links

- 🌐 [Website](https://reyrove.github.io/)
- 📷 [Instagram](https://www.instagram.com/rey._.rove/)
- 💼 [LinkedIn](https://www.linkedin.com/in/reyhaneh-daneshdoost-730481160/)
- 🐦 [X](https://x.com/reyrove)

---

## Credits

**Design & Generative System**  
Reyhaneh Daneshdoost

**Typefaces**  
Cormorant Garamond · DM Mono

**Edition**  
Mosaic Field — Autumn 2026

---

<p align="center">
  <em>Computational Textile Design</em><br />
  <sub>© Reyrove Studio · All compositions reproducible by seed</sub>
</p>