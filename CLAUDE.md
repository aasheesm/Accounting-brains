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
