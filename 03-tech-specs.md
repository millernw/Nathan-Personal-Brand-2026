# 03 — Technical Specs

> Use this file when scaffolding the project, setting up integrations, or making architecture decisions.
> Paste this alongside 00-master-prompt.md at the start of any technical build session.

---

## Framework & Output

- **Framework:** Next.js 14+ (App Router)
- **Output format:** Full project scaffold — pages, components, and layout files
- **CSS approach:** Tailwind CSS with custom config for brand tokens (colors, fonts, spacing)
- **JavaScript approach:** TypeScript throughout
- **Package manager:** pnpm

---

## Hosting & Deployment

- **Hosting target:** Vercel
- **Custom domain:** Yes — nathanmiller.cc
- **CI/CD needed:** Yes — deploy on push to main via Vercel GitHub integration
- **Environment:** Static pages + serverless API routes (for form handling)
- **Build command:** `pnpm build` / `next build`

---

## Integrations

| Integration | Purpose | Notes |
|-------------|---------|-------|
| HighLevel | CRM + form submission + email automation | Embed HighLevel forms or use HighLevel API to capture leads from "Work with me" and contact forms |
| Google Analytics | Analytics | GA4 — Measurement ID to be added to `.env.local` |
| Google Fonts | Typography | Instrument Serif + DM Sans — loaded via `next/font/google` |

---

## Forms & Data Collection

| Form | Fields | Where Data Goes | Notes |
|------|--------|----------------|-------|
| Work with me / Contact | First name, Last name, Email, Company, What you're working on | HighLevel CRM | Primary conversion form — on homepage and /contact |

> Use HighLevel's embed script or their API endpoint. Do NOT use a native `<form>` tag — wire the submit button to the HighLevel handler via JavaScript.

---

## Authentication

- **Auth needed:** No — public-facing site only at launch

---

## CMS & Content Management

- **CMS needed:** Yes — for blog/writing section
- **Who updates content:** Nathan (developer-comfortable, can edit markdown)
- **CMS preference:** MDX files in the repository — no external CMS at launch. Blog posts live in `/content/posts/` as `.mdx` files.
- **Content types managed:** Blog posts only at launch
- **Localization / multi-language:** No

---

## Performance & SEO

- **SEO priority:** Critical — personal brand and thought leadership site lives or dies on search presence
- **Core Web Vitals target:** LCP < 2.5s / CLS < 0.1 / INP < 200ms
- **Lighthouse score goal:** 90+ on all pages
- **Image optimization:** Yes — use `next/image` for all images. Portrait photography must be optimized and served in WebP.
- **Sitemap needed:** Yes — auto-generated via `next-sitemap` or Next.js built-in
- **Robots.txt needed:** Yes
- **Structured data / schema markup:** Yes — Person schema on home/about, Article schema on blog posts

---

## Browser & Device Support

- **Minimum browser support:** Last 2 major versions of Chrome, Firefox, Safari, Edge
- **Mobile breakpoints:**
  - Mobile: < 768px
  - Tablet: 768px – 1024px
  - Desktop: > 1024px
  - Wide: > 1440px
- **Accessibility target:** WCAG AA — proper heading hierarchy, alt text on all images, keyboard-navigable
- **Dark mode support:** Light only — no dark mode at launch

---

## Parallax & Animation Implementation Notes

> These are technical requirements that apply to every build session.

- Use CSS `transform: translateY()` driven by scroll position for parallax — do NOT use heavy JS scroll libraries
- Framer Motion is acceptable for scroll-triggered reveal animations (fade + slide-up)
- Overlapping section layers: use negative `margin-top` and `z-index` stacking, not absolute positioning hacks
- Image hover blur: `filter: blur(0)` on hover transitioning from `filter: blur(2px)` with `transition: filter 300ms ease`
- All animations must respect `prefers-reduced-motion` — wrap in a media query check

---

## Environment Variables Needed

> List variable names only — never put actual values in this file.

```
NEXT_PUBLIC_GA_MEASUREMENT_ID=
NEXT_PUBLIC_HIGHLEVEL_FORM_ID=
HIGHLEVEL_API_KEY=
NEXT_PUBLIC_SITE_URL=
```

*Keep actual values in `.env.local` — never commit to GitHub.*

---

## Known Constraints

- No paid npm packages — open source only (exception: if a Framer Motion license is needed, confirm first)
- Parallax and animation effects must degrade gracefully — core content must be accessible without JS
- Blog must support MDX — allow inline React components in posts for interactive elements later
- Do not implement a CMS admin panel — markdown files edited directly in the repo
