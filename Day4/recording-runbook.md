# Day 4 recording runbook

## Ubuntu environment

Run every live command from `~/src/agentic-ai-40days` in Ubuntu Bash with the Day 0 environment active:

```bash
source .venv/bin/activate
```

Ubuntu may run locally, in a VM, in the cloud, through WSL, or on another supported host. The host does not change these commands.


## Outcome and proof

The learner can inspect the API boundary and handle failure by evidence. Proof includes successful compile checks, deterministic status-code translation, a locally simulated provider failure that does not crash, and a written retry/idempotency decision.

## Before recording

- Work from `ALL/Agentic-AI-40Days` with `.venv` active.
- Open `Day4/demo-commands.html`; keep speaker notes off camera.
- Verify `.env` is ignored without displaying its contents.
- Hide provider dashboards, account identifiers, notifications, and terminal history.
- Use fake exception objects for failure demonstrations.
- Test live provider calls only with a valid private key and harmless prompt.

## Suggested segments

| Segment | Slides | Target | Result |
|---|---:|---:|---|
| API boundary | 1–5 | 12–15 min | Explain requests, responses, headers, and bodies |
| Secret handling | 6–7 | 8–10 min | Protect and rotate credentials |
| Reading responses | 8–9 | 8–10 min | Interpret content, usage, limits, and cost |
| Failure decisions | 10–14 | 15–18 min | Classify errors, backoff, and idempotency |
| Labs | 15–18 | 15–20 min | Inspect response and test error handler |
| Boundaries and gate | 19–20 | 5–8 min | Record evidence and limits |

## Demo sequence

1. Activate `.venv`, run the setup gate, and prove `.env` is ignored.
2. Compile both Day 4 scripts.
3. Inspect Lab 4.A request and response fields.
4. Run Lab 4.A only when provider authentication works.
5. Inspect Lab 4.B’s translator and wrapper.
6. Run deterministic fake status-code tests.
7. Replace the provider function in memory with a local exception and prove `safe_ask` returns normally.
8. Complete the API evidence template.

## Controlled failure

Use fake error objects. Do not alter or display the real key. The test must cover:

- 400: fix request;
- 401: fix or rotate key;
- 403: fix permission/model access;
- 429: bounded retry with backoff;
- 500: bounded retry and provider status check;
- unknown: safe generic message and technical logging.

## Production boundaries

- Set connect and response timeouts.
- Retry only temporary failures and only within a fixed budget.
- Add jitter to backoff in concurrent systems.
- Do not retry non-idempotent side effects without duplicate prevention.
- Redact authorization headers, keys, private prompts, and personal data.
- Separate user-safe messages from restricted technical logs.
- Track retry rate, error category, latency, and fallback usage.

## Publish checklist

- [ ] 20 slides match 20 transcript sections.
- [ ] Presentation and demo controls work.
- [ ] Both source scripts compile.
- [ ] All deterministic error cases pass.
- [ ] The simulated outside failure is caught without a crash.
- [ ] No secret value appears in files or recording.
- [ ] PDF was generated and visually inspected.
