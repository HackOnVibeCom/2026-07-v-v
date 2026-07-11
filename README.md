# AppPromoKit — AI App Launch Material Generator

> Built for **HackOnVibe July 2026** (theme: promote a newly launched mobile app). Team **v-v**.

🚀 **Live demo**: https://app-promo-kit.netlify.app

## Why the demo is on Netlify (not this repo's Cloudflare Pages)
This team repo's CI/CD deploys to Cloudflare Pages, which is **static-only** — see `.github/workflows/deploy.yml`, which explicitly routes Next.js SSR / API-route apps to Vercel/Netlify. AppPromoKit is a Next.js app with a server-side API route (`/api/generate` calls the DeepSeek API), so it needs a Node server runtime. The runnable demo therefore lives on **Netlify**; this repo holds the full source code for review. The Cloudflare team URL (`https://2026-07-v-v.hackonvibe.com`) serves a landing page that redirects to the Netlify demo.

## What it does
Enter an app name + one-line positioning → get **5 channels of launch materials** in seconds: landing page copy, App Store description + ASO keywords, tweets, a Reddit post, and a cold outreach email. One-click **Export kit** downloads all channels as Markdown. Light/dark theme toggle, bilingual (EN/中文).

## AI stack
- **DeepSeek v4** (flash/pro) via OpenAI-compatible API; `response_format: json_object` for reliable structured output.
- Prompt engineering encodes real marketing knowledge per channel — ASO best practices, Twitter engagement, Reddit authenticity norms, cold-email conventions. One call → 5 channels, each tone-adapted.

## Source code
Full Next.js source is in this repo (`src/`, `package.json`, etc.).
Mirror: https://github.com/XVSHIFU/app-promo-kit

## Tech
Next.js 16 + React 19 + Tailwind 4 + TypeScript · DeepSeek v4 API · Netlify deploy.

## License
MIT
