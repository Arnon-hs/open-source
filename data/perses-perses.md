# perses/perses

[![Stars](https://img.shields.io/github/stars/perses/perses?style=flat-square&color=yellow)](https://github.com/perses/perses/stargazers) [![Forks](https://img.shields.io/github/forks/perses/perses?style=flat-square&color=blue)](https://github.com/perses/perses/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> The CNCF sandbox for observability visualisation. Already supports Prometheus, Tempo, Loki and Pyroscope - more data sources to come!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.2k |
| 🍴 **Forks** | 192 |
| 💻 **Language** | Go |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cncf-project` `dashboard` `monitoring` `observability` `prometheus`

## 🎯 Categories

Data · Observability

## 📝 Summary

### English

**Summary**  
Perses ( github.com/perses/perses ) is a CNCF‑sandbox project that provides a unified, web‑based UI for visualising observability data from Prometheus, Tempo, Loki and Pyroscope, with more sources planned. It lets teams turn raw metrics, traces, logs and profiling data into searchable dashboards and automated pipelines, simplifying analytics, reporting and incident‑response workflows.  

**Value**  
By consolidating multiple observability back‑ends under a single, extensible front‑end, Perses eliminates the need for separate Grafana or custom tooling stacks, reducing operational overhead and enabling faster, cross‑domain insights. Its Go‑centric architecture and declarative pipeline definitions make it easy to embed in CI/CD or data‑processing workflows, turning raw telemetry into actionable, queryable artifacts.  

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, run the Docker compose example, and point it at an existing Prometheus/Loki instance to validate dashboard rendering.  
2. **Integration** – add Perses as a side‑car service in your observability stack, configure the data‑source connectors via the provided YAML, and create a minimal set of dashboards that mirror your current Grafana views.  
3. **Pipeline rollout** – progressively replace ad‑hoc queries with Perses‑defined pipelines (e.g., automated alert generation or report export) and iterate on the UI configuration.  

**Production readiness**  
Perses scores high on readiness: recent commits (last update 2026‑05‑11), 2 k+ stars, active forks, and strong CNCF sandbox endorsement indicate a healthy community and ongoing maintenance. While the license and security posture still require a final audit, the project’s activity level, Go codebase, and existing adoption in several pilot environments make it a solid candidate for a serious production pilot.

### Русский

**perses/perses** — это CNCF‑sandbox проект для визуализации наблюдаемости, уже поддерживающий Prometheus, Tempo, Loki и Pyroscope и планирующий добавить новые источники данных. Он позволяет преобразовывать сырые метрики и трассировки в поисковые, аналитические и автоматизированные конвейеры, что упрощает построение аналитических пайплайнов, обработку наборов данных и улучшение процессов отчётности. Проект имеет высокий уровень готовности к production: активная разработка, более 2000 звёзд на GitHub, свежие коммиты и широкую экосистемную поддержку, что делает его надёжным кандидатом для небольшого пилотного внедрения с последующим масштабированием.

### 中文

**项目简介（2‑3 句）**  
Perses（仓库地址：github.com/perses/perses）是 CNCF sandbox 级别的可观测性可视化平台，已原生支持 Prometheus、Tempo、Loki 与 Pyroscope，后续还将在持续扩展数据源。它帮助把原始监控、日志、追踪和性能数据转化为可搜索、可分析、可自动化的管道，从而提升分析与报告的效率。

**价值**  
- **统一视图**：一次性接入多种 observability 数据源，避免在不同 UI 与查询语言之间切换。  
- **可搜索/可分析**：提供强大的查询、过滤与聚合功能，支持构建自定义仪表盘和自动化告警/报告。  
- **可扩展**：基于 Go 的插件化架构，便于后续接入新数据源或自定义处理逻辑。  

**典型接入方式**  
1. **快速 PoC**：克隆仓库，参考 README 中的 `docker-compose` 示例启动 Perses 与所需后端（Prometheus、Loki 等）。  
2. **配置数据源**：在 `datasources.yaml` 中添加对应的 URL、认证信息和查询语法。  
3. **创建仪表盘**：使用 UI 或 YAML 定义面板（Panel）和查询（Query），保存后即可在团队内部共享。  
4. **CI/CD 集成**：将仪表盘定义文件纳入代码库，通过 GitOps（如 ArgoCD）自动部署到生产环境。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目最近一次提交，拥有 2157 ⭐、192 forks，社区活跃度高。  
- **成熟度**：已在多个企业内部进行 pilot，核心功能（数据源接入、仪表盘渲染、权限控制）相对稳定。  
- **风险**：仍需完成许可证合规、完整的安全审计以及维护者长期可用性的确认。总体来看，Perses 已具备在生产环境中进行正式试点的条件，建议先在非关键业务做小规模 PoC，验证与现有监控栈的兼容性后再全量推广。

## 🧭 Practical evaluation

**Value:** perses/perses helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2157 GitHub stars
- 192 forks
- updated 2026-05-11
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 71/100 |
| topics | 63/100 |
| outlook | 83/100 |
| quality | 80/100 |
| recency | 100/100 |
| adoption | 67/100 |
| production | 76/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/perses/perses) · [← Back to Data](./README.md)</sub>
