# Benchmark & Experiment Ledger

> This file is the **only approved source of quantitative claims for the resume**.

---

# 0. Benchmark Constitution

Never invent benchmark results.

A quantitative claim is valid only when all required fields exist:

- experiment ID;
- code commit;
- environment;
- workload/dataset;
- command;
- raw output path;
- metric definition;
- result;
- limitations.

If the experiment has not actually run:

```text
Status = PLANNED
```

not `DONE`.

Do not compare two numbers produced under materially different environments unless the difference is explicitly disclosed.

---

# 1. Status

```text
PLANNED
RUNNING
DONE
INVALID
SUPERSEDED
```

---

# 2. Experiment Index

| Experiment | Question | Project | Status | Commit | Resume Eligible |
|---|---|---|---|---|---|
| EXP-001 | | | PLANNED | | NO |

---

# 3. EXP-001 — Template

Status:

```text
PLANNED
```

Date:

```text
YYYY-MM-DD
```

Project:

```text
DOVideo-AI / Maoyan / Other
```

Owner:

```text
User
```

---

## 3.1 Question

What specific question are we trying to answer?

```text
Example:
Does hybrid retrieval improve Recall@5 over vector-only retrieval on my labeled query set?
```

---

## 3.2 Hypothesis

```text

```

What result would falsify the hypothesis?

```text

```

---

## 3.3 Code Version

Repository:

```text
<URL>
```

Branch:

```text

```

Commit:

```text
<SHA>
```

Uncommitted changes:

```text
NO / YES
```

If YES, benchmark is not resume-eligible until reproducible from a committed state.

---

## 3.4 Environment

Date/time:

```text

```

Machine:

```text
CPU:
RAM:
GPU:
OS:
```

Runtime:

```text
JDK:
Python:
Node:
Docker:
```

Service versions:

```text
MySQL:
Redis:
RocketMQ:
Vector Store:
```

Model configuration:

```text
LLM:
Embedding:
Reranker:
Temperature:
Other:
```

---

## 3.5 Dataset / Workload

Type:

```text
retrieval / API load / end-to-end / concurrency / other
```

Size:

```text

```

Source:

```text

```

Ground Truth construction:

```text

```

Data path:

```text
evaluation/data/...
```

Potential bias:

```text

```

---

## 3.6 Metric Definitions

Define each metric in plain language.

### Metric 1

Name:

```text

```

Definition:

```text

```

Why it matters:

```text

```

### Metric 2

Name:

```text

```

Definition:

```text

```

---

## 3.7 Baseline

Description:

```text

```

Config:

```text

```

Command:

```bash

```

Raw output:

```text
evaluation/results/EXP-001-baseline.*
```

Result:

```text

```

---

## 3.8 Candidate / Change

Description:

```text

```

What changed from baseline:

```text

```

Command:

```bash

```

Raw output:

```text
evaluation/results/EXP-001-candidate.*
```

Result:

```text

```

---

## 3.9 Result Table

| Metric | Baseline | Candidate | Difference | Better? |
|---|---:|---:|---:|---|
| | | | | |

---

## 3.10 Correctness Checks

- [ ] same dataset/workload;
- [ ] same hardware/environment or difference disclosed;
- [ ] same model/config unless model is the variable;
- [ ] warmup policy documented;
- [ ] repeated runs if variance matters;
- [ ] no cherry-picked run;
- [ ] raw outputs saved.

Number of repetitions:

```text

```

Variance / range:

```text

```

---

## 3.11 Analysis

What likely caused the result?

```text

```

Unexpected behavior:

```text

```

Confounders:

```text

```

---

## 3.12 Limitations

Examples:

- small dataset;
- synthetic workload;
- manually labeled ground truth;
- single model;
- single machine;
- no production traffic;
- short benchmark duration.

Actual limitations:

- 
- 

---

## 3.13 Conclusion

```text

```

Was the hypothesis supported?

```text
YES / NO / INCONCLUSIVE
```

---

## 3.14 Resume Eligibility

```text
NO
```

Requirements before switching to YES:

- [ ] committed code;
- [ ] reproducible command;
- [ ] raw result stored;
- [ ] metric definition valid;
- [ ] limitations understood;
- [ ] ChatGPT oral defense passed.

Approved resume wording:

```text
<Only fill after evidence + oral defense>
```

---

# 4. Suggested Agent/Retrieval Metrics

Use only if relevant.

## Retrieval

Possible metrics:

- Recall@K;
- Precision@K;
- MRR;
- nDCG;
- retrieval latency.

Do not use Recall@K without reasonable ground truth.

## Agent

Possible metrics:

- task success rate;
- tool-call success rate;
- invalid tool-call rate;
- average iterations;
- token use;
- cost;
- end-to-end latency.

Define task success before measuring it.

---

# 5. Suggested Backend Metrics

Possible metrics:

- throughput/QPS;
- requests/sec;
- P50;
- P95;
- P99;
- error rate;
- timeout rate;
- DB connection utilization;
- MQ backlog;
- CPU;
- memory.

Load parameters should include:

```text
concurrency:
duration:
request mix:
data size:
warmup:
```

---

# 6. Invalid Benchmark Examples

Mark experiment `INVALID` if:

- README numbers were copied;
- results were estimated;
- environment changed without disclosure;
- test data changed between baseline and candidate;
- only the best run was kept;
- metric definition is unclear;
- raw outputs are missing;
- user cannot explain what the metric means.

---

# 7. Resume Metric Export

Only copy rows from here after `Resume Eligible = YES`.

| Claim ID | Experiment | Approved Metric Statement | Gate |
|---|---|---|---|
| | | | |
