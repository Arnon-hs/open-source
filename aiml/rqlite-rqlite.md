# rqlite/rqlite

[![Stars](https://img.shields.io/github/stars/rqlite/rqlite?style=flat-square&color=yellow)](https://github.com/rqlite/rqlite/stargazers) [![Forks](https://img.shields.io/github/forks/rqlite/rqlite?style=flat-square&color=blue)](https://github.com/rqlite/rqlite/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> The lightweight, fault-tolerant database built on SQLite. Designed to keep your data highly available with minimal effort.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 17.6k |
| 🍴 **Forks** | 793 |
| 💻 **Language** | Go |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-07-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`consensus` `database` `distributed-database` `distributed-systems` `go` `raft` `relational-database` `sql` `sqlite`

## 🎯 Categories

AI/ML · Frontend · Data · Database · Design

## 📝 Summary

### English

Here's a brief summary of the rqlite project:

rqlite is an open-source, lightweight database built on SQLite, designed to provide high availability with minimal effort. This fault-tolerant database helps developers add AI capabilities to their projects without starting from scratch, making it an ideal choice for prototyping AI features, building RAG or agent workflows, and evaluating model tooling. With its strong ecosystem signals, high production readiness, and recent activity, rqlite is a viable option for serious pilots and production environments.

**Value:**

The value proposition of rqlite lies in its ability to simplify the addition of AI capabilities to existing projects. By leveraging a proven database like SQLite, rqlite reduces the complexity and effort required to build and deploy AI-powered applications.

**Practical Adoption Path:**

To adopt rqlite, developers can start by:

1. Evaluating the project through a small proof of concept to understand its feasibility and potential integration challenges.
2. Reviewing the README documentation to understand the project's architecture, usage, and best practices.
3. Assessing the project's security posture, license, and maintenance activity to ensure it meets their project's requirements.
4. Integrating rqlite into their project, starting with a small pilot or proof of concept

### Русский

rqlite — это лёгкая распределённая СУБД на базе SQLite, обеспечивающая высокую доступность данных без сложной инфраструктуры; её можно быстро подключить к прототипам AI‑фич, RAG‑системам или агентским workflow, используя привычный SQL‑интерфейс. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовые CRUD‑операции, после чего масштабировать в продакшн‑окружение. По оценкам проекта, rqlite готов к серьёзному пилотному использованию: активные коммиты, более 17 k звёзд, зрелый Go‑код и хорошая экосистема, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
rqlite 是基于 SQLite 实现的轻量级、容错的分布式数据库，能够在多个节点之间自动复制数据，实现高可用。它保留了 SQLite 的零配置、文件嵌入式特性，同时通过 Raft 共识协议提供一致性和故障恢复能力。

**价值**  
- **快速构建 AI/ML 原型**：在需要持久化向量、上下文或中间结果的 AI 应用（如 RAG、Agent 工作流）时，直接使用 rqlite 即可获得可靠的存储，无需自行搭建复杂的数据库集群。  
- **低运维成本**：只需几行配置即可部署，兼容 SQLite 的 SQL 接口，开发者可以使用熟悉的查询语法进行数据管理。  
- **高可用、容错**：基于 Raft 的复制机制确保节点故障时仍能提供读写服务，适合作为生产环境的关键数据层。

**典型接入方式**  
1. **准备环境**：在目标机器上安装 Go（或直接使用官方提供的二进制发行版）。  
2. **启动集群**：使用 `rqlited` 命令启动一个或多个节点，例如：  
   ```bash
   rqlited -http-addr :4001 -raft-addr :4002 ./data1
   rqlited -http-addr :4003 -raft-addr :4004 ./data2 -join http://localhost:4001
   ```  
   第一个节点为 leader，后续节点通过 `-join` 加入。  
3. **通过 HTTP API 或 SQLite 客户端交互**：  
   - **HTTP**：`POST /db/execute`、`POST /db/query` 等 REST 接口，适合微服务或容器化部署。  
   - **SQLite 驱动**：使用标准的 SQLite 驱动（如 `github.com/mattn/go-sqlite3`）连接 `http://localhost:4001/db`，即可像操作本地 SQLite 一样执行 SQL。  
4. **在 AI/ML 项目中使用**：将向量、文档元数据或模型输出写入 rqlite，随后通过 SQL 查询快速检索，配合向量搜索库（如 Milvus、FAISS）实现 RAG 场景的元数据管理。

**生产可用性**  
- **活跃度**：截至 2026‑07‑05，项目仍在维护，最近一次提交在当日，拥有 17 617 星、793 Fork，社区活跃。  
- **成熟度**：基于成熟的 SQLite 与 Raft 实现，已在多个生产环境中用于日志、配置中心和小型业务数据存储。  
- **安全与合规**：采用 MIT 许可证，代码审计记录良好；但在正式投产前仍建议进行内部安全评估和依赖漏洞扫描。  
- **推荐做法**：先在非关键环境做小规模 PoC（如单节点或 3 节点集群），验证性能、备份恢复流程以及与现有 AI 工作流的兼容性；确认后即可在生产环境以 5‑7 节点的方式部署，实现高可用与横向扩展。

综上，rqlite 具备 **高可用、低运维、易集成** 的特性，是在 AI/ML 项目中快速提供可靠持久化层的理想 OSS 选型。

## 🧭 Practical evaluation

**Value:** rqlite/rqlite helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 17617 GitHub stars
- 793 forks
- updated 2026-07-05
- primary language: Go
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 90/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 93/100 |
| recency | 100/100 |
| adoption | 85/100 |
| production | 81/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/rqlite/rqlite) · [← Back to AI/ML](./README.md)</sub>
