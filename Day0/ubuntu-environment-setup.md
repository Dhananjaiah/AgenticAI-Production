# Day 0 environment standard ? Ubuntu

## The rule for this course

Use **Ubuntu Linux** as the development environment. The course works whether Ubuntu runs on a local computer, a local VM, a cloud VM such as AWS EC2 or Oracle Cloud, WSL, or another supported host.

The host is an implementation detail. Every course lab, demo, and recording uses Ubuntu Bash and the same Linux project layout.

## Required capabilities

Before starting, ensure the Ubuntu host provides:

- shell access as a normal user with `sudo` when package installation is required;
- Python 3.11 or newer and the `python3-venv` package;
- Git;
- outbound network access to the selected AI provider when running live calls;
- an editor. VS Code is recommended, but it may connect locally, over SSH, through a browser, or through another supported remote workflow.

## Canonical course workspace

```bash
mkdir -p ~/src
if [ ! -d ~/src/agentic-ai-40days/.git ]; then
  git clone https://github.com/Dhananjaiah/Agentic-AI-40Days.git ~/src/agentic-ai-40days
fi
cd ~/src/agentic-ai-40days
```

Keep the repository and project virtual environment inside the Ubuntu home directory.

## Canonical Python workflow

```bash
cd ~/src/agentic-ai-40days
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m pip install -e .
```

## Local secrets

```bash
cp .env.example .env
git check-ignore -v .env
```

Open `.env` in your available editor and add the real provider credential privately. The Git check must print the rule that ignores `.env`.

## Optional host appendices

- **WSL:** install Ubuntu and open the repository through VS Code?s WSL connection if desired.
- **AWS EC2 / Oracle Cloud / other VM:** connect over SSH and use VS Code Remote SSH, a browser editor, or a terminal editor.
- **Local VM:** use the VM?s Ubuntu terminal and local or remote editor connection.

These host-specific steps are optional setup references. They do not change the lab commands.
