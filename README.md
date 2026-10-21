# Strategy Analysis Workbench

A single-page strategic analysis app. Open `index.html` in a browser; there is no build step and no server.

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
