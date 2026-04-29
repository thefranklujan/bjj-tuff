# BJJ Tough — Design Spec

**Version:** 1.0.0 (2026-04-28)
**Status:** Locked. No deviations without Frank's approval.

---

## Identity

- **Purpose:** A solo, sparring-free, belt-free fitness regimen built on Brazilian Jiu Jitsu movement. Strength, flexibility, and skill from BJJ shapes, drilled at pace.
- **Audience:** Adults (25 to 45) who want martial-arts intensity without dojo politics. Curious about BJJ but intimidated by sparring. Already pay for FightCamp, Peloton, F45, or Tonal. Want a workout, not a lifestyle.
- **Core Action:** Join the early-access waitlist (email).
- **Feel Words:** Raw. Mat-tested. Honest. High-output. Quiet confidence over hype. No belts, no ego, no excuses.
- **Category:** Fitness. Sits next to FightCamp, Tae Bo, Zumba, Les Mills BodyCombat. Distinct because it pulls from grappling, not striking or dance.

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
| `--bone-soft` | `#F5F1EA` at 70% | Secondary text, paragraph |
| `--blood` | `#E63946` | Accent, CTAs, highlights only |
| `--steel` | `#1C1C1C` | Card surfaces, dividers |

Three colors only (ink, bone, blood). Steel is a tonal shift of ink, not a fourth color.

### Typography
- **Display:** Anton (Google Fonts). Heavy condensed sans, all caps, tight tracking. Used for H1, H2, section labels.
- **Body:** DM Sans (Google Fonts). Geometric, wide aperture, sets at 17 to 19px for body, 14 to 15px for meta.
- **Mono:** JetBrains Mono (Google Fonts). For data, timecodes, labels.

Headline scale (mobile / desktop): 48 / 96. Subhead: 22 / 32. Body: 17 / 19.

### Density
Generous. Section padding 96px desktop, 64px mobile. Container max width 1200px. Inline spacing on all components matches the spacing law (no Tailwind utility classes for spacing on this build because it's static HTML; explicit pixel values throughout).

---

## Taste Parameters

- **DESIGN_VARIANCE:** 7 of 10. Distinctive, not safe. Pushes typographic scale and asymmetric grids.
- **MOTION_INTENSITY:** 4 of 10. Subtle reveals on scroll, no parallax circus, no autoplay video on mobile.
- **VISUAL_DENSITY:** 5 of 10. Generous whitespace around bold elements. Brutalist confidence, not stuffed.

---

## Layout

- **Primary Pattern:** Single page, vertically stacked sections. Hero, "What it is," "What you get," "How it works," Waitlist, Footer.
- **Navigation:** None at launch. The page is the funnel. A small wordmark in the top left, nothing else.
- **Hero Type:** Full-viewport black. Heavy condensed display headline, one-line subhead, single CTA above the fold.

---

## Components

- **Button (primary):** Blood background, ink text, square corners, 18px / 28px padding, all-caps Anton at 16px tracking 0.05em. Hover: bone background, ink text.
- **Button (secondary):** Transparent with 1px bone border, bone text. Hover: bone fill, ink text.
- **Card:** Steel background, 1px hairline border at bone 10% opacity, 32px padding, no shadows.
- **Form:** Underline-only inputs (no boxes), bone underline, blood underline on focus. Single horizontal row on desktop (email + button), stacked on mobile.
- **Icons:** Minimal stroke icons or none. Icon-free is acceptable; numeric labels (01, 02, 03) replace icons in the "How it works" section.

---

## Content

- **Copy Voice:** Clipped. Coach-like. Honest about what it is and what it isn't. Confident, not boastful. No exclamation points. No emoji. No dashes (per house rule).
- **Imagery Approach:** Hero may render as type-only at launch. Future: high-contrast black-and-white photography of BJJ shapes (shrimp, technical stand-up, guard pulls) with a single blood-red graphic overlay element.

---

## Technical

- **Mobile Support:** Mobile-first. Tested at 375 / 768 / 1280. No horizontal scroll. Tap targets 44px minimum.
- **Dark Mode:** The site IS dark mode. No light variant.
- **Animation Level:** Subtle. CSS-only. Fade-in-up on scroll for sections. No JS animation libraries.
- **Accessibility:** WCAG 2.1 AA. Contrast minimum 4.5:1 for body, 3:1 for large headlines. Keyboard-navigable form. `aria-label` on icon-free CTAs.
- **Build:** Plain `index.html` with embedded `<style>`. No framework. No build step. Vercel static.
- **Form Handler:** `https://formsubmit.co/frank@craftedsystems.io`. Replace later if migrated to Airtable or Mailchimp.

---

## References

- **Inspiration:** Whoop.com (athletic restraint), Tonal.com (typographic muscle), FightCamp.com (combat-fitness energy without copying their palette).
- **Anti-Inspiration:** Generic crossfit sites with neon yellow on black, MMA brand pages with skull graphics, gym sites that lead with stock photography.
- **Banned:** Gradients. Glass effects. Neon. Skulls. Flames. Dashes. Em-dashes. Inter. Roboto.
- **Required:** All-caps display headline. Three colors max. Single accent color reserved for action. Mobile-first. Waitlist form above the fold OR one scroll away on mobile.

---

## Derived Design Tokens

```css
:root {
  --ink: #0A0A0A;
  --bone: #F5F1EA;
  --bone-soft: rgba(245, 241, 234, 0.7);
  --blood: #E63946;
  --steel: #1C1C1C;
  --hairline: rgba(245, 241, 234, 0.1);

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

  --shadow-none: none;

  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
  --duration-fast: 200ms;
  --duration-base: 400ms;
}
```
