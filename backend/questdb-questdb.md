# questdb/questdb

[![Stars](https://img.shields.io/github/stars/questdb/questdb?style=flat-square&color=yellow)](https://github.com/questdb/questdb/stargazers) [![Forks](https://img.shields.io/github/forks/questdb/questdb?style=flat-square&color=blue)](https://github.com/questdb/questdb/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> QuestDB is a high performance, open-source, time-series database

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 17.1k |
| 🍴 **Forks** | 1.6k |
| 💻 **Language** | Java |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-06-25 |
| 🔍 **Source** | github |

## 🏷️ Topics

`capital-markets` `cpp` `database` `financial-analysis` `grafana` `java` `kdb` `low-latency` `market-data` `olap` `parquet` `postgresql`

## 🎯 Categories

Backend · Data · Database

## 📝 Summary

### English

**Brief Summary**  
QuestDB is a high‑performance, open‑source time‑series database written in Java, designed to ingest and query massive streams of timestamped data with sub‑second latency. With more than 17 k stars, active development, and a rich set of APIs/SDKs/CLI tools, it offers a ready‑to‑use backend component that teams can adopt instead of building their own time‑series storage layer.

**Value**  
By providing a purpose‑built, SQL‑compatible engine for time‑series workloads, QuestDB lets engineering teams standardize on a single, battle‑tested data store for metrics, logs, IoT telemetry, and financial tick data. This eliminates the need to reinvent ingestion pipelines, indexing strategies, and query optimizations, freeing resources to focus on domain‑specific logic and faster API delivery.

**Practical Adoption Path**  
1. **Evaluation** – Spin up a local Docker container or use the provided CLI to ingest a sample data set and run familiar SQL queries.  
2. **Integration** – Choose the appropriate client (Java, Python, Go, etc.) or the REST/InfluxDB line protocol to connect existing services.  
3. **Migration** – Replace legacy time‑series stores by replicating write paths to QuestDB while keeping read‑through queries unchanged, leveraging its drop‑in SQL compatibility.  
4. **Production Roll‑out** – Deploy QuestDB in a clustered mode (or use the managed cloud offering) behind a load balancer, configure retention policies, and monitor health via its built‑in metrics.

**Production Readiness**  
QuestDB scores high on production readiness: recent commits (as of 2026‑06‑25), a vibrant community (17 k stars, 1.6 k forks), extensive documentation, and multiple language bindings demonstrate strong ecosystem support. While the license and security posture should be verified in a formal review, the project's active maintainers and proven deployments in fintech and monitoring platforms make it a solid candidate for serious pilot projects and eventual full‑scale production use.

### Русский

QuestDB — это высокопроизводительная open‑source СУБД для временных рядов, позволяющая командам быстро переиспользовать готовую инфраструктуру бекенда вместо разработки собственных решений. Типичный сценарий — ускоренный запуск API‑сервисов и стандартизация паттернов работы с данными, благодаря простому подключению через API/SDK/CLI. Проект имеет высокий уровень готовности к production: активные обновления, более 17 k звёзд на GitHub, широкое принятие и зрелую экосистему, хотя окончательная проверка лицензии и безопасности всё же требуется.

### 中文

**简短介绍**  
QuestDB 是一款高性能、开源的时序数据库，专为海量写入和低延迟查询而设计，基于 Java 实现并拥有活跃的社区与生态。  

**价值**  
- 为团队提供即插即用的时序存储层，避免重复搭建和维护底层基础设施。  
- 通过统一的 API/SDK/CLI，帮助业务快速上线 API 服务、统一后端模式并提升运维效率。  

**典型接入方式**  
1. **JDBC/HTTP 接口**：直接使用标准 JDBC 驱动或 RESTful HTTP API 进行数据写入和查询。  
2. **官方 SDK**：提供 Java、Python、Node.js 等语言的客户端库，便于在现有服务中集成。  
3. **CLI 工具**：通过 `questdb` 命令行工具进行快速数据导入、表结构管理和监控。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，GitHub ★17.1k、Fork 1.6k，最近一次提交在 2026 年，社区活跃，Issue 处理及时。  
- **成熟度**：已在多个大规模生产环境中使用，提供完整的备份、复制与容错机制。  
- **可靠性**：支持持久化 WAL、零停机升级和高并发写入，满足实时监控、金融、IoT 等高可靠性场景的需求。  

综上，QuestDB 具备强大的时序处理能力、易于集成的接口以及经过验证的生产级稳定性，是构建高性能后端服务的可靠选择。

## 🧭 Practical evaluation

**Value:** questdb/questdb helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 17133 GitHub stars
- 1613 forks
- updated 2026-06-25
- primary language: Java
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 80/100 |
| stars | 90/100 |
| topics | 100/100 |
| outlook | 88/100 |
| quality | 94/100 |
| recency | 100/100 |
| adoption | 87/100 |
| production | 82/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/questdb/questdb) · [← Back to Backend](./README.md)</sub>
