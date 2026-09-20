# Agentic AI — Production

This is the production version of the 40-day Agentic AI course. It is designed as a complete Udemy learning journey, not a collection of unrelated slides.

The learner starts with no assumed AI engineering experience. By the end, the learner should be able to design, build, evaluate, secure, deploy, observe, operate, and clearly explain an AI-agent system.

## Start here

1. Read [`COURSE-CONTENT.md`](COURSE-CONTENT.md) for the complete Day 0–40 curriculum and current build status.
2. Read [`COURSE-DESIGN-STANDARD.md`](COURSE-DESIGN-STANDARD.md) before creating or changing any day.
3. Read [`AI-HANDOFF.md`](AI-HANDOFF.md) when continuing this work in another AI session or model.
4. Use [`DAY-BUILD-CHECKLIST.md`](DAY-BUILD-CHECKLIST.md) while building and reviewing each day.

## Current structure

```text
Agentic AI - Production/
├── README.md
├── COURSE-CONTENT.md
├── COURSE-DESIGN-STANDARD.md
├── DAY-BUILD-CHECKLIST.md
├── AI-HANDOFF.md
└── Day0/
    ├── README.md
    ├── index.html
    ├── demo-commands.html
    ├── presentation.pdf
    ├── speaker-notes.md
    └── recording-runbook.md
```

Every completed day with a live demo should use the same six-file learner/instructor package as `Day0`, including `demo-commands.html`. Temporary generators, verification scripts, browser previews, caches, and scratch files should be removed after final verification.

## Current status

| Day | Topic | Status |
|---:|---|---|
| 0 | Setup, expectations, course map, and first AI reply | Complete |
| 1 | Meet the LLM | Content complete; live API check pending |
| 2 | Reliable outputs | Content complete; local reliability proof passed; live API check pending |
| 3 | Just-enough Python | Content complete; local Python proof passed; live API check pending |
| 4 | APIs, secrets, and failures | Content complete; local API-error proof passed; live API check pending |
| 5 | Files and document ingestion | Content complete; local text/PDF ingestion proof passed; live API check pending |
| 6–40 | See `COURSE-CONTENT.md` | Planned |

## Source material

The detailed source curriculum currently lives in:

- `ALL/Agentic-AI-40Days/PRODUCTION-READY-COURSE-TOC.md`
- `ALL/Agentic-AI-40Days/COURSE-OUTLINE.md`
- Existing lessons under `ALL/Agentic-AI-40Days/`

Those files provide technical source material. This folder is the polished, recording-ready course. New work should preserve useful source content while improving its teaching flow, production depth, transcript quality, and visual consistency.
