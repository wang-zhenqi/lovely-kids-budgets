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

本文件说明目录里各放什么。Agent 的加载、写作、升格和整理步骤在技能 `knowledge-base`，不在这里复述。

## 目录

- `INDEX.md`：任务路由。一行一个任务，指向一个领域入口。
- `glossary.md`：正式名称。文档里的名词以这里为准。
- `domains/<领域>/`：该领域的正式文档。一篇只属于一个领域。
- `decisions/`：跨领域决定。一篇 ADR 一个编号，已接受的「决定」段不改。
- `inbox/`：待办和未核实笔记。不是正式知识。
- `archive/`：过时正文。原路径留一段重定向。

领域目前有四个：`kids`（孩子、预算、余额、存钱罐）、`categories`（消费分类）、`ledger`（记账、账本、金额、备注）、`storage`（本地保存）。不要为了凑齐教程、操作指南、参考说明和解释而建空目录。

## 一篇文档

每篇正式文档一份 frontmatter：`title`、`kind`、`audience`、`domain`、`status`、`updated`、`verified`、`source`。

- `kind`：`tutorial`、`how-to`、`reference`、`explanation` 之一。
- `audience`：`agent`、`developer`、`business`、`leadership` 之一。给产品负责人看的材料用 `leadership`。
- `domain`：领域目录名。本文件、`INDEX.md`、`glossary.md` 用 `meta`。ADR 用 `decisions`。收件箱用 `inbox`。归档说明用 `archive`。
- `status`：`draft`、`active`、`superseded`、`archived` 之一。

同一事实要给第二个读者时，另写一篇，用链接互指。

## 生命周期

收件箱里的草稿核实之后，移入所属领域或写成新 ADR，并更新 `INDEX.md`。过时的正式文档移到 `archive/`，原处留下指向新路径的短文。已升格或已无用的收件箱条目直接删除。
