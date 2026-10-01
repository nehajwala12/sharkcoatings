# Shark Coatings Diagnostic Demo — Vercel deployment

A static, single-page site: `index.html` carries all styles, scripts and data; fonts load from Google Fonts. No build step, no framework, no environment variables.

## Deploy (either way)

**Dashboard:** vercel.com → Add New → Project → drag this folder in (or import it from a Git repository) → Framework preset **Other** → leave Build Command and Output Directory empty → Deploy.

**CLI:**
```
npm i -g vercel
cd shark-diagnostic
vercel deploy --prod
```

## Before sharing with the board
- Turn on **Deployment Protection** (Project → Settings → Deployment Protection → Password Protection or Vercel Authentication). The page is marked noindex, but a URL alone is not access control.
- Optional: add a custom domain under Project → Settings → Domains.

## What is in the page
- 16 tabs; 340 exhibits; every exhibit is labelled **Public data**, **Illustrative data** or **Public + illustrative**, and each tab shows its own data key under the headline.
- 47 interactive exhibits (marked **Interactive**): controls re-compute the chart and a readout line states the result.
- Deep links: `/#pricing`, `/#monitor/wm-board` etc. Print (top right) expands every tab with final chart states.

## Data notice
Company figures are illustrative, calibrated to public anchors and to context shared by management; they are replaced by actual figures in week one of the diagnostic. Public figures cite their source and date on each exhibit.

## Updating
Replace `index.html` with a newer build and redeploy (`vercel deploy --prod`). Vercel keeps every previous deployment for instant rollback.
