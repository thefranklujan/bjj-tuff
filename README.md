# BJJ Tuff

Solo Brazilian Jiu Jitsu fitness. No sparring. No belts. Strength, flexibility, and skill drilled at pace.

A Crafted & Company brand.

---

## Stack

- Static `index.html` (no build step, no framework)
- Embedded CSS, vanilla JS for scroll reveals
- Google Fonts: Anton (display), DM Sans (body), JetBrains Mono (meta)
- Waitlist form posts to [formsubmit.co](https://formsubmit.co/) → frank@craftedsystems.io
- Hosted on Vercel (auto-deploy from GitHub `main`)

## Files

- `index.html` — landing page
- `design-spec.md` — locked design system (colors, type, taste params)
- `README.md` — this file

## Local preview

Open `index.html` in any browser. No build, no install.

```bash
open index.html
```

## Deploy

Push to `main` on GitHub → Vercel auto-deploys.

```bash
git add . && git commit -m "..." && git push origin main
```

## Waitlist activation (one-time)

The form points to `https://formsubmit.co/frank@craftedsystems.io`. After the first real submission, formsubmit will email Frank a one-click activation link. Click it once and every future submission lands directly in Frank's inbox.

To migrate to Airtable or Mailchimp later, swap the `action="..."` attribute on both `<form class="waitlist">` elements in `index.html`.

## Custom domain

Point the chosen domain (e.g., `bjjtuff.com`) at the Vercel project. Vercel will issue the SSL certificate automatically.
