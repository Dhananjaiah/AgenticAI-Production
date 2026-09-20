# Agentic AI — Production · Day 5

Day 5 moves useful work out of hard-coded prompts and into real documents. Learners build the read → validate → extract → process → write pipeline used by document tools.

## Learner outcome

By the end, the learner can read UTF-8 text, extract text from a text-based PDF, save a result safely, and explain what to do when a file is missing, too large, unsupported, unreadable, or scanned.

## Completion evidence

- Both Day 5 source scripts compile.
- The sample text file is read as UTF-8 and its size is measured.
- The sample PDF opens, reports two pages, and produces meaningful extracted text.
- A local preflight classifies supported and unsupported inputs without calling an AI provider.
- The learner records input, extraction, output, and known limits in `lab/document-evidence-template.md`.

## Files

- `index.html` — standalone 16:9 presentation with embedded narration.
- `demo-commands.html` — ordered and copyable document-ingestion walkthrough.
- `speaker-notes.md` — simple-English read-aloud transcript.
- `recording-runbook.md` — recording sequence, controlled failures, and publish checklist.
- `presentation.pdf` — printable 16:9 deck.
- `lab/document-evidence-template.md` — learner evidence template.

## Source material

- `ALL/Agentic-AI-40Days/phase-1-foundations/day-05/`
- `labs/lab-5.A-summarize-a-text-file/solution/summarize.py`
- `labs/lab-5.B-extract-from-pdf/solution/extract_points.py`

Local ingestion checks do not require an API key. Generating the AI summaries requires a valid private provider credential and may incur a small charge.

## Controls

Use arrows, Page Up/Page Down, Space, Home, and End to navigate. Press **N** for notes, **R** for recording mode, **F** for fullscreen, and **P** to print.
