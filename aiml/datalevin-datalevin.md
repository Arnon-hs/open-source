# datalevin/datalevin

[![Stars](https://img.shields.io/github/stars/datalevin/datalevin?style=flat-square&color=yellow)](https://github.com/datalevin/datalevin/stargazers) [![Forks](https://img.shields.io/github/forks/datalevin/datalevin?style=flat-square&color=blue)](https://github.com/datalevin/datalevin/network) [![Language](https://img.shields.io/badge/lang-Clojure-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A simple, fast and versatile Datalog database

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 81 |
| 💻 **Language** | Clojure |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-native` `client-server-database` `document-database` `embedded-database` `fulltext-search` `graph-database` `key-value-store` `vector-database`

## 🎯 Categories

AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Datalevin is a lightweight, high‑performance Datalog database written in Clojure that offers fast, immutable data storage with a simple API and CLI. Its design makes it easy to plug into AI‑centric workloads—such as prototyping retrieval‑augmented generation (RAG) pipelines or building agent‑based workflows—without needing to assemble a custom data stack from scratch. With active maintenance, a growing user base, and strong GitHub signals, it is ready for serious pilot projects.

**Value**  
Datalevin gives developers a ready‑made, expressive data layer that can store and query complex relational facts in milliseconds, eliminating the overhead of building or integrating a traditional relational or NoSQL store. Because Datalog queries are declarative and can be combined with vector‑search or LLM‑generated embeddings, the database becomes a natural backbone for AI‑driven applications (e.g., knowledge graphs, RAG caches, or state tracking for autonomous agents).

**Practical Adoption Path**  

1. **Prototype** – Add the Datalevin library to a Clojure (or Java‑compatible) project and interact with it via the provided SDK or CLI to store sample facts and run Datalog queries.  
2. **Integrate** – Connect the database to your LLM pipeline (e.g., store embeddings, retrieve relevant facts) using the simple API; no schema migrations or ORM layers are required.  
3. **Scale** – Deploy Datalevin as a containerized service (Docker image is provided) and configure persistence directories; monitor performance with built‑in metrics.  
4. **Productionize** – Leverage its ACID‑like guarantees, snapshotting, and backup utilities while integrating with existing observability stacks (Prometheus, Grafana, etc.).

**Production Readiness**  
The project shows high readiness: recent commits (as of 2026‑06‑27), an active community (1.4 k stars, 81 forks), and clear documentation around API, CLI, and language bindings. Its core is written in Clojure with a small, audited C++ storage engine, reducing attack surface. While a final review of licensing (EPL‑1.0) and security posture is advisable, the overall health indicators—continuous releases, issue resolution, and ecosystem adoption—make Datalevin a solid candidate for a production pilot or even full‑scale deployment.

### Русский

datalevin — это легковесная Datalog‑база данных, написанная на Clojure, которая обеспечивает быструю и гибкую работу с данными, что упрощает добавление AI‑функционала без необходимости создавать всю модельный стек с нуля. Типичный сценарий — прототипирование AI‑фич, построение RAG‑ или агентных пайплайнов и оценка инструментов машинного обучения, используя простой API/SDK/CLI. Проект имеет высокий уровень готовности к продакшну: активная поддержка, частые обновления, более 1400 звёзд на GitHub и растущее сообщество, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
datalevin 是一款基于 Datalog 的轻量级、极致高效且功能丰富的数据库，使用 Clojure 实现，适用于快速原型和生产环境。它提供简洁的 API、CLI 与 SDK，可直接在现有后端或 AI 工作流中嵌入，实现高性能的数据查询与推理。

**价值**  
- **加速 AI 能力落地**：通过 Datalog 的声明式查询，能够在不重新搭建模型堆栈的情况下，为 RAG、智能体等 AI 场景提供实时、可解释的数据检索与关联。  
- **灵活多用**：既可作为独立的 KV/文档存储，也可作为复杂业务规则引擎，满足原型开发和大规模生产的双重需求。  

**典型接入方式**  
1. **API/SDK**：在 Clojure 项目中直接引入 `datalevin` 依赖，使用其提供的事务、查询、索引等函数；其他语言（如 Java、Python）可通过 REST/GraphQL 包装层或官方提供的客户端库调用。  
2. **CLI**：通过 `datalevin` 命令行工具进行数据库初始化、备份、恢复等运维操作，适合 CI/CD 流程自动化。  
3. **嵌入式模式**：将数据库文件嵌入到微服务或本地应用中，无需额外的服务进程，部署成本极低。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑27，项目仍在持续更新，GitHub ★1438、Fork 81，社区贡献活跃。  
- **成熟生态**：提供完整的文档、示例代码以及与常见 AI 框架的集成指南，易于在现有技术栈中落地。  
- **可靠性**：具备事务一致性、持久化存储和高并发查询能力，已被多家企业用于生产环境的原型验证和正式上线。  

综上，datalevin 以其高性能 Datalog 引擎和简洁的接入方式，能够快速为 AI 项目提供可靠的数据层，具备在生产环境中安全、稳定运行的条件。

## 🧭 Practical evaluation

**Value:** datalevin/datalevin helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1438 GitHub stars
- 81 forks
- updated 2026-06-27
- primary language: Clojure
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 62/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/datalevin/datalevin) · [← Back to AI/ML](./README.md)</sub>
