# CLAUDE.md — AI Fundamental training-deck series

This repo holds a 4-module training-deck series ("AI Fundamental untuk Produktivitas
Kerja"). Each module is a self-contained slide deck rendered to PDF with the
**docsmith `make-pdf`** system using the **`claudecode-deck`** template. docsmith
ships from the [pangaealabs marketplace](https://github.com/labspangaea/pangaealabs-claude-plugins-marketplace)
— install it with `/plugin install docsmith@pangaealabs-claude-plugins-marketplace`.
When asked to add a module, fix a slide, or build a similar deck, follow the
conventions below so every module stays visually consistent.

## Layout — one folder per module, everything co-located
```
modul-N/
├── modul-N-<slug>.md        # the deck source (markdown + front-matter)
├── diagrams/                # every visual as a hand-written .svg (+ reused icons)
└── modul-N-<slug>.pdf       # the built deck
```
SVGs are embedded by **absolute path**, so keep the source, `diagrams/`, and PDF in
the same folder — moving a module means rewriting every SVG path.

## Front-matter (every module)
```yaml
---
template: claudecode-deck
title: "<Module title>"
subtitle: "Modul N"
author: "Anggraeni Wisono"      # overrides the profile → flows into the deck footer
date: auto
version: "v1.0"
---
```
Brand/company is **"Pangaea Digital Labs"**, passed at build time via `--company`
(NOT in front-matter). The footer auto-composes to `logo · Pangaea Digital Labs ·
Anggraeni Wisono · © 2026`.

## Build + verify
```bash
PLUGIN=/Users/harry/projects/pangaealabs-claude-plugins-marketplace/plugins/docsmith
python3 "$PLUGIN/scripts/build.py" \
  --in  modul-N/modul-N-<slug>.md \
  --out modul-N/modul-N-<slug>.pdf \
  --template claudecode-deck --company "Pangaea Digital Labs"
```
After building, **render the diagram-heavy pages and eyeball them**:
`pdftoppm -png -r 80 -f <page> -l <page> <pdf> /tmp/check` then view the PNG.
Confirm: every SVG actually appears (a size-less SVG silently collapses), no card
grid overflows into the footer, and the footer + page number sit on one line.

## Visuals — ALL hand-written raw SVG (no Mermaid / d2 / image-gen / R2)
Charts, diagrams, illustrations, and UI icons are plain XML (`<rect> <line> <text>
<path> <polygon> <circle>`) with manual coordinates. Rules:
- **No white background.** Figures sit directly on the cream wash — never paint a
  white `<rect>` background. Fill shapes with the palette tokens below; use
  `#FFFFFF` only for text/marks *on* clay/dark fills. Strokes give definition.
- **Explicit `width` AND `height`** on the root `<svg>` (not just a `viewBox`), or
  Chrome collapses the embedded `<img>` to nothing.
- **Validate before embedding:** `rsvg-convert -f pdf -o /tmp/x.pdf <file>.svg`.
- **Embed by absolute path:** `![caption](/Users/harry/project/ai-fundamental/modul-N/diagrams/x.svg)`.
- **Reuse icons across modules** (copy into the module's `diagrams/`): role icons
  `ic-hr/ic-sales/ic-cs/ic-ops/ic-marketing/ic-email` (modul-1), technique/concept
  icons in modul-2/3/4. UI icons are ~64×64, clay stroke, peach/surface fills,
  transparent ground.

### Palette (claudecode-deck warm editorial)
clay `#B85838` (primary) · clay-soft `#D8896B` · peach `#F5E6DA` · ink `#262620` ·
ink-2 `#54514A` · surface `#F7F6EF` · hairline `#E2E0D6` · espresso `#262218` ·
success `#2F7D4F` · error `#B5443B`. Page background is cream `#F0EEE6`.

## Slide classes (`<!-- _class: NAME -->`, one per slide, slides split by `---`)
Shared: `cover · agenda · statement · quote · closing · kpi · bigstat · pillars`
(2-col; good for 2 cards or 4 as 2×2) · `cards3` (3-col) · `compare2 · filegrid`
(4-col) · `versus · steps · people · split`.
Custom (this series leans on these):
- **`stack`** — heading + ONE large centered figure on top + an optional caption or
  `> callout` below. Use for wide diagrams/timelines/flows/roadmaps.
- **`iconcards`** — each list item `- ![](/abs/ic.svg) **Title** desc` becomes a
  card with the icon pinned left and title/desc stacked. Default 3-up; add `cols2`
  for 2-up. **Max 6 items** (3×2) or it overflows into the footer; for 4 items use
  `cols2`.
- **`procon`** — exactly 2 cards: first tinted success-green, last error-red. For
  ✅ vs ❌ / before–after / do–don't.
- **Callout** — a `> line` on any non-`quote` slide renders as a clay-spined peach
  pill (lift a takeaway out of the body).

### Authoring gotchas
- Eyebrow `###### EYEBROW`; headline `# Text with *accent*` (the `*accent*` becomes
  clay italic). Always put a **blank line before every list**.
- Markdown `[placeholder]` text renders literally (fine for prompt templates).
- Card grids with long text overflow vertically — keep card copy to 1–3 short lines.
- Roadmap convention: each module ends with a `roadmap-mN.svg` showing the 4-station
  path with completed modules in surface+✓ and the current module highlighted clay.

## Don't edit the template from here
The `claudecode-deck` theme/classes live in the docsmith plugin
(`/Users/harry/projects/pangaealabs-claude-plugins-marketplace/plugins/docsmith/...`),
which ships from the [pangaealabs marketplace](https://github.com/labspangaea/pangaealabs-claude-plugins-marketplace)
(`/plugin install docsmith@pangaealabs-claude-plugins-marketplace`) and is a separate
repo. Only change it deliberately (a genuine template improvement that should apply to
every deck) — routine module work only touches files under `modul-N/`.
