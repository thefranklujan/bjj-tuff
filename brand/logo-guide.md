# BJJ Tuff — Brand & Logo Guide

**Version:** 1.0.0 (2026-04-28)

The BJJ Tuff mark is built for three jobs: digital, print, and embroidery. Every file in this folder respects the tightest of those constraints (embroidery: solid shapes, limited colors, no fine detail).

---

## The system

### Asset matrix

| File | Use | Best for |
|------|-----|----------|
| `mark-default.svg` | Primary square mark, blood ground, bone type | Social avatars, app icons, full-color print, t-shirt back, embroidered patches |
| `mark-bone.svg` | Light variant: bone ground, ink type | Light backgrounds, low-color print runs |
| `mark-ink.svg` | Mono dark: ink ground, bone type | All-black single color print, neutral co-branding |
| `mark-outline.svg` | Outline only, single color (uses `currentColor`) | 1-thread embroidery, foil stamp, etching, debossing, anywhere a single ink/thread is needed |
| `lockup-horizontal.svg` | Square mark + wordmark beside, light background | Web headers, banners, business cards, email signatures |
| `lockup-horizontal-dark.svg` | Same lockup, dark background variant | Hero banners, social posts on dark backgrounds |
| `lockup-stacked.svg` | Square mark above wordmark | Posters, badges, jacket back panel, polaroid-style placements |
| `wordmark.svg` | Type only, with brand dot accent | Minimalist applications, footer, legal documents |
| `wordmark-dark.svg` | Wordmark on dark backgrounds | Dark UI, dark print substrates |
| `favicon.svg` | "BT" monogram for tiny sizes (under 32px) | Browser tabs, app icons under 32px, anywhere the full mark would lose legibility |

### Color tokens

| Token | Hex | Pantone (closest, uncoated) | Thread (Madeira Polyneon, closest) |
|-------|-----|----------------------------|------------------------------------|
| Blood | `#E63946` | PMS 178 U | 1747 (Cherry) |
| Bone | `#F5F1EA` | PMS 7527 U | 1170 (Off White) |
| Ink | `#0A0A0A` | PMS Black 6 U | 1800 (Black) |

Three colors. No more. Greys, navies, browns, accents are not part of the brand.

### Typography

- **Display:** Anton (Google Fonts). Used in the wordmark and inside the mark.
- **Production note:** for print and embroidery vendors, **convert text to outlines / paths** in Illustrator, Affinity Designer, Inkscape, or Figma before sending to the vendor. The SVG files reference Anton + Impact as fallback; outlining guarantees the vendor renders the exact letterforms.

---

## Sizing

| Application | Minimum size of the square mark |
|-------------|----------------------------------|
| Embroidery, single position (left chest, sleeve, hat front) | 1.5 in (38 mm) |
| Embroidery, large back panel | 4 in (100 mm) minimum, 6 to 10 in typical |
| Screen print on apparel | 0.5 in (12 mm) — but anything under 1 in will lose the inner type detail |
| DTG / DTF print | 0.75 in (20 mm) |
| Digital | 24 px minimum for the full square mark; under that, switch to `favicon.svg` (BT monogram) |

### Clear space

Always leave clear space equal to **1/4 the mark's width** on all sides. Nothing else (other type, other logos, edges) should enter that space.

For a 200 px mark, that's 50 px clear on every side.

---

## Production notes by medium

### Embroidery (caps, polos, jackets, patches)

- Use `mark-default.svg` (3-thread: blood, bone) or `mark-outline.svg` (1-thread).
- Outline the type before sending to vendor. Vendors often charge a digitization fee per design — submit one outlined SVG / EPS / AI per color variant.
- Madeira Polyneon thread numbers above are starting recommendations; ask your vendor to confirm against their swatch book and your fabric color.
- Avoid embroidering the mark under 1.5 in (38 mm) — the inner type will fill in.

### Screen print (t-shirts, rash guards, hoodies)

- Use `mark-default.svg`, `mark-bone.svg`, `mark-ink.svg`, or `mark-outline.svg` depending on substrate.
- For dark substrates: `mark-default.svg` (blood + bone reads bold) or `mark-ink.svg` flipped to bone outline.
- For white/cream substrates: any default works; `mark-bone.svg` will go to `mark-ink.svg` for crisp print.
- Print at 300 dpi minimum from outlined vector source.

### Rash guards (sublimation print)

- Sublimation reproduces full color cleanly. Use `mark-default.svg` directly — no thread limits, no halftone issues.
- Sleeve placement: 3 in (75 mm) tall mark. Chest placement: 4 to 5 in (100 to 125 mm) tall.

### Mats

- Edge stamp: `mark-outline.svg` or `mark-default.svg` at 6 to 8 in (150 to 200 mm).
- Center print: `mark-default.svg` at 18 to 24 in (450 to 600 mm) for visibility on camera.

### Digital

- Web headers, social avatars: `mark-default.svg` is the default.
- Favicons: `favicon.svg` (BT monogram).
- iOS / Android app icons: render `mark-default.svg` to a 1024x1024 PNG, then export the platform-specific icon set.
- Email signatures: `lockup-horizontal.svg` at 200 px wide.

---

## Do / Don't

### Do

- Use the supplied SVG files as the source of truth.
- Convert text to outlines before sending to print or embroidery vendors.
- Maintain the clear space rule.
- Reproduce in the three brand colors only.

### Don't

- Don't recolor outside the blood / bone / ink palette.
- Don't add gradients, shadows, glows, or strokes that aren't in the supplied files.
- Don't stretch the mark non-proportionally.
- Don't rotate the mark for decorative use.
- Don't redraw the type in a different font.
- Don't add an outline around the square fill version.
- Don't place the mark on busy photographic backgrounds; if you must, put it on a solid blood, bone, or ink card first.

---

## Future additions (when needed)

- `mark-default.png` and `mark-default@2x.png` raster exports for vendors who require PNG.
- `mark-default.eps` and `.ai` for legacy print vendors.
- iOS and Android app icon sets.
- Animated SVG mark for video bumpers (cast intros, channel idents).
- Full type system extension (custom outlined letterforms) once Frank confirms direction with Drop 01.
