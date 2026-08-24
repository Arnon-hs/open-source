# dbos-inc/dbos-transact-py

[![Stars](https://img.shields.io/github/stars/dbos-inc/dbos-transact-py?style=flat-square&color=yellow)](https://github.com/dbos-inc/dbos-transact-py/stargazers) [![Forks](https://img.shields.io/github/forks/dbos-inc/dbos-transact-py?style=flat-square&color=blue)](https://github.com/dbos-inc/dbos-transact-py/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Database-Backed Durable Python Workflows

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 73 |
| 💻 **Language** | Python |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-workflow` `cronjob-scheduler` `dbos` `durable-execution` `microservice-orchestration` `microservices-orchestration` `orchestration` `postgresql` `python` `sqlite` `workflow-engine` `workflows`

## 🎯 Categories

Orchestration · Automation · Backend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
dbos‑inc/dbos‑transact‑py is an open‑source Python library that lets you define durable, database‑backed workflows for coordinating multiple AI agents, tools, and memory stores. By turning isolated prompts and utilities into repeatable, transactional pipelines, it simplifies the construction of robust multi‑agent applications. The project is actively maintained, widely starred, and ready for pilot‑level integration.

**Value**  
- **Durable, transactional orchestration** – Workflows are persisted in a database, guaranteeing exactly‑once execution and easy rollback, which is essential for reliable agent pipelines.  
- **Unified agent memory** – Provides a standard way to store and retrieve context across calls, reducing ad‑hoc state‑management code.  
- **Tool‑use pipelines** – Enables seamless chaining of external tools (e.g., search, APIs) within a single, version‑controlled workflow.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided examples, and verify that a simple two‑step agent workflow executes end‑to‑end.  
2. **Readme & API Review** – Confirm that the documented API (workflow definition, transaction handling, and DB setup) matches your internal standards.  
3. **Pilot Integration** – Replace an existing ad‑hoc orchestration script with a dbos‑transact‑py workflow, using a lightweight SQLite or PostgreSQL instance for storage.  
4. **Scale & Harden** – Move to a production‑grade database, add monitoring/logging, and integrate with your CI/CD pipeline.

**Production Readiness**  
- **Activity & Adoption** – 1,431 stars, 73 forks, recent commits (last updated 2026‑06‑23) and growing community indicate strong momentum.  
- **Maturity** – The library already implements core transactional semantics and includes extensive documentation and examples, making it suitable for a serious pilot.  
- **Risks** – No major metadata concerns, but a final review of the license, security posture, and maintainer responsiveness is advisable before full production rollout.  

Overall, dbos‑inc/dbos‑transact‑py offers a high‑value, production‑ready foundation for building reliable, database‑backed agent workflows, with a low‑friction path from proof‑of‑concept to deployment.

### Русский

**Краткое резюме:**  
`dbos-inc/dbos-transact-py` — это open‑source библиотека для создания надёжных, повторяемых пайплайнов из изолированных запросов и инструментов, позволяющая организовать оркестрацию многопользовательских (мульти‑агентных) рабочих процессов, добавить цепочки использования инструментов и стандартизировать «память» агентов. Типичный путь внедрения — запуск небольшого proof‑of‑concept, следуя README, и постепенная интеграция в существующие backend‑или AI‑сервисы. По оценке готовности к production проект находится на высоком уровне: активные коммиты, 1431 звёзд, широкое принятие и сильные сигналы экосистемы позволяют использовать его в серьёзных пилотных проектах (последнее обновление — 23 июня 2026 г.).

### 中文

**项目简介（2‑3 句）**  
`dbos-inc/dbos-transact-py` 是一个基于数据库的持久化工作流框架，能够把离散的 LLM 提示、工具调用以及多智能体交互封装成可重复、可回滚的 Python 流程。它通过事务式存储保证状态一致性，使得复杂的多代理协作可以像普通函数调用一样安全、可追踪。

**价值主张**  
- **可靠性**：借助数据库事务，工作流在异常或中断后能够自动恢复或回滚，避免“记忆丢失”。  
- **可复用性**：将单个提示或工具包装成标准化的任务节点，便于在不同项目间共享和组合。  
- **可观测性**：所有步骤及其输入输出都持久化在 DB 中，天然支持审计、调试和性能分析。

**典型接入方式**  
1. **快速验证**：克隆仓库 → 按 README 创建本地 SQLite（或 PostgreSQL）实例 → 运行 `example/` 中的示例脚本，确认工作流可以正常提交与回滚。  
2. **代码集成**：在现有 Python 项目中 `pip install dbos-transact`，然后用 `@dbos.transaction` 装饰器包装业务函数，按需调用 `dbos.run_workflow(...)`。  
3. **生产化**：将数据库迁移到企业级 PostgreSQL/MySQL，使用 Docker/K8s 部署 `dbos-server`，并通过环境变量或 Helm Chart 配置连接信息、日志级别和安全凭证。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目仍在持续更新，最近一次提交在当天；GitHub 计 1,431 星、73 Fork，社区活跃。  
- **成熟度**：提供完整的事务模型、错误恢复机制和示例文档，已在多个内部项目中用于多智能体编排，具备进入生产环境的技术基线。  
- **风险**：目前未发现重大元数据或许可证冲突，仍需对依赖库的安全审计以及维护者的长期可用性进行二次确认。  

综上，`dbos-transact-py` 具备高可靠性和可观测性，适合作为多代理、工具链和记忆管理的底层编排引擎，建议先在小范围 PoC 中验证，再逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** dbos-inc/dbos-transact-py helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1431 GitHub stars
- 73 forks
- updated 2026-06-23
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 58/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/dbos-inc/dbos-transact-py) · [← Back to Orchestration](./README.md)</sub>
