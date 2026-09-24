# 21-Day Autumn Recruitment Learning Plan

## 0. Goal

Target roles:

1. Java Backend Engineer
2. AI Agent / AI Application Engineer

Primary learning objectives:

- understand a real Agent + backend project end-to-end;
- complete verified secondary development;
- build one backend-focused project story;
- convert implementation evidence into interview-ready knowledge;
- start applying before the entire plan is finished.

This plan is **Gate-driven, not calendar-driven**.

If a Gate fails, the next calendar day becomes remediation for the same stage.

---

# 1. Project Registry

## Primary Project

Name:

```text
DOVideo-AI
```

Repository:

```text
https://github.com/Emm-star-ggb/DOVideo-AI
```

Primary role:

```text
Agent + Java Backend main resume project
```

## Secondary Project

Name:

```text
Maoyan-Movie-System
```

Repository:

```text
TBD — personal fork not initialized yet
```

Primary role:

```text
Java high-concurrency backend supporting project
```

## Agent Source-Learning Project

Name:

```text
CoreCoder
```

Repository:

```text
https://github.com/he-yufeng/CoreCoder
```

Primary role:

```text
Agent fundamentals / source reading
```

---

# 2. Current State

Current Logical Day:

```text
D01
```

Current Stage:

```text
S1 — System Bootstrap
```

Current Gate:

```text
G01
```

Gate Status:

```text
NOT_STARTED
```

Current Project:

```text
DOVideo-AI
```

Last Verified Commit:

```text
510156d7366cf9a17d20714e02df3d5f1d8c0e30
```

Last Updated:

```text
2026-09-24
```

---

# 3. Daily Working Loop

Every active learning day follows:

```text
08:30 ChatGPT morning check
→ previous Gate check
→ closed-book recall
→ today's minimum scope

User self-study / first implementation
→ 60–90 min before asking Codex for core logic

Codex Learning/Review Mode
→ review, do not replace reasoning

User revision

Codex Test Engineer Mode
→ tests only

Update GitHub docs / commits

22:30 ChatGPT Gate Check
→ code
→ tests
→ benchmark or N/A
→ oral defense
→ PASS / FAIL
```

Recommended time allocation:

```text
Morning planning/recall      20 min
Source reading/debugging     90–120 min
Independent implementation  90 min
Codex review + revision      60–90 min
Theory tied to project       60 min
Documentation/evidence       30–45 min
Oral Gate                    30–60 min
```

---

# 4. Stage Overview

| Stage | Logical Days | Main Output | Gate |
|---|---|---|---|
| S1 System Bootstrap | D01-D03 | runnable system + verified architecture | G01-G03 |
| S2 Agent Fundamentals | D04-D06 | Agent Loop/RAG understanding | G04 |
| S3 First Secondary Development | D07-D09 | first resume-relevant enhancement | G05 |
| S4 Backend Engineering | D10-D14 | concurrency/consistency project depth | G06 |
| S5 Benchmark & Resume | D15-D17 | real metrics + resume v2 | G07 |
| S6 Interview Conversion | D18-D21 | interview defense | G08 |

---

# 5. D01 — Run DOVideo-AI

## Objective

Successfully run the primary project and complete one real business flow.

## User Must Do

- [ ] fork/clone repository;
- [ ] configure local environment;
- [ ] start required infrastructure;
- [ ] start backend;
- [ ] start frontend;
- [ ] execute one real request;
- [ ] record all blockers and fixes.

## Codex May Do

- locate startup config;
- explain error logs after the user attempts;
- identify relevant configuration files;
- review local-only fixes.

## Codex Must Not Do First

- rewrite all configuration without the user's attempt;
- silently skip failing services;
- claim system is running without evidence.

## Deliverables

- `DAILY_LOG.md` D01 entry;
- first `ARCHITECTURE.md` high-level map;
- startup commands;
- service status / request evidence;
- commit(s).

## Gate

`G01 — System Bootstrap`

---

# 6. D02 — Trace One End-to-End Request

## Objective

Trace one request through real code.

Target conceptual path:

```text
Frontend
→ Controller
→ Service
→ async boundary
→ processing
→ retrieval/agent
→ persistence
→ result delivery
```

Do not assume class names from README. Verify real code.

## Deliverables

- verified entry class/method;
- key service calls;
- producer/consumer if present;
- result delivery path;
- `ARCH-001` request flow.

## Gate

`G02 — Request Flow`

---

# 7. D03 — Data & Infrastructure Responsibilities

## Objective

Understand why the system uses each infrastructure component.

Focus:

- MySQL;
- Redis;
- MinIO;
- RocketMQ;
- Qdrant or actual vector store.

For each:

- what data enters it;
- what code accesses it;
- why it exists;
- failure impact;
- possible alternative.

## Deliverables

- storage responsibility table;
- failure map;
- at least 8 project-specific interview questions.

## Gate

`G03 — Backend Architecture`

---

# 8. D04 — Minimal Agent Loop via CoreCoder

## Objective

Understand Agent execution without hiding behind a framework.

## User Must Implement

A minimal learning Agent, preferably separately from production code, containing:

- model call;
- tool call request;
- tool execution;
- tool result appended to context;
- loop termination;
- error handling.

Use a tiny tool set.

## Required Explanation

- LLM chooses a tool; application executes it;
- how tool results return to context;
- how the loop ends;
- how loops become unsafe/unbounded.

## Deliverables

- minimal implementation;
- tests;
- Agent Loop diagram;
- questions in `INTERVIEW_QA.md`.

---

# 9. D05 — Trace DOVideo-AI Agent Path

## Objective

Trace the actual Agent path.

Candidate concepts to verify:

- Planner;
- Retrieval;
- Executor;
- Critic;
- retry/iteration;
- checkpoint/state.

Do not assume every concept exists exactly as named. Record actual implementation.

## Deliverables

- actual class/method map;
- state transitions;
- termination condition;
- failure path;
- `ARCH-00X` Agent flow.

---

# 10. D06 — RAG / Retrieval

## Objective

Connect theory to actual project code.

Learn only what the project needs:

- chunk/segment;
- embedding;
- vector retrieval;
- keyword retrieval if present;
- hybrid retrieval if present;
- reranking if present;
- Top-K;
- context construction.

## Required Questions

- why not send the entire source to the LLM?
- what does retrieval improve?
- what can retrieval miss?
- how would retrieval quality be measured?
- what is the latency/quality trade-off?

## Gate

`G04 — Agent Fundamentals`

---

# 11. D07 — Choose One Enhancement

Default recommended options:

1. Agent tracing / observability;
2. Agent evaluation;
3. retrieval evaluation/improvement;
4. MCP/tool integration.

Selection rule:

Choose one with:

- clear user/system problem;
- 2–3 day scope;
- testable output;
- interview value;
- limited infrastructure changes.

Document:

```text
Chosen enhancement:
Problem:
Why now:
Success criteria:
Out of scope:
```

---

# 12. D08 — First Implementation + Review

## User Must

- write first core implementation;
- commit it separately;
- explain current design before Codex review.

## Codex

Use Review Mode.

Review:

- correctness;
- edge cases;
- failure handling;
- unnecessary complexity;
- testing gaps;
- interview attack points.

## Deliverables

At least two commits if practical:

```text
commit A — user's first implementation
commit B — user revision after review
```

---

# 13. D09 — Test / Measure / Resume V1

## Objective

Prove the enhancement.

Do:

- normal tests;
- boundary tests;
- failure tests;
- metric if meaningful.

Create first resume draft.

Resume claims must distinguish:

- upstream project architecture;
- personal secondary development;
- personal experiments.

## Gate

`G05 — First Enhancement`

## Application Rule

After G05 passes, begin/continue applications.

Do **not** wait for D21.

---

# 14. D10 — Run Secondary Backend Project

Project:

```text
Maoyan-Movie-System
```

Objective:

Trace one high-concurrency transaction path.

Focus:

```text
request
→ rate limit
→ stock
→ order
→ MQ
→ database
→ payment/cancel
```

Ignore frontend depth unless necessary.

---

# 15. D11 — Redis / Lua / Locking

Study through real code:

- Redis data structures actually used;
- atomic stock deduction;
- Lua if present;
- Redisson if present;
- duplicate purchase prevention;
- hot-key behavior.

Required explanation:

- why GET + SET/DECR can be unsafe;
- what Lua atomicity means in this context;
- what a distributed lock protects;
- when a lock is unnecessary.

---

# 16. D12 — MySQL / Transaction / Index

Study through order flow:

- transaction boundary;
- isolation needs;
- optimistic/pessimistic locking;
- unique constraints;
- indexes;
- one real `EXPLAIN` if meaningful.

Deliverable:

`ARCHITECTURE.md` or project-local architecture notes for the secondary project.

---

# 17. D13 — MQ / Idempotency / Consistency

Study:

- why MQ instead of only a thread pool;
- duplicate delivery;
- retry;
- dead letter if applicable;
- idempotency;
- compensation;
- eventual consistency.

Required scenario:

```text
Redis decrement succeeds
→ downstream order processing fails
```

Explain system behavior and compensation.

---

# 18. D14 — Backend Secondary Development

Recommended scope:

- consumer idempotency;
- retry/dead-letter visibility;
- stock consistency validation;
- hotspot handling;
- rate limit correctness.

User writes first implementation.

Codex reviews and tests.

## Gate

`G06 — Backend Engineering`

---

# 19. D15 — Baseline Benchmark

Choose a meaningful workload.

For backend:

- throughput/QPS;
- P50/P95/P99;
- error rate;
- CPU/memory if available.

For retrieval:

- Recall@K;
- MRR/nDCG if justified;
- latency.

Record full experiment in `BENCHMARK.md`.

No resume metric before this record exists.

---

# 20. D16 — Diagnose and Improve

Use:

```text
baseline
→ observe bottleneck
→ hypothesis
→ change
→ rerun
→ compare
```

Do not make a change solely because a technology is fashionable.

---

# 21. D17 — Resume V2

For each project, prepare:

- 30-second introduction;
- 2-minute introduction;
- 5-minute deep dive;
- 4–5 resume bullets maximum;
- personal contribution statement;
- evidence link per bullet.

## Gate

`G07 — Resume Ready`

---

# 22. D18 — Resume Explosion: Project Questions

For every resume noun, generate questions.

Example:

```text
RocketMQ
→ why MQ?
→ why not @Async?
→ duplicate delivery?
→ loss?
→ accumulation?
→ consumer crash?
```

Target:

```text
80–120 project-derived questions total
```

Do not target a number by adding irrelevant questions.

---

# 23. D19 — Java Core Tied to Project

Focus:

- collections;
- ConcurrentHashMap;
- thread pool;
- synchronized;
- volatile;
- CAS/AQS;
- JVM memory;
- GC;
- class loading;
- Spring IOC/AOP;
- transactions.

For each major topic, link to project relevance where possible.

---

# 24. D20 — Database / Network / System Design

Focus:

- MySQL;
- Redis;
- MQ;
- HTTP/TCP;
- SSE/WebSocket;
- rate limiting;
- retry;
- idempotency;
- consistency.

System design drills:

1. high-concurrency ticketing/order system;
2. production Agent task platform.

---

# 25. D21 — Full Mock Interview

Suggested 60 minutes:

```text
5 min   self introduction
15 min  primary Agent project
10 min  backend project
10 min  Java/Redis/MySQL/MQ
10 min  Agent/RAG
10 min  algorithm or system scenario
```

## Gate

`G08 — Interview Ready`

---

# 26. Advancement Policy

A day is complete only when the relevant Gate permits advancement.

Example:

```text
Calendar: Sep 26
Logical state: D05 / G04 FAIL

Next day:
D05 remediation

Not:
automatic D06
```

---

# 27. Scope Reduction Policy

If progress falls behind:

Reduce in this order:

1. optional UI;
2. optional new infrastructure;
3. second enhancement;
4. non-resume theory breadth.

Do **not** reduce:

- real implementation;
- tests;
- explanation;
- critical interview debt;
- truthful resume attribution.

---

# 28. Resume Readiness Definition

A claim is ready when:

```text
implemented/verified
+ tested
+ measured if quantitative
+ user can explain
+ personal contribution is clear
```

Mark only such claims as `RESUME_READY`.
