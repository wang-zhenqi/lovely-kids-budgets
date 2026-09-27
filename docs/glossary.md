---
title: 术语表
kind: reference
audience: agent
domain: meta
status: active
updated: 2026-09-26
verified: 2026-09-26
source: index.html
---

# 术语表

正式文档只用下表中的名称。对话里的临时代号先在这里登记，再写入 `docs/domains/` 或 `docs/decisions/`。

| 正式名称 | 所指 | 代码位置 | 领域 |
| --- | --- | --- | --- |
| 芊芊 | 其中一个孩子 | `state.kids.qianqian`，`data-kid="qianqian"` | kids |
| 万万 | 其中一个孩子 | `state.kids.wanwan`，`data-kid="wanwan"` | kids |
| 预算 | 一个孩子的额度 | 字段 `budget` | kids |
| 余额 | 一个孩子当前剩余的金额 | 字段 `balance` | kids |
| 存钱罐 | 页面上显示当前孩子余额的区域 | 元素 `#jar` | kids |
| 消费分类 | 一笔花费所属的类别 | `state.cats` | categories |
| 账本 | 查看记账列表的界面 | 元素 `#ledgerSheet` | ledger |
| 记账 | 一笔花费记录 | `state.logs` | ledger |
| 金额 | 记账时填写的数字 | 输入 `#amount` | ledger |
| 备注 | 记账时可选的短说明 | 输入 `#note` | ledger |
| 本地保存 | 浏览器里持久化的应用状态 | `localStorage` 键 `lovely-kids-budget-v1`；函数 `load`、`save`、`normalize` | storage |
| 正式需求 | 已经决定的产品意图，也称 PRD | `docs/requirements/` | requirements |
| 理论碎片 | 还不能当依据的一条儿童金钱经验 | `docs/theory/fragments/` | theory |
| 理论文章 | 已收拢、可供设计正式需求时引用的理论正文 | `docs/theory/` | theory |

本表只固定名称和代码位置。行为规则写在对应领域的正式文档里。
