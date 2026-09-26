# lovely-kids-budgets

给孩子记录日常花费的单页应用。用浏览器打开仓库根目录的 `index.html`。数据在浏览器 `localStorage`，键名是 `lovely-kids-budget-v1`。

## 文档

先读 `docs/INDEX.md`。再读路由点名的一个领域 README，然后只读点名的那几篇。默认不读 `docs/archive/`、`docs/inbox/` 和其他领域。

正式文档只用 `docs/glossary.md` 里的名称。一篇一个种类：`tutorial`、`how-to`、`reference`、`explanation`。一篇一个主读者：`agent`、`developer`、`business`、`leadership`。

编写、查阅、捕获或整理文档时，遵循技能 `knowledge-base`。给人看的目录约定在 `docs/SCHEMA.md`。

## 捕获

待办追加到 `docs/inbox/todos.md`，写清下一步和阻塞。问题理解、踩坑和未核实的流程写成 `docs/inbox/YYYY-MM-DD-主题.md`，`status: draft`。不把收件箱直接改成正式文档。

## 代码入口

领域规则以 `docs/domains/` 为准。下面只标文件入口：

- 孩子与额度：`index.html` 的 `state.kids`
- 消费分类：`index.html` 的 `state.cats`
- 记账：`index.html` 的 `state.logs`
- 本地保存：`index.html` 的 `load`、`save`、`normalize`
