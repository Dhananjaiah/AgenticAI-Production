# Day 0 recording runbook

## Outcome

The learner finishes with evidence that:

- Python 3.11 or newer runs in a new terminal.
- VS Code opens the course repository.
- `.venv` is active and dependencies are installed.
- `.env` contains the selected provider credential and Git ignores it.
- The setup checker passes without making a model call.
- The Hello AI script returns generated text plus usage information.
- The learner can explain the secret, data, cost, and network boundaries.

## Before recording

- Work from the `ALL/Agentic-AI-40Days` repository root for live commands.
- Test every command immediately before recording.
- Confirm the Python version supported by the repository and the current dependency pins.
- Verify the chosen provider key, model, account credits or billing, usage limits, and current pricing.
- Turn off notifications and hide private browser tabs, account details, emails, and unrelated terminal history.
- Enlarge terminal and editor fonts.
- Keep `speaker-notes.md` on a non-recorded screen.
- Prepare a fake `.env.example` value for explanation. Never display the real `.env` file.
- Use a harmless prompt with no personal, confidential, or production data.

If a real key is accidentally recorded, stop, revoke it immediately, create a replacement, and remove the exposed recording segment. Editing the visible text does not remove copies from terminal history, Git history, logs, or an uploaded recording.

## Suggested recording segments

| Segment | Slides | Target | Learner outcome |
|---|---:|---:|---|
| 0.1 Welcome and course map | 1–3 | 10–12 min | Understand the finish line and production journey |
| 0.2 Agentic AI mental model | 4–5 | 10–12 min | Explain model, tools, state, loop, and when an agent is appropriate |
| 0.3 Toolkit | 6–7 | 8–10 min | Understand each local tool and evidence-based checks |
| Lab 0.5a Install tools | 8–9 | 12–15 min | Python version works and VS Code opens the repository |
| 0.4 API-key safety | 10–12 | 10–12 min | Explain `.env.example`, `.env`, Git ignore, data, and cost boundaries |
| Lab 0.5b Project setup | 13–16 | 15–20 min | `.venv`, packages, local config, and setup gate work |
| Lab 0.5c First AI call | 17–20 | 15–20 min | Run and vary one real model request |
| 0.6 Troubleshooting and gate | 21–27 | 12–15 min | Diagnose by layer and prove Day 0 completion |

Long installation waits should be edited or time-compressed. Do not conceal errors that materially change the instructions.

## Live terminal sequence

Run from `ALL/Agentic-AI-40Days`.

Open `demo-commands.html` as the command-by-command recording companion. It contains the same run order, a Copy button for every command block, simple What/Why explanations, pass conditions, troubleshooting, and operating-system differences.

### Verify Python

```text
python --version
```

On macOS or Linux, use `python3 --version` if `python` is unavailable. The course requires Python 3.11 or newer.

### Create and activate the virtual environment

Windows PowerShell:

```text
python -m venv .venv
.venv\Scripts\Activate.ps1
```

macOS or Linux:

```text
python3 -m venv .venv
source .venv/bin/activate
```

### Install dependencies

```text
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m pip install -e .
```

### Create local configuration

Windows:

```text
copy .env.example .env
```

macOS or Linux:

```text
cp .env.example .env
```

Stop screen capture before adding a real credential. Resume after closing the file, then verify the ignore rule:

```text
git check-ignore -v .env
```

Do not continue if this command produces no matching ignore rule.

### Run the no-cost setup check

```text
python phase-0-get-ready/day-00/labs/lab-0.5b-setup-project/solution/check_setup.py
```

Read the actual output. This verifies environment and key presence; it does not authenticate with the provider.

### Run the first model call

```text
python phase-0-get-ready/day-00/labs/lab-0.5c-hello-ai/solution/hello_ai.py
```

This command contacts the configured provider and may incur model usage. Verify a meaningful response and the usage metadata. Generated wording varies.

### Learner variation

Change only the prompt to:

```text
Explain an API key to a ten-year-old in two sentences.
```

Predict the effect, run once, and compare content, constraint-following, and token usage.

## Controlled troubleshooting demonstration

Choose one safe failure:

- Run the version command in an environment where Python is not on PATH, then explain the layer and fix.
- Use an inactive virtual environment to demonstrate an import failure, activate `.venv`, and rerun.
- Temporarily use a blank placeholder in a disposable local configuration to show the missing-key check, then restore the private configuration off-camera.

Never demonstrate an authentication failure with a real credential visible. Never intentionally commit a real or fake key that resembles an active credential.

Use this narration pattern:

1. Read the first useful error line.
2. Name the failing layer.
3. State one hypothesis.
4. Change one thing.
5. Rerun the same check.
6. Describe the observed evidence.

## Recording standards

- Show the finished result before a lab.
- Explain a command before executing it.
- Keep long provider or package output brief; focus on the first relevant error or final proof.
- Label illustrative slide output as illustrative and live output as observed.
- Never promise an exact generated sentence, token count, latency, or cost.
- Do not call the system production-ready after one successful request. State exactly what the check proves.
- Give visible pause points so learners can match results locally.

## Publish checklist

- [ ] The deck, notes, links, copy buttons, readiness gate, fullscreen, and PDF export work.
- [ ] Commands match the current repository paths and dependency setup.
- [ ] The setup checker passes on a clean supported environment.
- [ ] The selected provider call succeeds and prints usage information.
- [ ] No credential, private email, account ID, billing detail, or unrelated notification appears.
- [ ] Captions distinguish `.env.example` from `.env` and model call from agent.
- [ ] Provider pricing and model references were checked immediately before publication.
- [ ] The downloadable resources include the deck, transcript, runbook, and existing lab materials.
