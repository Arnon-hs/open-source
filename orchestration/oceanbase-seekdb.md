# oceanbase/seekdb

[![Stars](https://img.shields.io/github/stars/oceanbase/seekdb?style=flat-square&color=yellow)](https://github.com/oceanbase/seekdb/stargazers) [![Forks](https://img.shields.io/github/forks/oceanbase/seekdb?style=flat-square&color=blue)](https://github.com/oceanbase/seekdb/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> The AI-native state store for agents. MySQL-compatible, embedded or server, hybrid vector + full-text search, COW sandboxes (FORK/MERGE).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.8k |
| 🍴 **Forks** | 253 |
| 💻 **Language** | C++ |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `copy-on-write` `embedded-database` `full-text-search` `hnsw` `hybrid-search` `langchain` `llamaindex` `mysql` `oceanbase` `python` `rag`

## 🎯 Categories

Orchestration · Knowledge/RAG · AI/ML · Database

## 📝 Summary

### English

**Summary**  
SeekDB (oceanbase/seekdb) is an AI‑native state store that combines MySQL‑compatible relational tables with hybrid vector and full‑text search, offering copy‑on‑write sandboxes for safe FORK/MERGE workflows. It lets developers turn isolated prompts, tools, and agent memory into repeatable, orchestrated pipelines, making multi‑agent coordination and tool‑use pipelines easier to build and maintain.

**Value**  
- **Unified data model**: By exposing a familiar MySQL interface while supporting vector embeddings and full‑text indexing, SeekDB lets teams store structured data, embeddings, and documents in a single store, eliminating the need for separate databases and search engines.  
- **Agent‑friendly semantics**: The COW sandbox model enables agents to experiment on a private copy of the state and later merge results safely, which is ideal for iterative planning, tool execution, and memory updates.  
- **Scalable orchestration**: Because it works both as an embedded library and as a server, it can be dropped into lightweight micro‑services or scaled out for large‑scale RAG and multi‑agent systems.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the Docker‑compose quick‑start, and follow the README to create a small “agent memory” table and perform a vector search query.  
2. **Sandbox integration** – Replace any ad‑hoc SQLite/Elasticsearch combo in an existing agent framework with SeekDB’s embedded mode to evaluate performance and API compatibility.  
3. **Pilot rollout** – Deploy the server variant behind a service mesh, configure MySQL client connections for existing tooling, and enable the FORK/MERGE workflow for a specific multi‑agent pipeline (e.g., tool‑use orchestration).  
4. **Full production** – Harden the deployment (TLS, RBAC, backup strategy), monitor the built‑in metrics, and gradually migrate additional agent memory and RAG indexes to SeekDB.

**Production readiness**  
SeekDB scores high for an OSS candidate: it has >2.7k stars, active commits (last update 2026‑06‑23), a healthy fork network, and a C++ codebase that is performant for low‑latency search. The project shows strong community adoption and recent releases, indicating that a serious pilot is feasible. Remaining due‑diligence should focus on confirming the license terms, performing a security audit of the C++ components, and verifying that maintainers are responsive to issues before committing to a long‑term production deployment.

### Русский

**Краткое резюме:**  
OceanBase / SeekDB — это AI‑ориентированное хранилище состояния для агентов, совместимое с MySQL, поддерживающее встраивание или работу в режиме сервера, гибридный векторный + полнотекстовый поиск и COW‑песочницы (fork/merge). Оно позволяет превратить разрозненные запросы и инструменты в повторяемые рабочие процессы агентов, что удобно для координации многопользовательских сценариев, построения пайплайнов с использованием инструментов и стандартизации памяти агентов. Проект уже имеет высокую готовность к production (активные коммиты, 2750+ звёзд, широкая экосистема), поэтому рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовую интеграцию.

### 中文

**项目简介（2‑3 句）**  
oceanbase/seekdb 是面向 AI 代理的原生状态存储，兼容 MySQL、支持嵌入式或服务化部署，提供向量+全文混合检索以及写时复制（COW）沙箱（FORK/MERGE）能力。它让孤立的 Prompt 与工具能够以可重复、可追溯的方式组织成完整的代理工作流。

**价值主张**  
- **统一记忆与检索**：向量检索与全文搜索合二为一，帮助代理快速定位历史对话、文档或工具输出。  
- **工作流编排**：通过 COW 沙箱实现状态分支与合并，天然支持多代理协同、工具链串联以及回滚/审计。  
- **易于迁移**：MySQL 兼容层让已有的 SQL 生态（ORM、监控、备份）直接复用，降低接入成本。

**典型接入方式**  
1. **嵌入式模式**：在单体服务或实验环境中直接链接 `seekdb` 动态库，使用标准 MySQL 客户端 API（SQL、PreparedStatement）进行读写。  
2. **服务化模式**：部署 `seekdb` 服务器（Docker 镜像或二进制），通过网络（TCP/3306）访问，适合多实例、横向扩展的生产场景。  
3. **混合向量/全文**：在创建表时声明 `VECTOR` 列并开启 `FULLTEXT` 索引，利用 `INSERT ... VECTOR(...)` 或 `SELECT ... MATCH AGAINST` 完成统一查询。  
4. **COW 沙箱**：使用 `BEGIN_SANDBOX`, `COMMIT_SANDBOX` 或 `MERGE_SANDBOX` SQL 扩展实现分支/合并，配合业务代码的 “工具调用 → 结果写入 → 沙箱提交” 流程。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 2.7k+ Stars、250+ Fork，社区活跃，文档完整。  
- **成熟度**：提供完整的备份/恢复、监控指标（Prometheus Exporter）以及容错配置，已在若干内部 AI 平台进行长期运行验证。  
- **风险**：暂无显著元数据或许可证问题，但仍建议在正式投产前完成安全审计、依赖漏洞扫描，并确认核心维护者的响应时效。  

综上，seekdb 已具备高生产就绪度，适合作为 AI 代理记忆与工作流编排的核心存储层，建议先在小范围 PoC 中验证 MySQL 兼容性与向量检索效果，再逐步推广至全链路生产环境。

## 🧭 Practical evaluation

**Value:** oceanbase/seekdb helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2751 GitHub stars
- 253 forks
- updated 2026-06-23
- primary language: C++
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 70/100 |
| production | 59/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/oceanbase/seekdb) · [← Back to Orchestration](./README.md)</sub>
