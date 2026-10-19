# Daily Learning Log

> Append new days. Do not overwrite historical entries.

---

# Current Snapshot

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

Current Gate Status:

```text
NOT_STARTED
```

Primary Project:

```text
DOVideo-AI
```

Current Branch:

```text
learning
```

Snapshot Base HEAD:

```text
998595831b1fcb6a17a78d8397c3dc093aefc752
```

Last Evidence Commit:

```text
6a7c06f866525ff60446f963bd0b8d9bd2dc344a
```

> `Snapshot Base HEAD` 是开始本次 Gate 0 补救前，GitHub `learning` 分支的真实 HEAD。
>
> `Last Evidence Commit` is the latest commit that materially proves a learning result. It does **not** have to equal the current Git `HEAD`.
>
> 本次 docs remediation commit 完成后会产生新的 HEAD。不要为了把新 SHA 写回这里再次制造一个 commit。当前实时 HEAD 始终以 Git/GitHub 为准。
>
> Check the live repository state with:
>
> ```bash
> git branch --show-current
> git rev-parse --short HEAD
> ```

Last Updated:

```text
2026-09-24
```

---

# Commit / SHA Recording Rules

## 1. Do Not Mirror HEAD Manually

Git is the source of truth for current `HEAD`. Do not update this file after every documentation-only commit just to keep a SHA looking current.

## 2. What Counts as an Evidence Commit?

Record commits that materially prove learning progress, for example:

```text
core implementation
post-review correction
tests
benchmark/evaluation work
verified architecture investigation
```

Usually do not treat these as learning evidence:

```text
formatting
typos
recording an older SHA
minor Markdown cleanup
```

## 3. No Self-Reference Loop

Example history:

```text
34cd567  feat: implement initial agent tracing
56ef789  test: add agent tracing tests
78ab901  docs: record D07 evidence
```

Correct record:

```text
Feature Evidence: 34cd567
Test Evidence:    56ef789
```

Do not edit the file again merely to write `78ab901`, because that would create another SHA and an endless update cycle.

## 4. Daily Git Evidence Should Distinguish Roles

For meaningful feature work, prefer recording:

```text
Start-of-day HEAD:
User first-attempt commit:
Post-review revision commit:
Test commit:
Benchmark commit:
Last Evidence Commit:
Documentation commit: optional
```

Not every field is required every day.

## 5. Relationship to Other Files

```text
DAILY_LOG
→ records today's evidence commits

GATES
→ records commits that prove the Gate

BENCHMARK
→ records the exact commit benchmarked

LEARNING_PLAN Last Verified Commit
→ records the state actually verified by ChatGPT
```

A new commit does not automatically replace all older SHA references.

---

# Daily Entry Template

Copy this section for every learning day.

---

## DXX — YYYY-MM-DD

### 1. Start-of-Day Gate State

Current Gate:

```text
GXX
```

Status before work:

```text
NOT_STARTED / IN_PROGRESS / FAIL / PASS
```

If previous Gate was FAIL:

```text
Remediation target:
Why it failed:
```

---

### 2. Today's Minimum Goal

Must finish:

- [ ] 
- [ ] 
- [ ] 

Explicitly out of scope today:

- 
- 

---

### 3. Closed-Book Recall Before Study

Without reading notes, answer briefly:

#### Q1

> 

My answer:

```text

```

#### Q2

> 

My answer:

```text

```

#### Q3

> 

My answer:

```text

```

Weak points discovered:

- 
- 

---

### 4. My Initial Understanding / Design

Before Codex changes core logic, write what I currently think.

Problem:

```text

```

My proposed design:

```text

```

Why:

```text

```

Known uncertainty:

```text

```

---

### 5. Work I Personally Completed

Only list things I actually did.

- [ ] 
- [ ] 
- [ ] 

Important debugging performed:

```text

```

---

### 6. Codex Usage Record

Mode used:

```text
NONE / LEARNING / REVIEW / TEST / EXAM
```

What I asked Codex to do:

```text

```

What Codex actually contributed:

```text

```

Did Codex modify learning-critical core logic?

```text
NO / YES
```

If YES:

Why was this allowed?

```text

```

Can I explain every such change?

```text
YES / NO
```

If NO, create Critical Interview Debt.

---

### 7. Git Evidence

Repository:

```text
<URL>
```

Branch:

```text
<branch>
```

Start-of-day HEAD:

```text
<SHA>
```

Relevant commits created today:

```text
<SHA> <message>
<SHA> <message>
```

User first-attempt commit, if applicable:

```text
<SHA / N/A>
```

Post-review revision commit, if applicable:

```text
<SHA / N/A>
```

Test commit, if applicable:

```text
<SHA / N/A>
```

Benchmark/evaluation commit, if applicable:

```text
<SHA / N/A>
```

Last Evidence Commit for today's learning outcome:

```text
<SHA>
```

Documentation-only commit:

```text
<SHA / optional / do not self-reference>
```

Files changed:

- 
- 

Evidence mapping:

```text
Claim / Gate requirement:
→ supporting commit:

Claim / Gate requirement:
→ supporting commit:
```

---

### 8. Test Evidence

Test type:

```text
unit / integration / e2e / concurrency / startup / other
```

Command:

```bash

```

Result:

```text

```

Summary:

```text
Passed:
Failed:
Skipped:
```

Failures not fixed:

- 

---

### 9. Benchmark Evidence

Status:

```text
N/A / PLANNED / EXECUTED
```

If N/A:

Reason:

```text

```

Alternative verification:

```text

```

If EXECUTED:

Experiment ID:

```text
EXP-XXX
```

Raw result:

```text
evaluation/results/...
```

Key metrics:

```text

```

Do not copy a metric to the resume unless the experiment is fully recorded in `BENCHMARK.md`.

---

### 10. Architecture Evidence

Architecture entries updated:

```text
ARCH-XXX
```

Real code locations verified today:

```text
File:
Class:
Method:
```

Unverified assumptions remaining:

- 
- 

---

### 11. What I Can Now Explain Without Notes

#### Topic

Mastery estimate:

```text
L1 / L2 / L3 / L4
```

My explanation:

```text

```

Evidence:

```text
code/test/experiment
```

---

### 12. What I Still Cannot Explain

- 
- 
- 

Debt entries created:

```text
DEBT-XXX
DEBT-XXX
```

---

### 13. Interview Questions Added

```text
QA-XXX
QA-XXX
```

Questions I failed today:

```text
QA-XXX
```

---

### 14. Gate Evidence Checklist

Gate:

```text
GXX
```

Evidence A — Code / execution:

- [ ] complete

Evidence B — Test:

- [ ] complete

Evidence C — Metric or N/A rationale:

- [ ] complete

Evidence D — Oral defense:

- [ ] complete

---

### 15. ChatGPT Gate Result

Decision:

```text
NOT_TESTED / PASS / FAIL
```

Date:

```text
YYYY-MM-DD
```

Reason:

```text

```

Questions failed:

- 
- 

Required remediation:

- [ ] 
- [ ] 

---

### 16. Resume Evidence Produced Today

Candidate claim:

```text

```

Status:

```text
NOT_READY / EVIDENCE_READY / ORAL_PENDING / RESUME_READY
```

Why:

```text

```

---

### 17. End-of-Day Self Assessment

Confidence:

```text
1 / 2 / 3 / 4 / 5
```

Most important thing I learned:

```text

```

Most dangerous interview weakness:

```text

```

What I would do differently tomorrow:

```text

```

---

### 18. Next Logical Step

If Gate PASS:

```text

```

If Gate FAIL:

```text

```

---

# D00 — 2026-09-24

## 1. Start-of-Day Gate State

Current Gate:

```text
G00
```

Status before work:

```text
IN_PROGRESS
```

Remediation target:

```text
建立真正的 Gate 0 状态，
补齐 D00 初始化记录，
并让学习监督系统的 Git 状态与真实仓库状态一致。
```

## 2. Today's Minimum Goal

Must finish:

- [x]  验证仓库为个人 Fork
- [x]  验证 learning 分支存在
- [x]  验证根目录 AGENTS.md
- [x]  验证 docs/ 中 7 个学习控制文件
- [x]  在 GATES.md 建立 G00
- [x]  在 DAILY_LOG.md 建立 D00
- [x]  记录 Bootstrap initialization commit
- [x]  记录本次补救开始前真实 GitHub HEAD

Explicitly out of scope today:

- DOVideo-AI 启动
- Agent 学习
- RAG 学习
- 业务代码修改
- application test
- Benchmark
- Codex 修改业务代码

------

## 3. Bootstrap Facts Verified

Repository:

```text
Emm-star-ggb/DOVideo-AI
```

Fork Parent:

```text
Xiaoc7r/DOVideo-AI
```

Current Branch:

```text
learning
```

AGENTS.md:

```text
present at repository root
```

Required Learning Documents:

```text
docs/ARCHITECTURE.md
docs/BENCHMARK.md
docs/DAILY_LOG.md
docs/GATES.md
docs/INTERVIEW_DEBT.md
docs/INTERVIEW_QA.md
docs/LEARNING_PLAN.md
```

Bootstrap Initialization Commit:

```text
8299f644f156aa1a01b1ac4b7ea0cad8aff22e7d
```

Pre-remediation HEAD:

```text
998595831b1fcb6a17a78d8397c3dc093aefc752
```

------

## 4. Work Completed

- [x]  学习监督目录结构已经存在
- [x]  AGENTS.md 已存在
- [x]  learning 分支已存在
- [x]  初始化 commit 已存在
- [x]  Gate 0 所需 Git / Docs 证据已确认
- [x]  本阶段没有启动项目
- [x]  本阶段没有修改业务代码

------

## 5. Codex Usage Record

Mode used:

```text
NONE
```

Codex modified business code:

```text
NO
```

Reason:

```text
Gate 0 只允许进行学习监督系统初始化，
禁止 Codex 修改 DOVideo-AI 业务代码。
```

------

## 6. Git Evidence

Repository:

```text
https://github.com/Emm-star-ggb/DOVideo-AI
```

Branch:

```text
learning
```

Start-of-day / Pre-remediation HEAD:

```text
998595831b1fcb6a17a78d8397c3dc093aefc752
```

Bootstrap initialization evidence:

```text
8299f644f156aa1a01b1ac4b7ea0cad8aff22e7d
docs: initialize autumn recruitment learning system
```

Files changed in Gate 0 remediation commit 6a7c06f:

```text
AGENTS.md
docs/DAILY_LOG.md
docs/GATES.md
docs/LEARNING_PLAN.md

AGENTS.md change:
Added Commit / SHA Evidence Rules requested during supervision setup.

LEARNING_PLAN.md change:
Repository placeholder regression detected and corrected in the following docs-only correction commit.

Business code changed:
NONE
```

Business code changed:

```text
NONE
```

Gate 0 remediation commit:

```text
This D00 entry is part of the Gate 0 remediation docs commit.

Do not self-reference that commit SHA here.
Use Git/GitHub HEAD after commit to obtain the resulting SHA.
```

Evidence mapping:

```text
Learning supervision system initialization
→ 8299f644f156aa1a01b1ac4b7ea0cad8aff22e7d

Gate 0 state before remediation
→ 998595831b1fcb6a17a78d8397c3dc093aefc752
```

------

## 7. Test Evidence

Status:

```text
N/A
```

Reason:

```text
G00 validates repository and learning-supervision initialization.
It does not validate DOVideo-AI runtime behavior.
```

Alternative verification:

```text
GitHub repository metadata
+ fork relationship
+ learning branch existence
+ required file existence
+ commit history
```

------

## 8. Benchmark Evidence

Status:

```text
N/A
```

Reason:

```text
Gate 0 contains no performance, retrieval-quality,
Agent-quality, or application-runtime claim.
```

------

## 9. Architecture Evidence

Status:

```text
N/A
```

Reason:

```text
Architecture study has not started.
Architecture belongs to D01+ and must not be pulled into Gate 0.
```

------

## 10. What I Can Explain After Bootstrap

Topic:

```text
Learning Supervision Workflow
```

Expected knowledge:

```text
AGENTS.md controls AI/Codex working rules.

GATES.md controls learning progression.

DAILY_LOG.md records actual daily evidence.

GitHub is the source of truth for code and commits.

Codex reviews/tests after my own first attempt.

ChatGPT performs final closed-book Gate verification.
```

Mastery status:

```text
ORAL_PENDING
```

Do not mark MASTERED before ChatGPT oral defense.

------

## 11. Interview Debt

```text
N/A
```

Reason:

```text
Gate 0 is supervision-system bootstrap rather than resume technical learning.
```

------

## 12. Gate Evidence Checklist

Gate:

```text
G00
```

Evidence A — Git / repository / docs:

- [x] complete

Evidence B — Test:

- [x]  N/A with valid reason

Evidence C — Benchmark:

- [x]  N/A with valid reason

Evidence D — Oral Defense:

- [x]  complete

------

## 13. ChatGPT Gate Result

Decision:

```text
PASS
```

Date:

```text
2026-09-24
```

Reason:

```text
Gate 0 bootstrap evidence complete.
Closed-book oral defense passed.
```

Required oral topics:

```text
1. AGENTS.md 的作用是什么？
2. 为什么 GATES.md 是学习进度的 source of truth？
3. User → Codex → ChatGPT 的正确学习闭环是什么？
4. 为什么 G00 PASS 前不能进入 D01？
```

------

## 14. Resume Evidence Produced Today

```text
NONE
```

Reason:

```text
Gate 0 是学习系统初始化，
不是简历技术成果。
```

------

## 15. End-of-Day State

Current Logical Day:

```text
D00
```

Current Gate:

```text
G00
```

Gate Status:

```text
PASS
```

Business Code Modified:

```text
NO
```

DOVideo-AI Started:

```text
NO
```

Agent/RAG Study Started:

```text
NO
```

------

## 16. Next Logical Step

```text
进行 Gate 0 闭卷口试。

只有 G00 = PASS 后，
才允许进入 D01 — Run DOVideo-AI。
```

# D01 — YYYY-MM-DD

> Do not start D01 until G00 = PASS.



---

## D01 — Environment Bootstrap Debugging Record (2026-10-06)

### Current Gate

```text
G01 — System Bootstrap
Status: IN_PROGRESS
```

### Environment blockers discovered

1. Local branch was initially behind `origin/learning` by one documentation commit. The branch was safely fast-forwarded to `b4dc321` after confirming the worktree was clean and the README difference was only LF/CRLF noise.
2. Docker CLI / Docker Desktop was not installed on Windows, so the required Compose-based middleware stack could not start.
3. Local Java was JDK 17 (`D:\\Java\\JDK\\jdk17`) while the project requires JDK 21.
4. WSL2 setup initially failed while enabling `VirtualMachinePlatform` with DISM error 14098 (component store corruption), then succeeded on a later attempt.
5. After reboot, both `VirtualMachinePlatform` and `Microsoft-Windows-Subsystem-Linux` reported Enabled, `hypervisorlaunchtype` was Auto, firmware virtualization was reported enabled, and `HypervisorPresent=True`.
6. Despite those prerequisites, `wsl --status` continued to report that WSL2 could not start because virtualization was unavailable. Further low-level diagnosis was limited because `hcsdiag` was not present.

### Decision

To avoid spending the D01 learning block on Windows virtualization-stack repair, switch the runtime environment to a Linux VM in VMware Workstation Pro and continue G01 there.

Planned environment:

```text
VMware Workstation Pro
→ Ubuntu 24.04 LTS
→ Docker Engine + Docker Compose
→ JDK 21
→ Node.js
→ FFmpeg / Tesseract
→ DOVideo-AI middleware
→ backend
→ frontend
→ one real business flow
```

### Debugging evidence / learning notes

```text
docker command not found
→ Docker Desktop not installed
→ attempted WSL2 prerequisites
→ Windows optional component failure (14098)
→ component later enabled successfully
→ hypervisor present and virtualization firmware enabled
→ WSL2 still reports virtualization unavailable
→ stop sinking time into host OS repair
→ move project runtime to VMware Ubuntu
```

This is a blocker record only. G01 is not passed yet; execution, startup verification, one real business flow, and oral defense are still required.


---

## D01 — G01 Oral Defense Progress (2026-10-12)

Gate: G01 — System Bootstrap. Oral defense remains in progress; overall Gate has NOT passed.

### Operational evidence (observed in prior interactive session)
- Ubuntu VM middleware: MySQL, Redis, MinIO, Qdrant, RocketMQ started.
- Backend /health returned UP; frontend started.
- User exercised registration/login, video upload/playback, AI analysis and report display.
- Metric: N/A per G01. Outstanding quality observations: OCR stderr contamination and partial Critic validation; not a separate G01 performance threshold.

### Oral defense: long-running HTTP / asynchronous video analysis

**Initial response — FAIL:** User said synchronous HTTP may cause waiting/blockage; conflated chunk upload with AI task completion; called RocketMQ a cache.

**First retry — FAIL:** User correctly recognized HTTP 202 as acceptance, not completion, but was unsure of RocketMQ and reasons for async execution.

**Ordering exercise — PASS:** User answered `C E D A B` for submit request → enqueue task → HTTP 202 → background analysis → frontend checks completion. Assessor noted enqueue/202 ordering is implementation-dependent.

**100-task / 5-worker queue scenario — PASS (user-reported recovery):** User reported two follow-up questions were lost from chat UI, and reported the assistant had passed the scenario. Exact original answers unavailable; do not reconstruct or quote them as verbatim.

**Sync vs async comparison — PASS (2026-10-12):**
- Question: Scheme A holds HTTP request for 3-minute analysis; scheme B acknowledges with HTTP 202 and later status queries. Compare user experience and system risks.
- User original answer to user-experience part: “方案B，方案B的进度是可观看有掌握的，可以极大避免用户在等待过程中产生的焦虑与不确定性。”
- User original answer to system-risk part: “对于系统，如果任务接收和分析过程中发生了什么错误，http只能返回错误结果，无法确认是哪一环节出错，而方案B先让http返回接收结果，可以避免这一情况”
- Assessor: user-experience PASS; system-risk answer partial because synchronous systems can also log and diagnose errors, and 202 alone does not solve diagnostics. Follow-up required.
- Follow-up: Gateway closes HTTP connection at 60s while AI analysis takes 180s. Explain effects under A and B.
- User original A: “http连接在分析任务完成之前就断开，客户无法接收到分析任务的返回结果（我有疑问这时候分析任务还会接着进行吗还是因为http连接超时所以报错而停止呢？）”
- User original B: “后端返回http 202后，http端口就被解放了，之后的任务状态会由任务状态查询来反映，因此避免了http端口因长时间等待而超时报错的问题”
- Assessment: PASS for the HTTP timeout / async-status concept. Technical refinement: an HTTP connection closing does not *necessarily* stop backend work; behavior depends on cancellation propagation and execution architecture. The connection/request resources, not the TCP listening port itself, are released.

### Next oral topics
- Explain infrastructure services and storage responsibilities; failure scenarios; startup configuration changes; and the concrete evidence of the end-to-end operation, sampling as required by docs/GATES.md.
- Overall G01 oral defense and final PASS are pending. No business source changes in this documentation update.


### G01 Oral Defense — Storage Responsibilities (2026-10-13)

Result: PASS after follow-up. This is a question-level PASS, not a G01 Gate PASS.

Initial answers:
- MySQL: user knew it stores user data but could not name other data types; partial.
- Redis vs MySQL: user explained relational persistent storage versus in-memory cache and latency; basic PASS, with correction that MySQL also uses memory and indexes.
- MinIO: user knew it stores uploaded video files but was unsure why object storage is preferred over database BLOBs; partial.

Follow-up question: for a 2GB uploaded video, choose storage for video bytes, video metadata, and frequently queried analysis-task status.

User answer A (verbatim):
> MinIO，视频文件本身可以作为对象存储，适合于MinIO的存储方式。存入MySQL中对于数据库容量，备份，复制和维护的负担比较重。Redis同理。可能还与视频文件之后的使用频率有关？这个只是猜想。

User answer B (verbatim):
> 优先存在MySQL中，这些信息属于“用户上传一次视频”的业务信息，适合存于MySQL中进行长久保存。Redis适合存储经常使用的数据，且一般数据设有ttl。而MinIO以对象存储访问，将用户的一次操作作为对象存储感觉不太合适（关于MinIO我还是了解不多，可能有错误地方，你可以多纠正）

User answer C (verbatim):
> 被频繁查询的分析任务，如果有Redis，那么该任务应该被存入了Redis，在之后的查询中直接从内存中访问数据，响应速度快。Redis中没有对应数据，只能说明该数据没有存储在Redis中，不能说明任务不存在，需要再从MySQL进行查询，如果MySQL中也没有对应数据，才能说明该任务不存在。

Assessment:
- A PASS: MinIO for large video objects; avoids database BLOB operational overhead. Access frequency alone is not a deciding factor.
- B PASS: MySQL for structured metadata and durable business relationships; object key can refer to MinIO content.
- C PASS: understands cache miss versus absence of durable task state. Redis caching and MySQL source-of-truth are design choices, not yet verified as DOVideo-AI implementation.
- Architecture specifics must be confirmed from project source code in G02/G03. No claim of verified schema or Redis task-state cache.

Next oral topic: other infrastructure services, dependency failure, startup configuration, or evidence of end-to-end execution. G01 overall remains IN_PROGRESS.


### G01 Oral Defense — MinIO Failure Scenario (2026-10-13)

Question: MinIO becomes unavailable while MySQL, Redis, RocketMQ and backend remain running. Discuss new uploads, viewing previous AI reports, and troubleshooting.

User answer 1 (verbatim):
> 用户上传新视频时，可能会在上传视频时进行报错，因为MinIO服务停止，视频文件无法进行保存。

User answer 2 (verbatim):
> 用户查看之前已经生成的 AI 分析报告时，不一定会失败。之前生成的AI分析报告，应该是作为“用户进行了一次视频分析”业务中的结果数据存储与MySQL中，只是MinIO出现问题的话，MySQL的数据查询功能应该无碍，所以查看之前的分析报告应该不会失败。

User answer 3 (verbatim):
> 先判断是哪一环节出现问题，是否是因为网络原因，排除后查看日志中的相关信息。

Assessor decision: PASS for G01-level understanding.
- Correctly identifies object storage failure as a likely upload blocker.
- Correctly recognizes that a single dependency outage does not necessarily block all other functionality.
- Troubleshooting direction (network, logs) is acceptable at G01, but should later be strengthened by targeted MinIO health, object-access and backend-exception checks.
- Important qualification: MySQL report storage is the user's hypothesis, not a source-verified DOVideo-AI implementation fact. A report could still depend on MinIO-backed images/video or object data.
- This is a question-level PASS only. G01 overall remains IN_PROGRESS pending other oral topics and final evidence review.


### G01 Oral Defense — End-to-End Execution Evidence (2026-10-13)

Question 1: Does /health UP prove upload and AI analysis work?
User answer (verbatim):
> 仅仅看到后端 `/health` 返回 `UP`，能不证明视频上传和 AI 分析功能都正常。后端 `/health` 返回 `UP`，只能证明后端服务确实启动且可以运行，无法作为视频上传和AI分析功能正常的证据，要想确认功能正常，还需进行实际的业务操作，得到结果。

Question 2: What actual operations demonstrate a real business flow?
User answer (verbatim):
> 上传了四次视频，HTTP端口返回202，同时前端页面上显示上传成功。进行了四次AI分析，返回了分析失败的结果和分析成功的报告。

Question 3: How to describe successful upload/report with some analysis errors?
User answer (verbatim):
> 核心流程已跑通但存在局部问题，视频可以上传，AI分析成功生成报告，说明两个核心功能已经实现，但分析结果不如意，那么说明在AI分析这一块还有改进空间。

Assessment: PASS for G01-level oral understanding of operational evidence.
- Correctly distinguishes service health from end-to-end feature testing.
- Reports four upload attempts and four analysis attempts with both failed and successful results. These are user-reported observations; not independently verified by this documentation commit.
- Correctly avoids claiming full-system success from partial outcomes.
- Clarification: HTTP 202 acknowledges acceptance, not final persistence. Successful playback is stronger upload/storage evidence.
- Clarification: exceptions/missing output are functional failures, while low-quality analysis content is a quality issue; they require separate investigation.
- G01 overall remains pending final evidence review and remaining oral topics; no full Gate PASS declared.


### G01 Oral Defense — Startup Configuration and Troubleshooting (2026-10-13)

Status: PARTIAL, FOLLOW-UP PENDING. No question-level PASS yet.

Question 1: Why cannot JDK 17 be assumed compatible with project requiring JDK 21?
User answer (verbatim):
> 源项目中使用的是jdk21，不能直接使用JDK17是因为两个版本的JDK之间虽然大体上没变化但一些部分有差别。

Assessment: partial. Recognizes version differences but not source/API/bytecode compatibility; e.g. Java 21 bytecode may cause UnsupportedClassVersionError on Java 17.

Question 2: At least three startup failure checks and order.
User answer (verbatim):
> 检查网络状态和存储空间，根据日志进行排查。

Assessment: follow-up needed. Log, network and storage are relevant, but answer omitted Java version, startup configuration, and dependency service connectivity.

Question 3: Explain AI model change and Tesseract Chinese package.
User answer (verbatim):
> 调整AI模型配置，是为了解决一开始AI分析任务流程进行中因为配置中的规定的分析限时而中断导致分析失败的问题，我们先尝试了延长任务时限，发现仍无法解决而且每次重新分析后任务会从中断处继续进行，我们猜测是这个模型的问题，加之分析时长再加长对于用户来说不算友好，故选择了更换模型，由先前的Qwen3.5-4B换为DeepSeek-V4-Flash。安装Tesseract中文包是为了解决AI分析过程中无法识别视频中的中文这一问题。

Assessment: PASS for describing observed troubleshooting and OCR Chinese language support. Model change does not by itself establish definitive root cause of original failure.

Next: targeted follow-up on startup diagnostic ordering and Java compatibility. G01 overall remains pending.


### G01 Oral Defense — Startup Troubleshooting Follow-up (2026-10-13)

Status: A PASS, B PARTIAL; further targeted follow-up required. Overall G01 not yet passed.

Scenario: UnsupportedClassVersionError: class file version 65.0, runtime recognizes up to 61.0; then Connection refused.

User original answer:
> A、最可能的原因是JDK版本不兼容，更换项目要求的JDK版本。B、先查看其余后端中间件的状态，看它们是否正常启动。再排查日志，看看哪里出现了问题。之后再看网络和存储。

Assessment:
- A PASS: identifies Java runtime incompatibility; version 65 corresponds to Java 21 and version 61 to Java 17. Confirm java -version and actual runtime selection.
- B PARTIAL: checking middleware, logs and network is directionally correct, but user did not specify three concrete diagnostic checks. Connection refused calls for verifying exact target host, port, listener and service/container status. Storage capacity is not the immediate implication of this error.
- Next: narrow concrete troubleshooting follow-up; do not declare overall question PASS yet.


### G01 Oral Defense — Redis Connection Refused Follow-up (2026-10-13)

Status: PARTIAL; practical troubleshooting follow-up still pending.

Scenario: RedisConnectionFailureException; unable to connect to Redis at localhost:6379; Connection refused.

Question 1 (identify service, host, port), user answer:
> Redis依赖出现了连接问题。目标地址为localhost和端口为6379。
Assessment: PASS.

Question 2 (give a Docker or Redis command to check service), user answer:
> 不知道。
Assessment: FAIL for concrete command recall. Teaching provided: docker ps; docker logs <Redis容器名>; docker exec <Redis容器名> redis-cli ping.

Question 3 (container running but still connection refused), user answer:
> 检查端口是否正确或被占用。
Assessment: PARTIAL. Port check is relevant; also verify host/port config and whether backend runs on host or in a separate Docker container. localhost is namespace-dependent; a container's localhost is not another container.

No full question PASS or G01 PASS declared. Next: short recheck of concrete Redis verification and Docker network address distinction.


### G01 Oral Defense — Startup Troubleshooting Final Recheck (2026-10-13)

Question A: How to check Redis container/service from Ubuntu?
User verbatim:
> docker exec <Redis容器名> redis-cli ping

Question B: Why may localhost:6379 fail when backend and Redis run in different Docker containers?
User verbatim:
> 因为这时localhost指向的是后端容器自己，而Redis在另一个容器中，两个容器需要通过Docker网络中的Redis服务名连接。

Assessor: PASS for both, and PASS for the overall startup troubleshooting oral question after iterative follow-ups.
- docker exec ... redis-cli ping tests whether Redis responds inside its container; docker ps is the direct container-running check.
- Container-local localhost refers to that container, not a separate Redis container. Use an appropriate service name on the same configured Docker network.
- Previous failed/partial attempts remain preserved above as learning history.
- Overall G01 Gate decision NOT YET PASS: final A/B/C/D evidence reconciliation remains necessary.


## D01 — G01 final verification (2026-10-13)

Final decision: PASS. Evidence A: user confirmed learning branch; Docker ps -a showed six middleware containers Up (MySQL and Redis healthy); Spring Boot JDK 21 started on port 9090; Vite frontend started on port 5173 and browser rendered logged-in homepage. Existing MinIO container was restarted after quay.io image pull returned HTTP 401.

Evidence B: curl -i http://localhost:9090/health returned HTTP 200 and JSON data UP. curl -I http://localhost:5173 returned HTTP 200. User explicitly confirmed opening/uploading a video, playback and seeking, submitting AI analysis, final task success and opening the report. E2E outcome is user-reported, not an independently captured automated test.

Evidence C: N/A; bootstrap checks operability, not performance. Alternative: health and E2E.

Evidence D: PASS after the recorded oral defense and targeted follow-ups for asynchronous HTTP/MQ, storage responsibilities, dependency failures, startup configuration, Docker networking and E2E proof.

Deferred: intermittent AI analysis failures, OCR stderr contamination, report quality and MinIO image-registry reproducibility. No benchmark or business-code change claimed.


---

## D01 — G01 Oral Defense Completeness Audit (2026-10-13)

Purpose: reconcile all G01 oral-defense exchanges available in the conversation with the entries above. This is an archival supplement, not a new examination or a change to the G01 Gate decision.

### Question-by-question archive index

| Sequence | Oral topic | Final outcome | Existing record / completeness |
| --- | --- | --- | --- |
| 1 | Why long-running AI processing should not block synchronous HTTP | PASS after multiple follow-ups | Existing 2026-10-12 async section; first two user responses previously summarized rather than quoted |
| 2 | Five-step async ordering C/E/D/A/B | PASS | Existing async section, answer recorded as C E D A B |
| 3 | 100 incoming tasks with capacity for 5; queueing and worker outage | PASS (user-reported recovery) | Existing async section; original answer unavailable after chat UI rollback |
| 4 | 3-minute sync HTTP versus HTTP 202 + status lookup, including 60-second gateway timeout | PASS | Existing async section, user answer and follow-up verbatim |
| 5 | MySQL/Redis/MinIO responsibilities and 2GB video follow-up | PASS | Existing storage responsibilities section, follow-up answers verbatim |
| 6 | MinIO outage effects on upload, report viewing, and diagnosis | PASS | Existing MinIO failure section, answers verbatim |
| 7 | /health versus real upload/playback/analysis evidence | PASS | Existing end-to-end evidence section, answers verbatim |
| 8 | JDK 21 versus JDK 17; startup diagnosis; AI model and Tesseract | PASS after follow-ups | Existing startup and Redis sections, initial and follow-up answers verbatim |

### Supplemental recoverable user statements for the early async question

Initial user answer, as preserved in earlier conversation summary (not a verbatim full transcript):
> 同步HTTP请求可能导致视频分析时间变长，多个任务等待一个HTTP端口造成堵塞，一个视频分析要好长时间，用户体验不佳。视频上传采用分片+整合...每一个分片处理完...判断分析任务完成。RocketMQ起到一个缓存作用.

Assessment at the time: FAIL; conflated chunk upload with AI task execution and described MQ as cache. Ellipses above reflect an incomplete recovered quote; they do NOT represent exact omitted user text.

First retry, recoverable answer fragments (not complete verbatim response):
- HTTP 202 indicates request accepted, not analysis finished.
- On RocketMQ: “不知道”.
- On frontend: “根据返回的分析结果”.
- On asynchronous advantages: “不知道”.
Assessment at the time: FAIL; later recovered via ordering, queueing and timeout follow-ups.

### Missing chat UI rounds: question text recovered, answer not recoverable

The user explicitly reported two follow-up rounds had disappeared from the chat UI after answering the ordering exercise. The user later reconstructed the question prompts:

**Queueing and worker-outage question:**
> 假如有100个任务提交，但服务器只能同时处理5个视频，在方案A直连和方案B使用RocketMQ中，①如果使用方案B，剩下的95个任务怎么办？②若是后台AI视频分析程序突然无法执行，方案B与直连相比有什么潜在优势？

User stated the question was answered and passed. Original answer and exact assessor wording are not available; retain PASS as user-reported, not as an independently recovered verbatim transcript.

**Synchronous versus asynchronous HTTP question:**
> 方案A等待3分钟视频分析完成后再响应和方案B任务接收后先返回http202再任务状态查询①对用户来说，哪个方案更好，优势在哪里？②对于系统来说，方案A会有什么隐患？方案B有解决方法吗？

The user said they were composing the answer when chat rolled back. This question was subsequently re-asked and fully answered, with PASS and original answer recorded in the earlier async section. Do not treat the interrupted draft as an additional completed round.

### Completeness and integrity statement

- All G01 question topics and their final outcomes known from the current conversation have a persistent index in this file.
- Where exact answers are available, original answers remain in the existing sections above; this audit avoids duplicating those long answers.
- Where text was lost, preserve only recoverable fragments and explicitly label missing material. Do not invent missing answers or silently upgrade user-reported evidence.
- D00/G00 oral record in this file records the four oral topics and PASS, but not complete verbatim Q&A. This audit is scoped to the G01 oral exchanges discussed here; a complete G00 transcript is not available in the present conversation.
- Current G01 Gate decision in docs/GATES.md was already PASS at the time of this audit. This supplement does not change Gate status or claim a new runtime test.

---

# Reusable Oral / Test Attempt Archive Templates

> Use these templates as **append-only entries within the active DXX day** after every oral answer or test run. Keep prior FAIL/PARTIAL attempts. Do not substitute a summary for a recoverable original answer. This section defines a template; it is not an executed test or oral result.

## Oral attempt — ORAL-DXX-001

- Date/time and timezone: `YYYY-MM-DD HH:MM TZ / UNKNOWN`
- Logical Day / Gate: `DXX / GXX`
- Topic / linked QA or DEBT ID: `...`
- Attempt number / status: `1 / PASS | FAIL | PARTIAL | FOLLOW_UP_PENDING`
- Full examiner question (verbatim):

> ...

- User's original answer (verbatim):

> ...

- Follow-up question(s) and user answer(s), verbatim:

> ...

- Assessment and reason: `...`
- Correct understanding / corrections / remaining uncertainty: `...`
- Final question-level decision: `PASS | FAIL | FOLLOW_UP_PENDING`
- Gate-level status (separate): `...`
- Evidence limitations: `verbatim / summary / user-reported / missing`
- Archive verification: `GitHub commit SHA and link reported after write; do not self-reference in same commit`

## Test attempt — TEST-DXX-001

- Date/time and timezone: `YYYY-MM-DD HH:MM TZ / UNKNOWN`
- Logical Day / Gate: `DXX / GXX`
- Operator: `User | Codex | ChatGPT`
- Test type / objective: `unit | integration | E2E | startup | benchmark | manual | other`
- Environment and exact code revision: `...`
- Commands / manual procedure (exact):

```bash
# ...
```

- Expected outcome: `...`
- Observed result / stdout / stderr / screenshot or raw artifact path: `...`
- Exit code and pass/fail/skipped counts (if applicable): `...`
- Status: `PASS | FAIL | NOT_RUN | BLOCKED`
- Failure cause, limitations and next action: `...`
- Evidence provenance: `directly executed / user-provided / Codex-reported`
- Archive verification: `GitHub commit SHA and link reported after write; do not self-reference in same commit`

## Archiving discipline

1. Append a record **after each attempt**, including failures and partial oral answers, before moving to the next question or test.
2. Preserve the original answer/output and distinguish user-reported results from tool-verified observations.
3. Add related QA/debt entries when warranted, and update Gate/learning state only when evidence changes.
4. Commit, re-fetch and verify the actual repository content. If unsuccessful, label the record `NOT ARCHIVED` and pause or obtain explicit permission to continue.
5. Redact secrets; never write credentials, tokens, or private keys into Git.


### ORAL-D02-001 — Controller and Service identification (2026-10-14, +08:00)

Gate: G02; topic: D02-01, request entry and Spring MVC basics.
Evidence provenance: user-provided terminal output and verbatim chat answers; source path cross-checked on GitHub. No runtime trace was executed.

First attempt:
Q1: 哪个 Controller 负责接收 AI 视频分析请求？请给出文件路径、类名和方法名。
User answer (verbatim):
> 这个问题我不知道，仅能猜测一下，你看一下我说的对不对，可以向我普及一下相关知识。我猜是`` `AnalysisController ``。文件路径为`server/src/main/java/com/example/server/controller/AnalysisController.java`，类名和方法名不知道，感觉好像没有出现类似内容。
Assessment: PARTIAL. Correct file/controller identification, missing Java method name.

Q2: 这个 Controller 调用了哪个 Service 方法？
User answer (verbatim):
> 调用了`@RequestMapping`、`@PostMapping`、`@GetMapping`（在此声明。我对Spring-boot框架没有了解，如果你觉得我需要补这方面知识，你可以为我列出清单，我们可以之后补）。
Assessment: FAIL. Request mapping annotations are not Service methods.

Second attempt — closed-book recheck:
Q1: `@PostMapping("/ai")` 和 `aiAnalyze` 分别是什么？为什么它们不是一回事？
User answer (verbatim):
> @PostMapping("/ai")是注解，用来声明接收POST请求的接口。  aiAnalyze是Controler中的方法。前者是调用的接口声明，后者是使用的方法。
Assessment: PASS. Clarification: annotation maps request to handler; it does not itself invoke the method.

Q2: `AnalysisController` 为什么还要调用 `AnalysisDispatchService`？Controller 和 Service 的职责有什么区别？
User answer (verbatim):
> 前者需要使用后者中的方法，有些方法写在Service层比起写在Contorller层更加易于维护。Controller主要负责接收请求，参数和调用服务，而Service负责具体业务的执行。
Assessment: PASS.

Q3: 如果请求 `POST /analysis/ai` 返回 HTTP 202，能不能直接认定 AI 分析已经成功生成报告？为什么？
User answer (verbatim):
> 不能。因为返回HTTP 202只能说明分析任务被接收，不能证明AI分析依据成果生成报告，是否成功生成分析报告要看前端是否返回了可以查看的报告。
Assessment: PASS. Clarification: use task status, persisted report and logs as additional evidence.

Final question-level decision: PASS (second attempt 3/3). G02 gate status remains NOT_STARTED / pending actual request trace, execution evidence and final oral defense. Do not conflate question-level PASS with Gate PASS.
Archive timestamp precision: date known; exact time not recorded.


### ORAL-D02-002 — Dispatch submission first attempt (2026-10-14, +08:00)

Gate: G02. Status: PARTIAL (Q1 PARTIAL, Q2 FAIL, Q3 PASS, Q4 PASS); targeted follow-up pending. Evidence: user-reported source search and original answers in chat, not a runtime execution trace.

Q1. 为什么要先执行 Redis 的 setIfAbsent，再发送 RocketMQ 消息？如果 setIfAbsent 返回 false，会发生什么？
User answer (verbatim):
> 先执行Redis的setIfAbsent进行去重判断后再创建分析任务，创建成功后返回true，才能进行下一步发送RocketMQ，以保证任务不被重复创建占用空间和任务que'shu'chuang'ji确实创建。从代码来看如果返回false，SubmissionResult.DUPLICATE无法返回，不过SubmissionResult.DUPLICATE是什么？
Assessment: PARTIAL. Redis true means active key set, not task creation; false causes early return DUPLICATE.

Q2. 为什么限流失败后要执行 redisTemplate.delete(activeKey)？如果不删除，可能有什么问题？
User answer (verbatim):
> 不知道。可能为了防止占据空间或者消息队列。
Assessment: FAIL. Cleanup prevents a rejected submission from retaining an active marker and blocking retry.

Q3. rocketMQTemplate.convertAndSend() 返回后，能否认为 AI 分析已经完成？为什么？
User answer (verbatim):
> 不能，rocketMQTemplate.convertAndSend() 返回只能说明新的任务消息AnalysisTaskMsgch创建成功，AI分析是另外的进程进行，无法由它确定是否分析完成。
Assessment: PASS with qualification: successful send is evidence of message submission, not consumer execution or final completion; separate process not yet verified.

Q4. 如果 MQ 消息发送成功，但 taskEventService.publishAnalysis() 抛出异常，最终返回 ACCEPTED 还是 FAILED？为什么？
User answer (verbatim):
> ACCEPTED。相应的try-catch语句中对于taskEventService.publishAnalysis() 抛出异常只有返回日志警告消息，return语句仍然返回ACCEPTED。不过这个功能是干嘛的？
Assessment: PASS. Event publication failure is logged and does not change accepted MQ submission.

Teaching clarification given: enum SubmissionResult, one-statement if early return, active-key cleanup on rate limiting, distinction between MQ message and status notification. Follow-up pending. Gate G02 not passed.


#### ORAL-D02-002 — Second attempt / targeted recheck (2026-10-14, +08:00)

Q1. 用户连续两次提交相同视频、相同分析目标的任务。第一次已经成功写入 Redis 活动标记，尚未过期。第二次执行 setIfAbsent() 时会返回什么？submit() 接下来会怎样执行？
User answer (verbatim):
> 第二次执行会返回False。submit()接下来会返回DUPLICATE，然后退出方法。
Assessment: PASS.

Q2. 用户第一次提交时成功写入 Redis 活动标记，但随后被限流。如果没有执行 redisTemplate.delete(activeKey)，用户稍后重新提交时可能遇到什么问题？
User answer (verbatim):
> 如果Redis活动标记未过期的话，可能会显示重复提交提交失败，但任务实际上并没有被接收。如果Redis活动标记过期的话，并且消息队列已经有空闲的话，可以成功写入创建Redis KEY并接着传递给RocketMQ。
Assessment: PASS with qualification: key expiry alone does not guarantee acceptance; rate limit and MQ send must also succeed. MQ spare capacity is not explicitly checked in this method.

ORAL-D02-002 final question-level decision: PASS after targeted recheck (2/2). First-attempt PARTIAL/FAIL preserved above. G02 overall still pending consumer tracing, runtime evidence and final defense.


### D02-03 — Source navigation micro-practice (2026-10-14)

- **问题**：已知消费者中调用 \`rejectionReason(msg)\`，如何自主定位方法定义并读取实现？
- **核心方法**：使用 \`rg -n 'rejectionReason\('\` 区分调用位置（第 84 行）和定义位置（第 216 行）；使用 \`sed -n '215,250p'\` 查看目标方法；首次误写 \`sed -n '215p,250p'\`，自行修正。
- **掌握情况**：**PASS（源码定位与命令实践）**。用户提供了成功执行的终端输出；方法的业务语义尚需后续独立口试验证。G02 整体仍进行中。


### ORAL-D02-003 — Message validation and poison-message handling (2026-10-14)

Q1: \`rejectionReason()\` 返回 \`null\` 和非 \`null\` 分别代表什么？
User answer (verbatim):
> \`rejectionReason()\` 返回 \`null\` 代表消息通过结构性检验；返回非 \`null\`代表消息未通过结构性检验。
Assessment: PASS.

Q2: 为什么结构性非法的消息不能简单地反复重试？根据 \`discardPoisonMessage()\` 的注释，系统准备如何处理这些消息？
User answer (verbatim):
> 为什么结构性非法的消息不能简单地反复重试？不知道。不知道，注释看不太懂，落台账和转投是什么意思？
Assessment: NOT YET PASS; needs explanation and targeted recheck. Teaching provided: structural invalidity cannot be repaired by unchanged retry; \`failedTaskService.record\` records failure and \`rocketMQTemplate.convertAndSend(deadLetterTopic, msg)\` forwards to failure topic. Per code comment at least one trace must succeed before acknowledging invalid message.

Status: PARTIAL (Q1 PASS, Q2 pending). G02 overall remains IN_PROGRESS.


#### ORAL-D02-003 — Second attempt / targeted recheck (2026-10-14, +08:00)

Q1: 一条 RocketMQ 消息缺少 \`mediaId\`，消费者重试 3 次，为什么仍然可能无法成功？这与数据库短暂不可用有什么区别？
User answer (verbatim):
> 因为消息缺少必要信息，无法通过结构性检验，无论多少次都没办法成功。与数据库短暂不可用的暂时性、可修复性错误不同，该任务属于消息结构性错误，无法通过重试恢复。
Assessment: PASS.

Q2: 对于结构性非法消息，\`failedTaskService.record()\` 和向 \`deadLetterTopic\` 发送消息分别有什么作用？为什么至少要有一种方式成功？
User answer (verbatim):
> failedTaskService.record() 可以记录失败任务消息的信息，向 deadLetterTopic 发送消息将异常消息转投到失败主题。至少有一种方式成功才能说明异常消息得到了处理，为了避免系统将异常消息忽略，无法处理。
Assessment: PASS. Qualification: traceable handling is not successful repair or analysis completion.

Final decision for ORAL-D02-003: PASS after second attempt (2/2). First-attempt PARTIAL preserved above. G02 overall remains IN_PROGRESS; normal-message execution path and runtime evidence still pending.


### ORAL-D02-004 — First attempt (2026-10-14, +08:00)

Q1: \`lock.tryLock()\` 返回 \`false\` 后，为什么不会继续执行 AI 分析？这里使用分布式锁的主要目的是什么？
User answer (verbatim):
> 不知道。
Assessment: FAIL.

Q2: 在什么情况下，消费者会直接复用历史分析结果，而不调用 \`aiService.asyncAnalyze()\`？
User answer (verbatim):
> 出现AgentLoopService.BudgetExceededException e错误时，和Exception e并且!permanent && acquired && attempt > 0 && attempt < MAX_DELIVERY_ATTEMPTS。不知道。
Assessment: FAIL; confused result-reuse path with exception handlers.

Q3: 某次 AI 分析发生可恢复异常，当前是第 1 次投递。代码为什么设置 \`retrying = true\`，并且不立即删除 \`activeKey\`？
User answer (verbatim):
> retrying = true为了标志这个消息是失败后重试的，立即删除activeKey的话，前端会以为任务结束，注释说会重新塞进来一份相同工作是为什么？
Assessment: PARTIAL; recognized retry state and activity flag, asked why another same request could be admitted.

Overall ORAL-D02-004 first attempt: FAIL. Teaching given on \`tryLock\` and \`return\`, result reuse via completedKey/checkpoint/reuseResult, and Redis \`setIfAbsent(activeKey)\` duplicate suppression during retry. Preserve this first attempt; recheck pending. G02 overall IN_PROGRESS.


#### ORAL-D02-004 — Second attempt / targeted recheck (2026-10-16, +08:00)

Q1: 消费者 A 已经持有某任务的锁，消费者 B 的 \`tryLock()\` 返回 \`false\`。B 接下来会怎样？为什么？
User answer (verbatim):
> B接下来会退出onMessage（）方法，等待消费者持有的锁释放出来后才能执行。
Assessment: PARTIAL. B exits current \`onMessage()\` invocation; zero-argument \`tryLock()\` does not wait for the lock or automatically resume after A unlocks.

Q2: 历史结果复用成功后，为什么不会执行 \`aiService.asyncAnalyze()\`？指出起决定作用的语句。
User answer (verbatim):
> 历史结果复用成功后，直接return退出onMessage（）方法。
Assessment: PASS.

Q3: 原任务正在等待 RocketMQ 重试时，如果 \`activeKey\` 被提前删除，提交端再次收到同样的分析请求，可能发生什么？
User answer (verbatim):
> setIfAbsent判断该任务未执行，将该分析请求传递给RecketMQ，此时有两条相同的任务等待RecketMQ执行。
Assessment: PASS, with precision note: \`setIfAbsent\` tests absence of the Redis key, not actual AI execution; a duplicate message may be submitted.

Overall ORAL-D02-004 after second attempt: PARTIAL (Q1 misconception remains). First-attempt FAIL preserved. G02 IN_PROGRESS.


#### ORAL-D02-004 — Third attempt / lock semantics recheck (2026-10-16, +08:00)

Q1: 假设消费者 A 持有锁，消费者 B 执行 \`tryLock()\` 返回 \`false\`，随后 A 释放锁。B 刚才退出的 \`onMessage()\` 会不会自动恢复执行？
User answer (verbatim):
> 不会自动恢复执行。但这样因为无法获取锁而暂停的任务该怎么办呢？不能依靠用户重新提交任务吧，后面有对应的处理吗？
Assessment: PASS for non-resumption. User raised valid further investigation about potential loss of work on lock contention and normal consumer return.

Q2: 如果 B 想再次获取这把锁，需要满足什么条件？
User answer (verbatim):
> 消费者B调用onMessage()方法。
Assessment: PASS (a new invocation must retry acquisition).

Overall ORAL-D02-004: PASS after third attempt (2/2 recheck); prior FAIL and PARTIAL retained. Open investigation: does \`if (!acquired) return;\` acknowledge a still-needed task without a retry/recovery mechanism? G02 remains IN_PROGRESS.


### ORAL-D02-005 — First attempt (2026-10-16, +08:00)

Q1: 为什么 \`asyncAnalyze()\` 不能仅凭方法名就判断它一定启动了新线程？目前源码能证明什么？
User answer (verbatim):
> 仅靠方法名无法确定该方法中具体进行了什么操作，是否启动了新线程等信息还需要看具体的源码。能证明什么？
Assessment: PARTIAL. Correct that name is insufficient; missing observed synchronous direct call path and lack of visible explicit thread creation in supplied method.

Q2: \`checkpointService.loadResult()\` 返回已有有效结果时，代码会怎样处理？还会执行 \`agentLoopService.run()\` 吗？
User answer (verbatim):
> checkpointService.loadResult() 返回已有有效结果时，代码会接着进行执行persistResult(mediaFile, agentState);
> telemetry.increment(traceId, "checkpointHits", 1);然后return退出方法。
Assessment: PASS.

Q3: \`agentLoopService.run()\` 抛出普通运行时异常后，\`AiService\` 会怎样处理？消费者为什么能够感知到失败？
User answer (verbatim):
> 执行对于的catch语句，catch (RuntimeException e) {
>                 telemetry.stage(traceId, TaskStage.AGENT_LOOP.name(), agentStarted, false);
>                 throw e;抛出异常e。之后执行对应的catch语句catch (Exception e) {
>             try {
>                 checkpointService.saveFailure(mediaId, userGoal, resolvedMode, currentStage, e);
>             } catch (RuntimeException checkpointError) {
>                 e.addSuppressed(checkpointError);
>                 log.error("agent_failure_checkpoint_write_failed traceId={} mediaId={}",
>                         traceId, mediaId, checkpointError);
>             }
>             log.error("agent_analysis_failed traceId={} mediaId={}", traceId, mediaId, e);
>             if (e instanceof AgentLoopService.BudgetExceededException budgetExceeded) {
>                 throw budgetExceeded;
>             }
>             throw new IllegalStateException("AI analysis failed", e);
>         } 。不知道。
Assessment: PARTIAL. Located inner and outer catch, but did not explain exception propagation to \`VideoAnalysisConsumer.onMessage()\`.

Overall ORAL-D02-005 first attempt: PARTIAL; targeted recheck needed for Q1 and Q3. G02 overall IN_PROGRESS.


#### ORAL-D02-005 — Second attempt / targeted recheck (2026-10-16, +08:00)

Q1: HTTP 接口已经返回 202，但 RocketMQ 消费者正在执行 \`aiService.asyncAnalyze()\`。为什么这不代表 \`asyncAnalyze()\` 一定创建了新线程？
User answer (verbatim):
> 因为asyncAnalyze()方法中没有显式创建线程、提交线程池任务或通过 @Async 调度的代码，所以无法通过aiService.asyncAnalyze()正在执行来确定一定创建了新线程。
Assessment: PASS.

Q2: \`agentLoopService.run()\` 抛出异常后，为什么 \`VideoAnalysisConsumer.onMessage()\` 的 \`catch\` 能捕获它？请用自己的话描述异常从 \`AgentLoopService\` 到消费者的传播过程。
User answer (verbatim):
> 不知道。
Assessment: FAIL. Teaching given: exception propagates up call stack, inner \`catch\` rethrows, outer \`catch\` saves failure and wraps ordinary exception, consumer catches propagated exception.

Overall ORAL-D02-005 after second attempt: PARTIAL (Q1 PASS, Q2 pending). First attempt retained. G02 IN_PROGRESS.


#### ORAL-D02-005 — Third attempt / basic Java exception propagation (2026-10-16, +08:00)

Question: 为什么异常是在 `B()` 中抛出的，却能够被 `A()` 中的 `catch` 捕获？
User answer (verbatim):
> 因为A()中调用了B()，A()调用B()时，B()抛出异常，A()检测到异常转向执行catch语句，异常被A()中的catch捕获
Assessment: PASS for basic exception propagation. Precision: exception propagates through the call stack; A does not explicitly poll for errors. Project-specific explanation of AgentLoopService → AiService → VideoAnalysisConsumer remains to be verified before ORAL-D02-005 overall PASS. G02 IN_PROGRESS.


#### ORAL-D02-005 — Fourth attempt / project-level exception propagation (2026-10-16, +08:00)

Question: `AgentLoopService.run()` 抛出普通运行时异常后，异常经过 `AiService.asyncAnalyze()` 的哪两层处理？为什么最终能够进入 `VideoAnalysisConsumer.onMessage()` 的 `catch (Exception e)`？
User answer (verbatim):
> `AgentLoopService.run()` 抛出普通运行时异常后，  异常先经过AiService.asyncAnalyze()内层的catch，异常未得到处理，之后又传递给AiService.asyncAnalyze()外层catch，外层catch再抛出异常，因为VideoAnalysisConsumer.onMessage()调用了AiService.asyncAnalyze()，所以异常向上传递到消费者
Assessment: PASS. Inner catch records failed telemetry and rethrows; outer catch attempts to save failure checkpoint and wraps ordinary exception in IllegalStateException, which propagates to caller's catch.

Final ORAL-D02-005: PASS after fourth attempt (Q1 threading semantics, Q2 checkpoint early return, Q3 exception propagation). Previous attempts preserved. D02-05 oral complete; full G02 remains IN_PROGRESS pending additional source tracing and runtime evidence.


#### ORAL-D02-006 — First attempt (2026-10-19, +08:00)

Q1: 为什么 \`resolveContext()\` 在尝试获取分布式锁后，还要再次检查 Checkpoint 和内容复用结果？如果不重新检查，可能出现什么问题？
User answer (verbatim):
> 不知道。这个checkpoint是干什么的？请为我介绍一下。
Assessment: FAIL. User requested explanation of checkpoint and double-check after lock.

Q2: 两个消费者同时处理相同视频。如果其中一个正在构建上下文，另一个等待超时且没有命中复用结果，后者会怎样处理？这与 Consumer 中 \`tryLock()\` 失败后的处理有什么区别？
User answer (verbatim):
> 不知道。
Assessment: FAIL. Needs contrast of normal return vs throw and upstream retry handling.

Q3: Agent 成功生成结果后，\`persistResult()\` 做了什么？最终报告保存在哪里？为什么还要调用 \`invalidateUserList()\`？
User answer (verbatim):
> 执行了下面语句:
>         mediaFile.setAiSummary(agentState.result().toMarkdown());
>         mediaFileMapper.updateById(mediaFile);
>         mediaService.invalidateUserList(mediaFile.getUserId());
> 将结果转化为markdown，写入aiSummary。更新数据库记录，是相关用户列表缓存失效。前两布我都知道为什么，最后一步呢？是为什么啊？
Assessment: PARTIAL. Identifies Markdown conversion, MediaFile update and cache invalidation, but not why cache invalidation is needed.

Overall ORAL-D02-006 first attempt: FAIL; targeted remediation required. Instruction given: context checkpoint allows reuse, double-check after lock prevents duplicate ASR/OCR, throw propagates for possible retry, cache invalidation prevents stale user-list reads. G02 IN_PROGRESS.
