# BJJ Tuff — Design Spec

**Version:** 2.0.0 (2026-04-28)
**Status:** Locked. No deviations without Frank's approval.

> v2 expands BJJ Tuff from a future workout app into a sister-led BJJ fitness content + commerce brand. Three pillars: content (YouTube long form + Instagram/TikTok daily drops), cast (Sofia, Olivia, and Ariana on camera), and commerce (rash guards, shirts, mats, accessories). Same locked visual system (ink / bone / blood, Anton + DM Sans).

---

## Identity

- **Purpose:** A sister-led BJJ fitness content and merchandise brand. Free workouts and drills on YouTube, daily short-form drops on Instagram and TikTok, a merchandise line built around the cast and the discipline.
- **Audience:** Three concentric circles.
  1. **Core:** Adults (25 to 45) who want martial-arts intensity without dojo politics. Already pay for FightCamp, Peloton, F45, or Tonal.
  2. **Adjacent:** Parents and kids who train BJJ or want to start. The cast lowers the entry barrier for anyone intimidated by a traditional dojo.
  3. **Fan layer:** People who follow the channel, buy the merch, and turn the brand into identity.
- **Core Action:** Join the early-access waitlist (email). Secondary action: follow the channel on YouTube, Instagram, TikTok. Tertiary: shop coming soon.
- **Cast:** Sofia, Olivia, and Ariana. Three sisters. They demonstrate the moves and lead the rounds. The brand is built around them.
- **Feel Words:** Raw. Mat-tested. Honest. Family-rooted but not soft. Real movement, real sweat, real sisters.
- **Category:** Hybrid. Fitness creator brand (Chloe Ting model). Merch-driven creator brand (MrBeast / Logan Paul model). Sits at the intersection of FightCamp, a YouTube fitness channel, and a streetwear-grade combat-sports apparel line.

---

## Visual System

### Aesthetic
Gritty athletic minimalism. Black-dominant. Brutalist hierarchy. Photography-driven if available, otherwise typographic muscle. Closer to Whoop and Tonal than to a generic gym site.

### Base Theme
Dark. Black is the canvas. Bone white is the type. One accent (blood red) reserved for action.

### Colors
| Token | Hex | Use |
|-------|-----|-----|
| `--ink` | `#0A0A0A` | Background, dominant surface |
| `--bone` | `#F5F1EA` | Primary text, headlines |
| `--bone-soft` | `#F5F1EA` at 70% | Secondary text |
| `--blood` | `#E63946` | Accent, CTAs, highlights only |
| `--steel` | `#1C1C1C` | Card surfaces, dividers |

### Typography
- **Display:** Anton (Google Fonts).
- **Body:** DM Sans (Google Fonts).
- **Mono:** JetBrains Mono (Google Fonts).

### Density
Generous. Section padding 96px desktop, 64px mobile. Container max width 1200px.

---

## Taste Parameters

- **DESIGN_VARIANCE:** 7 of 10.
- **MOTION_INTENSITY:** 4 of 10.
- **VISUAL_DENSITY:** 5 of 10.

---

## Layout

Single page, vertically stacked:

1. Header (wordmark + small "Watch on YouTube" link)
2. Hero (headline + subhead + waitlist primary CTA + social link strip)
3. What it is (vs traditional dojo)
4. The Cast (Sofia, Olivia, Ariana)
5. What you get (Strength / Flexibility / Skill)
6. Where to drill (YouTube / Instagram / TikTok platform cards)
7. The Shop (merch category tiles)
8. How it works (three steps reframed for content workflow)
9. Bottom CTA (waitlist)
10. Footer (social links + brand line)

---

## Components

- **Button (primary):** Blood background, bone text, square corners, 16/28 padding, all-caps Anton 16px tracking 0.05em. Hover: bone background, ink text.
- **Button (secondary, social link):** Transparent with 1px hairline border, bone text, mono font, all-caps. Includes trailing arrow glyph (`↗`).
- **Card (cast):** Steel background, hairline border, 32px padding. Numbered cast position, name in display, one-line role.
- **Card (platform / shop):** Steel background, hairline border, 32px padding. Platform/category title in display, one-line body, optional meta.
- **Form:** Underline-only inputs.
- **Social link strip:** Row of three text-only links (YouTube ↗ / Instagram ↗ / TikTok ↗) under the primary CTA.

---

## Content

- **Copy Voice:** Clipped. Coach-like. Confident. No exclamation points. No emoji. No dashes. The cast (Sofia, Olivia, Ariana) is named explicitly as the on-camera team, not described as "kids."
- **Imagery Approach:** Type-only at launch. Future: high-contrast black and white photography of the sisters performing technique. Treat them as athletes, not as cute kids. Posed shots are out; mid-movement shots are in.

---

## Technical

- **Mobile Support:** Mobile-first. Tested at 375 / 768 / 1280.
- **Dark Mode:** The site IS dark mode.
- **Animation Level:** Subtle. CSS-only. Fade-in-up on scroll.
- **Accessibility:** WCAG 2.1 AA.
- **Build:** Plain `index.html` with embedded `<style>`. No framework. Vercel static.
- **Form Handler:** `https://formsubmit.co/frank@craftedsystems.io`.
- **Social handles (placeholder, register before launch):**
  - YouTube: `youtube.com/@bjjtuff`
  - Instagram: `instagram.com/bjjtuff`
  - TikTok: `tiktok.com/@bjjtuff`
- **Shop:** "Drop 01 coming soon" framing pre-launch. When the shop goes live, swap the shop section CTAs to point at the Shopify (or chosen) storefront.

---

## References

- **Inspiration:** Whoop.com, Tonal.com, FightCamp.com (aesthetic). Chloe Ting (free YouTube content + premium funnel). MrBeast Feastables, Logan Paul Maverick (creator-led merch). Shaka Hislop's Born Wrestler (sister-led athletic content brand model).
- **Anti-Inspiration:** Generic crossfit sites with neon yellow on black. MMA brand pages with skull graphics. Family-vlog aesthetics. Posed-cute kid photography.
- **Banned:** Gradients (other than radial atmospheric tints in hero). Glass effects. Neon. Skulls. Flames. Dashes. Em-dashes. Inter. Roboto. Family-vlog framing of the cast.
- **Required:** All-caps display headline. Three colors max. Cast named on the page. Social link strip visible. Shop section visible (even if pre-launch). Mobile-first.

---

## Derived Design Tokens

```css
:root {
  --ink: #0A0A0A;
  --bone: #F5F1EA;
  --bone-soft: rgba(245, 241, 234, 0.7);
  --bone-faint: rgba(245, 241, 234, 0.5);
  --blood: #E63946;
  --steel: #1C1C1C;
  --hairline: rgba(245, 241, 234, 0.1);
  --hairline-strong: rgba(245, 241, 234, 0.2);

  --font-display: "Anton", "Impact", sans-serif;
  --font-body: "DM Sans", system-ui, sans-serif;
  --font-mono: "JetBrains Mono", "Menlo", monospace;

  --space-xs: 8px;
  --space-sm: 16px;
  --space-md: 32px;
  --space-lg: 64px;
  --space-xl: 96px;
  --space-2xl: 128px;

  --radius: 0px;
  --radius-pill: 999px;

  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
  --duration-fast: 200ms;
  --duration-base: 400ms;
}
```
