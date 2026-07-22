# Pathogen Intelligence Pages v17.4-r4

本公开仓采用双分支职责隔离：

- `main`：仅保存本仓 README、`.gitignore` 和 `.github/workflows/deploy-pages.yml` 等处理代码与配置；
- `pages-data`：由 Factory 自动维护，仅保存 `.pages-data-branch` 与 `public/` 静态成品。

Factory 将完整公开站点推送到 `pages-data`，随后发送 `pages-data-updated` 仓库调度事件。默认分支 `main` 上的部署工作流检出 `pages-data/public`，完成静态安全审计并部署到 GitHub Pages。

不得把自动生成的 `public/profiles/`、`public/portal.json` 或 `public/index.html` 提交回 `main`。这可避免工程更新与在线成品在同一分支发生修改/删除冲突。
