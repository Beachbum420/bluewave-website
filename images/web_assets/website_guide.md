# Blue Wave Construction — Website Implementation Guide

For your in-progress website build. Tells you which logo files go where, technical specs, and a recommended site structure.

---

## LOGO PLACEMENT BY PAGE LOCATION

| Location | File to use | Notes |
|---|---|---|
| Main navigation header (light bg) | `01_logo_horizontal_navy.svg` | Render at ~180–220px wide |
| Main navigation header (dark/navy bg) | `02_logo_horizontal_reverse.svg` | Same size |
| Hero section (large) | `01_logo_horizontal_navy.svg` or `02_logo_horizontal_reverse.svg` | Up to 600px wide |
| Footer | `02_logo_horizontal_reverse.svg` | Render at ~160px wide on a navy footer |
| Mobile menu | `05_logo_compact_navy.svg` | Stacked version fits better on narrow screens |
| Browser tab (favicon) | `07_favicon.svg` | Also export as `favicon.ico` for older browser support |
| OG / social share image | Build a 1200×630 image with `02_logo_horizontal_reverse.svg` centered on navy background | This shows when someone shares your URL on Facebook, Twitter, LinkedIn |

**Important — SVG embedding:**
Most modern site builders (Webflow, Squarespace, Wix, Framer, custom) accept SVG directly. If yours doesn't (some older WordPress themes), open the SVG in any browser, right-click, "Save image as PNG" at 2x or 3x intended display size to keep it sharp on Retina screens.

---

## RECOMMENDED SITE STRUCTURE

Don't overthink your site. A construction company doesn't need 12 pages. Here's the lean structure that converts:

### Single-page layout (recommended for V1)

A long single page, navigation links scroll to anchors. Sections in order:

1. **Hero** — Logo, single confident headline, subheadline, primary CTA
2. **What we do** — 3 services maximum (e.g., "Renovations · Ground-up · Investor partnerships")
3. **Recent work** — Photo grid of 6–9 projects (if you have them; if not, skip until you do)
4. **About / Why us** — 2-3 short paragraphs + your headshot + license numbers
5. **Process** — Numbered list of how a project flows with you
6. **Contact** — Form + phone + email + service area map

That's the entire site for now. Add a separate "Projects" page when you have 10+ projects with photos worth showing in detail.

---

## COPY SUGGESTIONS

### Hero headline options (pick one):

- "Built on the coast. Built to last."
- "South Bay construction, done right."
- "Coastal builds. Investment-grade execution."
- "Ground-up. Renovations. Real investment returns."

### Hero subheadline:

> Licensed general contractor and developer serving the South Bay — Manhattan Beach, Hermosa, Redondo, El Segundo, and surrounding cities.

### Primary CTA button:

> "Start a project" or "Schedule a walkthrough"

(Avoid "Get a quote" — quote-seekers are price shoppers, you want clients who want *you*.)

---

## TECHNICAL SPECS

### Performance

- **Logo file size:** Each SVG in this package is under 2KB. Don't replace them with bloated PNGs.
- **Images:** Compress jobsite/project photos before uploading. Use [squoosh.app](https://squoosh.app) — aim for under 200KB per image. Use WebP format if your site supports it.
- **Fonts:** Inter Tight + JetBrains Mono. Both are on Google Fonts (free). Self-host if you can; if using a builder, just link from Google Fonts.

### Color values for CSS

```css
:root {
  --navy: #0A2540;       /* Primary brand color */
  --deep: #0E3A5F;       /* Subtle gradient pair */
  --wave: #1B6CA8;       /* Accent — wave underline, hover states */
  --sky:  #4FA3D1;       /* Reverse-mode wave, demoted text on dark */
  --sand: #E8D9B8;       /* Warm secondary background */
  --bone: #F5EFE4;       /* Off-white default light bg */
  --char: #141B24;       /* Near-black for body text */
}
```

### Typography stack

```css
font-family: 'Inter Tight', -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif;
```

For mono/labels:
```css
font-family: 'JetBrains Mono', 'Courier New', monospace;
```

---

## CONTENT YOU NEED TO GATHER NOW

While you build the site, gather these — without them, the site looks empty:

- [ ] **Headshot** — Outdoors, soft daylight, navy or neutral shirt. NOT a stock photo or a corporate office shot. South Bay light, casual but composed. Could be on a job site, on the bluffs, in front of a recent project.
- [ ] **Project photos** — Even if you only have 2-3 finished. iPhone in landscape, golden hour, no people. Both wide context shots and detail shots. If you have nothing yet, use a relevant high-quality stock photo of South Bay coastline as a hero placeholder until you do.
- [ ] **License numbers** — CSLB #1153965 and DRE #02185763. Include in footer of every page (legal requirement for licensed work).
- [ ] **Service area** — List specific cities: Manhattan Beach, Hermosa Beach, Redondo Beach, El Segundo, Hawthorne, Lawndale, Gardena, Torrance, Palos Verdes
- [ ] **Phone number for the brand** — Either keep your existing number or get a Google Voice / RingCentral number specifically for the business
- [ ] **Email** — `ryan@bluewaveconstruction.la` (or your domain). Forward to your existing email if you don't want a separate inbox yet.

---

## SEO BASICS (don't go down a rabbit hole)

You're a local service business in a tight geographic area. SEO for you = three things, in order:

1. **Google Business Profile** — Create one immediately at business.google.com. Get verified (they mail you a postcard). Add photos, hours, services, service area cities. This is your single biggest SEO investment.
2. **Page title and meta description** — Keep it simple:
   - Title: `Blue Wave Construction · South Bay General Contractor & Developer`
   - Meta: `Licensed general contractor serving Manhattan Beach, Hermosa, Redondo, El Segundo. Renovations, ground-up builds, investor partnerships. CSLB #1153965.`
3. **City pages** — If you have time later, create simple sub-pages like `/manhattan-beach-contractor` with 300-500 words about your work in that specific city. Helps rank locally.

Skip everything else (link building, blog content, technical SEO audits) until you have the basics nailed and a steady project flow.

---

## DOMAIN NOTES

You mentioned `bluewavela.com` is your current site for the home services business. For the construction brand, recommended domains in order of preference:

1. `bluewaveconstruction.la` — best, matches the brand exactly, geographic
2. `bluewaveconstruction.com` — most universal, check availability
3. `bluewavedev.com` — short, signals "developer"
4. Keep `bluewavela.com` and put the construction site there once you fully transition

When you transition, set up a 301 redirect from `bluewavela.com` to your new domain to preserve any SEO equity.

---

## EMAIL SIGNATURE TEMPLATE

Copy this into your email client (Gmail Settings > General > Signature). Replace [link] with the actual logo image hosted on your site.

```
Ryan Verbiest
Founder · General Contractor

Blue Wave Construction
[Wave underline here, optional]
(310) 995-7741
bluewaveconstruction.la

CSLB #1153965 · DRE #02185763
```

For HTML version with the logo as image, host `02_logo_horizontal_reverse.svg` on your site, link to it. Keep image under 80px tall in the signature.

---

## FINAL NOTE

Resist the urge to make your website do everything. A construction site needs: who you are, what you do, what you've done, how to reach you. That's it. The brand discipline of *not* over-stuffing the site is itself part of the luxury positioning.
