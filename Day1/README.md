# Agentic AI — Production · Day 1

Day 1 explains what a language model receives and returns, tokens and context in plain language, prompt anatomy, variable output, and the request/response boundary. The learner finishes with a repeatable first-call script run and prompt notes that record evidence and limits.

## Learner outcome

By the end, the learner can explain an LLM without calling it magic, identify the parts of a model request and response, write a clear prompt, run the same request again, and describe what the result proves.

## Completion evidence

- `first_call.py` runs from the course repository and prints response text, model, input tokens, output tokens, and approximate cost.
- The vague and specific prompt experiment has been run and compared.
- `lab/prompt-notes-template.md` has been completed with observed output and limits.
- No API key or private data appears in code, notes, screenshots, or Git.

## Files

- `index.html` — standalone 16:9 presentation with navigation, embedded read-aloud notes, recording mode, and print layout.
- `demo-commands.html` — from-start demo walkthrough with copyable commands and simple What/Why explanations.
- `speaker-notes.md` — word-for-word transcript in simple, everyday English.
- `recording-runbook.md` — recording preparation, exact demo sequence, safe failure, pass conditions, and publish checks.
- `presentation.pdf` — printable and shareable slide export.
- `lab/prompt-notes-template.md` — learner evidence template for the prompt experiment.

## Source material

- `ALL/Agentic-AI-40Days/phase-1-foundations/day-01/`
- `ALL/Agentic-AI-40Days/phase-1-foundations/day-01/labs/lab-1.1-first-ai-call/`
- `ALL/Agentic-AI-40Days/phase-1-foundations/day-01/labs/lab-1.2-change-the-prompt/`

Run all commands from `ALL/Agentic-AI-40Days`. Day 0 must already be complete: `.venv` exists, dependencies are installed, and the private provider key is stored only in `.env`.

## Presentation controls

- Left/Right, Page Up/Page Down, or Space: navigate.
- Home/End: first or last slide.
- **N**: show or hide the read-aloud notes.
- **R**: toggle recording mode.
- **F**: enter fullscreen.
- **P**: print or save as PDF.

Provider responses, token usage, latency, and approximate cost can vary. Check active provider documentation and account settings before recording.
