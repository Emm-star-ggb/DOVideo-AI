# Project-Derived Interview Q&A

> This is not an internet question dump.
>
> Questions should originate from actual project code, design choices, experiments, resume claims, or failed oral defenses.

---

# 0. Mastery Status

```text
NEW
LEARNING
FAILED_ORAL
ORAL_PENDING
MASTERED
```

A question may be `MASTERED` only when:

- user answers in own words;
- can point to real project code when applicable;
- can explain why;
- can name at least one alternative when relevant;
- understands at least one failure scenario;
- passes closed-book oral follow-up.

---

# 1. Summary

| Category | New | Learning | Failed | Mastered |
|---|---:|---:|---:|---:|
| Architecture | 0 | 0 | 0 | 0 |
| Agent | 0 | 0 | 0 | 0 |
| RAG/Retrieval | 0 | 0 | 0 | 0 |
| Java/Spring | 0 | 0 | 0 | 0 |
| Redis | 0 | 0 | 0 | 0 |
| MySQL | 0 | 0 | 0 | 0 |
| MQ | 0 | 0 | 0 | 0 |
| System Design | 0 | 0 | 0 | 0 |

---

# 2. Question Index

| ID | Category | Question | Related Gate | Status |
|---|---|---|---|---|
| QA-001 | Architecture | | G01 | NEW |

---

# 3. QA-001 — Template

Category:

```text
Architecture / Agent / RAG / Java / Redis / MySQL / MQ / Network / System Design
```

Status:

```text
NEW
```

Created From:

```text
DXX / commit / review / benchmark / mock interview
```

Related Gate:

```text
GXX
```

Related Resume Claim:

```text
NONE / CLAIM-XXX
```

---

## Question

> 

---

## My Answer

Write from memory. Do not paste documentation.

```text

```

---

## Project Evidence

Repository:

```text

```

File:

```text

```

Class:

```text

```

Method:

```text

```

Commit:

```text

```

---

## Why This Design Exists

```text

```

---

## Alternative

```text

```

Trade-off:

```text

```

---

## Failure Scenario

```text

```

---

## Test / Metric Evidence

Test:

```text

```

Benchmark:

```text
EXP-XXX / N/A
```

---

## Follow-Up Questions

1. 
2. 
3. 

---

## ChatGPT Oral History

### Attempt 1

Date:

```text

```

Result:

```text
PASS / FAIL
```

Failure reason:

```text

```

### Attempt 2

Date:

```text

```

Result:

```text

```

---

## Final Mastery

```text
NEW
```

Reason:

```text

```

---

# 4. Required Question Families

Generate questions only as related code is learned.

## Architecture

Examples:

- Why is this processing async?
- Where is the async boundary?
- What data lives in each storage component?
- Why SSE instead of polling/WebSocket?
- What happens if dependency X is unavailable?

## Agent

Examples:

- Agent vs normal LLM call?
- Who actually executes tools?
- How is a tool result returned to the model?
- How does the loop terminate?
- What prevents infinite loops?
- What does Planner solve?
- What does Critic/validation solve?
- How do retries affect cost/latency?

## RAG / Retrieval

Examples:

- Why retrieval instead of full context?
- Vector retrieval limitations?
- Keyword retrieval limitations?
- Why hybrid retrieval?
- Why RRF/additive weighting?
- Why reranker?
- How choose Top-K?
- How prove retrieval improved?

## MQ

Examples:

- Why MQ instead of `@Async`?
- Why this MQ?
- Can a message be delivered twice?
- Consumer crashes after side effect but before ACK?
- How is idempotency implemented?
- What happens when backlog grows?

## Redis

Examples:

- What exactly is stored in Redis in this project?
- Why Lua?
- Why a distributed lock?
- What race does the lock protect?
- What happens if Redis is unavailable?
- How does cache consistency work?

## MySQL

Examples:

- What is transaction boundary?
- What index supports this query?
- Optimistic vs pessimistic lock?
- What prevents duplicate order?
- What happens on partial failure?

---

# 5. Resume Bullet Explosion Template

For every resume bullet, create questions.

Resume claim:

```text

```

Explode into:

1. Problem?
2. Why this solution?
3. Exact code?
4. Personal contribution?
5. Alternative?
6. Failure?
7. Test?
8. Metric?
9. Limitation?
10. What would you improve next?

Question IDs:

```text
QA-...
```

---

# 6. Mock Interview Set

## Primary Project — 5-Minute Drill

Start:

> Please introduce the project and your personal contribution.

Follow-up pool:

- 
- 
- 

## Secondary Project — 5-Minute Drill

Follow-up pool:

- 
- 
- 

## Random Code Drill

Ask:

> Show me the exact class/method implementing X.

Targets:

- 
- 
- 

---

# 7. Mastered Questions

Move nothing manually into this section unless oral status is `MASTERED`.

| ID | Question | Last Pass Date | Gate |
|---|---|---|---|
| | | | |
