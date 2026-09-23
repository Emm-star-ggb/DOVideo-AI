# Architecture Knowledge Base

> Record only architecture that has been verified through source code, runtime behavior, or official project configuration.
>
> README claims may be noted as hypotheses, but should not be marked VERIFIED until checked.

---

# 0. Verification Legend

```text
HYPOTHESIS
Inferred from README/config but not yet traced.

PARTIALLY_VERIFIED
Some code/runtime evidence exists.

VERIFIED
Real code path and/or runtime evidence has been checked.

STALE
Was verified on an older commit and needs re-checking.
```

Last Verified Project Commit:

```text
<SHA>
```

Last Updated:

```text
YYYY-MM-DD
```

---

# 1. System Context

Project:

```text
DOVideo-AI
```

Primary user problem:

```text
<Fill after reading/running the project>
```

Main external dependencies:

```text
<LLM provider>
<ASR/OCR dependencies>
<object/vector/database/message services>
```

Status:

```text
HYPOTHESIS
```

---

# 2. High-Level Architecture

Do not treat this sketch as truth until components are verified.

```text
User
 │
 ▼
Frontend
 │
 ▼
Spring Boot / API
 │
 ├──────────────┬──────────────┬──────────────┐
 ▼              ▼              ▼              ▼
MySQL?         Redis?         Object Store?   MQ?
                                  │             │
                                  └──────┬──────┘
                                         ▼
                                    Processing
                                  /      |      \
                                ASR?    OCR?    Other?
                                  \      |      /
                                   Structured Context
                                         │
                                         ▼
                                   Vector Store?
                                         │
                                         ▼
                                      Retrieval
                                         │
                                         ▼
                                     Agent Flow
                                         │
                                         ▼
                                    Result / SSE?
```

Verified components:

- [ ] 
- [ ] 

Unverified:

- [ ] 
- [ ] 

---

# 3. ARCH-001 — Startup Architecture

Status:

```text
HYPOTHESIS
```

## Services Required

| Service | Why Needed | Config File | Runtime Evidence | Status |
|---|---|---|---|---|
| Backend | | | | |
| Frontend | | | | |
| MySQL | | | | |
| Redis | | | | |
| MQ | | | | |
| Object Storage | | | | |
| Vector Store | | | | |

## Startup Dependency Order

```text

```

## Failure Notes

What happens when each service is missing?

```text

```

---

# 4. ARCH-002 — End-to-End Request Flow

Status:

```text
HYPOTHESIS
```

Use one specific request.

Request:

```text

```

## Entry

```text
HTTP method/path:
File:
Class:
Method:
```

## Call Chain

```text
1.
2.
3.
4.
5.
```

For every step:

| Step | File/Class/Method | Input | Output | Sync/Async | Verified |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

## Runtime Evidence

Logs / debugger / request ID:

```text

```

## Open Questions

- 
- 

---

# 5. ARCH-003 — Asynchronous Processing

Status:

```text
HYPOTHESIS
```

## Async Boundary

Producer:

```text
File:
Class:
Method:
```

Message/event type:

```text

```

Consumer:

```text
File:
Class:
Method:
```

ACK / retry behavior:

```text

```

## Why Async?

Project-specific reason:

```text

```

Alternatives:

### Thread Pool / `@Async`

Pros:

```text

```

Cons:

```text

```

### Other MQ

Pros/cons:

```text

```

## Failure Scenarios

### Duplicate delivery

Current behavior:

```text

```

Tested?

```text
YES / NO
```

### Consumer crashes after side effect but before acknowledgement

Expected behavior:

```text

```

Observed behavior:

```text

```

### Queue unavailable

```text

```

---

# 6. ARCH-004 — Storage Responsibility

Status:

```text
HYPOTHESIS
```

| Component | Actual Data | Real Caller | Consistency Concern | Failure Impact | Status |
|---|---|---|---|---|---|
| MySQL | | | | | |
| Redis | | | | | |
| MinIO/Object Store | | | | | |
| Qdrant/Vector Store | | | | | |

Do not write generic definitions such as “Redis stores cache” unless the project really does so and the data is identified.

---

# 7. ARCH-005 — Video / Document Processing Pipeline

Status:

```text
HYPOTHESIS
```

Input:

```text

```

Pipeline:

```text
raw media
→ extraction
→ ASR/OCR
→ segmentation
→ structured representation
→ embedding/index
```

For each stage:

| Stage | Code Location | Input | Output | Failure Behavior | Verified |
|---|---|---|---|---|---|
| | | | | | |

---

# 8. ARCH-006 — Retrieval

Status:

```text
HYPOTHESIS
```

## Indexing

Chunk/segment unit:

```text

```

Metadata:

```text

```

Embedding model:

```text

```

Storage:

```text

```

## Query

Query transformation:

```text

```

Vector retrieval:

```text

```

Keyword/BM25:

```text

```

Fusion/RRF:

```text

```

Reranker:

```text

```

Final context construction:

```text

```

## Retrieval Questions

- What relevant evidence can be missed?
- What irrelevant evidence can be retrieved?
- How is Top-K selected?
- Is latency measured?
- Is Recall@K measurable with current data?

---

# 9. ARCH-007 — Agent Execution

Status:

```text
HYPOTHESIS
```

Do not force the project into this conceptual shape if actual code differs.

Possible conceptual view:

```text
User Goal
   │
   ▼
Planner?
   │
   ▼
Retrieval / Tools
   │
   ▼
Executor?
   │
   ▼
Critic / Validation?
   │
   ├── PASS → Final
   └── RETRY → Additional work
```

## Actual Entry

```text
File:
Class:
Method:
```

## State

What persistent/in-memory state exists?

```text

```

## Planner

Exists?

```text
YES / NO / PARTIAL
```

Input:

```text

```

Output:

```text

```

## Tool Calling

Tool registry:

```text

```

Tool execution:

```text

```

Tool result returned to model:

```text

```

## Critic / Validation

Exists?

```text

```

Decision structure:

```text

```

## Termination

Maximum iterations:

```text

```

Other termination conditions:

```text

```

Failure handling:

```text

```

## Checkpoint / Recovery

```text

```

---

# 10. ARCH-008 — Result Delivery

Status:

```text
HYPOTHESIS
```

Mechanism:

```text
SSE / WebSocket / polling / other
```

Server code:

```text

```

Client code:

```text

```

Reconnect behavior:

```text

```

Failure behavior:

```text

```

Why this mechanism:

```text

```

Alternative:

```text

```

---

# 11. Data Flow

Create one real example.

```text
Input
→ persisted metadata
→ processing artifact
→ searchable unit
→ retrieved evidence
→ Agent context
→ output
```

Example IDs/fields:

```text

```

Sensitive data considerations:

```text

```

---

# 12. Failure Map

| Failure | Expected System Behavior | Actual Code | Tested | Debt |
|---|---|---|---|---|
| Redis unavailable | | | | |
| MQ unavailable | | | | |
| DB slow/unavailable | | | | |
| Object store unavailable | | | | |
| Vector store unavailable | | | | |
| LLM timeout | | | | |
| invalid tool/model output | | | | |
| duplicate message | | | | |
| user repeats request | | | | |

---

# 13. Architecture Trade-Off Log

## ADR-LITE-001 — <Decision>

Problem:

```text

```

Current solution:

```text

```

Alternative A:

```text

```

Alternative B:

```text

```

Why current solution:

```text

```

Evidence:

```text

```

Uncertainty:

```text

```

---

# 14. Open Architecture Questions

## ARCH-Q001

Question:

```text

```

Why it matters:

```text

```

Status:

```text
OPEN
```

Answer/evidence when resolved:

```text

```

## ARCH-Q002

Question:

```text

```

Status:

```text
OPEN
```

---

# 15. Interview Map

For each important architecture component:

```text
Component:
Why:
Code:
Alternative:
Failure:
Test:
Metric:
Personal contribution:
```

This section should become the 5-minute project deep-dive outline.
