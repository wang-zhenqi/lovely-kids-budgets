---
title: 文档路由
kind: reference
audience: agent
domain: meta
status: active
updated: 2026-09-26
verified: 2026-09-26
source: docs/SCHEMA.md
---

# 文档路由

先读本表里对应该任务的一行。再读「先读」那一篇，然后只读「再读」点名的文档。

| 任务 | 先读 | 再读 | 不读 |
| --- | --- | --- | --- |
| 改孩子、预算、余额或存钱罐 | [kids](domains/kids/README.md) | 尚无，只读领域 README | `docs/archive/`、`docs/inbox/`、其他领域 |
| 改消费分类 | [categories](domains/categories/README.md) | 尚无，只读领域 README | `docs/archive/`、`docs/inbox/`、其他领域 |
| 改记账、账本、金额或备注 | [ledger](domains/ledger/README.md) | 尚无，只读领域 README | `docs/archive/`、`docs/inbox/`、其他领域 |
| 改本地保存 | [storage](domains/storage/README.md) | 尚无，只读领域 README | `docs/archive/`、`docs/inbox/`、其他领域 |
| 查名称或给对话代号起正式名称 | [术语表](glossary.md) | 不需要 | `docs/archive/`、其他领域正文 |
| 查或写跨领域决定 | [decisions](decisions/README.md) | 被点名的那一篇 ADR | `docs/archive/`、`docs/inbox/`、领域正文，除非 ADR 链接了它 |
| 记录待办、问题理解或未核实流程 | [inbox](inbox/README.md) | `docs/inbox/todos.md` 或新建当天草稿 | 正式文档，除非要对齐术语表 |
| 整理、归档、拆分或迁移文档 | [SCHEMA](SCHEMA.md) | 技能 `knowledge-base` 的整理段 | 与这次整理无关的领域 |

新增、迁移或归档一篇正式文档时，同时改对应领域 README 和本表。行格式见技能 `knowledge-base` 的 `references/index-row.md`。
