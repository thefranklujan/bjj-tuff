# BJJ TUFF — Brand & Logo Guide

**Version:** 2.0.0 (2026-04-28)

The BJJ TUFF mark is a two-color wordmark. No symbol, no patch — just the type and the dot.

- **BJJ** sets in bone (or ink on light backgrounds).
- **TUFF** sets in blood red.
- A single blood-red square dot anchors the lockup.
- Type is **Anton** (Google Fonts) — the same display font used on the landing page.

---

## The system

| File | Use |
|------|-----|
| `wordmark.svg` | Light backgrounds — BJJ in ink, TUFF in blood, dot accent |
| `wordmark-dark.svg` | Dark backgrounds — BJJ in bone, TUFF in blood, dot accent |
| `favicon.svg` | Tiny applications (browser tab, app icon under 32 px) — solid blood square with bone "T" |
| `og-image.png` | 1200 × 630 social preview render of the wordmark on dark |
| `og-image.html` | Source template for the OG render |
| `legacy/` | Earlier concept marks (square patch, lockups). Kept for reference. Not part of the active system. |

### Color tokens

| Token | Hex | Pantone (closest, uncoated) | Thread (Madeira Polyneon) |
|-------|-----|-----------------------------|---------------------------|
| Blood | `#E63946` | PMS 178 U | 1747 (Cherry) |
| Bone | `#F5F1EA` | PMS 7527 U | 1170 (Off White) |
| Ink | `#0A0A0A` | PMS Black 6 U | 1800 (Black) |

Three colors. No more. Greys, navies, browns are not part of the brand.

### Typography

- **Display:** Anton (Google Fonts).
- For print and embroidery vendors, **convert text to outlines / paths** in Illustrator, Affinity Designer, Inkscape, or Figma before sending the file. The SVGs reference Anton + Impact as fallback; outlining guarantees the vendor renders the exact letterforms.

---

## Sizing

| Application | Minimum size of the wordmark |
|-------------|------------------------------|
| Embroidery, single position | 2.5 in (64 mm) wide minimum so the type stays legible |
| Screen print on apparel | 1.5 in (38 mm) wide minimum |
| Digital | 96 px wide minimum for the full wordmark; under that, switch to `favicon.svg` |

### Clear space

Leave clear space equal to **the height of the J in BJJ** on all sides. Nothing else (other type, other logos, edges) should enter that space.

---

## Production notes by medium

### Embroidery (caps, polos, jackets, patches)

- Two-color (blood + bone, or blood + ink on light-color garments).
- Outline the type before sending to vendor.
- Wordmarks under 2 in (50 mm) wide may lose detail in the J counters and the F crossbars; bump up to 3 in (75 mm) for hat fronts.

### Screen print (t-shirts, rash guards, hoodies)

- Two-color screen print works great. For dark substrates, use `wordmark-dark.svg` (BJJ bone, TUFF blood).
- For light substrates, use `wordmark.svg` (BJJ ink, TUFF blood).
- Print at 300 dpi minimum from outlined vector source.

### Mats

- Edge stamp: full wordmark at 8 to 12 in (200 to 300 mm) wide.
- Center print: full wordmark at 24 to 36 in (600 to 900 mm) wide for visibility on camera.

### Digital

- Web headers, social avatars: render `wordmark-dark.svg` for the brand's standard dark canvas.
- Favicons: `favicon.svg`.
- iOS / Android app icons: render `favicon.svg` to a 1024 × 1024 PNG, then export the platform-specific icon set.

---

## Do / Don't

### Do

- Use the supplied SVG files as the source of truth.
- Convert text to outlines before sending to print or embroidery vendors.
- Maintain the clear space rule.
- Keep the BJJ/TUFF color split (BJJ neutral, TUFF blood) — this is the brand's signature treatment.

### Don't

- Don't reverse the color split (TUFF should never appear in bone or ink while BJJ is blood).
- Don't recolor outside the blood / bone / ink palette.
- Don't add gradients, shadows, glows, or strokes that aren't in the supplied files.
- Don't stretch the wordmark non-proportionally.
- Don't redraw the type in a different font.
- Don't place the wordmark on busy photographic backgrounds; if you must, put it on a solid blood, bone, or ink card first.

---

## Future additions (when needed)

- `wordmark.png` and `wordmark@2x.png` raster exports for vendors who require PNG.
- `wordmark.eps` and `.ai` for legacy print vendors.
- iOS and Android app icon sets.
- Animated SVG wordmark for video bumpers (cast intros, channel idents).
