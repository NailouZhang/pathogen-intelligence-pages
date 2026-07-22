# Pathogen Intelligence Pages v17.4-r2.1

公开静态仓，只接收Factory生成并通过公开白名单检查的站点树。仓库不保存Factory源码、API密钥、原始私有审计、公众号密钥、Runner配置或发布状态。

部署工作流：`.github/workflows/deploy-pages.yml`。

网页正文由Factory生成；v17.4-r2.1会在发布前清除后台复核措辞，并通过HTML审计禁止“审查得出的结论是”“范围说明”等处理过程文本进入公开页面。
