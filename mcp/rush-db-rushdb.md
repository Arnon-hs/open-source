# rush-db/rushdb

[![Stars](https://img.shields.io/github/stars/rush-db/rushdb?style=flat-square&color=yellow)](https://github.com/rush-db/rushdb/stargazers) [![Forks](https://img.shields.io/github/forks/rush-db/rushdb?style=flat-square&color=blue)](https://github.com/rush-db/rushdb/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> RushDB is a graph + vector database and memory layer for AI agents. Push any JSON, get typed, searchable, relationship-aware records back — no schema, no migrations. Built on Neo4j.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 229 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `ai-memory` `ai-tools` `app-backend` `cloud` `database` `docker` `embeddings` `graph-database` `graphs` `instant-apps`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Summary**  
RushDB is an open‑source graph‑plus‑vector database built on Neo4j that lets AI agents store arbitrary JSON and retrieve typed, searchable, relationship‑aware records without needing a predefined schema or migrations. It provides a standard protocol for connecting AI assistants to tools and data, making it easy to expose Model Context Protocol (MCP) services or build custom integrations. With active maintenance, a growing community, and a TypeScript SDK/CLI, it is ready for serious pilot projects.

**Value**  
- **Schema‑free, relationship‑aware storage**: Developers can push any JSON payload and later query it with rich graph semantics and vector similarity, eliminating the overhead of schema design and migration cycles.  
- **Unified protocol for AI tooling**: By exposing a consistent API/SDK, RushDB becomes a common “data glue” that lets diverse AI agents (RAG pipelines, autonomous assistants, tool‑calling bots) interact with real‑world data and external services through a single interface.  
- **Built on Neo4j**: Leverages Neo4j’s mature graph engine for reliability, scalability, and ACID guarantees while adding vector search capabilities needed for modern LLM‑driven workflows.

**Practical adoption path**  
1. **Prototype** – Install the TypeScript SDK or use the provided CLI to spin up a local RushDB instance, push sample JSON documents, and test graph + vector queries.  
2. **Integrate** – Replace ad‑hoc data stores in your AI agent’s tool‑calling layer with RushDB calls (e.g., `push`, `search`, `traverse`). The SDK abstracts the underlying Neo4j details, so integration is a few lines of code.  
3. **Deploy** – Deploy RushDB in a containerized environment (Docker/K8s) using the official Helm chart or Docker image; configure authentication and TLS as per your security policies.  
4. **Scale** – Leverage Neo4j’s clustering features for high‑availability and horizontal scaling as query volume grows; the vector index can be tuned independently for performance.  

**Production readiness**  
- **Activity & community**: 229 stars, recent commits (as of 2026‑06‑23), 20+ topics, and active issue response indicate a healthy open‑source project.  
- **Maturity**: The combination of Neo4j’s proven graph engine and a TypeScript front‑end gives strong reliability and type safety.  
- **Ecosystem fit**: Clear API/SDK/CLI surface, support for MCP, and straightforward Docker/Helm deployment make it easy to evaluate and roll out in pilot environments.  
- **Risks**: Final due diligence is needed on licensing (check the exact OSS license), security posture (review CVEs for Neo4j and the RushDB codebase), and maintainership continuity, but no major red flags have been identified.  

Overall, RushDB is a production‑ready OSS candidate for teams looking to give AI agents a unified, schema‑free graph‑vector store and a standard integration point for real‑world tools and data.

### Русский

RushDB — это графово‑векторная база данных и слой памяти для AI‑агентов, позволяющий без схемы и миграций сохранять любые JSON‑объекты и получать типизированные, поисковые и взаимосвязанные записи; построена на Neo4j и доступна через API/SDK/CLI. Типичный сценарий — подключение AI‑ассистентов к реальным инструментам и данным через единый протокол (Model Context Protocol), что упрощает интеграцию и стандартизацию сервисов. Проект имеет высокий уровень готовности к продакшн: активные коммиты, 229★ на GitHub, поддержка TypeScript, обширные метаданные и сильные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё же требуется.

### 中文

**项目简介**  
RushDB（`rush-db/rushdb`）是基于 Neo4j 构建的图+向量数据库与内存层，专为 AI 代理设计。它可以直接存储任意 JSON，返回带类型、可搜索、关联感知的记录，无需预定义 schema 或执行迁移。

**价值主张**  
- **统一协议**：提供标准化的 API/SDK/CLI，使 AI 助手能够像调用本地工具一样轻松访问真实数据和服务。  
- **即插即用**：无需数据库迁移或模式管理，开发者只需推送 JSON，即可获得结构化、可检索的图谱和向量检索能力。  
- **加速 RAG 与工具调用**：在模型上下文协议（Model Context Protocol）服务器、工具集成以及知识库构建等场景中，快速实现“模型‑数据‑工具”闭环。

**典型接入方式**  
1. **API 调用**：通过 REST/GraphQL 接口推送 JSON，获取带有类型和关系的响应。  
2. **SDK**：使用官方 TypeScript SDK（亦可在其他语言中通过 OpenAPI 生成客户端）进行 CRUD、向量搜索和图遍历。  
3. **CLI**：在 CI/CD 或本地调试时，直接使用 `rushdb` 命令行工具执行数据导入、查询和迁移检查。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目仍在维护，最近一次提交在同日；GitHub 统计 229 ★、20 Fork，拥有 20+ 主题标签，表明社区关注度和生态兼容性良好。  
- **技术成熟度**：基于业界成熟的 Neo4j 图数据库，结合向量索引，具备高可用、可水平扩展的特性。  
- **风险评估**：暂无重大元数据风险；仍需对许可证（MIT）和安全审计进行最终确认，但整体成熟度足以支持正式的生产试点。  

综上，RushDB 为 AI 代理提供了“一站式”图‑向量存储与检索能力，接入简便，且已具备在生产环境中进行可靠试验的条件。

## 🧭 Practical evaluation

**Value:** rush-db/rushdb helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 229 GitHub stars
- 20 forks
- updated 2026-06-23
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 59/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/rush-db/rushdb) · [← Back to Mcp](./README.md)</sub>
