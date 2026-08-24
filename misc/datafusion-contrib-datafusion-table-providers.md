# datafusion-contrib/datafusion-table-providers

[![Stars](https://img.shields.io/github/stars/datafusion-contrib/datafusion-table-providers?style=flat-square&color=yellow)](https://github.com/datafusion-contrib/datafusion-table-providers/stargazers) [![Forks](https://img.shields.io/github/forks/datafusion-contrib/datafusion-table-providers?style=flat-square&color=blue)](https://github.com/datafusion-contrib/datafusion-table-providers/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> DataFusion TableProviders for reading data from other systems

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 192 |
| 🍴 **Forks** | 72 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
`datafusion-contrib/datafusion-table-providers` supplies a collection of TableProvider implementations for Apache DataFusion, enabling the engine to read directly from external storage systems and services. By plugging these providers into DataFusion, developers can query heterogeneous data sources with SQL‑like syntax without writing custom adapters. The crate is actively maintained (last update 2026‑06‑25) and written in Rust, with a modest community footprint (≈190 ★, 70 forks).

**Value proposition**  
- **Unified access** – Turn disparate data stores (e.g., CSV, Parquet, S3, custom APIs) into first‑class tables that DataFusion can scan, filter, and join, accelerating analytics and ETL pipelines.  
- **Low‑code integration** – Instead of building bespoke readers, you import the appropriate TableProvider crate and register it with a DataFusion context, reducing development effort and bugs.  
- **Extensibility** – The TableProvider trait is open, so you can extend the library with your own connectors while reusing DataFusion’s query optimizer and execution engine.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1. **Evaluate source compatibility** | Review the list of built‑in providers (e.g., `csv`, `parquet`, `s3`, `http`) and test them against a representative sample of your data. | Confirms that the provider can read your format and that performance meets expectations. |
| 2. **Prototype a DataFusion query** | Create a small Rust binary or notebook, add the provider crate as a dependency, register the table (`ctx.register_table("my_data", provider)`) and run a simple SQL query. | Validates the integration surface and helps you discover any missing configuration (auth, schema inference, etc.). |
| 3. **Integrate into your pipeline** | Replace the prototype code with the provider registration in your existing ETL or analytics service, handling error propagation and connection pooling as needed. | Moves from proof‑of‑concept to a reusable component. |
| 4. **Add tests & monitoring** | Write integration tests that cover schema discovery, data correctness, and failure modes; instrument query latency and resource usage. | Guarantees reliability before promotion to production. |
| 5. **Lock dependencies & CI** | Pin the provider version, enable Cargo audit, and add the crate to your CI pipeline for regular updates and security checks. | Mitigates supply‑chain risk and ensures reproducible builds. |

**Production readiness**  
- **Maturity:** Medium. The library is functional and receives regular updates, but the integration documentation is thin and the ecosystem around TableProviders is still evolving.  
- **Suitable workloads:** Internal prototypes, analytics sandboxes, and low‑to‑moderate volume data pipelines where the convenience of a unified query layer outweighs the overhead of an extra abstraction.  
- **Risks & mitigations:**  
  - *Integration ambiguity*: Because metadata on supported back‑ends is sparse, you must manually verify that a provider works with your specific storage configuration (authentication, schema evolution, etc.).  
  - *Dependency churn*: Keep an eye on the upstream DataFusion version compatibility; pinning versions and running automated compatibility tests reduces breakage.  
  - *Performance*: TableProviders may not be as optimized as native connectors; benchmark critical queries and consider custom providers for high‑throughput paths.  

Overall, `datafusion-table-providers` is a practical way to accelerate analytics prototyping and can be hardened for production with thorough testing, dependency management, and performance validation.

### Русский

**datafusion-contrib/datafusion-table-providers** — это набор TableProvider‑ов для Apache DataFusion, позволяющий подключать и читать данные из внешних систем (БД, файловых хранилищ, API) непосредственно в запросах DataFusion. Типичный сценарий: разработчик быстро собирает прототип аналитического пайплайна, подключая новые источники без написания собственного коннектора, а затем использует полученные таблицы в SQL‑аналитике или автоматических ETL‑процессах. Готовность к продакшн — средняя: проект имеет активную поддержку (192★, 72 форка, последний коммит 25 июня 2026), но интеграция требует ручной проверки и настройки, поэтому рекомендуется использовать его в прототипах или внутренних workflow после тщательной валидации зависимостей и стабильности.

### 中文

**项目简介**  
`datafusion-contrib/datafusion-table-providers` 是一套基于 Apache DataFusion 的 TableProvider 实现，能够让 DataFusion 直接读取 MySQL、PostgreSQL、CSV、Parquet 等外部存储或服务的数据，进而在统一的 SQL 引擎中进行查询和分析。

**价值**  
- **统一查询入口**：无需为每个数据源单独写 ETL，直接在 DataFusion 中通过 `SELECT` 跨系统查询，极大降低数据整合成本。  
- **加速原型与内部分析**：开发者可以快速把原始业务系统的数据挂载为表，立刻用于探索、报表或机器学习特征工程。  
- **可组合的查询管道**：结合 DataFusion 的算子优化与并行执行，引入外部数据时仍能享受向量化计算和查询计划优化。

**典型接入方式**  
1. **在 Rust 项目中添加依赖**  
   ```toml
   [dependencies]
   datafusion-table-providers = { git = "https://github.com/datafusion-contrib/datafusion-table-providers", tag = "v0.1.0" }
   ```
2. **创建对应的 TableProvider**（示例：PostgreSQL）  
   ```rust
   use datafusion_table_providers::postgres::PostgresTableProvider;
   use datafusion::execution::context::SessionContext;

   let ctx = SessionContext::new();
   let pg_provider = PostgresTableProvider::new(
       "postgres://user:pwd@host:5432/dbname",
       "public.my_table",
   )?;
   ctx.register_table("my_pg_table", Arc::new(pg_provider))?;
   ```
3. **直接使用 SQL 查询**  
   ```sql
   SELECT * FROM my_pg_table WHERE created_at > CURRENT_DATE - INTERVAL '7 days';
   ```
4. **在更复杂的管道中组合**（如与本地 Parquet 表联表、窗口函数等），无需额外的 ETL 作业。

**生产可用性**  
- **成熟度**：Medium。项目已有 192 星、72 Fork，活跃维护至 2026‑06‑25，代码质量和文档基本完整，适合作为原型或内部数据平台的“数据桥”。  
- **依赖与运维**：依赖 DataFusion（Rust）和对应外部驱动（如 `tokio-postgres`、`csv`、`parquet`），需要在 CI/CD 中锁定版本并定期检查安全更新。  
- **上线建议**  
  1. **先在测试环境验证**：对目标数据源执行一次全表扫描，确认字段映射、时区、NULL 处理等细节。  
  2. **监控查询成本**：外部系统的网络延迟和并发限制会直接影响 DataFusion 的执行计划，建议开启查询日志并设置超时。  
  3. **容错设计**：在生产环境可将关键查询预先 materialize 为本地 Parquet，降低对外部系统的实时依赖。  

综上，`datafusion-table-providers` 能帮助团队快速构建跨系统的分析查询层，适合原型、内部报表或作为数据湖的入口层；在正式生产环境使用时，需要做好依赖管理、性能基准和容错措施。

## 🧭 Practical evaluation

**Value:** datafusion-contrib/datafusion-table-providers helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 192 GitHub stars
- 72 forks
- updated 2026-06-25
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 49/100 |
| topics | 0/100 |
| outlook | 44/100 |
| quality | 47/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 48/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/datafusion-contrib/datafusion-table-providers) · [← Back to Misc](./README.md)</sub>
