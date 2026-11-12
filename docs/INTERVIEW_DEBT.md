# Interview Debt Ledger

> Interview Debt = technology/design already used or likely to appear on the resume, but the user cannot yet defend it.

This is not a generic study TODO list.

---

# 0. Priority

## CRITICAL

One or more:

- appears on the resume;
- central to a resume bullet;
- user cannot explain code already committed;
- AI contributed core code the user cannot explain;
- blocks a Gate.

## NORMAL

Relevant to project, but not currently a central resume claim.

## OPTIONAL

Useful depth, but not required for current Gate or resume.

---

# 1. Status

```text
OPEN
LEARNING
ORAL_PENDING
RESOLVED
DEFERRED
```

---

# 2. Summary

| Priority | Open | Learning | Oral Pending | Resolved |
|---|---:|---:|---:|---:|
| CRITICAL | 0 | 0 | 0 | 0 |
| NORMAL | 0 | 0 | 0 | 0 |
| OPTIONAL | 0 | 0 | 0 | 0 |

Critical Debt blocking current Gate:

```text
NONE
```

---

# 3. Debt Index

| ID | Topic | Priority | Source | Deadline | Status |
|---|---|---|---|---|---|
| DEBT-001 | | CRITICAL | | | OPEN |

---

# 4. DEBT-001 — Template

Topic:

```text

```

Status:

```text
OPEN
```

Priority:

```text
CRITICAL / NORMAL / OPTIONAL
```

Created:

```text
YYYY-MM-DD
```

Source:

```text
DXX / GXX / QA-XXX / code review / mock interview
```

Related Resume Claim:

```text
NONE / CLAIM-XXX
```

---

## Why This Is Debt

What have I already used or claimed?

```text

```

What can I not explain?

```text

```

Why would an interviewer reasonably ask this?

```text

```

---

## Questions I Cannot Answer Yet

- 
- 
- 

---

## Code Evidence I Need To Locate

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

Current status:

```text
NOT_FOUND / FOUND_NOT_UNDERSTOOD / VERIFIED
```

---

## Required Learning

Minimum concepts:

- 
- 

Do not expand into unrelated theory.

---

## Required Practical Evidence

To resolve this debt, I must do:

- [ ] locate real code;
- [ ] reproduce behavior;
- [ ] test one failure/edge case;
- [ ] explain one alternative;
- [ ] pass ChatGPT oral follow-up.

Additional metric if relevant:

```text
EXP-XXX / N/A
```

---

## My Current Answer

Write in my own words.

```text

```

---

## Failure Scenarios

```text

```

---

## Alternatives / Trade-Offs

Alternative A:

```text

```

Why not chosen:

```text

```

Alternative B:

```text

```

---

## Deadline

Resolve before:

```text
GXX / interview date
```

---

## Resolution Evidence

Commit:

```text

```

Test:

```text

```

Benchmark:

```text
EXP-XXX / N/A
```

Oral defense:

```text
NOT_TESTED / PASS / FAIL
```

Resolved date:

```text

```

Final status:

```text
OPEN
```

---

# 5. Example Debt Topics To Add Only When They Actually Occur

Do not pre-create these as fake debt. Add them when encountered.

Potential examples:

- RocketMQ duplicate delivery;
- Redis Lua atomicity;
- Redisson lock granularity;
- DB transaction propagation;
- cache/database consistency;
- Agent loop termination;
- Critic retry limit;
- tool-call invalid output;
- retrieval Top-K choice;
- SSE reconnect semantics;
- checkpoint recovery;
- vector retrieval evaluation;
- model timeout retry strategy.

---

# 6. Weekly / 3-Day Review

Every 3 days, review:

1. Which Critical Debt grew?
2. Which resume keyword has only L1/L2 understanding?
3. Which debt came from AI-written code?
4. Which debt can be removed by shrinking the resume claim?
5. Which debt must block the next Gate?

Record:

```text
Date:
New Critical Debt:
Resolved:
Deferred:
Gate impact:
```


---

# V2 Learning-State vs Interview-Debt Policy (2026-11-12)

**Do not create Interview Debt for first exposure to an untaught concept.** Track such topics in the teaching plan or QA record instead. Existing historical debt IDs and evidence remain unchanged.

## Learning state (separate from existing debt priority and workflow status)

- NOT_LEARNED — not yet taught; not debt and never a Gate failure on its own.
- LEARNING — taught and currently practicing; may be a learning note, not automatically debt.
- NEEDS_REVIEW — after instruction/practice, the user still cannot reliably explain or apply a relevant concept; record cause and retest.
- CRITICAL — demonstrated unresolved gap in resume-critical, personally adopted or Gate-blocking knowledge; must cite actual evidence, not a first-attempt guess.

Existing priority CRITICAL/NORMAL/OPTIONAL and workflow OPEN/LEARNING/ORAL_PENDING/RESOLVED/DEFERRED remain valid. These new learning states do **not** replace those fields or silently reclassify historical entries.

## Additional record fields

```text
Learning State: NEEDS_REVIEW / CRITICAL (or track NOT_LEARNED / LEARNING outside debt index)
Teaching Module: M1–M6
Taught On: YYYY-MM-DD / NOT_VERIFIED
Observed Gap: user's actual explanation or failed test (do not fabricate)
Root Cause: concept / source mapping / implementation / expression / unknown
Remediation: specific small learning or engineering action
Review Date: YYYY-MM-DD / TBD
Retest Date: YYYY-MM-DD / TBD
Retest Result: NOT_TESTED / PARTIAL / PASS / FAIL
Related QA / Gate / Resume Claim: identifiers or NONE
Evidence: verified path / commit / oral record
```

Review unresolved gaps at the three-day review; only mark RESOLVED when the required explanation, code/test evidence and retest standard are actually met. Never treat a classroom comprehension check as a formal Gate oral defense.
