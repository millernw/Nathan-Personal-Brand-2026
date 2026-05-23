# 04 — Site Structure & Layout

> Use this file when building navigation, page layouts, or any structural scaffolding.
> Paste this alongside 00-master-prompt.md when starting a new page or layout session.

---

## Site Map

| Page | Route | Priority | Notes |
|------|-------|----------|-------|
| Home | `/` | P1 | Main landing — hero, services, about teaser, writing teaser, CTA |
| About | `/about` | P1 | Full story, philosophy, credentials, photo-forward |
| Work / Projects | `/work` | P1 | Case studies or featured client outcomes |
| Blog index | `/blog` | P1 | Writing archive — card grid, filterable by topic |
| Blog post | `/blog/[slug]` | P1 | Article template — MDX rendered with reading time, share |
| Contact | `/contact` | P1 | Simple form page — wired to HighLevel |
| Privacy Policy | `/privacy` | P2 | Legal — simple text page |
| Terms of Service | `/terms` | P2 | Legal — simple text page |

---

## Navigation

**Header nav:**
- **Style:** Sticky top bar — transparent over hero, transitions to `#FFFFFF` with subtle border-bottom on scroll
- **Logo position:** Left — "Nathan Miller" wordmark in Instrument Serif
- **Nav links:** About, Work, Writing, Contact
- **CTA in nav:** Yes — "Work with me" — accent blue button, right side
- **Mobile nav:** Hamburger → full-screen overlay with large nav links (staggered fade-in animation)
- **Transparent on hero?** Yes — transparent with white text over hero image, becomes solid on scroll

**Footer nav:**
- **Columns:** 3-column on desktop, stacked on mobile
- **Column 1:** Nathan Miller — tagline + social icons (LinkedIn, Instagram, Facebook)
- **Column 2:** Site: Home, About, Work, Writing, Contact
- **Column 3:** Legal: Privacy, Terms
- **Social icons:** Yes — LinkedIn, Instagram, Facebook
- **Newsletter in footer:** No

---

## Homepage Section Order

> Every section in exact scroll order. Each should feel visually distinct but flow together.

1. **Hero**
   - Layout: Full-viewport height. Large editorial portrait of Nathan — occupies right ~60% of screen, slightly oversized and clipped. Headline and subhead left-aligned on the left. Primary CTA + secondary CTA stacked below headline. Parallax: portrait scrolls at 70% speed of text.
   - Goal: Establish who Nathan is and drive to "Work with me" within 5 seconds

2. **Authority Bar**
   - Layout: Full-width strip below hero — subtle background (#F8FAFC). Text: "Trusted by founders and executives at:" followed by 4–6 logo placeholders or company names in muted gray.
   - Goal: Establish credibility immediately below the fold

3. **What I Do (Services)**
   - Layout: 4-card grid on desktop (2x2 on tablet, 1 column on mobile). Each card: icon, service name, 1-sentence description, subtle hover effect (slight lift + border color change). Not a traditional pricing card — these are service categories.
   - Goal: Communicate the four ways to work with Nathan clearly

4. **The Problem (Narrative Section)**
   - Layout: Full-width, alternating background (#0F172A dark). Large editorial text only — no image. A short, punchy statement about why marketing fails for most founders. Possibly 2–3 sentences displayed large (think magazine pull quote). Accent blue used for emphasis word or phrase.
   - Goal: Create recognition — the visitor should think "that's me"

5. **About Teaser**
   - Layout: Asymmetric 2-column — large Nathan photo left (slight parallax), editorial text right. Photo slightly overlaps into the previous section on scroll. 2–3 sentences from the about copy + "Read my story" link.
   - Goal: Make Nathan feel real and compelling — drive to /about

6. **Featured Writing**
   - Layout: "From the blog" header + 3 latest post cards in a horizontal row (vertical stack on mobile). Each card: post title, date, 1-line description, "Read" arrow link. Subtle image or illustration optional.
   - Goal: Show depth of thinking and drive blog traffic

7. **Testimonials**
   - Layout: Full-width, alternating background (#F8FAFC). 3 testimonial cards displayed horizontally. Each: large quotation mark (accent blue), quote text, name, title/company. On mobile: single card with left/right swipe.
   - Goal: Social proof from real clients

8. **Final CTA (Work With Me)**
   - Layout: Full-width section, dark background (#0F172A). Large centered headline: "Ready to get clear?" Subhead: "Clarity on your message. Systems that run it. Results that compound." Single large CTA button: "Work with me" in accent blue. No other elements — maximum focus.
   - Goal: Final conversion push before footer

9. **Footer**
   - See footer nav spec above
   - Goal: Navigation, social, legal

---

## About Page Structure

1. **Hero** — Large full-width photo of Nathan. Name + tagline overlaid. Parallax scroll.
2. **Story section** — 3–4 paragraphs. Personal, direct, credible. Why Nathan does this work.
3. **Philosophy / values** — 3–4 belief statements (e.g. "I believe clarity is a competitive advantage") displayed as large pull quotes or a numbered list with editorial styling.
4. **Credentials** — Understated. Brief list: years experience, industries worked in, notable outcomes. Not a résumé.
5. **CTA** — "Work with me" link/button

---

## Work / Projects Page Structure

1. **Page header** — "Work" heading + 1-sentence description
2. **Case study cards** — Each card: client type (not necessarily name), the problem, the outcome (metric if available), services used. Hover: image blur-to-sharp reveal.
3. **CTA** — "Want results like these? Work with me."

---

## Component Library

**Navigation components:**
- [ ] Top navigation bar (desktop) — transparent + solid scroll variant
- [ ] Mobile hamburger menu + full-screen overlay
- [ ] Footer — 3-column

**Hero components:**
- [ ] Homepage hero — parallax portrait + editorial headline
- [ ] Page hero — full-width photo with text overlay (for About, Work, Blog)

**Content components:**
- [ ] Service card (4-up grid)
- [ ] Testimonial card (horizontal 3-up)
- [ ] Blog post card (3-up grid)
- [ ] Work/case study card with blur-reveal hover
- [ ] About teaser block (asymmetric 2-col with overlapping photo)
- [ ] Narrative/pull quote section (dark background, large text)
- [ ] Authority/logo bar

**Form components:**
- [ ] Work with me / Contact form (wired to HighLevel)

**UI primitives:**
- [ ] Primary button (accent blue fill, slide-door hover)
- [ ] Secondary button (outlined, transparent fill)
- [ ] Ghost / text link with animated underline
- [ ] Section heading + subheading component

**Page-specific:**
- [ ] Blog post layout (MDX article template with reading time)
- [ ] 404 page

---

## Responsive Behavior

| Section | Mobile (< 768px) | Tablet (768–1024px) | Desktop (> 1024px) |
|---------|------------------|---------------------|---------------------|
| Hero | Stacked — photo below text, portrait cropped square | Text left, photo right at 50/50 | Text left 40%, photo right 60%, oversized and parallax |
| Services | 1 column | 2x2 grid | 2x2 grid with more spacing |
| About teaser | Stacked, photo first | Photo left 40%, text right 60% | Photo left 45%, text right, photo slightly bleeds into prev section |
| Featured writing | 1 column, vertical | 2 columns | 3 columns horizontal |
| Testimonials | 1 card, swipe gesture | 2 cards | 3 cards side by side |
| Footer | Stacked, all 3 columns vertical | 2 columns | 3 columns |

---

## Interaction Patterns

- **Scroll behavior:** Smooth scroll — `scroll-behavior: smooth` on html element
- **Sticky elements:** Nav only — sticks to top after hero
- **Modal triggers:** No modals at launch
- **Parallax:** Hero portrait + About photo sections — scroll-driven via JS `requestAnimationFrame`
- **Carousel/slider behavior:** Testimonials on mobile — swipe gesture, no auto-play
- **Accordion behavior:** Not used at launch
- **Back to top button:** No — site is scroll-forward by design

---

## Whitespace & Density

- **Section vertical padding:** Generous — 120px desktop, 80px tablet, 60px mobile
- **Card internal padding:** Standard — 24px all sides, 32px on featured/hero cards
- **Line height (body):** Open — 1.7 for body copy, 1.1–1.2 for large display headings
- **Overall feel:** Open and airy — let the typography and photography do the work, don't fill space with decoration
