# monoscope-tech/timefusion

[![Stars](https://img.shields.io/github/stars/monoscope-tech/timefusion?style=flat-square&color=yellow)](https://github.com/monoscope-tech/timefusion/stargazers) [![Forks](https://img.shields.io/github/forks/monoscope-tech/timefusion?style=flat-square&color=blue)](https://github.com/monoscope-tech/timefusion/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> A timeseries database created for events, logs, traces and metrics. Speaks the postgres dialect, and stores data in s3 via delta lake protocol

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 172 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Rust |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Database · Observability

## 📝 Summary

### English

**Brief Summary**  
monoscope‑tech/timefusion is an open‑source time‑series database written in Rust that stores events, logs, traces, and metrics in S3 using the Delta Lake format while exposing a PostgreSQL‑compatible SQL dialect. It is positioned as a lightweight analytics layer for building searchable, query‑driven pipelines on raw observability data.

**Value Proposition**  
- **Unified query surface:** By speaking the familiar PostgreSQL dialect, teams can use existing SQL tools, BI dashboards, and data‑science notebooks without learning a new query language.  
- **Cost‑effective storage:** Leveraging S3 and Delta Lake means data is kept in cheap, durable object storage while still supporting ACID‑style operations and schema evolution.  
- **Observability‑first model:** The schema is tuned for high‑cardinality time‑series (logs, traces, metrics), making it easier to build dashboards, alerting pipelines, or automated anomaly‑detection workflows directly on raw event streams.

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the provided Docker compose (or binary) against a test S3 bucket, and point your existing PostgreSQL client or ETL tool at the endpoint to validate query behavior.  
2. **Data Ingestion:** Use the built‑in Delta Lake writer or an external connector (e.g., Spark, Flink, or a simple Rust client) to stream logs/traces into the S3 lake. Verify that partitioning and compaction meet your latency requirements.  
3. **Integration Review:** Because the repository’s metadata lacks detailed integration guides, perform a manual audit of required connectors, authentication (IAM/S3, TLS), and any custom Rust crates the project depends on. Document any missing pieces before scaling.  
4. **Pilot in Production‑like Environment:** Deploy the service on a staging Kubernetes cluster, enable monitoring (Prometheus metrics are exposed), and run a subset of your production workloads to measure query latency, storage cost, and failure recovery.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (latest commit 2026‑06‑24) and has modest community traction (≈172 ⭐, 8 forks).  
- **Stability:** Core functionality (SQL engine, Delta Lake writer) appears stable, but the ecosystem around authentication, backup, and scaling is not yet documented, requiring extra engineering effort.  
- **Operational Considerations:**  
  * **Dependency management:** Verify Rust toolchain versions and the compatibility of the Delta Lake library with your S3 provider.  
  * **Maintenance overhead:** Plan for periodic updates of the underlying Delta Lake and S3 SDKs to avoid security regressions.  
  * **Failure handling:** Implement monitoring for S3 write failures and Delta Lake compaction jobs; the project does not ship out‑of‑the‑box alerting.  
- **Fit for Production:** Suitable for internal analytics pipelines, prototypes, or low‑to‑moderate traffic workloads after a thorough integration validation. For mission‑critical, high‑throughput observability stacks, additional investment in testing, observability, and possibly a fallback storage layer is advisable.

### Русский

**monoscope-tech/timefusion** — это открытая timeseries‑БД на Rust, которая хранит события, логи, трассы и метрики в S3 по протоколу Delta Lake, при этом поддерживая SQL‑dialect PostgreSQL. Она удобна для построения аналитических и автоматизированных пайплайнов — от организации потоков данных до улучшения отчетности, но из‑за скудной метаданных интеграция требует ручного аудита и проверки зависимостей. Проект находится на среднем уровне готовности: подходит для прототипов и внутренних сервисов, однако перед запуском в продакшн следует оценить затраты на настройку и сопровождение.

### 中文

**项目简介**  
monoscope‑tech/timefusion 是一款面向事件、日志、链路追踪和指标的时序数据库。它使用 PostgreSQL 方言作为查询接口，底层数据写入 S3 并遵循 Delta Lake 协议进行存储，天然兼容大数据生态。

**价值**  
- **统一查询**：开发者可以直接用熟悉的 PostgreSQL SQL 对各种时序数据进行检索、聚合和分析，无需学习新 DSL。  
- **弹性存储**：数据落在 S3 上，借助 Delta Lake 的事务日志实现 ACID、版本回滚和增量读取，兼顾成本与可靠性。  
- **可观测性管道**：将原始日志/trace/metric 原样写入后，可快速构建搜索、告警、仪表盘或机器学习特征工程等自动化流水线。

**典型接入方式**  
1. **数据写入**：在业务服务或采集代理（如 Fluent Bit、OpenTelemetry Collector）中配置 JDBC/SQL‑compatible 连接，使用 `INSERT INTO ...` 或 `COPY` 将事件写入 TimeFusion；也可通过官方提供的 Rust 客户端库直接调用批量写入 API。  
2. **查询与分析**：在 BI 工具、Grafana、Superset 等支持 PostgreSQL 的前端，配置指向 TimeFusion 的连接字符串，即可使用标准 SQL 进行时序分析、窗口函数、JOIN 等高级查询。  
3. **数据治理**：利用 Delta Lake 的时间旅行功能，对历史快照进行审计或回滚；配合 S3 生命周期策略实现冷热分层存储。

**生产可用性**  
- **成熟度**：当前评分 50/100，GitHub 172 星、8 Fork，最近一次提交在 2026‑06‑24，代码主要使用 Rust 实现，社区活跃度一般。  
- **适用场景**：适合作为原型、内部实验或中小规模的可观测性平台；在正式生产环境使用前，需要对以下方面进行验证：  
  - **集成路径**：项目元数据中缺乏完整的接入示例，建议先在测试集群中手动搭建并验证写入/查询链路。  
  - **依赖与运维**：确保 S3 与 Delta Lake 兼容的版本已部署，监控写入延迟和事务日志大小，以防存储成本失控。  
  - **安全与权限**：PostgreSQL 方言的认证仍依赖外部 IAM/密码方案，需要自行实现 RBAC 与审计。  

综上，TimeFusion 在 **快速构建统一时序查询层** 方面具备明显优势，但在 **集成成熟度** 与 **运维成熟度** 上仍需自行补齐，适合作为内部原型或经充分验证后的生产服务。

## 🧭 Practical evaluation

**Value:** monoscope-tech/timefusion helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 172 GitHub stars
- 8 forks
- updated 2026-06-24
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 48/100 |
| topics | 0/100 |
| outlook | 43/100 |
| quality | 43/100 |
| recency | 40/100 |
| adoption | 41/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/monoscope-tech/timefusion) · [← Back to Database](./README.md)</sub>
