# Learning Notes

本目录保存按教学模块整理的学习讲义。讲义用于复习，不替代 Gate 证据。

## 规则

- 每个模块一份 Markdown 讲义，采用「知识地图 → 业务背景 → 原理 → 源码映射 → 流程/异常 → 面试八股 → 易错点 → 掌握状态」结构。
- 明确区分 **源码已核实**、**教学抽象/推论**、**待验证问题**。
- 源码映射必须记录文件路径、类/方法；行号可能随提交变化，复习时以当前分支为准。
- 不把课堂理解检查记为正式 Gate Oral Defense，不虚构测试、Benchmark 或个人实现。
- 每个模块完成后，在本目录增加讲义，并在 DAILY_LOG.md 记录归档提交。
- 新对话从 learning 分支读取本 README、对应讲义、GATES.md 和 DAILY_LOG.md 继续。

## 讲义索引

| 模块 | 讲义 | 状态 |
|---|---|---|
| M1 系统架构基础 | [M1-系统架构基础.md](M1-系统架构基础.md) | 教学主体已整理；源码练习与 G02 验收待完成 |


## Fixed teaching-to-archive workflow

For every teaching module, follow this sequence:

1. Systematic top-down teaching: knowledge map, business context, principles, worked example.
2. Map concepts to verified source files/classes/methods; label inference and unknowns.
3. Run a comprehension check only after teaching; it is not formal Gate oral evidence.
4. Write a complete module Markdown note using the structure above.
5. Save it under this directory on the `learning` branch.
6. Update this README index.
7. Append the archive commit and accurate learning/Gate status to `docs/DAILY_LOG.md`.
8. Read back all changed files to verify; never change Gate status without its required evidence.
9. Continue source-location practice, user-owned implementation, Codex review and tests.
10. Conduct closed-book Gate oral defense only when the required evidence is ready.

If teaching is incomplete, label the note `PARTIAL`. Never skip the archive steps merely because the session moves to a new conversation.
