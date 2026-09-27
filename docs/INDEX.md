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

先判断问题属于意图、行为还是取舍，再只打开那一个归属。原料不回答「现在是什么」。

| 问题 | 先读 | 再读 | 不读 |
| --- | --- | --- | --- |
| 孩子、预算、余额或存钱罐现在怎样 | [kids](domains/kids/README.md) | 该领域里被点名的那一篇 | 收件箱、`docs/superpowers/`、其他领域 |
| 消费分类现在怎样 | [categories](domains/categories/README.md) | 该领域里被点名的那一篇 | 收件箱、`docs/superpowers/`、其他领域 |
| 记账、账本、金额或备注现在怎样 | [ledger](domains/ledger/README.md) | 该领域里被点名的那一篇 | 收件箱、`docs/superpowers/`、其他领域 |
| 本地保存现在怎样 | [storage](domains/storage/README.md) | 该领域里被点名的那一篇 | 收件箱、`docs/superpowers/`、其他领域 |
| 产品决定做成什么样 | [需求](requirements/README.md) | 被点名的那一篇正式需求 | 收件箱、设计说明、实现计划 |
| 为什么这样选 | [decisions](decisions/README.md) | 已接受的那一篇 ADR | 已取代的 ADR，除非问题是「曾经为什么」 |
| 查名称 | [术语表](glossary.md) | 不需要 | 原料 |
| 记下尚未决定的想法、会议或探查 | [收件箱](inbox/README.md) | `now.md`、`todos.md` 或新建一篇原料 | 不要把原料写成第二个正式文档 |
| 执行手头这份设计说明或实现计划 | [superpowers](superpowers/README.md) | 正在执行的那一篇 | 其他计划、已收束后应已删除的文件 |
| 收束或修正文档 | [SCHEMA](SCHEMA.md) | 技能 `knowledge-base` 的收束段 | 与这次事实无关的领域 |

改了代码，就更新对应领域文档。改了产品决定，就更新那一篇正式需求。改了取舍，就新写 ADR。然后删除承载这些事实的原料。
