# Day 2 recording runbook

## Outcome and proof

The learner builds a structured customer-review sorter and can explain the safety pipeline:

1. Request an exact output contract.
2. Parse JSON text into data.
3. Validate fields and allowed values.
4. Retry malformed output within a fixed limit.
5. Return a flagged fallback for human review.

Proof includes a live sorter run when provider access works and a deterministic local test that rejects known malformed records.

## Before recording

- Work from `ALL/Agentic-AI-40Days`.
- Activate `.venv` and run the Day 0 setup checker.
- Confirm Pydantic and `shared.llm` import.
- Test both solution scripts immediately before recording.
- Open `Day2/demo-commands.html`; keep speaker notes off the captured screen.
- Hide `.env`, account pages, keys, customer data, and unrelated terminal history.
- Use only the fictional reviews included in the lab.
- Check provider model access, current prices, account limits, and retention rules.

## Suggested segments

| Segment | Slides | Target | Result |
|---|---:|---:|---|
| 2.1 Why structure matters | 1–4 | 8–10 min | Explain why paragraphs are hard for software |
| 2.2 System instructions | 5–6 | 8–10 min | Use role, task, rules, unsure, format |
| 2.3 JSON and parsing | 7–9 | 10–12 min | Explain filled-in forms and parsing limits |
| Lab 2.1 Structured sorter | 10–14 | 15–20 min | Produce and inspect structured review rows |
| Lab 2.2 Reliability | 15–18 | 15–20 min | Validate, retry, fallback, force bad data |
| Boundaries and gate | 19–20 | 6–8 min | State limits and record evidence |

## Exact demo sequence

Use `demo-commands.html` in order:

1. Activate the Day 0 environment and run the no-cost gate.
2. Prove local imports and inspect both solution files.
3. Run the structured review sorter if provider authentication works.
4. Run the reliable sorter if provider authentication works.
5. Run the deterministic malformed-data validation separately. This must work without a model call.
6. Run a deterministic fallback simulation without a model call.
7. Copy and complete the evidence template.

## Safe live wording

Success: “The response parsed, passed the schema, and produced the expected fields. This does not prove every classification is correct.”

Provider unavailable: “The external call did not complete. I will name the provider error and continue with the local validation proof.”

Malformed data: “Validation rejected this record before normal business logic used it. The error identifies the field and rule.”

Fallback: “Every allowed attempt failed, so the program returned a clearly marked result for human review.”

## Controlled failure

Use the included broken dictionaries. Do not corrupt `.env` and do not wait for random model failure.

Known failures:

- `sentiment="ecstatic"` violates the allowed-value rule.
- A missing `summary` violates the required-field rule.

## Production boundaries

- Validate all model output at the trust boundary.
- Put a fixed limit on retries; add timeouts, backoff, and rate-limit awareness in production.
- Do not retry permanent authentication or permission failures.
- A fallback must be visible and owned; do not silently treat it as a real classification.
- Schema validity does not prove semantic accuracy.
- Customer reviews may contain personal data; use authorized, minimized input and approved provider handling.
- Cost estimates are approximate and provider-dependent.

## Publish checklist

- [ ] 20 slides and 20 transcript sections match.
- [ ] Presentation controls, notes, recording mode, print layout, and PDF work.
- [ ] Every demo command has Copy, What, Why, and expected evidence.
- [ ] Local validation and fallback simulations pass.
- [ ] Live provider output is labelled observed only when it actually ran.
- [ ] No credentials, private customer data, or account details appear.
- [ ] PDF pages were generated and visually inspected.
