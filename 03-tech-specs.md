# 03 — Technical Specs

> Use this file when scaffolding the project, setting up integrations, or making architecture decisions.
> Paste this alongside 00-master-prompt.md at the start of any technical build session.

---

## Framework & Output

- **Framework:** [HTML/CSS/JS (vanilla) / React / Next.js / Astro / Vue / Svelte / No preference]
- **Output format:** [Single HTML file / Multi-file component structure / Full project scaffold]
- **CSS approach:** [Embedded `<style>` / CSS file / Tailwind / CSS Modules / Styled Components]
- **JavaScript approach:** [Vanilla JS / TypeScript / JSX / No preference]
- **Package manager:** [npm / yarn / pnpm / None (no build step)]

---

## Hosting & Deployment

- **Hosting target:** [Vercel / Netlify / GitHub Pages / Cloudflare Pages / AWS / Other: specify]
- **Custom domain:** [Yes — [yourdomain.com] / No / Not yet]
- **CI/CD needed:** [Yes — deploy on push to main / No / Not yet]
- **Environment:** [Static only / Serverless functions needed / Full backend needed]
- **Build command (if known):** [e.g. `npm run build` / `next build` / None]

---

## Integrations

> *For each integration, specify what it does and any relevant account/config details.*

| Integration | Purpose | Notes |
|-------------|---------|-------|
| [e.g. Stripe] | [Payments] | [Test mode / Live mode / Which products] |
| [e.g. Mailchimp] | [Email list] | [Which audience ID] |
| [e.g. Supabase] | [Database / Auth] | [Project URL needed] |
| [e.g. Google Analytics] | [Analytics] | [Measurement ID: G-XXXXXXX] |
| [e.g. Calendly] | [Booking] | [Embed or link] |
| [e.g. Formspree] | [Form handling] | [Form ID: xxxxxxx] |

*Add rows as needed. Remove rows that don't apply.*

---

## Forms & Data Collection

| Form | Fields | Where Data Goes | Notes |
|------|--------|----------------|-------|
| [e.g. Contact form] | [Name, Email, Message] | [Formspree / email] | [Any validation rules] |
| [e.g. Newsletter] | [Email only] | [Mailchimp] | [Double opt-in?] |
| [e.g. Waitlist] | [Name, Email] | [Supabase table] | [Confirmation email?] |

---

## Authentication

- **Auth needed:** [Yes / No]
- **If yes — auth method:** [Email + password / Magic link / Google OAuth / GitHub OAuth / Multiple]
- **Auth provider:** [Supabase / Firebase / Auth0 / NextAuth / Clerk / Custom]
- **Protected pages/routes:** [List which pages require login]
- **User roles:** [Single role / Admin + User / Custom: describe]

---

## CMS & Content Management

- **CMS needed:** [Yes / No]
- **Who updates content:** [Developer only / Non-technical editor / Both]
- **CMS preference:** [Sanity / Contentful / Notion / Prismic / Strapi / Markdown files / None]
- **Content types managed via CMS:** [Blog posts / Team members / Products / Testimonials / All / None]
- **Localization / multi-language:** [Yes — languages: [list] / No]

---

## Performance & SEO

- **SEO priority:** [Critical (content/blog site) / Important (marketing site) / Low (internal tool)]
- **Core Web Vitals target:** [LCP < 2.5s / FID < 100ms / CLS < 0.1 — or "best effort"]
- **Lighthouse score goal:** [90+ / 80+ / Not a priority]
- **Image optimization:** [Yes — use next/image or similar / Manual / Not needed]
- **Sitemap needed:** [Yes / No]
- **Robots.txt needed:** [Yes / No]
- **Structured data / schema markup:** [Yes — type: [Article/Product/FAQ/etc] / No]

---

## Browser & Device Support

- **Minimum browser support:** [Last 2 versions / IE11 / Modern only (Chrome/Firefox/Safari/Edge)]
- **Mobile breakpoints:**
  - Mobile: [< 768px]
  - Tablet: [768px – 1024px]
  - Desktop: [> 1024px]
  - Wide: [> 1440px — optional]
- **Accessibility target:** [WCAG AA / WCAG AAA / Best effort / Not specified]
- **Dark mode support:** [System preference / Manual toggle / Light only / Dark only]

---

## Environment Variables Needed

> *List variable names only — never put actual values in this file.*

```
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
STRIPE_PUBLIC_KEY=
MAILCHIMP_API_KEY=
GOOGLE_ANALYTICS_ID=
```

*Keep actual values in `.env.local` (never commit to GitHub).*

---

## Known Constraints

> *Anything the AI must know that doesn't fit above.*

- [e.g. "Must work without JavaScript for core content (progressive enhancement)"]
- [e.g. "No external API calls on the client — proxy through serverless functions"]
- [e.g. "Bundle size must stay under 200kb"]
- [e.g. "No paid npm packages — open source only"]
