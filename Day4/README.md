# Agentic AI — Production · Day 4

Day 4 opens the API boundary. Learners inspect what leaves the program, what returns, how secrets grant access, how status codes describe failures, and when retrying is safe.

## Learner outcome

By the end, the learner can inspect a request and response, keep credentials out of code, classify common failure layers, translate technical errors into useful actions, and distinguish retryable failures from failures that require a real fix.

## Completion evidence

- Both Day 4 source scripts compile.
- The error translator returns correct guidance for 400, 401, 403, 429, 500, connection, and unknown cases.
- A simulated failing provider call is caught and the program continues.
- Retry decisions are documented with an idempotency check.
- `lab/api-evidence-template.md` records request fields, response fields, error category, action, and limits.

## Files

- `index.html` — standalone 16:9 presentation with embedded narration.
- `demo-commands.html` — ordered, copyable API and failure walkthrough.
- `speaker-notes.md` — simple-English read-aloud transcript.
- `recording-runbook.md` — recording sequence, safe failure, and publish checklist.
- `presentation.pdf` — printable 16:9 deck.
- `lab/api-evidence-template.md` — learner evidence template.

## Source material

- `ALL/Agentic-AI-40Days/phase-1-foundations/day-04/`
- `labs/lab-4.A-read-a-response/solution/read_response.py`
- `labs/lab-4.B-handle-an-error/solution/handle_error.py`

The local error-handling proof does not require a real API key. A live response inspection does.

## Controls

Use arrows, Page Up/Page Down, Space, Home, and End to navigate. Press **N** for notes, **R** for recording mode, **F** for fullscreen, and **P** to print.
