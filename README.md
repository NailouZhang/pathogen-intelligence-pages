# Pathogen Intelligence Pages v17.1

这是三仓系统中的公开静态展示仓。私有 `NailouZhang/pathogen-intelligence-factory` 生成并验证静态站后，只把公开白名单内容同步到本仓 `public/`；本仓自己的 `.github/workflows/deploy-pages.yml` 负责 GitHub Pages 部署。

本仓允许出现的主要内容为：

```text
public/index.html
public/profiles/*/index.html
public/assets/*
public/images/*
public/portal.json
public/robots.txt
public/.nojekyll
```

不得加入 Python 源码、提示词、21种病毒词库、内部审计、Provider 状态、密钥、Factory 配置或 Publisher 配置。工作流会在部署前再次检查公开目录。

公开站点地址：

```text
https://nailouzhang.github.io/pathogen-intelligence-pages/
```

手动重新部署：

```bash
gh workflow run deploy-pages.yml \
  --repo NailouZhang/pathogen-intelligence-pages \
  --ref main
```
