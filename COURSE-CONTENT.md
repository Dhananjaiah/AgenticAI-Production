# Complete course content — Day 0 to Day 40

## Course promise

By the end of the course, a learner can design, build, evaluate, secure, deploy, observe, operate, and explain an AI-agent system—not only demonstrate one.

Every day uses short explanations, real examples, hands-on work, visible evidence, and plain-English narration. Every project ends with something a learner can show in a portfolio.

## Phase 0 — Get ready and work safely

| Day | Lesson | Learner outcome | Main evidence | Status |
|---:|---|---|---|---|
| 0 | Setup, expectations, and course map | Install tools, protect the API key, create a virtual environment, and make the first model call | Setup checker passes; `.env` is ignored; first AI reply includes usage | Complete |

## Phase 1 — Foundations and engineering habits

| Day | Lesson | Learner outcome | Main evidence | Status |
|---:|---|---|---|---|
| 1 | Meet the LLM | Explain models, tokens, context, prompts, requests, and responses | Repeatable first-call script and prompt notes | Content complete; live API check pending |
| 2 | Reliable outputs | Use system instructions, structured output, validation, retries, and fallback | Review sorter that handles malformed output | Content complete; local reliability proof passed; live API check pending |
| 3 | Just-enough Python | Use variables, functions, lists, loops, conditions, and basic debugging | Sorter refactored into small functions | Content complete; local Python proof passed; live API check pending |
| 4 | APIs, secrets, and failures | Understand HTTP, JSON, status codes, rate limits, backoff, and idempotency | API response inspector and safe error handler | Content complete; local API-error proof passed; live API check pending |
| 5 | Files and document ingestion | Read text and PDFs, write output, handle encoding and unsupported documents | Document summary workflow with clear failure messages | Content complete; local text/PDF ingestion proof passed; live API check pending |
| 6 | Project 1: Smart Summarizer | Scope, build, test, document, and review a small production-minded AI feature | Portfolio project with tests, cost note, README, and Git history | Planned |

Phase 1 must also introduce formatting, linting, type hints, one test command, dependency pinning, Git branches, pull requests, review, merge conflicts, and a simple error taxonomy.

## Phase 2 — LLM building blocks and production RAG

| Day | Lesson | Learner outcome | Main evidence | Status |
|---:|---|---|---|---|
| 7 | Prompt engineering that works | Use examples, constraints, output contracts, and prompt versions | Prompt regression suite with stable cases | Planned |
| 8 | Embeddings and semantic search | Understand vectors, meaning-based search, similarity, and trade-offs | Measured similarity and clustering experiment | Planned |
| 9 | Vector databases and retrieval | Build an index with metadata, filtering, and persistence | Local searchable document index | Planned |
| 10 | Basic RAG | Retrieve useful context, answer from evidence, cite it, or safely abstain | Answers cite approved chunks or say “I do not know” | Planned |
| 11 | Better RAG | Compare chunking, hybrid search, reranking, query rewrite, and context budgets | Retrieval benchmark comparing configurations | Planned |
| 12 | Project 2: Ask My Documents | Build document Q&A with ingestion, citations, provenance, and starter evals | Portfolio RAG project with measured retrieval and known limits | Planned |

Phase 2 must also cover incremental indexing, index versions, OCR limits, freshness, data lineage, access-aware retrieval, tenant isolation, retrieval metrics, answer metrics, and prompt injection through documents.

## Phase 3 — From LLM to safe single-agent systems

| Day | Lesson | Learner outcome | Main evidence | Status |
|---:|---|---|---|---|
| 13 | Agent versus chatbot | Choose between a model call, chatbot, workflow, and agent | Written design decision with reasons | Planned |
| 14 | Tool and function calling | Define typed tool inputs, validate them, allow only approved tools, and handle failures | Safe typed tool call | Planned |
| 15 | The agent loop | Build observe-decide-act cycles with limits and stop conditions | Bounded loop with traceable steps | Planned |
| 16 | Memory | Use short-term and long-term memory with retention and deletion rules | Memory feature with clear privacy behavior | Planned |
| 17 | Planning and replanning | Create a plan, track progress, react to change, and recover from failure | Bounded plan-execute-replan workflow | Planned |
| 18 | Reflection and self-correction | Use a rubric to check and improve output without endless loops | Measured reflection workflow | Planned |
| 19 | Human approval and kill switches | Classify risk, pause for approval, log decisions, and stop dangerous execution | Tested approval state and emergency stop | Planned |
| 20 | Project 3: Useful Single Agent | Combine model, tools, state, evaluation, approval, and handoff | Portfolio agent with threat model, traces, evals, and safe escalation | Planned |

Phase 3 must include timeouts, retries, idempotency, compensation for side effects, approval states, least-privilege credentials, uncertainty messages, and human handoff.

## Phase 4 — Orchestration, MCP, and multi-agent systems

| Day | Lesson | Learner outcome | Main evidence | Status |
|---:|---|---|---|---|
| 21 | Framework selection | Understand what frameworks add and hide; compare major approaches | Architecture decision record | Planned |
| 22 | LangGraph fundamentals | Use typed state, nodes, edges, and tool nodes | Small working graph agent | Planned |
| 23 | LangGraph reliability | Add branches, retries, checkpoints, interrupts, and approval nodes | Tested approval and failure branches | Planned |
| 24 | Role-based orchestration | Compare role-based teams with graph workflows | Two-role quality, cost, and latency comparison | Planned |
| 25 | MCP client and server | Understand tools, resources, transports, trust, and authentication | Safe MCP client plus learner-built MCP server | Planned |
| 26 | Multi-agent design | Use planner, worker, and checker roles with isolated permissions and budgets | Three-agent workflow with clear role contracts | Planned |
| 27 | Agent-to-agent handoffs | Validate handoff data, reduce context, and handle cross-system failures | Audited two-agent handoff with fallback | Planned |
| 28 | Project 4: Multi-Agent Workflow | Justify multi-agent complexity against a single-agent baseline | Portfolio workflow with benchmark, traces, permissions, cost, and latency | Planned |

Phase 4 must cover MCP trust, authorization, tool allowlists, credential isolation, failure containment, saved state, resume and replay behavior, and concurrency limits.

## Phase 5 — Quality, security, deployment, and operations

| Day | Lesson | Learner outcome | Main evidence | Status |
|---:|---|---|---|---|
| 29 | Evaluation foundations | Design normal, edge, escalation, adversarial, and regression cases | Versioned evaluation set | Planned |
| 30 | Automated quality gates | Combine deterministic checks, calibrated model judges, human review, and release thresholds | CI gate that blocks a known regression | Planned |
| 31 | Observability and tracing | Use spans, correlation IDs, safe logs, dashboards, and traces | Diagnose a broken run from evidence | Planned |
| 32 | Guardrails and AI security | Defend against prompt injection, unsafe tools, and data exfiltration | Attack suite with safe containment | Planned |
| 33 | Cost, speed, and reliability | Measure tokens, caching, routing, streaming, concurrency, and latency | Before-and-after cost and p50/p95 benchmark | Planned |
| 34 | Packaging and deployment | Build an authenticated API, container, health checks, staging release, and rollback | Agent service deployed to staging | Planned |
| 35 | Governance and incident response | Define audit, authorization, retention, roles, scanning, and incident response | Threat model, audit record, retention decision, and incident drill | Planned |
| 36 | Project 5: Harden an Agent | Apply evaluations, tracing, guardrails, rate limits, deployment, and rollback | Production-ready portfolio project with release evidence | Planned |

Phase 5 must distinguish offline evaluation, pre-release gates, and production monitoring. It must include authentication, authorization, tenant isolation, least privilege, secret rotation, data minimization, malicious retrieved content, SSRF risk, sandboxing, queues, streaming, canary releases, rollback, alerts, on-call runbooks, and postmortems.

## Phase 6 — Capstone, operations drill, and career evidence

| Day | Lesson | Learner outcome | Main evidence | Status |
|---:|---|---|---|---|
| 37 | Capstone Day 0: Plan and design | Define users, scope, success, architecture, risks, cost, and evaluation before coding | Approved design package | Planned |
| 38 | Capstone Day 1: Build and deploy | Implement tools, data flow, approvals, tracing, tests, CI, and staging release | Staging deployment passing release gates | Planned |
| 39 | Capstone Day 2: Operate and improve | Use dashboards, diagnose a deliberate failure, roll back, and prevent recurrence | Incident report, regression test, and updated runbook | Planned |
| 40 | Get hired | Present architecture, evidence, trade-offs, limitations, and decisions | Final repository and job-ready portfolio walkthrough | Planned |

## Portfolio projects

Every portfolio project must include, at the level appropriate for that phase:

1. Problem, users, scope, success measures, and architecture.
2. Safe and repeatable setup with no secrets in code.
3. Happy path, invalid-input path, outside-service failure, and safety or approval path.
4. Automated tests and versioned evaluations when model behavior matters.
5. Logs and traces that avoid secrets and unnecessary personal data.
6. Clear model, tool, data, authorization, cost, and latency boundaries.
7. Deployment, rollback, and operational guidance for production projects.
8. A README that shows evidence, trade-offs, limits, and next steps.

## Planned folder sequence

Use `Day0`, `Day1`, `Day2`, through `Day40`. Do not create empty day folders far in advance. Create the next folder when its content is actively being built.
