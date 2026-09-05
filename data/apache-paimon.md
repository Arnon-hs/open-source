# apache/paimon

[![Stars](https://img.shields.io/github/stars/apache/paimon?style=flat-square&color=yellow)](https://github.com/apache/paimon/stargazers) [![Forks](https://img.shields.io/github/forks/apache/paimon?style=flat-square&color=blue)](https://github.com/apache/paimon/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Apache Paimon is a lake format that enables building a Realtime Lakehouse Architecture with Flink and Spark for both streaming and batch operations.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.3k |
| 🍴 **Forks** | 1.3k |
| 💻 **Language** | Java |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`big-data` `data-ingestion` `flink` `paimon` `real-time-analytics` `spark` `streaming-datalake` `table-store`

## 🎯 Categories

Data

## 📝 Summary

### English

**Summary**  
Apache Paimon is an open‑source lake‑format that lets you build a real‑time lakehouse on top of Flink or Spark, supporting both streaming and batch workloads. By providing built‑in change‑data‑capture, schema evolution and incremental reads, it eliminates many of the manual glue code and operational scripts that are usually required to keep data pipelines in sync.  

**Value** – Paimon turns repetitive, error‑prone steps (e.g., file‑format conversions, compaction jobs, metadata syncing) into declarative operations, enabling teams to create repeatable, end‑to‑end data flows without custom scripting.  

**Practical adoption path** – Start with a small proof‑of‑concept: clone the repo, run the README examples against a local Flink or Spark cluster, and verify that the lake‑format tables can be read/written both in streaming and batch mode. Once the PoC succeeds, incrementally replace existing file‑based sinks or batch tables with Paimon tables, and integrate the provided connectors into your orchestration (e.g., Airflow, Dagster).  

**Production readiness** – The project shows strong OSS maturity: >3 k GitHub stars, >1 k forks, frequent commits (last update 2026‑06‑23), and active adoption in the Flink/Spark ecosystem. Its Java codebase is well‑documented, and the community offers support channels, making it suitable for a serious pilot. The main risk is that the integration steps are not fully documented in the metadata, so you should validate setup costs (cluster configuration, catalog integration, and checkpoint handling) before committing to a full rollout.

### Русский

Apache Paimon — это открытый lake‑format, позволяющий построить Realtime Lakehouse‑архитектуру на базе Flink и Spark, автоматизируя как потоковые, так и пакетные задачи и устраняя повторяющиеся ручные операции в пайплайнах данных. Типичный сценарий внедрения — небольшое proof‑of‑concept, где Paimon подключается к существующим потоковым/батч‑задачам, после чего его можно масштабировать до продакшн‑уровня благодаря активному развитию (3305 звёзд, 1334 форка) и сильной экосистеме. Готовность к production высокая, однако перед полномасштабным rollout‑ом следует уточнить детали интеграции и оценить затраты на настройку.

### 中文

**项目简介（2‑3 句）**  
Apache Paimon 是面向实时湖仓（Realtime Lakehouse）的开源存储格式，提供统一的批流一致性语义，支持 Flink 与 Spark 在流式和离线作业中直接读写。它通过增量写入、事务日志和时间旅行等特性，帮助企业摆脱手工数据搬迁和同步的繁琐工作。

**价值**  
- **消除重复人工操作**：一次写入即生成可供批、流两种计算引擎直接消费的湖表，省去 ETL、数据同步、脚本调度等重复步骤。  
- **统一实时与离线分析**：在同一湖表上同时支持 Flink 实时流处理和 Spark 离线查询，降低数据治理成本。  
- **可靠的事务与回溯**：内置两阶段提交、快照与时间旅行，确保数据一致性并支持错误回滚与审计。

**典型接入方式**  
1. **环境准备**：在已有的 Flink / Spark 集群上加入 Paimon 依赖（Maven/Gradle），或使用官方提供的 Docker 镜像进行快速验证。  
2. **创建湖表**：通过 SQL DDL（`CREATE TABLE … WITH ('connector'='paimon', …)`）或 Java/Scala API 定义表结构和存储路径。  
3. **写入数据**：在 Flink DataStream / Table API 或 Spark Structured Streaming 中使用 `INSERT INTO` 或 `writeToSink` 将实时数据写入 Paimon 表。  
4. **读取数据**：同样使用 Flink SQL / Spark SQL 直接查询 Paimon 表，支持批处理作业、交互式分析或 BI 工具连接。  
5. **小规模 PoC**：先在开发环境跑一个“从 Kafka → Flink → Paimon → Spark 查询”的完整链路，验证兼容性与性能，再逐步扩展到生产。

**生产可用性**  
- **成熟度**：GitHub ★3305、Fork ★1334，最近一次提交（2026‑06‑23）仍在活跃维护；社区已有多家大厂在生产环境使用。  
- **稳定性**：提供完整的事务日志、快照管理和自动清理机制，已在大规模流批混合作业中验证。  
- **生态兼容**：原生支持 Flink 1.18+、Spark 3.4+，并可通过 Hive Metastore、Catalog API 与现有元数据系统对接。  
- **风险**：集成文档相对分散，建议先阅读官方 README 与示例代码，评估部署脚本、资源配额及运维监控成本后再投入生产。

综上，Apache Paimon 具备高可用的技术特性和活跃的社区支持，适合作为实时湖仓的核心存储层，在完成小规模概念验证后即可在生产环境中稳健运行。

## 🧭 Practical evaluation

**Value:** apache/paimon helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3305 GitHub stars
- 1334 forks
- updated 2026-06-23
- primary language: Java
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 75/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/apache/paimon) · [← Back to Data](./README.md)</sub>
