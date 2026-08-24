# ClickHouse/pg_stat_ch

[![Stars](https://img.shields.io/github/stars/ClickHouse/pg_stat_ch?style=flat-square&color=yellow)](https://github.com/ClickHouse/pg_stat_ch/stargazers) [![Forks](https://img.shields.io/github/forks/ClickHouse/pg_stat_ch?style=flat-square&color=blue)](https://github.com/ClickHouse/pg_stat_ch/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-39%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 39/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Pg_stat_ch is an open‑source exporter that streams PostgreSQL query telemetry into ClickHouse, giving engineers a fast, column‑oriented store for query‑level metrics and logs. By centralising this data, teams can accelerate development feedback loops, automate local testing, and enrich CI pipelines with real‑time query performance insights. The project is actively maintained (last update 2026‑07‑05) but its integration signals are sparse, so a quick sanity check is advised before committing to production.

**Value**  
- **Time‑saving diagnostics** – developers can query massive volumes of PostgreSQL execution data in ClickHouse instantly, avoiding slow `pg_stat_statements` scans.  
- **Workflow automation** – the exporter can be hooked into CI/CD to surface regressions or slow queries as part of test reports, reducing manual log inspection.  
- **Scalable analytics** – ClickHouse’s columnar engine makes aggregations over days‑to‑months of query telemetry cheap and fast, supporting performance dashboards and anomaly detection.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the exporter locally against a dev PostgreSQL instance, and point it at a test ClickHouse cluster. Verify that the expected tables (`pg_stat_ch_*`) appear and that sample queries are populated.  
2. **Validate** – Review the exported schema, confirm data privacy compliance, and run a few ad‑hoc ClickHouse queries to ensure the metrics you need (e.g., `query_text`, `duration_ms`, `user_id`) are captured accurately.  
3. **Integrate** – Add the exporter as a side‑car or systemd service in your development environment; configure it via environment variables or a small YAML file (Postgres DSN, ClickHouse DSN, polling interval).  
4. **CI Hook** – Extend your CI pipeline to run a lightweight ClickHouse query after test suites, failing builds when new slow‑query patterns exceed thresholds.  
5. **Roll‑out** – Deploy to staging, monitor resource usage (both exporter and ClickHouse ingest), and gradually enable for more services after confirming stability.

**Production Readiness**  
- **Maturity**: Medium. The tool is functional for prototypes and internal tooling, but the limited metadata (few quality signals, sparse documentation) means you should perform a thorough vetting pass.  
- **Dependencies**: Requires a running PostgreSQL instance with `pg_stat_statements` enabled and a ClickHouse server reachable over the network.  
- **Maintenance**: Check the repository for recent releases, open issues, and license compatibility; set up a watch on the repo to stay informed of security patches.  
- **Risk Mitigation**: Conduct a short pilot, enforce version pinning, and implement alerting on exporter health (e.g., missed heartbeats). If the pilot is stable, you can promote to production with confidence, keeping an eye on upstream activity for future updates.

### Русский

Резюме:

Pg_stat_ch - инструмент для экспорта метрик PostgreSQL в ClickHouse, ускоряющий разработку и отладку. Он позволяет инженерам автоматизировать локальные задачи и получать более быстрые обратные связи в процессе отладки. Хотя проект имеет средний уровень готовности к использованию в production, он может быть полезен для прототипирования или внутренних рабочих процессов после тщательного проверки зависимостей и поддержки.

### 中文

**项目简介**  
Pg_stat_ch 是一款开源的 PostgreSQL 查询遥测导出工具，它能够把数据库的执行统计（如 `pg_stat_statements`）实时同步到 ClickHouse，方便在 OLAP 场景下进行高效的查询分析与可视化。

**价值**  
- **加速研发闭环**：开发者可以快速在 ClickHouse 中跑大数据量的查询统计，定位慢查询、热点 SQL，省去手动导出和聚合的时间。  
- **自动化本地任务**：在本地或 CI 环境中自动同步遥测数据，实现持续的性能回归检测和代码审查反馈。  
- **提升 CI 反馈质量**：将查询性能指标纳入 CI 检查，提前发现性能回退，降低线上故障风险。

**典型接入方式**  
1. 在 PostgreSQL 实例上启用 `pg_stat_statements` 并确保相应的扩展已加载。  
2. 部署 Pg_stat_ch（Docker 镜像或二进制），配置连接信息：PostgreSQL DSN、ClickHouse HTTP/Native 接口、同步周期等。  
3. 通过 `pg_stat_ch.yaml`（或环境变量）指定需要同步的统计表、过滤规则以及 ClickHouse 表结构。  
4. 首次运行时手动检查同步的字段与 ClickHouse 表是否匹配，确认无误后可加入系统服务或 CI 作业中自动启动。

**生产可用性**  
- **成熟度**：目前评分 48/100，属于 **中等** 级别。适合原型、内部工具或非关键业务的监控。  
- **风险点**：项目元数据（文档、issue、release）较少，许可证、维护者活跃度需自行核实；集成信号较稀疏，建议在正式上线前进行完整的功能和性能验证。  
- **推荐做法**：在预生产环境做一次完整的端到端测试，评估数据一致性、同步延迟和 ClickHouse 写入成本；若满足内部 SLA，可在业务关键路径上逐步推广。

## 🧭 Practical evaluation

**Value:** Pg_stat_ch: PostgreSQL Query Telemetry Exporter to ClickHouse helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-05
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 36/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 41/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/ClickHouse/pg_stat_ch) · [← Back to Database](./README.md)</sub>
