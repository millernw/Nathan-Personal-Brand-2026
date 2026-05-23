# 02 — Design Direction

> Use this file when building any UI component, page layout, or visual element.
> Paste this alongside 00-master-prompt.md when starting a design-heavy build.
> The reference URLs in this file are the highest-impact input you can give an AI.

---

## Aesthetic Direction

- **Vibe keywords (3–5):** editorial, minimal, confident, polished, human
- **Overall tone:** Authoritative and trustworthy — feels like a premium personal brand, not a corporate website. Warm enough to feel human, structured enough to feel credible.
- **Light or dark theme:** Light — white and near-white backgrounds with near-black text
- **Density:** Airy and open with generous whitespace — sections breathe, headlines have room to be dramatic

---

## Color Palette

| Role | Hex | Usage |
|------|-----|-------|
| Background | `#FFFFFF` | Main page background |
| Surface | `#F8FAFC` | Cards, alternate section backgrounds, nav when scrolled |
| Primary | `#0F172A` | Headings, key text, strong UI elements |
| Accent | `#2563EB` | CTAs, active states, links, hover highlights |
| Text primary | `#0F172A` | All headings and body text |
| Text secondary | `#64748B` | Captions, meta info, labels, secondary copy |
| Border | `#E2E8F0` | Dividers, card outlines, subtle separators |
| Success | `#10B981` | Confirmations, positive states |
| Error | `#EF4444` | Warnings, form validation errors |

---

## Typography

- **Heading font:** Instrument Serif
  - Source: Google Fonts
  - Weight: 400 (regular — Instrument Serif reads beautifully at display sizes without needing bold)
  - Style: Use italic variant for emphasis or pull quotes — very editorial
- **Body font:** DM Sans
  - Source: Google Fonts
  - Weight: 400 regular, 500 medium, 600 semi-bold for UI elements
- **Mono font:** Not used — unless displaying technical content in blog posts
- **Type scale:** Large and dramatic — h1 at 72–80px desktop, 40px mobile. Subheadings generous. Body at 17–18px for readability.
- **Letter spacing:** Tight on large headings (-0.02em), normal on body text

---

## Reference Sites

> Listed in priority order. Study these before generating any UI.

**Sites I love (and what specifically I like):**

1. URL: https://www.melrobbins.com/
   What I like: The editorial feel, the way photography is used as a design element, the confidence of the layout, how personal it feels without being unprofessional. The layered sections where content overlaps scroll zones.

2. URL: https://myrongolden.com/
   What I like: The personal brand authority it communicates immediately — you know who this person is and why they matter within seconds. Strong typographic hierarchy.

3. URL: https://jennakutcher.com/
   What I like: The way different sections feel layered as you scroll — content overlaps, images bleed into the next section, it has depth and motion. The overall warmth that doesn't sacrifice professionalism.

4. URL: https://tonyrobbins.com/
   What I like: The sheer scale of the hero, how the photography commands attention, the strong CTA hierarchy, how trust signals are woven into the layout rather than bolted on.

**Sites I do NOT want to look like:**

1. Generic SaaS landing pages — blue gradient hero, stock photo team, pricing table
   What I dislike: Impersonal, templated, feels like it was made in an afternoon. No sense of a human being behind the brand.

2. Cluttered speaker bureau pages
   What I dislike: Too many elements competing for attention, poor whitespace, feels like a résumé not a brand.

---

## Layout & Spacing

- **Border radius:** Small — 8px on cards, 6px on buttons, 0 on hero/full-bleed elements
- **Shadow style:** Subtle — light drop shadows on cards only (0 2px 12px rgba(0,0,0,0.08)). No dramatic shadows.
- **Grid system:** 12-column for section layouts, asymmetric on hero and feature sections for editorial interest
- **Section padding:** Generous — 120px vertical on desktop, 80px on tablet, 60px on mobile
- **Max content width:** 1280px centered with 24px edge padding on mobile

---

## Animation & Motion

- **Animation level:** Expressive — this site should feel crafted and alive, like the reference sites
- **Preferred animation style:**
  - Parallax scroll on hero image and large portrait sections (image moves at 60% scroll speed of content)
  - Overlapping layers: sections should slightly overlap or bleed into each other on scroll, not be hard-cut cards stacked vertically
  - Scroll-triggered fade + slide-up for content blocks (staggered for cards)
  - Image blur-to-sharp transition on hover for project/work cards
  - Background image subtle zoom on scroll for full-bleed photo sections
- **Hover states:** Image cards — scale 1.03 + blur clears to sharp. Buttons — background fills from left (sliding door effect). Nav links — underline draws in from left.
- **Page load animation:** Yes — brief, confident fade-in on hero text (200ms delay, 400ms duration). Nothing flashy.
- **Transition speed:** Standard 250ms for UI interactions, 400–600ms for scroll-triggered reveals, 800ms for parallax sections

---

## Imagery & Media

- **Photography style:** Real editorial photography of Nathan — dramatic, high contrast, magazine-quality. Not headshots. Images should feel like they belong in a feature article. Full-bleed usage wherever possible.
- **Illustration style:** None — photography is the primary visual element
- **Icon set:** Lucide icons — clean, consistent, minimal. Used sparingly in service cards only.
- **Video usage:** None at launch — potential future addition for a "watch my talk" section

---

## What to Absolutely Avoid

> Paste this block into every prompt. Non-negotiables for this project.

- NO purple or blue gradients as backgrounds
- NO stock photo people smiling at laptops
- NO Lorem Ipsum or placeholder text
- NO Inter, Roboto, or Arial fonts
- NO generic SaaS look — this is a personal brand site, it should feel like a person, not a product
- NO flat, lifeless sections — every scroll zone should have visual interest: texture, overlap, parallax, or motion
- NO heavy drop shadows or 3D button effects — keep it flat and editorial
- NO card grids that look like a pricing comparison table when listing services
