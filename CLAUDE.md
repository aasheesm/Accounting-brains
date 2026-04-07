# Accounting-Brains — Marketing Website + Content Engine

## Purpose
Marketing website for outsourced accounting firm serving US, Canada, UAE, and Australia markets. Also includes LinkedIn carousel content pipeline.

## Stack
- **SSG:** Eleventy (11ty)
- **CSS:** Tailwind CSS
- **CMS:** Decap CMS (git-based)
- **Email:** Brevo
- **Workers:** Cloudflare Workers (forms, OAuth)
- **AI:** OpenRouter (blog generation), SERP API, Hunter.io

## ⚠️ Unactivated Paid Integrations (Never Used)
The following scripts are fully coded but have NO `.env` file configured — they have never run and are not currently active. All are paid services:

| Integration | Script | Purpose | Cost |
|---|---|---|---|
| **OpenRouter** | `scripts/generate-blog.js` | AI blog post generation via Claude 3.5 Sonnet | Pay-per-token (~$3–15/M tokens) |
| **SERP API** (serpapi.com) | `scripts/scrape-leads.js` | Google search scraping to find business leads | Free: 100/mo → $50+/mo |
| **Hunter.io** | `scripts/scrape-leads.js` | Email discovery from company domains | Free: 25/mo → $49+/mo |
| **Bland.ai** | `scripts/ai-calling.js` | AI outbound calling to leads (code commented out) | ~$0.09/min per call |

**Status:** Built as a future lead-generation pipeline. Before activating, create a real `.env` from `.env.example` and add API keys. Review costs carefully — running the full pipeline (SERP → Hunter → OpenRouter → Bland) incurs charges on all four services.

## Running
```bash
npm run dev          # Local dev server
npm run build        # Production build
```

## Structure
```
src/                 11ty source (templates, data, content)
brands/              Brand-specific carousel configs (see marketing-engine)
cloudflare/          Workers for form handling and OAuth
```

## Key Features
- **Multi-country SEO** — areaServed schema for US/Canada/UAE/Australia
- **Lead capture** — email gating on downloadable resources
- **AI blog pipeline** — auto-generates posts via OpenRouter
- **Git-based CMS** — editors use Decap CMS on GitHub, no server needed
- **27 LinkedIn carousels** — generated via marketing-engine

## Deployment
Deployed to GitHub Pages. Push to main = auto-deploy via GitHub Actions.

## Integrations
- Brevo for transactional email
- Cloudflare Workers for serverless form handling
- Hunter.io for email verification
- Bland.ai for voice demo (if configured)

## Vault Patterns (reference before building new features)
- **SSG:** `vault/patterns/eleventy-static-site-architecture.md` — 11ty setup
- **CMS:** `vault/patterns/decap-cms-git-based.md` — Decap CMS + GitHub
- **Forms:** `vault/patterns/cloudflare-worker-form-handler.md` — Cloudflare Workers
- **Leads:** `vault/patterns/lead-capture-email-gate.md` — email gating
- **AI Blog:** `vault/patterns/ai-blog-generation-pipeline.md` — blog generation
- **SEO:** `vault/patterns/seo-meta-schema-org.md` — SEO + schema.org
- **GDPR:** `vault/patterns/cookie-consent-gdpr.md` — cookie consent
