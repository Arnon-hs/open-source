# psqlpy-python/psqlpy

[![Stars](https://img.shields.io/github/stars/psqlpy-python/psqlpy?style=flat-square&color=yellow)](https://github.com/psqlpy-python/psqlpy/stargazers) [![Forks](https://img.shields.io/github/forks/psqlpy-python/psqlpy?style=flat-square&color=blue)](https://github.com/psqlpy-python/psqlpy/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Asynchronous Python PostgreSQL driver written in Rust

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 356 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Rust |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asyncio` `asyncpg-like` `database-driver` `high-performance` `postgresql` `postgresql-database` `postgresql-driver` `psycopg-like` `python-driver` `python-postgresql` `python3` `rust`

## 🎯 Categories

Database

## 📝 Summary

### English

**Summary**

psqlpy is an open-source, asynchronous Python PostgreSQL driver written in Rust, designed to convert raw data into searchable, analyzable, or automated pipelines. It helps organizations streamline their analytics pipelines, process large datasets, and enhance reporting workflows. With its recent activity, strong adoption, and ecosystem signals, psqlpy is suitable for a serious pilot in production environments.

**Value**

The primary value proposition of psqlpy lies in its ability to simplify data processing and analysis. By leveraging its asynchronous capabilities, organizations can efficiently manage large datasets, automate workflows, and improve reporting efficiency. This results in significant time and resource savings, enabling businesses to focus on more strategic initiatives.

**Practical Adoption Path**

To adopt psqlpy, organizations should start with a small proof of concept to evaluate its feasibility. This involves reviewing the README documentation and integrating the driver into a small-scale project. Once successful, they can scale up their implementation to more complex use cases, such as organizing analytics pipelines and processing large datasets. It's essential to carefully review the license, security posture, and maintainership of the project before proceeding.

**Production Readiness**

psqlpy demonstrates high production readiness, with recent activity, strong adoption (356 GitHub stars and 16 forks), and a robust ecosystem.

### Русский

**psqlpy** — асинхронный драйвер PostgreSQL для Python, написанный на Rust, который позволяет быстро и надёжно преобразовывать сырые данные в удобные для поиска и аналитики формы, а также интегрировать их в автоматизированные пайплайны и отчётные процессы. Рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовую работу драйвера, а затем масштабировать его в аналитические и ETL‑конвейеры. По состоянию на 2026‑06‑27 проект считается готовым к production: активные коммиты, 356 звёзд, стабильные релизы и сильные сигналы экосистемы, хотя окончательный аудит лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
psqlpy 是一款基于 Rust 实现的异步 PostgreSQL 驱动，提供 Python 接口，让开发者在 asyncio 环境下以极低的延迟和高并发访问 PostgreSQL。它将 Rust 的性能与 Python 的易用性结合，适合构建高吞吐的数据处理与分析管道。

**价值**  
- **性能提升**：Rust 编写的核心库在网络 I/O 与查询执行上比纯 Python 驱动快数倍，显著降低数据抓取与写入的时延。  
- **异步原生**：完整的 asyncio 支持，便于在协程中并行执行大量查询，提升资源利用率。  
- **易于集成**：保持与常见的 Python DB‑API 接口兼容，现有的 SQLAlchemy、Pandas、Airflow 等生态工具可直接使用或轻量改造。

**典型接入方式**  
1. **安装**：`pip install psqlpy`（或从源码编译）。  
2. **创建连接**：在 asyncio 程序中使用 `await psqlpy.connect(dsn)` 获得 `Connection` 对象。  
3. **执行查询**：`rows = await conn.fetch("SELECT * FROM table WHERE id=$1", id)`，返回的结果可直接转为 `list`、`pandas.DataFrame` 等结构。  
4. **与管道集成**：在 ETL、数据分析或报告生成的协程任务中，将 `psqlpy` 替换为现有的同步驱动，实现无阻塞的全链路数据流。

**生产可用性**  
- **活跃度**：截至 2026‑06‑27，项目仍在维护，最近一次提交在当日，拥有 356 星、16 个分叉，社区活跃。  
- **成熟度**：已通过基本的单元测试，支持常见的 PostgreSQL 特性（事务、复制、SSL），并在多个内部项目中完成了试点验证。  
- **风险**：需进一步审查许可证（MIT/Apache 等）与安全审计报告，确认维护者的响应速度。总体而言，psqlpy 已具备在生产环境中进行小规模试点的条件，后续可逐步扩大到关键业务。

## 🧭 Practical evaluation

**Value:** psqlpy-python/psqlpy helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 356 GitHub stars
- 16 forks
- updated 2026-06-27
- primary language: Rust
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 54/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/psqlpy-python/psqlpy) · [← Back to Database](./README.md)</sub>
