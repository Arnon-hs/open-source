# Netflix/atlas

[![Stars](https://img.shields.io/github/stars/Netflix/atlas?style=flat-square&color=yellow)](https://github.com/Netflix/atlas/stargazers) [![Forks](https://img.shields.io/github/forks/Netflix/atlas?style=flat-square&color=blue)](https://github.com/Netflix/atlas/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> In-memory dimensional time series database.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.6k |
| 🍴 **Forks** | 354 |
| 💻 **Language** | Scala |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Database

## 📝 Summary

### English

Here's a brief summary of the Netflix/atlas project:

Netflix/atlas is an open-source, in-memory dimensional time series database that helps convert raw data into searchable, analyzable, or automated pipelines. Its value proposition lies in its ability to organize analytics pipelines, process datasets, and improve reporting workflows. While it's suitable for prototypes or internal workflows, its adoption requires manual inspection and validation of setup costs before committing to production use.

As for the practical adoption path, here are the next steps:

1. **Manual Inspection**: Netflix/atlas requires manual inspection before adoption due to sparse integration signals in the discovered metadata. This involves carefully reviewing the project's documentation and code to understand its architecture and potential integration points.
2. **Dependency and Maintenance Checks**: Before production, it's essential to validate the project's dependencies and maintenance requirements to ensure they align with your organization's standards.
3. **Validate Setup Costs**: Estimate the setup costs, including development time, resources, and potential infrastructure requirements, to ensure they fit within your project's budget and timeline.

Regarding production readiness, Netflix/atlas is rated as Medium, indicating that it's useful for prototypes or internal workflows but may require additional validation and testing before being deployed in production environments.

### Русский

Netflix Atlas — это in‑memory многомерная временная база данных, позволяющая быстро преобразовывать сырые метрики в индексируемые наборы данных для аналитических и автоматизированных пайплайнов. Типичное внедрение выглядит так: команда подключает Atlas к существующим системам мониторинга, формирует измерения (dimensions) и метрики, а затем использует их в аналитических запросах, отчётах и автоматических реакциях; однако перед запуском в продакшн требуется ручная проверка интеграции, так как готовой схемы подключения в метаданных мало. Готовность к production — средняя: проект подходит для прототипов и внутренних воркфлоу, но требует проверки зависимостей и затрат на настройку перед масштабным использованием.

### 中文

**项目简介（2‑3 句）**  
Netflix/atlas 是一款基于内存的多维时序数据库，采用 Scala 实现，专注于对海量监控指标进行高速写入、查询和聚合。它能够把原始监控数据即时转化为可搜索、可分析的时间序列，帮助构建自动化的数据管道和实时分析系统。

**价值**  
- **快速分析**：内存存储 + 多维索引，使得数十亿级别的时序点在毫秒级返回，适合实时仪表盘和告警。  
- **统一管道**：将原始日志、业务指标统一写入 Atlas，后续可直接在同一平台完成聚合、过滤和导出，降低了多系统之间的 ETL 成本。  
- **灵活扩展**：支持自定义维度（tag）和聚合函数，能够满足从业务监控到容量规划的多种场景。

**典型接入方式**  
1. **依赖引入**：在 Scala/Java 项目中加入 `com.netflix.atlas:atlas-core`（或对应的 client 包）作为依赖。  
2. **指标上报**：使用 Atlas 提供的 `Registry`、`Timer`、`Counter` 等 API，在业务代码中直接记录指标；也可以通过 StatsD/Graphite 协议的网关将已有监控数据推送到 Atlas。  
3. **查询与可视化**：通过 Atlas 自带的查询语言（AtlasQL）或 REST API 检索数据，常配合 Grafana、Kibana 等前端进行可视化。  
4. **运维集成**：在容器/虚拟机启动脚本中加入 Atlas Agent，自动收集 JVM、系统指标并上报。

**生产可用性**  
- **成熟度**：GitHub ★3554，活跃维护（截至 2026‑07‑03），但官方文档和集成示例相对有限。  
- **适用场景**：适合内部原型、研发实验或对时序查询性能要求极高的业务监控；在生产环境使用前建议进行依赖审计、灾备和容量评估。  
- **风险**：集成路径不够透明，元数据中缺乏完整的接入指南，需要自行进行探索和验证；此外，内存存储对资源消耗较大，需做好容量规划和持久化备份。  

综上，Netflix/atlas 在需要高吞吐、低延迟时序分析的内部项目中价值突出，但在正式生产环境部署前，需要进行充分的集成测试和运维准备。

## 🧭 Practical evaluation

**Value:** Netflix/atlas helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3554 GitHub stars
- 354 forks
- updated 2026-07-03
- primary language: Scala

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 76/100 |
| topics | 0/100 |
| outlook | 64/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 72/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/Netflix/atlas) · [← Back to Database](./README.md)</sub>
