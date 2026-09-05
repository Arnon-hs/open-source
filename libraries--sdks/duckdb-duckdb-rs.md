# duckdb/duckdb-rs

[![Stars](https://img.shields.io/github/stars/duckdb/duckdb-rs?style=flat-square&color=yellow)](https://github.com/duckdb/duckdb-rs/stargazers) [![Forks](https://img.shields.io/github/forks/duckdb/duckdb-rs?style=flat-square&color=blue)](https://github.com/duckdb/duckdb-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Ergonomic bindings to duckdb for Rust

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 928 |
| 🍴 **Forks** | 230 |
| 💻 **Language** | Rust |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`arrow` `database` `duckdb` `ffi` `ffi-bindings` `olap` `rust`

## 🎯 Categories

Libraries & SDKs · Database

## 📝 Summary

### English

**Summary**  
duckdb‑rs provides idiomatic, high‑level Rust bindings for DuckDB, letting developers embed an in‑process analytical database directly into Rust applications. The crate streamlines data ingestion, transformation, and querying, making it ideal for building analytics pipelines, dataset processing jobs, and automated reporting workflows. With active maintenance, a growing community, and recent releases, it is ready for serious pilot projects.

**Value**  
By exposing DuckDB’s powerful SQL engine through ergonomic Rust APIs, duckdb‑rs turns raw data files (CSV, Parquet, JSON, etc.) into instantly queryable tables without external services. This enables low‑latency analytics, reproducible data pipelines, and cost‑effective reporting—all within the same binary that runs the business logic, reducing operational overhead and simplifying deployment.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repository, run the examples in the README, and connect the crate to a small sample dataset to validate query correctness and performance.  
2. **Integration** – Add `duckdb = { version = "...", features = ["bundled"] }` to your Cargo.toml, wrap the connection in a service layer, and replace ad‑hoc CSV reads or external DB calls with DuckDB queries.  
3. **Testing & CI** – Write integration tests that spin up an in‑process DuckDB instance, ensuring query results remain stable across versions.  
4. **Scaling** – For larger workloads, consider using DuckDB’s parallel execution settings, persisting the on‑disk database, and monitoring resource usage.

**Production readiness**  
The project scores high on readiness: it has 928 stars, 230 forks, recent commits (as of 2026‑07‑03), active issue handling, and a well‑documented API. Its Rust‑first design aligns with modern systems programming stacks, and the DuckDB engine itself is battle‑tested in analytics use cases. While a final review of licensing (MIT) and security posture is still advisable, the overall signal suggests duckdb‑rs is mature enough for a production pilot and can be safely promoted to a core component once the small‑scale proof of concept validates the expected performance and stability.

### Русский

**duckdb/duckdb-rs** — это удобные Rust‑биндинги к встраиваемой аналитической базе DuckDB, позволяющие быстро превращать сырые данные в индексируемые таблицы и подключать их к автоматическим аналитическим пайплайнам. Типичное внедрение начинается с небольшого proof‑of‑concept: подключаем crate, загружаем CSV/Parquet в DuckDB и строим запросы/агрегации, после чего расширяем решение до полноценного ETL‑ или reporting‑модуля. По показателям активности, популярности (928 звёзд, 230 форков) и поддержке сообществом проект готов к продакшн‑использованию, однако перед масштабным запуском следует проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
`duckdb/duckdb-rs` 为 Rust 提供了 ergonomics 极佳的 DuckDB 绑定，使得在本地或嵌入式环境中即可使用 SQL 对结构化数据进行快速查询、分析和管道化处理。它将 DuckDB 的高性能列式存储与 Rust 的安全、零成本抽象相结合，适合构建轻量级数据分析或 ETL 工作流。

**价值**  
- **快速转化原始数据**：在 Rust 程序中直接执行 SQL，省去手写解析、聚合等逻辑。  
- **统一分析管道**：可把数据清洗、特征工程、报表生成等步骤统一在同一个库里完成，降低系统复杂度。  
- **高性能、低资源占用**：DuckDB 是内存/磁盘混合的列式数据库，适合单机或边缘设备的批量分析。  

**典型接入方式**  
1. **阅读 README 并运行示例**：确认编译环境（Rust 1.70+）和依赖（`duckdb` 动态库或通过 `bundled` feature 自动编译）。  
2. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   duckdb = { version = "0.10", features = ["bundled"] }
   ```
3. **创建连接并执行 SQL**  
   ```rust
   use duckdb::{Connection, Result};

   fn main() -> Result<()> {
       let conn = Connection::open_in_memory()?; // 或者打开文件路径
       conn.execute_batch(
           r#"
           CREATE TABLE sales (id BIGINT, amount DOUBLE, date DATE);
           INSERT INTO sales VALUES (1, 100.0, '2023-01-01');
           "#,
       )?;
       let mut stmt = conn.prepare("SELECT SUM(amount) FROM sales")?;
       let total: f64 = stmt.query_row([], |row| row.get(0))?;
       println!("Total sales: {}", total);
       Ok(())
   }
   ```
4. **在实际项目中封装为数据访问层**，配合 `async`、`tokio` 或 `rayon` 实现并行查询或批处理。  
5. **先做小规模 PoC**：在测试数据集上验证查询性能、错误处理和资源占用，再逐步扩展到生产数据量。

**生产可用性**  
- **活跃度**：截至 2026‑07‑03，项目仍在频繁更新，拥有 928 ★、230 Fork，且最近一次提交仅几天前。  
- **生态兼容**：Rust 官方推荐的数据库绑定之一，已被多个开源项目（如 Polars、DataFusion）采纳。  
- **成熟度**：DuckDB 本身在数据科学社区拥有广泛的生产使用案例，`duckdb-rs` 继承了其稳定的查询引擎。  
- **风险评估**：暂无重大元数据或许可证风险，但仍建议在正式上线前完成安全审计（检查依赖的 C/C++ 编译器链、动态库签名等）并确认维护者的响应时效。  

综上，`duckdb/duckdb-rs` 在功能、性能和社区支持方面均已具备进入生产环境的条件，适合作为 Rust 项目中轻量级分析或 ETL 的核心组件。

## 🧭 Practical evaluation

**Value:** duckdb/duckdb-rs helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 928 GitHub stars
- 230 forks
- updated 2026-07-03
- primary language: Rust
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 63/100 |
| topics | 88/100 |
| outlook | 71/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/duckdb/duckdb-rs) · [← Back to Libraries--sdks](./README.md)</sub>
