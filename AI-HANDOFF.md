# AI handoff — read this before continuing the course

## Project identity

You are continuing **Agentic AI — Production**, a 40-day, beginner-friendly but technically serious Udemy course.

The goal is to help a learner move from a clean machine to a production-style AI-agent portfolio. The course must teach design, implementation, evaluation, security, deployment, observability, operations, and clear technical explanation.

This folder is the polished course. The older repository under `ALL/Agentic-AI-40Days` is source material. Do not overwrite the source course unless the user explicitly asks.

## Current state

- `Day0` is complete and includes the standard standalone demo walkthrough.
- `Day1` has its complete six-file teaching package plus a prompt-notes learner artifact.
- Day 1 local setup and import checks pass. Live Anthropic and OpenAI requests currently return HTTP 401 because both saved local credentials are invalid, so live API verification remains pending.
- `Day2` has its complete six-file teaching package plus a reliability-evidence learner artifact.
- Day 2 deterministic validation and fallback tests pass against the real source code. Live review classification remains pending because provider credentials are invalid.
- `Day3` has its complete six-file teaching package plus a Python-evidence learner artifact.
- Day 3 compile checks, decision tests, and local batch simulation pass. Provider-backed lab runs remain pending because credentials are invalid.
- `Day4` has its complete six-file teaching package plus an API-evidence learner artifact.
- Day 4 compile checks, deterministic status mapping, and local graceful-failure simulation pass. Provider-backed response inspection remains pending because credentials are invalid.
- `Day5` has its complete six-file teaching package plus a document-evidence learner artifact.
- Day 5 compile checks, real UTF-8 text ingestion, two-page PDF extraction, and controlled input-classification checks pass. Provider-backed summaries remain pending because credentials are invalid.
- Days 6–40 are planned and listed in `COURSE-CONTENT.md`.
- After provider credentials are repaired, rerun the pending live scripts for Days 1–5. The next normal build target is `Day6 — Project 1: Smart Summarizer`.
- Day 0 establishes the visual style, navigation, transcript style, runbook depth, demo walkthrough, and final six-file package.

## Required reading order

Before making changes:

1. Read this file completely.
2. Read `README.md`.
3. Read `COURSE-CONTENT.md` for the complete journey and the target day.
4. Read `COURSE-DESIGN-STANDARD.md`.
5. Read `DAY-BUILD-CHECKLIST.md`.
6. Read the completed `Day0` files to understand the expected format.
7. Read matching source lessons under `ALL/Agentic-AI-40Days`.

Do not build a day from the table-of-contents row alone. The phase requirements and course-wide production standards are part of the scope.

## What “the same way as Day 0” means

Every completed day has:

```text
DayN/
├── README.md
├── index.html
├── demo-commands.html
├── presentation.pdf
├── speaker-notes.md
└── recording-runbook.md
```

The HTML deck is standalone and interactive. The separate `demo-commands.html` starts from the stated environment, puts commands in run order, provides a Copy button for each block, and explains What and Why in simple English. The transcript is written so the instructor can read it aloud. The runbook contains the real setup, commands, safety rules, expected results, troubleshooting flow, and publishing checks. The PDF is the shareable slide export.

Keep the final folder clean. Temporary build scripts, browser-test scripts, screenshots, cache folders, and scratch notes must be removed after they have served their purpose.

## Teaching voice

Use simple, everyday English. Assume the learner is intelligent but new to the topic.

Good narration:

> A virtual environment is a private Python toolbox for one project. Packages installed here will not mix with packages from another project.

Avoid narration like:

> Virtual environments facilitate dependency isolation across heterogeneous execution contexts.

Explain one idea at a time. Use short sentences. Give a real example. Then connect it to the next idea.

Technical accuracy must remain strong. Do not remove an important boundary only because it takes time to explain.

## Course-wide story

The learner progresses through this sequence:

1. Make one safe, understood model call.
2. Make outputs reliable and handle failures.
3. Work with files, APIs, and Python confidently.
4. Retrieve trusted information and measure retrieval quality.
5. Give a model controlled tools, state, limits, and approval.
6. Orchestrate larger workflows only when complexity is justified.
7. Evaluate, secure, deploy, observe, and operate the system.
8. Demonstrate those skills through evidence in a capstone and portfolio.

Do not introduce advanced complexity before the learner has the mental model and evidence needed to understand it.

## Day 6 target

Day 6 is **Project 1: Smart Summarizer**.

Before marking Days 1–5 complete, rerun their live solution scripts with a valid provider key and update their statuses.

Day 6 should teach:

- Scoping a small useful tool before coding.
- Combining text and PDF ingestion with structured, validated output.
- Handling unsupported input and provider failure clearly.
- Adding a repeatable test command and checking key failure paths.
- Documenting setup, use, privacy, cost, and known limits.
- Using small, meaningful Git commits and preparing a GitHub-ready portfolio project.

The final evidence is a portfolio-ready Smart Summarizer with tests, a cost note, README, and clear Git history.

Keep Day 6 focused on combining the Phase 1 skills into one reviewed project. Do not introduce embeddings, retrieval, or agent orchestration yet.

## Working rules for any future AI

- Continue autonomously when the user asks to build or update a day.
- Preserve completed learner content unless the requested change requires editing it.
- Make reasonable choices from these documents instead of repeatedly asking the user for minor preferences.
- Check the filesystem before creating new files.
- Do not create all future day folders as empty placeholders.
- Verify current facts through official documentation when they may have changed.
- Never place a real API key, private data, or account detail in course files.
- Never claim that an illustrative output came from a live run.
- Never state a fixed provider price, model name, or service limit without current verification.
- Test the final HTML and PDF, then remove temporary development artifacts.
- Update the course status and this handoff after completing a day.

## Definition of complete for a day

A day is complete only when:

- The learner outcome and evidence match `COURSE-CONTENT.md`.
- The six final files exist, including the standalone demo walkthrough when the day has a live demo.
- The deck and transcript tell one clear story.
- The narration is simple enough to read naturally.
- Commands and code have been tested.
- Safety and operational boundaries are included where relevant.
- Browser controls and interactions work.
- Slides have no clipped content.
- The PDF has been generated and inspected.
- The final folder contains no unnecessary development files.
- Root status documents identify the next day accurately.

## Open decisions

Days 1–5 need one external-state fix before their statuses can become Complete: configure a valid Anthropic or OpenAI API key in the private source-repository `.env`, then rerun their live solution scripts. Do not copy the key into this polished course folder or any report.

After the live scripts pass, update their statuses. Build `Day6` next unless the user selects another day or asks for a course-wide change.
