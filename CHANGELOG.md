# CHANGELOG.md · 版本记录

> 项目无正式版本号，按提交里程碑记录。

## v1.1.0 · 2026-11-19

**补齐 knowledge-base 单项目规范 v2.1.4 的四件套。**

- 新增 `DEVELOPMENT.md`：AGENTS.md 里 7 条关键坑改写为一坑一篇（TL;DR + 问题 / 根因 / 解决 / 预防）。
- `AGENTS.md` 顶部补文档基线行（日期 + commit hash）。
- `CHANGELOG.md` 改为按版本分节；`README.md` 文档索引加入 DEVELOPMENT.md。
- 未改 `index.html`，GitHub Pages 页面与本地查看方式不变。

## v1.2.0 · 2026-11-19

**接入 repo-kit v2.9.0（单项目规范 v2.1.4，`link-only` 档），补齐机器层校验。**

- 新增 `schema/kit.lock.json`、`schema/taxonomy.json`、`schema/frontmatter.schema.json`、`schema/skills.schema.json`。
- 新增 `tools/repo-kit/check_repo.py`、`tools/update-repo-kit.ps1`。
- 新增 `.github/workflows/repo-check.yml`：PR / push 到 `main` 时跑结构校验 + kit 锁校验。
- 文档检查依赖（PyYAML / markdown-it-py / jsonschema）在 CI 显式安装，本仓不引入 `requirements.txt`。
- `DEVELOPMENT.md` 新增「校验与 CI」，并修正原「无机器层」表述；`AGENTS.md` 补校验命令。
- 未改 `index.html`，GitHub Pages 页面与离线查看方式不变。

## 里程碑

- **深色模式改版**：界面改为深色模式（粉色强调色 #ff9292，玻璃拟态卡片风格）
- **初始版本**：基于 Obsidian 笔记整理的 NTLite 精简 Windows 镜像操作指南（单文件 HTML，配图内嵌，可离线查看）

## 备注

- 仓库原名 `ntlite-windows-guide-2`，2026-08-03 重命名为 `ntlite-windows-guide`
- 无版本 tag / Release
