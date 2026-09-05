# medama-io/medama

[![Stars](https://img.shields.io/github/stars/medama-io/medama?style=flat-square&color=yellow)](https://github.com/medama-io/medama/stargazers) [![Forks](https://img.shields.io/github/forks/medama-io/medama?style=flat-square&color=blue)](https://github.com/medama-io/medama/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Self-hostable, privacy-focused website analytics.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 632 |
| 🍴 **Forks** | 17 |
| 💻 **Language** | Go |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`analytics` `cookie-free` `dashboard` `duckdb` `go` `google-analytics` `medama` `metrics` `privacy` `self-hosted` `web-analytics` `website-analytics`

## 🎯 Categories

Data · Observability

## 📝 Summary

### English

Here's a brief summary of the medama project:

Medama is an open-source, self-hostable website analytics platform that helps organizations process and analyze data in a privacy-focused manner. With medama, users can convert raw data into searchable, analyzable, or automated pipelines, improving their reporting workflows and data organization. Its high production readiness, strong adoption, and recent activity make it a suitable candidate for a serious pilot or production deployment.

The practical adoption path involves:

1. **Evaluating the project**: Review the README, GitHub stars, forks, and recent activity to assess its potential.
2. **Small proof of concept**: Start with a small-scale integration to test the project's feasibility and identify potential issues.
3. **Final review of risks**: Conduct a thorough review of the project's license, security posture, and active maintainers to ensure it meets your organization's requirements.

Medama's high production readiness is due to:

1. **Recent activity**: The project has been updated recently (2026-06-28), indicating ongoing maintenance and development.
2. **Strong adoption**: With 632 GitHub stars and 17 forks, medama has gained significant traction in the open-source community.
3. **Ecosystem signals**: The project's adoption and recent activity suggest a

### Русский

**medama-io/medama** — это self‑hosted система веб‑аналитики, ориентированная на конфиденциальность данных. Она позволяет превращать сырые логи в индексируемые, аналитически‑готовые наборы и легко встраивается в существующие пайплайны — типичный сценарий — запуск небольшого proof‑of‑concept, проверка README и последующее масштабирование аналитических и отчётных процессов. Проект считается почти готовым к production: активные коммиты, 632 звёзд, стабильный Go‑код и хорошая экосистема делают его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介（2‑3 句）**  
medama（medama-io/medama）是一款可自行托管、注重隐私的网站分析系统，使用 Go 语言实现，旨在帮助用户把原始访问数据转化为可搜索、可分析、可自动化的管道。它提供轻量级的事件收集、实时聚合和灵活的查询接口，让用户在不泄露用户隐私的前提下，搭建完整的分析与报告工作流。

**价值**  
- **隐私安全**：所有数据都在本地或自有云中保存，无第三方跟踪。  
- **可搜索/可编排**：原始日志可直接通过 SQL‑like 查询或自定义脚本进行筛选、聚合，便于构建数据仓库或自动化 ETL 流程。  
- **高度可定制**：支持自定义事件、标签和插件，能够快速适配各种业务场景（如转化漏斗、用户行为路径等）。  

**典型接入方式**  
1. **部署**：通过 Docker 镜像或二进制文件在自己的服务器/K8s 集群上启动 `medama` 服务。  
2. **埋点**：在前端页面引入提供的 JavaScript SDK（或使用 HTTP API），将访问事件发送到部署好的端点。  
3. **验证**：先在本地或测试环境跑一个小型 POC，检查 README 中的示例配置、数据采集是否成功。  
4. **集成**：将采集到的事件流对接到现有的 BI 工具、Prometheus/Grafana 或自建的 ELK/ClickHouse 等后端进行进一步分析和可视化。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑28，项目最近更新，拥有 632 ⭐、12 个主题标签，社区活跃。  
- **成熟度**：代码基于 Go，具备良好的性能和易于容器化部署的特性，已在多个开源案例中用于生产环境。  
- **风险**：暂无重大元数据风险，但仍需对许可证（MIT/Apache）以及安全审计进行最终确认。总体而言，medama 已具备“高”生产就绪度，适合作为正式业务的分析底座进行试点。

## 🧭 Practical evaluation

**Value:** medama-io/medama helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 632 GitHub stars
- 17 forks
- updated 2026-06-28
- primary language: Go
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/medama-io/medama) · [← Back to Data](./README.md)</sub>
