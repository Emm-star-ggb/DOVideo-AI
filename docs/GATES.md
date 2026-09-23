# Learning Gates

This file is the authoritative progression state.

**Calendar date does not determine progression.**

Only Gate status determines whether the next stage may start.

---

# 0. Status Definitions

```text
NOT_STARTED
No meaningful evidence yet.

IN_PROGRESS
Some evidence exists, but the Gate is not ready for oral defense.

ORAL_PENDING
Code/test/metric evidence is ready; ChatGPT oral defense remains.

FAIL
Gate was attempted and failed.

PASS
All required evidence and oral defense passed.
```

Only ChatGPT may record the final oral-defense `PASS`.

Codex may produce evidence but must not declare a learning Gate passed.

---

# 1. Evidence Standard

Every Gate considers four evidence classes.

## A — Code / Execution

Possible evidence:

- commit SHA;
- successfully executed flow;
- specific class/method locations;
- implemented feature.

## B — Test

Possible evidence:

- unit;
- integration;
- E2E;
- concurrency;
- startup/health check.

Actual commands and results must exist.

## C — Metric

If quantitative measurement is meaningful:

- actual executed benchmark;
- experiment ID;
- raw output.

If not meaningful:

```text
N/A
Reason:
Alternative verification:
```

## D — Oral Defense

User must demonstrate:

- why;
- how;
- alternatives;
- failure cases;
- code location;
- test/measurement interpretation.

---

# G01 — System Bootstrap

Status:

```text
NOT_STARTED
```

Logical Day:

```text
D01
```

## Goal

Prove that the user can independently run the primary system and understand its high-level components.

## Evidence A — Execution

- [ ] primary repository accessible;
- [ ] required infrastructure starts;
- [ ] backend starts;
- [ ] frontend starts;
- [ ] one real business flow completes.

Commit / evidence:

```text

```

## Evidence B — Test

Required minimum:

- [ ] backend health or equivalent startup verification;
- [ ] one end-to-end business operation.

Command:

```bash

```

Result:

```text

```

## Evidence C — Metric

```text
N/A
```

Reason:

```text
Bootstrap Gate measures operability and basic architecture understanding.
Performance/quality optimization is not yet the target.
```

Alternative verification:

```text
service health + end-to-end operation
```

## Evidence D — Oral Topics

ChatGPT should ask a random subset and follow up.

Do not pre-fill answers here.

- Why should long-running video/AI processing not remain entirely in the synchronous HTTP request path?
- What major infrastructure services are running?
- What does each storage component appear to own?
- What happens if one infrastructure dependency is unavailable?
- Show the startup configuration you changed, if any.
- Which result proves the end-to-end flow really ran?

## PASS Criteria

- operational evidence exists;
- user can explain high-level request path;
- no critical unknown blocks basic operation.

## Decision

```text
NOT_TESTED
```

Verified date:

```text

```

Reason:

```text

```

---

# G02 — Verified Request Flow

Status:

```text
NOT_STARTED
```

Logical Day:

```text
D02
```

## Goal

Prove that the user traced a real request through source code rather than repeating README architecture.

## Evidence A

Must identify verified code locations for:

- [ ] request entry;
- [ ] main service path;
- [ ] async boundary if present;
- [ ] producer/consumer if present;
- [ ] processing path;
- [ ] result/persistence path.

Record:

```text
File:
Class:
Method:
```

## Evidence B

- [ ] execute the traced flow;
- [ ] correlate logs/debugger/breakpoints with the documented flow.

## Evidence C

```text
N/A
```

Alternative verification:

```text
runtime traces / logs / debugger
```

## Evidence D — Oral Topics

- Start from an HTTP request and walk through the actual classes.
- Where does execution become asynchronous?
- Where is state persisted?
- Which steps are retried?
- How does the client receive final/progress results?
- Which part of your earlier architecture guess turned out to be wrong?

## Decision

```text
NOT_TESTED
```

---

# G03 — Backend Architecture

Status:

```text
NOT_STARTED
```

Logical Day:

```text
D03
```

## Goal

Reach at least L3 understanding of infrastructure directly used by the primary project.

Target components only if actually present:

- MySQL;
- Redis;
- MinIO;
- RocketMQ;
- Qdrant/vector store.

## Evidence A

For every component, record:

```text
real code caller
data stored/processed
reason used
```

## Evidence B

At least one practical verification relevant to the component.

Examples:

- inspect persisted record;
- inspect object storage;
- observe queue consume;
- inspect Redis state;
- execute retrieval.

## Evidence C

```text
N/A
```

unless an actual relevant metric is measured.

## Evidence D — Oral Topics

For each component:

- What project-specific problem does it solve?
- Why not replace it with another component already present?
- What breaks if it fails?
- What data consistency problem exists around it?
- Where is its real integration code?

## Blocking Debt

Any infrastructure explicitly planned for the resume but still only understood at L1/L2 is `CRITICAL`.

## Decision

```text
NOT_TESTED
```

---

# G04 — Agent Fundamentals

Status:

```text
NOT_STARTED
```

Logical Days:

```text
D04-D06
```

## Goal

Understand the Agent and retrieval mechanism beyond framework usage.

## Evidence A

- [ ] user-written minimal Agent Loop;
- [ ] actual DOVideo Agent path mapped;
- [ ] termination/retry behavior identified;
- [ ] retrieval context construction located.

## Evidence B

Minimum tests:

- [ ] normal tool call;
- [ ] tool failure or invalid result;
- [ ] loop termination;
- [ ] at least one project retrieval/agent flow.

## Evidence C

If no retrieval benchmark has been executed yet:

```text
N/A
```

Reason:

```text
Current Gate verifies mechanism understanding; retrieval quality benchmarking may be part of G05/G07.
```

## Evidence D — Oral Topics

- Agent vs one-shot LLM call;
- Agent vs deterministic workflow;
- who executes a Tool;
- how Tool result reaches the model;
- Planner purpose;
- Critic/reflection purpose if present;
- termination;
- context growth;
- why retrieval exists;
- vector vs keyword retrieval;
- quality/latency trade-off.

## Minimum Mastery

Core topics:

```text
L3
```

At least one personally implemented Agent mechanism:

```text
L4
```

## Decision

```text
NOT_TESTED
```

---

# G05 — First Resume-Relevant Enhancement

Status:

```text
NOT_STARTED
```

Logical Days:

```text
D07-D09
```

Feature:

```text
TBD
```

Problem Statement:

```text

```

Success Criteria:

```text

```

Out of Scope:

```text

```

## Evidence A — Code

User's first implementation commit:

```text
<SHA>
```

Post-review revision:

```text
<SHA>
```

Personal contribution:

```text

```

## Evidence B — Test

Required when applicable:

- [ ] normal;
- [ ] boundary;
- [ ] failure;
- [ ] retry/timeout;
- [ ] concurrency.

Command/result:

```text

```

## Evidence C — Metric

Experiment ID:

```text
EXP-XXX / N/A
```

If N/A:

Reason:

```text

```

## Evidence D — Oral Topics

- What problem existed before the enhancement?
- Why this design?
- What alternative did you reject?
- What failure scenario is still imperfect?
- What exactly did you personally write?
- Show the code.
- How did you test it?
- What claim can now be truthfully placed on the resume?

## Decision

```text
NOT_TESTED
```

---

# G06 — Backend Engineering

Status:

```text
NOT_STARTED
```

Logical Days:

```text
D10-D14
```

Secondary Project:

```text
Maoyan-Movie-System
```

## Goal

Prove ability to reason about a high-concurrency transaction path.

## Evidence A

Verified path:

```text
request
→ traffic control
→ stock
→ order
→ MQ
→ database
→ payment/cancel/compensation
```

User secondary development:

```text

```

Commit:

```text

```

## Evidence B

Relevant tests:

- [ ] duplicate request/message;
- [ ] stock boundary;
- [ ] failed downstream processing;
- [ ] idempotency;
- [ ] concurrency where practical.

## Evidence C

Benchmark may be deferred to G07 if not ready.

```text
EXP-XXX / N/A
```

## Evidence D — Oral Topics

- Why Redis here?
- Why Lua?
- Why lock or why no lock?
- Why MQ instead of only `@Async`/thread pool?
- How can duplicate consumption occur?
- What is the idempotency key?
- Redis success + DB failure: what happens?
- What consistency guarantee is actually provided?
- Where is transaction boundary?
- What happens under hotspot load?

## Decision

```text
NOT_TESTED
```

---

# G07 — Resume Ready

Status:

```text
NOT_STARTED
```

Logical Days:

```text
D15-D17
```

## Goal

Every important resume claim has evidence.

## Resume Claim Registry

### CLAIM-001

Proposed wording:

```text

```

Project:

```text

```

Personal contribution clear:

- [ ] yes

Code evidence:

```text
commit:
files:
```

Test evidence:

```text

```

Benchmark evidence:

```text
EXP-XXX / N/A
```

Oral defense:

```text
PASS / FAIL / NOT_TESTED
```

Status:

```text
NOT_READY / RESUME_READY
```

---

## Project Presentation

Primary project:

- [ ] 30-second version;
- [ ] 2-minute version;
- [ ] 5-minute version.

Secondary project:

- [ ] 30-second version;
- [ ] 2-minute version;
- [ ] 5-minute version.

## Attribution Rule

The user must explicitly distinguish:

- upstream open-source architecture;
- personal implementation;
- personal experiment/optimization.

## Decision

```text
NOT_TESTED
```

---

# G08 — Interview Ready

Status:

```text
NOT_STARTED
```

Logical Days:

```text
D18-D21
```

## Goal

Pass a realistic mock interview based on the actual resume.

## Required Evidence

- [ ] 80–120 relevant project-derived questions, without padding;
- [ ] Critical Interview Debt resolved;
- [ ] one complete mock interview;
- [ ] random code-location questions passed;
- [ ] failure/trade-off questions passed.

## Mock Interview Record

Date:

```text

```

Duration:

```text

```

Sections:

```text
self introduction:
primary project:
secondary project:
Java/backend:
Agent/RAG:
system design/algorithm:
```

Major failures:

- 
- 

## Final Decision

```text
NOT_TESTED
```

Reason:

```text

```

---

# Gate History

| Gate | First Attempt | Final Status | Pass Date | Evidence Commit |
|---|---|---|---|---|
| G01 | | | | |
| G02 | | | | |
| G03 | | | | |
| G04 | | | | |
| G05 | | | | |
| G06 | | | | |
| G07 | | | | |
| G08 | | | | |
