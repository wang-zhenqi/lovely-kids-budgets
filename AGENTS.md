# lovely-kids-budgets

给孩子记录日常花费的单页应用。用浏览器打开仓库根目录的 `index.html`。数据在浏览器 `localStorage`，键名是 `lovely-kids-budget-v1`。

## 文档

先读 `docs/INDEX.md`，再只打开该问题的那一个归属。默认不读 `docs/archive/`、`docs/inbox/` 和与该问题无关的目录。

正式文档只用 `docs/glossary.md` 里的名称。一篇一个种类：`tutorial`、`how-to`、`reference`、`explanation`。一篇一个主读者：`agent`、`developer`、`business`、`leadership`。

产品意图在 `docs/requirements/`。代码行为在 `docs/domains/`。实施原则和架构取舍在 `docs/decisions/`。想法、会议和未完成的计划是原料，放在 `docs/inbox/` 或 `docs/superpowers/`，收束后删除。

编写、查阅、捕获或收束文档时，遵循技能 `knowledge-base`。给人看的目录约定在 `docs/SCHEMA.md`。

## 捕获

尚未决定的内容和待办写入 `docs/inbox/`。当前迭代只在 `docs/inbox/now.md` 列出正式需求链接。活动结束前把事实写入唯一归属，并删除原料。

## Cursor Cloud specific instructions

没有包管理器、lint、测试或构建。安装阶段只确认仓库根目录的 `index.html` 可读：

`python3 -c 'import pathlib; p=pathlib.Path("index.html"); assert p.is_file() and p.stat().st_size>0'`

环境启动时在 8765 端口提供页面。该端口已在监听时，启动命令立刻退出：

`bash -c 'if (echo >/dev/tcp/127.0.0.1/8765) >/dev/null 2>&1; then exit 0; fi; exec python3 -m http.server 8765 --bind 0.0.0.0'`

用浏览器打开 `http://127.0.0.1:8765/`。记一笔账时，把存钱罐拖到消费分类上，再填写金额。

## 代码入口

领域规则以 `docs/domains/` 为准。下面只标文件入口：

- 孩子与额度：`index.html` 的 `state.kids`
- 消费分类：`index.html` 的 `state.cats`
- 记账：`index.html` 的 `state.logs`
- 本地保存：`index.html` 的 `load`、`save`、`normalize`
