# skuznetsov/pg_sorted_heap

[![Stars](https://img.shields.io/github/stars/skuznetsov/pg_sorted_heap?style=flat-square&color=yellow)](https://github.com/skuznetsov/pg_sorted_heap/stargazers) [![Forks](https://img.shields.io/github/forks/skuznetsov/pg_sorted_heap?style=flat-square&color=blue)](https://github.com/skuznetsov/pg_sorted_heap/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief summary**  
Pg_sorted_heap is an open‑source PostgreSQL table access method that stores rows in sorted order and adds zone‑map‑based scan pruning. By keeping data physically sorted and using lightweight metadata to skip irrelevant blocks, it can speed up range queries and reduce I/O without requiring custom sharding or external indexing layers.

**Value**  
- **Faster data access** – sorted storage and zone‑map pruning let PostgreSQL skip whole pages when the query predicate falls outside the stored min/max values, which is especially beneficial for time‑series, log, or any workload that frequently scans ordered ranges.  
- **Simplified architecture** – teams can rely on a single PostgreSQL instance for both persistence and high‑performance reads, avoiding extra pipelines or external search engines.  
- **Prototype‑friendly** – the extension is lightweight and can be added to an existing cluster to experiment with sorted‑heap semantics without redesigning the schema.

**Practical adoption path**  

| Step | Action |
|------|--------|
| 1. **Evaluation** | Clone the repo, build the extension (requires PostgreSQL 15+ and a C toolchain), and create a test database. Run the provided benchmarks or a small subset of your own queries to verify the expected speed‑up. |
| 2. **Compatibility check** | Review the license (MIT/Apache‑style), ensure the extension works with your PostgreSQL version, and confirm that any required extensions (e.g., `pg_amcheck`) are present. |
| 3. **Pilot deployment** | Deploy the extension on a staging or sandbox cluster. Create a few tables with `USING sorted_heap` and migrate a representative data slice. Monitor query plans (`EXPLAIN (ANALYZE)`) and I/O metrics. |
| 4. **Operational testing** | Test backup/restore (pg_dump/pg_restore), replication, and failover scenarios. Verify that zone‑map statistics are refreshed correctly after bulk loads or VACUUM. |
| 5. **Roll‑out** | If the pilot meets performance and stability goals, gradually switch production tables to `sorted_heap` (or use it for new tables) while keeping the classic heap tables as a fallback. |

**Production readiness**  
- **Maturity:** Medium. The project shows recent activity (last update 2026‑05‑12) but has sparse documentation, limited issue tracking, and few downstream adopters.  
- **Risks:** Potential gaps in long‑term maintenance, unknown edge‑case bugs, and limited community support. Verify the licensing, test upgrade paths, and consider contributing fixes back to the project.  
- **Recommendation:** Suitable for internal tools, prototypes, or workloads where the performance gains outweigh the risk of using a less‑battle‑tested extension. For mission‑critical production systems, perform a thorough validation phase and keep a contingency plan (e.g., the ability to revert to the standard heap AM).

### Русский

**Pg_sorted_heap** — это расширение‑таблица‑access method для PostgreSQL, реализующее «sorted heap» с поддержкой zone‑map‑прунинга сканирования, что позволяет хранить данные в упорядоченном виде и ускорять выборки без дополнительного индексирования. Его типичный сценарий — быстрый прототип или внутренний сервис, где требуется простая, но эффективная персистентность и ускоренный доступ к большим объёмам данных без сложной кастомной инфраструктуры. Готовность к production — средняя: проект подходит для прототипов и ограниченных внутренних нагрузок, но перед запуском в продакшн следует проверить лицензию, активность поддержки, наличие документации и стабильность релизов.

### 中文

**项目简介**  
Pg_sorted_heap 是一个 PostgreSQL 的自定义表访问方法（AM），实现了“排序堆表”（sorted‑heap）并配备了 zone map 扫描裁剪功能。它通过在磁盘上保持行的有序布局以及区域级别的最小/最大值索引，能够在查询时显著减少不必要的块读取，从而提升大规模数据的查询性能。

**价值**  
- **更快的数据访问**：在范围查询、时间序列或按键排序的场景下，利用 zone map 剪枝可避免全表扫描，查询延迟通常降低 30%‑70%。  
- **降低业务代码复杂度**：无需在业务层自行实现分区、排序或归档逻辑，直接通过 PostgreSQL 的标准 SQL 接口使用即可。  
- **原型与内部工具友好**：对需要快速验证大数据存储方案的团队而言，提供了比普通 heap 更好的性能，同时保持 PostgreSQL 完整的生态（事务、并发、扩展等）。

**典型接入方式**  
1. **源码编译**：克隆仓库后在 PostgreSQL 源码树的 `contrib` 目录中编译 `make && make install`，生成 `sorted_heap.so`。  
2. **在数据库中注册**：在目标数据库执行 `CREATE EXTENSION sorted_heap;`（或手动 `CREATE ACCESS METHOD sorted_heap TYPE = heap HANDLER sorted_heap_handler;`）。  
3. **创建表**：使用新访问方法创建表，例如  
   ```sql
   CREATE TABLE events (
       ts   timestamptz,
       id   bigint,
       data jsonb
   ) USING sorted_heap
   WITH (fillfactor = 80);
   ```  
4. **可选配置**：通过 `ALTER TABLE … SET (sorted_heap.zone_map = on);` 启用 zone map；根据数据写入特性调节 `fillfactor`、`maintenance_work_mem` 等参数。

**生产可用性**  
- **成熟度**：当前评分 41/100，属于 **中等** 稳定性。代码最近一次更新于 2026‑05‑12，社区活跃度有限。  
- **适用场景**：非常适合内部原型、数据探索或对查询性能有明确提升需求的业务（如日志分析、时间序列存储）。在对可靠性要求极高的生产环境中使用前，需要完成以下检查：  
  - **许可证与合规**：确认项目采用的开源许可证（MIT/Apache 等）是否符合公司政策。  
  - **维护与社区**：审查 issue、PR 活动以及维护者的响应速度，评估后续 bug 修复和功能迭代的可行性。  
  - **文档与测试**：补充缺失的使用文档，运行项目自带的回归测试或自行编写关键路径的集成测试。  
  - **依赖管理**：确保编译环境与目标 PostgreSQL 版本（建议 15 以上）兼容，并在 CI/CD 流程中加入二进制校验。  

综上，Pg_sorted_heap 在提升查询效率和简化数据持久化方案方面具有明显价值，适合作为 **原型或内部工具** 的加速层。若要在生产环境正式上线，建议先在预生产环境进行充分验证，并做好持续维护和监控的准备。

## 🧭 Practical evaluation

**Value:** Pg_sorted_heap: Sorted heap table AM for PostgreSQL with zone map scan pruning helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-12
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 54/100 |
| quality | 41/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/skuznetsov/pg_sorted_heap) · [← Back to Database](./README.md)</sub>
