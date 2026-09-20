# Day build checklist

Copy this checklist into the working notes for each new day. Do not mark the day complete until every required item is satisfied.

## A. Understand the day

- [ ] Read the matching row and phase notes in `COURSE-CONTENT.md`.
- [ ] Read related source lessons under `ALL/Agentic-AI-40Days`.
- [ ] Identify facts that may have changed and verify them with official sources.
- [ ] Write one learner outcome in the form: “By the end, the learner can…”
- [ ] Define the real artifact and visible evidence.
- [ ] Define one safe failure to diagnose.
- [ ] Define data, secret, authorization, cost, latency, and safety boundaries that apply.

## B. Design the lesson

- [ ] Start with a real problem or decision.
- [ ] Explain new terms in everyday language.
- [ ] Show how the parts connect.
- [ ] Show the finished result before the build.
- [ ] Build in small steps with reasons.
- [ ] Verify the happy path.
- [ ] Demonstrate a controlled failure and recovery.
- [ ] Include production limits and trade-offs.
- [ ] Add a knowledge check.
- [ ] Add a final evidence-based readiness gate.

## C. Create the six-file package

- [ ] `README.md`
- [ ] `index.html`
- [ ] `demo-commands.html` for a day with a live demo, or a README explanation when it does not apply
- [ ] `presentation.pdf`
- [ ] `speaker-notes.md`
- [ ] `recording-runbook.md`

## D. Review the transcript

- [ ] Every slide has matching narration.
- [ ] The script uses simple, everyday English.
- [ ] New words are explained before use.
- [ ] Sentences sound natural when read aloud.
- [ ] Transitions create one meaningful story.
- [ ] Silent instructions use `[SQUARE BRACKETS]`.
- [ ] Live steps include success and failure wording where needed.
- [ ] The script never exposes or asks for secrets.

## E. Test the deck

- [ ] Arrow keys, Page Up, Page Down, Home, and End work.
- [ ] Slide selector works.
- [ ] Notes open with **N**.
- [ ] Fullscreen and recording mode work.
- [ ] Copy buttons work.
- [ ] Interactive diagrams or checks work.
- [ ] No browser JavaScript errors occur.
- [ ] No content is clipped at 1920×1080.
- [ ] No content is clipped at 1280×720.
- [ ] Print layout includes every slide.
- [ ] PDF is generated and visually inspected.

## F. Verify technical content

- [ ] Commands run from the stated directory.
- [ ] Demo commands start from the stated environment and follow the real run order.
- [ ] Every demo command has a working Copy button and simple What/Why explanation.
- [ ] Important demo checkpoints show a clear pass condition or expected result.
- [ ] Code and tests pass.
- [ ] Expected output is accurate or clearly marked illustrative.
- [ ] Provider or package details are current.
- [ ] No credentials or private data appear in any file.
- [ ] Links and paths work.
- [ ] Claims state exactly what the evidence proves.

## G. Finish and hand off

- [ ] Remove generators, verification scripts, previews, caches, and scratch files.
- [ ] Keep only final deliverables and real learner artifacts.
- [ ] Update the day status in `COURSE-CONTENT.md`.
- [ ] Update the status section in the root `README.md`.
- [ ] Update `AI-HANDOFF.md` with the next day and any open decisions.
