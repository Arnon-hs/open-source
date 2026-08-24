# datafusion-contrib/datafusion-federation

[![Stars](https://img.shields.io/github/stars/datafusion-contrib/datafusion-federation?style=flat-square&color=yellow)](https://github.com/datafusion-contrib/datafusion-federation/stargazers) [![Forks](https://img.shields.io/github/forks/datafusion-contrib/datafusion-federation?style=flat-square&color=blue)](https://github.com/datafusion-contrib/datafusion-federation/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-42%2F100-brightgreen?style=flat-square)](#)

> Allow DataFusion to resolve queries across remote query engines while pushing down as much compute as possible down.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 184 |
| 🍴 **Forks** | 30 |
| 💻 **Language** | Rust |
| 📈 **Score** | 42/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`datafusion-contrib/datafusion-federation` extends the Apache Arrow‑based DataFusion query engine with federated query capabilities, allowing it to push down computation to remote query engines and combine results locally. The crate lets you build analytics pipelines that span heterogeneous data sources while keeping as much processing as possible on the source systems.  

**Value Proposition**  
- **Unified analytics**: Treat multiple, potentially disparate query engines (e.g., Postgres, ClickHouse, Snowflake) as a single logical data source, simplifying data discovery and reporting.  
- **Performance‑first**: By automatically pushing down filters, projections, and aggregates, the library reduces data movement and leverages the native performance of each remote engine.  
- **Rust‑native integration**: Fits naturally into Rust‑centric data stacks, preserving zero‑copy Arrow semantics and enabling type‑safe pipelines.  

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Prototype** – Add the crate to a sandbox Rust project and point it at a single remote engine (e.g., a local PostgreSQL instance). Verify that simple SELECTs and filter push‑downs work. | Confirms basic compatibility and lets you explore the API without affecting production code. |
| 2️⃣  | **Add a second source** – Configure a second remote engine (e.g., a ClickHouse cluster) and run a federated query that joins tables from both sources. Observe the generated execution plan via `DataFusion::explain`. | Demonstrates the federation logic and reveals any limitations in join push‑down or type mapping. |
| 3️⃣  | **Integrate with your pipeline** – Replace ad‑hoc SQL calls in your existing Rust analytics service with a `DataFusion` context that registers the remote tables via the federation API. | Provides a single entry point for downstream services and reduces duplicated query logic. |
| 4️⃣  | **Automated tests** – Write integration tests that spin up lightweight containers for each remote engine (Docker Compose) and assert query correctness and performance expectations. | Guarantees regressions are caught early and clarifies the maintenance burden. |
| 5️⃣  | **Observability & monitoring** – Hook into DataFusion’s `ExecutionPlan` metrics and log the remote push‑down decisions. | Helps you tune which operations should stay remote vs. be performed locally. |
| 6️⃣  | **Production hardening** – Freeze the crate version, add CI checks for dependency updates, and document the required remote‑engine configurations (authentication, network access, supported SQL dialects). | Reduces the risk of breaking changes and clarifies operational responsibilities. |

**Production Readiness**  
- **Maturity**: The project has modest adoption (≈184 ★, 30 forks) and recent activity (last commit 2026‑07‑02), indicating it is maintained but not yet a widely‑used component.  
- **Readiness Level**: *Medium* – suitable for internal prototypes, proof‑of‑concepts, or low‑risk production workloads after a validation phase.  
- **Risks**: Integration details (authentication, dialect mapping, error handling) are not fully described in the metadata, so you’ll need to invest time in manual testing and possibly contribute patches. Dependency management is straightforward (pure Rust), but keep an eye on the upstream DataFusion version compatibility.  

**Bottom line** – `datafusion-federation` can be a powerful building block for Rust‑based analytics platforms that need to query across heterogeneous data stores with minimal data movement. With a small but focused integration effort—starting with a sandbox prototype, adding tests, and documenting the remote‑engine setup—you can move it from prototype to a reliable internal service, while remaining cautious about the limited community support before committing to a large‑scale production deployment.

### Русский

**datafusion-contrib/datafusion-federation** — это библиотека на Rust, расширяющая DataFusion возможностью выполнять запросы к удалённым движкам и максимально «проталкивать» вычисления к источникам данных. Она подходит для построения аналитических пайплайнов и автоматизированных отчётных процессов, где требуется объединять данные из разных систем без копирования их в один хранилище. Готовность к продакшн — средняя: проект стабилен для прототипов и внутренних сервисов, но требует ручной проверки интеграции и контроля зависимостей перед масштабным внедрением.

### 中文

**项目简介**  
`datafusion-contrib/datafusion-federation` 为 Apache DataFusion 增加了跨远程查询引擎的联邦查询能力，能够在尽可能多的层面向下推送计算，从而在统一的 SQL 接口下查询分布在不同系统（如 ClickHouse、PostgreSQL、Parquet 存储等）中的数据。

**价值**  
- **统一查询层**：开发者只需编写一次 SQL，即可跨多个后端数据源获取结果，省去手动 ETL 与数据搬迁的成本。  
- **计算下推**：尽量把过滤、投影、聚合等操作下推到原始数据源执行，降低网络传输和中心节点的计算压力。  
- **加速原型与内部分析**：在数据湖、数据仓库或微服务数据库之间快速搭建分析管道，提升业务洞察速度。

**典型接入方式**  
1. **依赖引入**：在 Cargo.toml 中加入 `datafusion-federation`（或通过 `datafusion-contrib` 的 workspace）。  
2. **注册远程数据源**：使用 `FederatedTableProvider` 为每个远程查询引擎创建 `TableProvider`，并在 DataFusion 的 `SessionContext` 中注册（如 `ctx.register_table("orders", provider)`）。  
3. **查询执行**：直接在 `SessionContext::sql` 中编写跨源 SQL，DataFusion 会在执行计划阶段自动决定哪些子计划可以下推到对应的远程引擎。  
4. **可选调优**：通过 `FederationConfig` 调整下推策略、连接池、超时等参数，以适配不同后端的性能特性。

**生产可用性**  
- **成熟度**：Medium。项目已获得 184 星、30 fork，最近一次提交在 2026‑07‑02，代码质量和活跃度较好，但官方文档和集成示例仍较少。  
- **适用场景**：适合原型开发、内部数据分析平台或对跨源查询有明确需求的团队。若用于关键业务，建议在预生产环境进行充分的 **依赖兼容性、错误恢复和性能基准** 测试。  
- **风险与注意事项**  
  - 集成路径不够显式，需自行检查远程引擎的 SQL 方言兼容性以及网络/认证配置。  
  - 下推能力受限于后端引擎的功能支持，复杂的聚合或自定义函数可能仍在 DataFusion 本地执行。  
  - 维护成本：随着 DataFusion 主库升级，联邦插件可能需要同步更新。  

**结论**  
`datafusion-federation` 为需要在多个异构数据源上进行统一分析的团队提供了一个轻量级、Rust 原生的解决方案。通过合理的配置与充分的前期验证，可在原型和内部业务系统中快速实现跨源查询；在进入生产环境前，需要完成依赖审计、性能压测以及容错机制的补充。

## 🧭 Practical evaluation

**Value:** datafusion-contrib/datafusion-federation helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 184 GitHub stars
- 30 forks
- updated 2026-07-02
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 48/100 |
| topics | 0/100 |
| outlook | 44/100 |
| quality | 45/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/datafusion-contrib/datafusion-federation) · [← Back to Misc](./README.md)</sub>
