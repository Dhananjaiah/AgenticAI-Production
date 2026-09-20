# Day 1 recording runbook

## Ubuntu environment

Run every live command from `~/src/agentic-ai-40days` in Ubuntu Bash with the Day 0 environment active:

```bash
source .venv/bin/activate
```

Ubuntu may run locally, in a VM, in the cloud, through WSL, or on another supported host. The host does not change these commands.


## Outcome and evidence

The learner can explain models, tokens, context, prompts, requests, and responses, then prove understanding with:

- a successful run of the repeatable first-call script;
- observed response text, model, input tokens, output tokens, and approximate cost;
- a vague-versus-specific prompt comparison;
- completed prompt notes that state observed behavior and limits.

## Before recording

- Complete Day 0 and verify `.venv`, dependencies, editable install, and local `.env`.
- Work from `~/src/agentic-ai-40days` in Ubuntu Bash.
- Open `Day1/demo-commands.html` on the presenter screen.
- Keep `speaker-notes.md` on a non-recorded screen.
- Test both solution scripts with the selected provider immediately before recording.
- Check the current model setting, account access, usage limits, and provider pricing.
- Use no personal, customer, confidential, or production data.
- Hide notifications, account pages, billing details, terminal history, and `.env`.

## Suggested segments

| Segment | Slides | Target | Result |
|---|---:|---:|---|
| 1.1 What an LLM does | 1–6 | 12–15 min | Explain prediction, hallucination, and request/response |
| 1.2 Tokens and context | 7–8 | 8–10 min | Explain usage and working-space limits |
| 1.3 Prompt anatomy | 9–10 | 8–10 min | Turn a vague request into checkable instructions |
| Lab 1.1 First proper call | 11–15 | 15–20 min | Run and inspect response evidence |
| Lab 1.2 Prompt comparison | 16–17 | 12–15 min | Compare prompts and uncertainty instruction |
| Evidence and gate | 18–20 | 8–10 min | Record evidence, troubleshoot, and finish |

## Exact live sequence

Use `demo-commands.html`. Its commands are ordered for Ubuntu Bash and include copy buttons, reasons, pass conditions, troubleshooting, and optional cleanup.

1. Open the repository and activate `.venv`.
2. Run the Day 0 no-cost setup checker.
3. Open `first_call.py` and identify request and response fields.
4. Run `first_call.py`; read observed output and usage.
5. Run it again; compare without expecting identical wording.
6. Open and run `change_the_prompt.py`.
7. Create a learner-owned variation and change one prompt property.
8. Copy and complete `prompt-notes-template.md`.
9. Demonstrate a safe missing-import diagnosis only if prepared.

## Safe narration for variable output

Success: “The script returned meaningful text and the response fields we expected. This request path worked.”

Different wording: “The wording changed, which is normal for generated output. We will compare required properties instead of exact sentences.”

Failure: “The request did not complete. I will read the first useful error, name the failing layer, change one thing, and rerun the same command.”

## Controlled failure

Use a disposable terminal with `.venv` inactive to show an import error. Do not alter `.env` on camera and do not demonstrate failure with a visible credential.

Recovery:

```bash
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m pip install -e .
```

Rerun the same failed command and describe the evidence.

## Boundaries to say aloud

- Prompt and system content leave the local machine and go to the configured provider.
- Never send data without authorization and an approved retention policy.
- A fluent answer can be wrong.
- A system instruction can guide behavior but cannot guarantee truth.
- Token counts come from the provider response; approximate cost comes from a local table and may be stale.
- One success does not prove stable quality, privacy approval, predictable cost, or production readiness.

## Publish checklist

- [ ] All 20 slides and transcript sections match in order.
- [ ] Deck navigation, Notes, recording mode, fullscreen, copy buttons, and print layout work.
- [ ] Demo page copy buttons and What/Why explanations work.
- [ ] Both model-call labs were tested immediately before recording.
- [ ] Variable output is described honestly.
- [ ] No API key, `.env` content, private prompt, account data, or unrelated notification appears.
- [ ] Prompt notes contain evidence and limits without private data.
- [ ] PDF pages were generated and visually inspected.
