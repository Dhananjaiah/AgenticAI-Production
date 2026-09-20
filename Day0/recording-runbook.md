# Day 0 recording runbook ? Ubuntu environment

## Environment standard

This course is **Ubuntu-first**. The learner may use Ubuntu on a local computer, a local VM, a cloud VM such as AWS EC2 or Oracle Cloud, WSL, or another supported Ubuntu host. The hosting method does not change the course commands.

- Canonical shell: Ubuntu Bash.
- Canonical repository location: `~/src/agentic-ai-40days`.
- Canonical environment activation: `source .venv/bin/activate`.
- The repository and `.venv` live in the Ubuntu home directory.
- VS Code is optional but recommended. Use a local, Remote SSH, Remote Tunnels, or WSL connection as appropriate for the learner?s host.

## Outcome

The learner finishes with evidence that:

- Ubuntu shell access works and Python 3.11 or newer runs.
- The course repository is under `~/src/agentic-ai-40days`.
- VS Code or another editor can open the Ubuntu-hosted repository.
- `.venv` is active and dependencies are installed.
- `.env` contains the selected provider credential and Git ignores it.
- The setup checker passes without making a model call.
- The Hello AI script returns generated text plus usage information.
- The learner can explain secret, data, cost, network, and host boundaries.

## Before recording

- Work from `~/src/agentic-ai-40days` in an Ubuntu terminal for all live course commands.
- State the host only when useful for the audience, for example local Ubuntu, a VM, cloud instance, or WSL. Do not make it a prerequisite for the lesson.
- Confirm the repository?s supported Python version and current dependency pins.
- Verify the chosen provider key, model, account credits or billing, usage limits, and current pricing.
- Confirm the editor opens the Ubuntu repository using the connection appropriate to that host.
- Turn off notifications and hide private browser tabs, account details, emails, and unrelated terminal history.
- Enlarge terminal and editor fonts.
- Keep `speaker-notes.md` on a non-recorded screen.
- Prepare a fake `.env.example` value for explanation. Never display the real `.env` file.
- Use a harmless prompt with no personal, confidential, or production data.

If a real key is accidentally recorded, stop, revoke it immediately, create a replacement, and remove the exposed recording segment. Editing visible text does not remove copies from terminal history, Git history, logs, or an uploaded recording.

## Suggested recording segments

| Segment | Slides | Target | Learner outcome |
|---|---:|---:|---|
| 0.1 Welcome and course map | 1?3 | 10?12 min | Understand the finish line and production journey |
| 0.2 Agentic AI mental model | 4?5 | 10?12 min | Explain model, tools, state, loop, and when an agent is appropriate |
| 0.3 Ubuntu toolkit | 6?7 | 8?10 min | Understand the Linux development environment and evidence-based checks |
| Lab 0.5a Ubuntu and tools | 8?9 | 12?15 min | Ubuntu, Python, and an editor open the Linux repository |
| 0.4 API-key safety | 10?12 | 10?12 min | Explain `.env.example`, `.env`, Git ignore, data, and cost boundaries |
| Lab 0.5b Project setup | 13?16 | 15?20 min | `.venv`, packages, local config, and setup gate work in Ubuntu |
| Lab 0.5c First AI call | 17?20 | 15?20 min | Run and vary one real model request |
| 0.6 Troubleshooting and gate | 21?27 | 12?15 min | Diagnose by layer and prove Day 0 completion |

Long installation waits should be edited or time-compressed. Do not conceal errors that materially change the instructions.

## Live terminal sequence

Open `demo-commands.html` as the command-by-command recording companion. It contains the canonical Ubuntu run order, Copy buttons, simple What/Why explanations, pass conditions, and Linux troubleshooting.

### Verify Ubuntu tools

```bash
python3 --version
git --version
```

The course requires Python 3.11 or newer. Use VS Code, another editor, or an editor connection appropriate to the Ubuntu host.

### Clone or open the Ubuntu-hosted repository

```bash
mkdir -p ~/src
if [ ! -d ~/src/agentic-ai-40days/.git ]; then
  git clone https://github.com/Dhananjaiah/Agentic-AI-40Days.git ~/src/agentic-ai-40days
fi
cd ~/src/agentic-ai-40days
pwd
```

Confirm `pwd` begins with `/home/`. If VS Code is available on the host connection, run `code .`; otherwise open this folder using the editor?s supported remote or local workflow.

### Create and activate the virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### Install dependencies

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m pip install -e .
```

### Create local configuration

```bash
cp .env.example .env
```

Open `.env` in the available editor, add the credential privately, then verify:

```bash
git check-ignore -v .env
```

Do not continue if the Git command produces no matching ignore rule.

### Run the no-cost setup check

```bash
python phase-0-get-ready/day-00/labs/lab-0.5b-setup-project/solution/check_setup.py
```

This verifies environment and key presence; it does not authenticate with the provider.

### Run the first model call

```bash
python phase-0-get-ready/day-00/labs/lab-0.5c-hello-ai/solution/hello_ai.py
```

This command contacts the configured provider and may incur model usage. Verify a meaningful response and usage metadata. Generated wording varies.

## Controlled troubleshooting demonstration

Choose one safe failure:

- If `python3 -m venv .venv` reports a missing venv package, use the Ubuntu package manager available on the host to install `python3-venv`, then rerun the same command.
- Use an inactive virtual environment to demonstrate an import failure, activate `.venv`, and rerun.
- Temporarily use a blank placeholder in a disposable local configuration to show the missing-key check, then restore the private configuration off-camera.

Never demonstrate an authentication failure with a real credential visible. Never intentionally commit a real or fake key that resembles an active credential.

## Recording standards

- Show the finished result before a lab.
- Explain a command before executing it.
- Keep long provider or package output brief; focus on the first relevant error or final proof.
- Label illustrative slide output as illustrative and live output as observed.
- Never promise an exact generated sentence, token count, latency, or cost.
- Do not call the system production-ready after one successful request. State exactly what the check proves.
- Give visible pause points so learners can match results locally.

## Publish checklist

- [ ] Deck, notes, links, copy buttons, readiness gate, fullscreen, and PDF export work.
- [ ] Commands work on a supported Ubuntu host and use the Linux-hosted repository path.
- [ ] The setup checker passes on a clean supported Ubuntu environment.
- [ ] The selected provider call succeeds and prints usage information.
- [ ] No credential, private email, account ID, billing detail, or unrelated notification appears.
- [ ] Captions distinguish `.env.example` from `.env` and model call from agent.
- [ ] Provider pricing and model references were checked immediately before publication.
- [ ] Downloadable resources include the deck, transcript, runbook, and existing lab materials.
