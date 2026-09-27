---
title: 文档目录约定
kind: reference
audience: developer
domain: meta
status: active
updated: 2026-09-26
verified: 2026-09-26
source: docs/SCHEMA.md
---

# 文档目录约定

知识库只回答现在可以相信什么。每条事实有一个归属。开发过程里的笔记是原料，收束进归属之后删除。Agent 的操作步骤在技能 `knowledge-base`。

## 三类事实

- **意图**：产品决定做成什么样。唯一归属是 `requirements/` 里的正式需求。
- **行为**：代码现在怎样运行。唯一归属是 `domains/<领域>/`。文档写明 `source` 和 `verified`，并与代码一致。
- **取舍**：为什么这样选。唯一归属是 `decisions/` 里已接受的 ADR。被取代的 ADR 留在原处，只说明曾经的决定。

意图和行为可以暂时不同。这个差距记在收件箱的待办里，直到改产品决定或改代码。

## 原料

`inbox/` 和进行中的 `superpowers/` 都不是事实。

- 一句话需求、需求分析、迭代计划、探查、开工、桌面检查、某一次测试记录、回顾：写在 `inbox/`。预期归属写在笔记开头。
- 当前迭代选了哪些正式需求：只放在 `inbox/now.md` 的链接里。迭代结束时清空。
- brainstorming 和写计划仍使用 `superpowers/specs/`、`superpowers/plans/`。工作结束后，把事实收进上面三类归属，然后删除这些文件。

不为这些活动另建长期目录。拒绝的想法不保留。成立的想法不在正式需求之外再留一份。

## 其余目录

- `INDEX.md`：按问题指向唯一归属。
- `glossary.md`：正式名称。
- `archive/`：已退出的正式文档。原路径只留重定向。原料不进这里，直接删除。

领域目前有 `kids`、`categories`、`ledger`、`storage`。不要为了凑齐四类文档而建空目录。

## 一篇正式文档

frontmatter 包含 `title`、`kind`、`audience`、`domain`、`status`、`updated`。领域文档还包含 `source` 和 `verified`。

- `kind`：`tutorial`、`how-to`、`reference`、`explanation` 之一。
- `audience`：`agent`、`developer`、`business`、`leadership` 之一。正式需求用 `leadership`。
- `domain`：领域目录名。本文件和索引、术语表用 `meta`。正式需求用 `requirements`。ADR 用 `decisions`。原料用 `inbox` 或 `superpowers`。
- `status`：`draft`、`active`、`superseded`、`archived` 之一。

一篇一个种类、一个主读者。第二个读者另写一篇，用链接互指。

## 防止腐化

每次活动结束时收束原料。改了代码就同时改对应的领域文档。事实若出现在两个文件里，删掉其中一个，或把它改成链接。索引只指向仍然有效的归属。
