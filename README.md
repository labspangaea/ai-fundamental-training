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

The decks are built with the **docsmith** plugin — its `claudecode-deck` template,
`scripts/build.py`, and marp-cli — distributed through the
**[Pangaea Labs plugin marketplace](https://github.com/labspangaea/pangaealabs-claude-plugins-marketplace)**.
You also need `rsvg-convert` and a headless Chrome on `PATH`.

Add the marketplace and install the plugin once (from the Claude Code REPL):

```
/plugin marketplace add labspangaea/pangaealabs-claude-plugins-marketplace
/plugin install docsmith@pangaealabs-claude-plugins-marketplace
```

**Recommended — let the `/make-pdf` skill rebuild it** (portable, no paths to manage):

```
/make-pdf rebuild modul-1/modul-1-ai-fundamental.md as a claudecode-deck for Pangaea Digital Labs
```

Conventions for editing or adding modules (front-matter, slide classes, the
SVG/no-white-background rule, build + verify workflow) are documented in
[`CLAUDE.md`](CLAUDE.md).

---

Decks rendered with [docsmith](https://github.com/labspangaea/pangaealabs-claude-plugins-marketplace)'s `/make-pdf`.

© 2026 [Pangaea Digital Labs](https://www.pangaea.id). All rights reserved.
