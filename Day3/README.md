# Agentic AI — Production · Day 3

Day 3 teaches the Python already visible in earlier labs: variables, strings, f-strings, functions, type hints, lists, dictionaries, loops, and conditions. Every idea is applied to the customer-review workflow instead of isolated toy code.

## Course environment

Run the labs from **Ubuntu Bash** on any supported Ubuntu host: local Ubuntu, a VM, cloud instance, WSL, or another Ubuntu environment. Use the Day 0 workspace and environment:

```bash
cd ~/src/agentic-ai-40days
source .venv/bin/activate
```

The host does not change the course commands.

## Learner outcome

By the end, the learner can read and change a small Python workflow, split work into focused functions, process a list, choose an action with `if/elif/else`, and diagnose the first useful error.

## Completion evidence

- The review sorter is organized into `classify`, `flag_if_complaint`, and `main`.
- The action function is tested locally for positive, negative, and unclear inputs.
- A loop processes a list, skips a blank item, and counts completed work.
- A learner variation adds one routing rule without changing unrelated code.
- `lab/python-evidence-template.md` records inputs, outputs, tests, failure, and fix.

## Files

- `index.html` — standalone 16:9 presentation with embedded narration.
- `demo-commands.html` — from-start demo with copyable commands and What/Why explanations.
- `speaker-notes.md` — read-aloud transcript in simple English.
- `recording-runbook.md` — preparation, demo sequence, controlled failure, and publish checks.
- `presentation.pdf` — printable 16:9 deck.
- `lab/python-evidence-template.md` — learner evidence template.

## Source material

- `ALL/Agentic-AI-40Days/phase-1-foundations/day-03/`
- `labs/lab-3.A-review-sorter-with-functions/`
- `labs/lab-3.B-loop-over-questions/`

The local Python evidence does not require a provider call. Live classification and question answering require a valid private provider key.

## Controls

Use arrows, Page Up/Page Down, Space, Home, and End to navigate. Press **N** for notes, **R** for recording mode, **F** for fullscreen, and **P** to print.
