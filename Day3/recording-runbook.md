# Day 3 recording runbook

## Ubuntu environment

Run every live command from `~/src/agentic-ai-40days` in Ubuntu Bash with the Day 0 environment active:

```bash
source .venv/bin/activate
```

Ubuntu may run locally, in a VM, in the cloud, through WSL, or on another supported host. The host does not change these commands.


## Outcome and proof

The learner can read and change the Python used in the course. Evidence includes:

- focused functions with inputs and return values;
- local decision tests for three sentiment paths;
- a batch loop that skips blank input and counts completed work;
- one controlled error, one focused fix, and a successful rerun;
- completed Python evidence notes.

## Before recording

- Work from `ALL/Agentic-AI-40Days` with `.venv` active.
- Run the Day 0 setup checker and Python compile checks.
- Open `Day3/demo-commands.html` and keep speaker notes off camera.
- Use learner copies for edits; preserve source solutions.
- Hide `.env`, credentials, account pages, and unrelated terminal history.
- Test local-only commands before testing provider-dependent scripts.

## Suggested segments

| Segment | Slides | Target | Result |
|---|---:|---:|---|
| 3.1 Variables and text | 1–5 | 10–12 min | Read names, strings, assignment, and f-strings |
| 3.2 Functions and types | 6–8 | 10–12 min | Explain inputs, return values, hints, dictionaries |
| 3.3 Lists and loops | 9–10 | 8–10 min | Process and collect many items |
| 3.4 Conditions | 11–12 | 8–10 min | Route results with if/elif/else |
| Lab 3.A | 13–16 | 15–20 min | Inspect, locally test, and optionally run sorter |
| Lab 3.B and debugging | 17–19 | 12–15 min | Skip blanks and fix one safe error |
| Completion | 20 | 3–5 min | Record evidence and limits |

## Demo order

Follow `demo-commands.html`:

1. Activate the environment and verify local imports.
2. Compile both solution scripts without calling a provider.
3. Open Lab 3.A and trace `main` into its two functions.
4. Run local tests for `flag_if_complaint`.
5. Run a local fake-classifier batch through the real loop concepts.
6. Run the live sorter only with valid provider access.
7. Inspect Lab 3.B and demonstrate blank-input skipping locally.
8. Create a learner copy, make one routing change, and record evidence.

## Controlled failure

Use a disposable learner file. A safe example is calling a misspelled function name to produce `NameError`. Read:

1. error type;
2. file and line;
3. message;
4. one hypothesis.

Correct the spelling and rerun the exact command.

## Boundaries

- A loop can multiply provider calls, cost, and latency.
- Blank and invalid inputs should be rejected before a call.
- Type hints document intent; they do not enforce all runtime behavior.
- Dictionary keys still require validated data.
- Local tests prove local logic, not provider access or classification quality.
- Never use private customer reviews in the course demo.

## Publish checklist

- [ ] 20 slides match 20 transcript sections.
- [ ] Presentation and demo controls work.
- [ ] Local compile, decision, and batch tests pass.
- [ ] Provider-dependent output is labelled honestly.
- [ ] Controlled failure uses only a learner copy.
- [ ] No secret or private data appears.
- [ ] PDF was generated and visually inspected.
