# Day 5 recording runbook

## Outcome and proof

The learner can ingest text and text-based PDFs, validate inputs before processing, save results intentionally, and explain unsupported or unreadable documents. Proof includes compile checks, real local text and PDF extraction, controlled unsupported-input failures, and a completed evidence sheet.

## Before recording

- Work from `ALL/Agentic-AI-40Days` with `.venv` active.
- Open `Day5/demo-commands.html`; keep speaker notes off camera.
- Confirm the shipped `article.txt` and `it-helpdesk-handbook.pdf` exist.
- Hide private documents, provider dashboards, notifications, and terminal history.
- Use only the supplied fictional documents during recording.
- Run provider-backed summaries only with a valid private key and after confirming the content is approved.

## Suggested segments

| Segment | Slides | Target | Result |
|---|---:|---:|---|
| Pipeline and trust | 1–4 | 8–10 min | Explain the real workflow and data decision |
| Text ingestion | 5–7 | 10–12 min | Read paths and UTF-8 safely |
| PDF ingestion | 8–10 | 10–12 min | Extract text and explain OCR limits |
| Output and failures | 11–13 | 10–12 min | Bound input, write safely, classify errors |
| Labs | 14–18 | 18–22 min | Run deterministic text, PDF, and failure proof |
| Production gate | 19–20 | 5–8 min | Record boundaries and evidence |

## Demo sequence

1. Activate `.venv` from the source repository root.
2. Confirm the two supplied input files and inspect only safe metadata.
3. Compile both Day 5 solution scripts.
4. Run the local UTF-8 text preflight.
5. Run the local PDF page and extraction preflight.
6. Run the local extension and missing-path classifier.
7. Inspect output paths and explain that `"w"` replaces existing content.
8. Optionally run the two provider-backed labs.
9. Open the generated files and check that they contain meaningful output.
10. Complete the document evidence template.

## Controlled failures

Use made-up paths only. Demonstrate:

- unsupported extension → explain the allowed types;
- missing file → ask the user to check the path;
- nearly empty extraction → explain that the PDF may be scanned and require OCR.

Do not upload an unknown or private document merely to demonstrate a failure.

## Production boundaries

- Decide whether the data may leave the machine before any provider call.
- Allow only required extensions and inspect actual file content in a production upload service.
- Set byte, page, extracted-text, and model-context limits.
- Treat parsers as an untrusted-input boundary and keep packages patched.
- Scan uploads where the threat model requires it.
- Restrict output to an approved folder and prevent path traversal.
- Avoid logging document bodies, personal data, or model prompts by default.
- Keep OCR separate and measure its accuracy on the documents you support.

## Publish checklist

- [ ] 20 slides match 20 transcript sections.
- [ ] Presentation and demo controls work.
- [ ] Both source scripts compile.
- [ ] Text preflight reports a meaningful character count.
- [ ] PDF preflight reports two pages and meaningful text.
- [ ] Unsupported and missing inputs produce clear local messages.
- [ ] Live steps are labeled optional and their status is stated honestly.
- [ ] No private document or secret appears in the files or recording.
- [ ] PDF was generated and visually inspected.
