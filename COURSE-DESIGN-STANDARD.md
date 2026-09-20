# Course design standard

This document defines how every day in **Agentic AI — Production** must be designed. It keeps the course consistent even when a different person, AI model, or session continues the work.

## 1. Design from the learner outcome

Before writing slides, define:

- What the learner can do after the day.
- What the learner must understand in plain language.
- What real artifact the learner creates.
- What command, test, output, or demonstration proves completion.
- What common failure the learner will diagnose.
- What safety, data, cost, and authorization boundary applies.

Do not start by choosing a slide count. Start with the learning outcome and evidence.

## 2. Use a meaningful teaching flow

Each day should normally follow this story:

1. **Why this matters** — begin with a real problem or decision.
2. **What it means** — explain new ideas in everyday words.
3. **How the parts connect** — show a small diagram or sequence.
4. **Show the finished result** — let the learner see the target.
5. **Build it step by step** — explain each command or code block before using it.
6. **Check the result** — compare real output with a clear pass condition.
7. **Break one safe case** — read the error, identify the layer, fix one cause, and rerun.
8. **Explain production boundaries** — data, secrets, permissions, cost, latency, failure, and limits.
9. **Check understanding** — short questions that test important distinctions.
10. **Finish with evidence** — a checklist that says exactly when the day is complete.

The flow can change when the topic needs it, but it must remain easy to follow.

## 3. Write for a beginner without making the topic shallow

- Use common, everyday words.
- Keep sentences short enough to speak naturally.
- Introduce one new idea at a time.
- Explain a technical word before asking the learner to use it.
- Give a concrete example immediately after an abstract idea.
- Say what an action proves and what it does not prove.
- Avoid unexplained acronyms, marketing language, and vague claims.
- Do not describe a model as “thinking” without explaining the practical system behavior.
- Never promise that generated wording, latency, token count, price, or external-service behavior will be exact.

Simple English does not mean removing technical truth. It means explaining technical truth clearly.

## 4. Use real workflows

Examples should look like work a learner may meet in a real team: customer support, document search, review triage, order lookup, approvals, incidents, deployment, and monitoring.

Avoid examples that exist only to show syntax. A small example is acceptable when it represents a real boundary or pattern.

Clearly label:

- Illustrative output versus output captured from a real run.
- Simulation versus a live external action.
- Placeholder hostnames, emails, IDs, credentials, and prices.
- Assumptions and environment-specific details.

## 5. Required files for every completed day

```text
DayN/
├── README.md
├── index.html
├── demo-commands.html
├── presentation.pdf
├── speaker-notes.md
└── recording-runbook.md
```

Keep only final learner and instructor deliverables. Remove build scripts, verification scripts, preview images, caches, temporary exports, and scratch notes after verification.

If a day includes code or labs, add only the folders needed for those real learner artifacts. Explain them in the day README.

## 6. HTML presentation requirements

Every deck must:

- Use a 16:9 layout that scales to the browser window.
- Work as a standalone local HTML file.
- Use consistent Agentic AI — Production colors, typography, spacing, headers, and footers.
- Support arrow-key and Page Up/Page Down navigation.
- Support Home and End.
- Show slide number and total count.
- Provide a slide selector.
- Provide fullscreen and recording modes.
- Provide a Notes control using the **N** key.
- Embed the full narration for each matching slide.
- Include copy buttons for important commands when helpful.
- Include print styles for PDF export.
- Avoid clipped content at 1920×1080 and 1280×720.
- Avoid external assets unless they are necessary, licensed, and stored with the course.

Use diagrams only when they make a relationship or sequence easier to understand.

## 7. Demo commands HTML requirements

Every day with a live demo must include a separate `demo-commands.html`. It is the instructor's command-by-command walkthrough and a learner reference. It must:

- Start with short bullet lists that explain the main idea and the complete demo outcome.
- Begin from a clean or clearly stated starting point instead of relying on hidden setup.
- Put commands in the exact order they should be run.
- State the terminal, working directory, and operating system where those details matter.
- Give every command block its own Copy button.
- Explain every command block with **What this does** and **Why we do it** in simple English.
- Show a clear pass condition or expected result after important checkpoints.
- Separate commands that must run in different terminals.
- Mark manual steps, network calls, possible costs, secret handling, destructive cleanup, and commands that keep running.
- Include focused troubleshooting commands and optional cleanup when relevant.
- Use the same visual language as the day's presentation while remaining a normal scrolling page.
- Work as a standalone local HTML file without external runtime dependencies.
- Never contain a real credential, private value, or output presented as live evidence when it is illustrative.

If a day has no terminal or code demo, document why `demo-commands.html` is not applicable in the day README. Do not create an empty placeholder page.

## 8. Transcript requirements

The transcript is a script the instructor can read aloud.

It must:

- Use simple, natural, everyday English.
- Match the slide exactly.
- Explain what the learner is looking at.
- Include smooth transitions from the previous slide and into the next idea.
- Tell the instructor when to pause, click, switch to the terminal, run a command, or wait for the learner.
- Put silent directions inside `[SQUARE BRACKETS]`.
- Provide separate words for success, pending, and failure when live output can vary.
- Never instruct the presenter to claim a result before checking it.
- Never ask the presenter to reveal a secret or private account detail.

Read every transcript aloud during review. Rewrite any sentence that sounds formal, crowded, or unnatural when spoken.

## 9. Recording runbook requirements

The runbook must include:

- The day’s learner outcome and proof of completion.
- Preparation and environment requirements.
- A suggested video or chapter breakdown.
- Exact commands in the correct working directory.
- Safe recording rules.
- Expected output shape, clearly labeled as illustrative where appropriate.
- Common failures and a controlled troubleshooting demonstration.
- Pause points for learner work.
- A publish checklist.

## 10. Safety and production depth

Teach safety as part of the normal workflow, not as a warning added at the end.

For relevant days, cover:

- Secret handling and rotation.
- Data sent to models and outside services.
- Authentication and authorization.
- Least-privilege tool access.
- Input validation and output validation.
- Timeouts, retries, rate limits, and idempotency.
- Human approval and reversible actions.
- Cost and latency measurement.
- Logs and traces without unnecessary sensitive data.
- Testing, evaluation, release gates, rollback, and incident response.

State the limits of every demonstration. One successful run proves only the path that was actually tested.

## 11. Source and freshness rules

- Begin with `COURSE-CONTENT.md` and the matching source material under `ALL/Agentic-AI-40Days`.
- Prefer official documentation for commands, APIs, model behavior, security guidance, and current product details.
- Verify facts that may change: package versions, model names, prices, service limits, supported platforms, and installation steps.
- Put changing details in the runbook when possible, so slides remain useful longer.
- Do not silently copy outdated commands from an older lesson.

## 12. Quality review

Before a day is marked complete:

1. Check the learning flow against the outcome.
2. Verify all commands and code in the intended environment.
3. Check that no real secret or private data is present.
4. Validate every internal link and file path.
5. Open every slide in a browser and check for clipping.
6. Test keyboard navigation, notes, presentation copy controls, interactions, recording mode, and print output.
7. Check every demo command in order, confirm each command has a working Copy button and matching What/Why explanation, and verify important pass conditions.
8. Confirm the transcript count and order match the slides.
9. Read the transcript aloud and simplify awkward sentences.
10. Generate and inspect the PDF.
11. Remove development-only files.
12. Update `COURSE-CONTENT.md`, `README.md`, and `AI-HANDOFF.md` status.
