# Team 1 — Design Portfolio

ME 455 Analytical Product Design · University of Michigan
Gate Review 1: Product Definition and Market Analysis

Live site: https://osestic.github.io/design-science-portfolio/

## Working on it

Static HTML — no build step, no dependencies. Clone, open `index.html`, edit the
files directly.

```bash
git clone https://github.com/Osestic/design-science-portfolio.git
cd design-science-portfolio
python -m http.server 8000     # then open http://localhost:8000
```

Commit and push as normal; GitHub Pages redeploys from `main` within a minute.

## Pages

| File | Section |
|---|---|
| `index.html` | Introduction, product goal, section links |
| `customers.html` | Customers & benefits, journey map, contextual considerations |
| `research.html` | Market research — survey, interviews, synthesis |
| `product-definition.html` | Product definition |
| `qfd.html` | QFD matrix |
| `characteristics.html` | Characteristics & targets |
| `competition.html` | Competition analysis, design gap, positioning chart |
| `value-proposition.html` | Value proposition, risks, problem statement, recommendation |

`assets/css/site.css` holds all styling.

## Editing patterns

Classes available in the stylesheet:

- `.card`, `.grid grid-2`, `.grid grid-3` — content blocks
- `.stat` with `.stat-value` / `.stat-label` / `.stat-source` — headline numbers
- `.badge badge-survey | badge-interview | badge-benchmark | badge-qfd | badge-assumption`
- `.callout callout-limit` — stated limitation
- `.table-wrap` around every table; add class `qfd` for the rotated-header matrix
- `figure` + `figcaption`, captioned `<b>Figure n.</b>`

Charts are inline SVG. Series colours are `--series-1` … `--series-5`.

## Source documents

Survey responses, interview write-ups, the journey map and the QFD workbook are kept
in a local `Resources/` folder that is **not tracked by git** — the survey involves
human participants and this repository is public. Keep it that way.

## Submitting

Paste the live URL into the Canvas box. Check the site on a phone first; the QFD
table scrolls horizontally.
