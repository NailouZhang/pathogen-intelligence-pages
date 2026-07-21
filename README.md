# Pathogen Intelligence Pages v17.2

这是三仓系统中的公开静态展示仓。私有 `NailouZhang/pathogen-intelligence-factory` 完成抓取、终审、双语分析、渲染和安全审计后，只把公开白名单静态成品同步到本仓 `public/`；本仓自己的 `.github/workflows/deploy-pages.yml` 负责GitHub Pages部署。

允许的主要内容：

```text
public/index.html
public/profiles/*/index.html
public/assets/*
public/images/*
public/portal.json
public/robots.txt
public/.nojekyll
```

禁止加入Python源码、提示词、21种病原词库、私有审计、Provider状态、Secrets、Factory配置和Publisher配置。部署工作流会再次检查公开目录。

合法的多语种原始标题可以出现在明确的来源元数据位置；英文/中文分析字段仍分别遵守语言契约。若正常渲染存在结构问题，Factory会先确定性修复，再进行元数据级安全回退，Pages仓不接收未经验证的深度内容。

公开地址：

```text
https://nailouzhang.github.io/pathogen-intelligence-pages/
```

手动部署：

```bash
gh workflow run deploy-pages.yml \
  --repo NailouZhang/pathogen-intelligence-pages \
  --ref main
```
