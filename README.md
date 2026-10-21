# Strategy Analysis Workbench

A strategic analysis app that installs on your computer or phone (a Progressive Web App) and works offline. There is no build step.

## What it does

| Tab | Technique | Ratings |
| --- | --- | --- |
| Assessment | Multiple-choice readiness questions, grouped by dimension | Each question has a **relevance** (High 1.0, Medium 0.6, Low 0.3, Not relevant excluded) that weights its score |
| PEST | Political, Economic, Social, Technological factors | **Impact** (1–5) × **likelihood** (1–5) × relevance weight = priority out of 25; each factor is marked opportunity, threat or neutral |
| SWOT | Strengths, Weaknesses, Opportunities, Threats | Impact × relevance weight = weight out of 5. PEST opportunities and threats can be sent straight into the SWOT |
| Strategy & TOWS | SO, ST, WO, WT strategies in a TOWS matrix | Strategic fit (mean weight of linked SWOT items) × feasibility (1–5) = strategy score out of 25, ranked in a strategic options table |
| Risk register | 5 × 5 likelihood × impact **risk rating** with heat map | Inherent and residual ratings: Low 1–4, Medium 5–9, High 10–16, Critical 17–25 |
| Overview | Dashboard | KPIs, automatic findings, heat map, PEST pressure, readiness by dimension, SWOT summary |

Threats and weaknesses from PEST and SWOT can be added to the risk register with one click.

## Data

Work is saved automatically in the browser's local storage. Under **Project & data** you can export or import JSON, copy a Markdown summary report, load the example (a coffee roaster entering the German market) or clear everything.

## Install it as an app

The app has to be served from an https address to be installable. GitHub Pages does this for free:

1. In this repository on GitHub, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to *Deploy from a branch*, pick the branch that holds `index.html` and the `/ (root)` folder, then **Save**.
3. After a minute the app is live at `https://<your-username>.github.io/<repository>/`.

Then open that address and install it:

- **Chrome or Edge (Windows, Mac, Linux, ChromeOS):** click the install icon in the address bar, or the **Install app** button in the app's header.
- **Android:** Chrome menu ⋮ → **Install app**.
- **iPhone / iPad:** Safari → **Share** → **Add to Home Screen**.

The installed app opens in its own window and keeps working offline. When you change `index.html`, bump `VERSION` in `sw.js` so installed copies pick up the update.

## Files

- `index.html`: the whole app (HTML, CSS and JavaScript)
- `manifest.webmanifest`: app name, colours and icons used when installing
- `sw.js`: service worker that caches the app for offline use
- `icons/`: app icons
