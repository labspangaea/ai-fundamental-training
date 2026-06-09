# AI Fundamental untuk Produktivitas Kerja

A four-module training series that takes a non-technical audience from *"what is AI"*
all the way to *"a 30-day plan to use AI at work"* — built as polished, on-brand 16:9
slide decks (PDF). Each module is self-contained and builds on the previous one:

> **AI → cara berkomunikasi dengan AI → AI berbasis dokumen → implementasi di pekerjaan.**

- **Audience:** staff & managers across departments (HR, Sales, Customer Service, Ops, Management) — no coding background needed.
- **Language:** Bahasa Indonesia.
- **Branding:** Pangaea Digital Labs · author Anggraeni Wisono.
- **Total:** 91 slides across 4 modules (~3.5–5 hours of material).

## The modules

| # | Module | Topic | Duration | Deck |
|---|--------|-------|----------|------|
| 1 | **AI Fundamental** | What AI/ML/GenAI/LLM are, where AI already shows up, strengths & limits, AI as a copilot | 30–45 min | [`modul-1/`](modul-1/) · 22 pp |
| 2 | **Prompt Engineering untuk Pemula** | Why prompts matter (GIGO), the Role+Task+Context+Output formula, 7 techniques, ready-to-use templates | 45–60 min | [`modul-2/`](modul-2/) · 23 pp |
| 3 | **NotebookLM & Knowledge Management** | "ChatGPT for your own documents", ChatGPT vs NotebookLM, citations, summaries/FAQ/quiz/audio, KM cycle | 60–90 min | [`modul-3/`](modul-3/) · 20 pp |
| 4 | **Implementasi AI & NotebookLM** | Spotting AI opportunities, department use-cases, one-source→many-outputs workflow, 5-stage adoption roadmap, 30-day action plan | 60–90 min | [`modul-4/`](modul-4/) · 26 pp |

Each module folder contains the deck source (`modul-N-<slug>.md`), the built PDF, and a
`diagrams/` folder of hand-written SVGs.

## Design

Warm, editorial Claude-style decks (the docsmith **`claudecode-deck`** template):
cream page, clay accent, Instrument Serif headlines. **Every chart, diagram, and icon
is hand-written raw SVG** (no Mermaid / image generation) sitting directly on the page
— summaries, comparison tables, timelines, roadmaps, KM cycles, and a consistent set
of line-icons reused across modules.

## Rebuilding a deck

Requires the [docsmith](https://github.com/) `make-pdf` plugin (provides
`scripts/build.py`, marp-cli, and the `claudecode-deck` template) plus `rsvg-convert`
and a headless Chrome.

```bash
PLUGIN=/Users/harry/projects/claude-plugins/plugins/docsmith
python3 "$PLUGIN/scripts/build.py" \
  --in  modul-1/modul-1-ai-fundamental.md \
  --out modul-1/modul-1-ai-fundamental.pdf \
  --template claudecode-deck --company "Pangaea Digital Labs"
```

Conventions for editing or adding modules (front-matter, slide classes, the
SVG/no-white-background rule, build + verify workflow) are documented in
[`CLAUDE.md`](CLAUDE.md).

---

© 2026 [Pangaea Digital Labs](https://www.pangaea.id). All rights reserved.
