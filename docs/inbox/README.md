---
title: 收件箱
kind: reference
audience: agent
domain: inbox
status: active
updated: 2026-09-26
source: docs/SCHEMA.md
---

# 收件箱

这里存放执行中的待办、问题理解和尚未核实的流程。这里的文件不是正式知识。

- 待办追加到 [todos.md](todos.md)：下一步、阻塞、日期。
- 其他笔记写成 `YYYY-MM-DD-主题.md`，frontmatter 的 `status` 为 `draft`，`domain` 为 `inbox`。

升格时核对 `docs/glossary.md`，把正文移到所属领域或写成新 ADR，更新领域 README 和 `docs/INDEX.md`，然后删除本目录中的原文。步骤在技能 `knowledge-base`。
