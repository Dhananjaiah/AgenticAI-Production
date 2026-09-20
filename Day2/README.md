# Agentic AI — Production · Day 2

Day 2 turns model text into data that software can safely inspect. Learners build a customer-review sorter with a five-part system instruction, JSON parsing, schema validation, bounded retries, and a safe fallback.

## Course environment

Run the labs from **Ubuntu Bash** on any supported Ubuntu host: local Ubuntu, a VM, cloud instance, WSL, or another Ubuntu environment. Use the Day 0 workspace and environment:

```bash
cd ~/src/agentic-ai-40days
source .venv/bin/activate
```

The host does not change the course commands.

## Learner outcome

By the end, the learner can request a predictable output shape, parse it, validate every field, retry a malformed result a limited number of times, and return a clearly flagged fallback instead of crashing or trusting bad data.

## Completion evidence

- The review sorter turns five free-text reviews into structured rows.
- The reliable sorter validates sentiment, topic, and summary before use.
- Deliberately malformed examples are rejected with clear reasons.
- Retry count is bounded and the fallback is marked for human review.
- `lab/reliability-evidence-template.md` records the observed happy path, forced failure, fallback, usage, and limits.

## Files

- `index.html` — standalone 16:9 presentation with embedded narration and recording controls.
- `demo-commands.html` — ordered demo commands with Copy buttons, What/Why explanations, checkpoints, and troubleshooting.
- `speaker-notes.md` — simple-English, read-aloud transcript.
- `recording-runbook.md` — recording sequence, safe failure, output guidance, and publish checks.
- `presentation.pdf` — printable and shareable deck.
- `lab/reliability-evidence-template.md` — learner evidence template.

## Source material

- `ALL/Agentic-AI-40Days/phase-1-foundations/day-02/`
- `labs/lab-2.1-review-sorter/solution/review_sorter.py`
- `labs/lab-2.2-validation-retries-fallback/solution/reliable_sorter.py`

Run commands from `ALL/Agentic-AI-40Days`. Day 0 setup must pass. Live classification also requires a valid configured provider key.

## Presentation controls

- Left/Right, Page Up/Page Down, or Space: navigate.
- Home/End: first or last slide.
- **N**: show or hide notes.
- **R**: recording mode.
- **F**: fullscreen.
- **P**: print or save as PDF.

Generated labels and summaries can vary. Validation proves that data matches the declared schema; it does not prove that each classification is correct.
