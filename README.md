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

Navigation follows the course template: **Home** (the introduction), one dropdown per
gate review, and **Team**. Gate Review 1 sits under *Customer & Market Research*; later
phases (Concept, Development, Business Plan) are greyed placeholders in the nav and on
the home page until their pages exist.

| File | Section |
|---|---|
| `index.html` | Home: introduction, product goal, links to every section |
| `customers.html` | GR1 · Customers & benefits, journey map, contextual considerations |
| `research.html` | GR1 · Market research: survey, interviews, synthesis |
| `product-definition.html` | GR1 · Product definition, House of Quality (`#qfd`), characteristics & targets (`#targets`) |
| `competition.html` | GR1 · Competition analysis, design gap, positioning chart |
| `value-proposition.html` | GR1 · Value proposition, risks, problem statement, recommendation |
| `team.html` | Team members and roles |

`qfd.html` and `characteristics.html` only redirect to the matching anchors on
`product-definition.html`, so old links keep working.

To add a phase: create its pages, then in every page's `<header class="nav">` replace that
phase's `<span class="nav-soon">` with a `has-menu` dropdown like the Gate Review 1 one.

`assets/css/site.css` holds all styling.

## Editing patterns

Classes available in the stylesheet:

- `.card`, `.grid grid-2`, `.grid grid-3` — content blocks
- `.stat` with `.stat-value` / `.stat-label` / `.stat-source` — headline numbers
- `.badge badge-survey | badge-interview | badge-benchmark | badge-qfd | badge-assumption`
- `.callout callout-limit` — stated limitation
- `.table-wrap` around every table; add class `qfd` for the rotated-header matrix
- `figure` + `figcaption`, captioned `<b>Figure n.</b>`
- Citations: give each reference `<li id="ref-N">[N] …</li>` and cite it in the text as
  `<a class="cite" href="#ref-N">[N]</a>`

Charts are inline SVG. Series colours are `--series-1` … `--series-5`.

## Source documents

Survey responses, interview write-ups, the journey map and the QFD workbook are kept
in a local `Resources/` folder that is **not tracked by git** — the survey involves
human participants and this repository is public. Keep it that way.

## Submitting

Paste the live URL into the Canvas box. Check the site on a phone first; the QFD
table scrolls horizontally.
