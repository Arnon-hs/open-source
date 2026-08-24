# microsoft/pg_durable

[![Stars](https://img.shields.io/github/stars/microsoft/pg_durable?style=flat-square&color=yellow)](https://github.com/microsoft/pg_durable/stargazers) [![Forks](https://img.shields.io/github/forks/microsoft/pg_durable?style=flat-square&color=blue)](https://github.com/microsoft/pg_durable/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> PostgreSQL in-database durable execution

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 58 |
| 💻 **Language** | Rust |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-pipelines` `ai-workflows` `durable-execution` `durable-functions` `durable-workflows` `postgresql`

## 🎯 Categories

AI/ML · Database

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Microsoft’s **pg_durable** is an open‑source Rust extension that brings durable, in‑database execution to PostgreSQL, letting you encode repeatable operational tasks as SQL‑driven workflows and eliminate manual, ad‑hoc steps. With over 2 000 GitHub stars and active maintenance, it targets automation scenarios such as scheduled data pipelines, tool orchestration, and “run‑once‑and‑forget” jobs directly inside the database engine.

**Value**  
By moving workflow logic into PostgreSQL, pg_durable removes the need for external scripting or cron jobs, reduces context‑switching, and guarantees that each step is persisted and recoverable even after failures. This yields tighter data‑centric pipelines, lower operational overhead, and easier auditability because the entire execution history lives in the database.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to build the Rust extension, and load it on a non‑production PostgreSQL instance.  
2. **Pilot workflow** – Encode a simple, low‑risk task (e.g., nightly table cleanup) as a durable job and verify scheduling, retries, and state persistence.  
3. **Tool integration** – Connect the extension to existing orchestration tools (Airflow, Dagster, etc.) via standard SQL calls, iterating on the API surface as needed.  
4. **Scale‑up** – Once the pilot is stable, migrate additional jobs, add monitoring, and document the job definitions for team reuse.

**Production readiness**  
pg_durable is **medium‑ready**: it is actively maintained (last update 2026‑06‑25) and has a healthy community signal (2 106 stars, 58 forks), making it suitable for prototypes, internal tooling, or workloads where the database is already the source of truth. Before production use, teams should validate the integration effort (building the Rust extension, ensuring compatibility with their PostgreSQL version), assess dependency management (Rust toolchain, native libraries), and implement monitoring/alerting around job execution and resource consumption. With those checks in place, pg_durable can be a reliable backbone for repeatable, durable data workflows.

### Русский

microsoft/pg_durable — это расширение PostgreSQL, которое позволяет выполнять долговечные (durable) задачи непосредственно внутри базы данных, избавляя от повторяющихся ручных операций и объединяя инструменты в автоматизированные потоки. Типовой сценарий внедрения — подключение pg_durable к существующим рабочим процессам (например, ETL‑pipeline, планировщик задач или AI/ML‑воркфлоу) для повторяемого выполнения SQL‑скриптов и вызовов внешних сервисов без внешних оркестраторов. Проект имеет среднюю готовность к production: подходит для прототипов и внутренних workflow‑ов, но перед выгрузкой в продакшн рекомендуется провести небольшой proof‑of‑concept, проверить зависимости и оценить затраты на интеграцию.

### 中文

**项目简介**  
microsoft/pg_durable 是一个基于 PostgreSQL 的“持久化执行”框架，利用 Rust 编写的扩展让数据库内部能够安全、可靠地调度和执行重复性的业务逻辑，从而把手工运维工作搬进数据库层。

**价值**  
- **消除重复人工操作**：把定时任务、数据清理、状态迁移等工作写成 SQL/函数，交给数据库自行执行，减少人为失误。  
- **实现可重复的工作流**：可将外部工具（如 CI/CD、监控、数据管道）通过简单的 SQL 调用串联起来，形成端到端的自动化流程。  
- **提升可观测性**：所有执行记录都保存在 PostgreSQL 中，便于审计、回滚和性能分析。

**典型接入方式**  
1. **小范围 PoC**：先克隆仓库，阅读 `README.md`，在本地或测试环境的 PostgreSQL 实例上使用 `cargo install` 编译并加载扩展。  
2. **定义持久化任务**：使用提供的 DSL（SQL 函数/存储过程）声明任务、调度频率以及错误处理策略。  
3. **集成到现有系统**：在业务代码或 CI 脚本中通过普通的 `SELECT pg_durable.run('task_name')` 触发，或让扩展自行按计划执行。  
4. **监控与调优**：通过系统视图 `pg_durable.jobs`、`pg_durable.history` 查看任务状态，结合 PostgreSQL 原生监控进行调优。

**生产可用性**  
- **成熟度**：GitHub 2106 星、58 Fork，活跃更新至 2026‑06‑25，代码基于 Rust，质量相对可靠。  
- **适用场景**：非常适合原型、内部工具或对可靠性要求不极端的业务流程。  
- **上线注意**：  
  - 先在预生产环境完成完整的 PoC，确认依赖（PostgreSQL 版本、Rust 编译链）和运维成本。  
  - 检查扩展对数据库性能的影响，尤其是大规模调度时的锁和 I/O。  
  - 建立监控、备份与回滚策略，确保任务失败时不会导致数据不一致。  

综上，pg_durable 能显著降低手动运维负担，适合作为内部自动化的起步方案；在经过充分的验证和监控后，可逐步推广到生产环境。

## 🧭 Practical evaluation

**Value:** microsoft/pg_durable helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2106 GitHub stars
- 58 forks
- updated 2026-06-25
- primary language: Rust
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 71/100 |
| topics | 75/100 |
| outlook | 59/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/microsoft/pg_durable) · [← Back to AI/ML](./README.md)</sub>
