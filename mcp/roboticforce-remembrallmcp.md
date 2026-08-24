# roboticforce/remembrallmcp

[![Stars](https://img.shields.io/github/stars/roboticforce/remembrallmcp?style=flat-square&color=yellow)](https://github.com/roboticforce/remembrallmcp/stargazers) [![Forks](https://img.shields.io/github/forks/roboticforce/remembrallmcp?style=flat-square&color=blue)](https://github.com/roboticforce/remembrallmcp/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Whole-codebase knowledge for AI coding agents. A field-aware code graph (functions, classes, methods, fields, references) plus persistent memory. Rust, Postgres + pgvector, MCP.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 26 |
| 🍴 **Forks** | — |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `blast-radius` `claude-code` `code-analysis` `code-graph` `code-intelligence` `cursor` `dependency-graph` `developer-tools` `field-references` `knowledge-graph` `mcp`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
Roboticforce’s **remembrallmcp** is an open‑source knowledge‑graph engine that captures a whole‑codebase as a field‑aware graph (functions, classes, methods, fields, and references) and stores it in a persistent vector store (Postgres + pgvector). It exposes the Model Context Protocol (MCP) via a Rust‑based server, enabling AI coding agents to query and reason over code with context‑aware precision.

**Value**  
- **Rich, structured code knowledge**: By turning source code into a searchable graph, AI assistants can retrieve exact symbols, dependencies, and usage patterns, dramatically improving code‑completion, bug‑fixing, and refactoring suggestions.  
- **Standardized integration**: MCP provides a language‑agnostic, HTTP/JSON‑compatible contract, letting any MCP‑compliant model or tool plug into the service without custom adapters.  
- **Scalable persistence**: Leveraging Postgres + pgvector gives you both relational durability (for metadata, versioning, access control) and fast vector similarity search for semantic queries.

**Practical Adoption Path**  
1. **Spin up the server** – clone the repo, run the provided Docker compose (or build the Rust binary) which brings up PostgreSQL with the pgvector extension and the MCP server.  
2. **Ingest a codebase** – use the CLI/SDK to point the tool at a repository; it parses the code, builds the field‑aware graph, and stores embeddings in pgvector.  
3. **Connect your AI agent** – configure the agent’s MCP client (e.g., LangChain, LlamaIndex, or a custom model) to point at the server’s endpoint; queries such as “list all callers of `User::login`” or “find similar implementations of `hash_password`” are now available.  
4. **Iterate & extend** – add custom metadata (e.g., code ownership, security tags) via the API, and optionally expose a CLI for developers to run ad‑hoc queries during CI/CD pipelines.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑07‑03), has 26 stars, and provides a clear API/CLI, making it suitable for prototypes, internal tooling, or staged roll‑outs.  
- **Dependencies**: Relies on Rust (stable), PostgreSQL, and the pgvector extension—well‑known components with mature ecosystems.  
- **Risks**: Licensing and security posture need a final review; the codebase is relatively small, so extensive load‑testing and monitoring should be added before high‑traffic production use.  
- **Recommendation**: Start with a sandbox environment to validate integration and performance, then harden the deployment (TLS, auth, audit logs) and run a controlled pilot before full production rollout.

### Русский

**roboticforce/remembrallmcp** — открытый проект, который предоставляет AI‑агентам полную «картину кода»: граф функций, классов, методов, полей и их взаимных ссылок, а также персистентную память через PostgreSQL + pgvector. Типичный сценарий — развертывание сервера Model Context Protocol (MCP) и подключение к нему код‑генерирующих или автодополняющих AI‑ассистентов, что упрощает интеграцию моделей с реальными инструментами и данными. Готовность к продакшну — средняя: проект уже стабилен для прототипов и внутренних воркфлоу, но перед запуском в продакшн стоит проверить лицензирование, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
roboticforce/remembrallmcp 为 AI 编码助手提供了完整的代码库知识图谱——包括函数、类、方法、字段及其相互引用，并配合持久化记忆。基于 Rust 实现，使用 PostgreSQL + pgvector 存储向量化语义信息，遵循 Model Context Protocol（MCP）标准，实现 AI 与真实工具、数据的无缝对接。

**价值主张**  
- **统一协议**：通过 MCP 为 AI 代理提供统一的“代码知识+记忆”接口，降低不同工具之间的集成成本。  
- **高效检索**：利用向量化存储和字段感知的代码图，实现语义搜索与上下文补全，显著提升 AI 代码生成的准确性与可解释性。  
- **可扩展生态**：Rust 的高性能与 PostgreSQL 的成熟生态，使其易于在现有后端系统中嵌入，支持大规模企业级部署。

**典型接入方式**  
1. **API/SDK**：项目提供 HTTP API 与 Rust SDK，开发者可直接调用 `GET /graph`, `POST /memory` 等端点，或在 Rust 项目中引入 `remembrallmcp` crate。  
2. **CLI**：内置命令行工具支持本地调试、数据导入导出以及图谱查询，适合作为 CI/CD 流程的辅助步骤。  
3. **MCP Server**：部署为标准 MCP 服务器后，任何遵循 MCP 协议的 AI 代理（如 OpenAI、Claude、Gemini）即可通过统一协议获取代码上下文和记忆，实现“一键接入”。  

**生产可用性评估**  
- **成熟度**：当前得分 67/100，GitHub 26 星，最近一次提交为 2026‑07‑03，代码活跃度尚可。  
- **依赖与运维**：核心依赖为 Rust、PostgreSQL 与 pgvector，技术栈成熟，部署相对简单；但需要自行管理数据库备份、向量索引维护以及安全审计。  
- **适用场景**：非常适合作为原型、内部工具或研发团队的代码助手后端；在对可靠性、容灾和安全合规有更高要求的生产环境中，仍需完成许可证合规、漏洞扫描以及运维监控的额外审查。  

总体而言，remembrallmcp 为 AI 编码代理提供了“一站式”代码知识与记忆解决方案，接入门槛低，性能优秀，适合作为企业内部研发流程的加速器；在完成安全与运维检查后，可逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** roboticforce/remembrallmcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 26 GitHub stars
- updated 2026-07-03
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 22/100 |
| production | 51/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/roboticforce/remembrallmcp) · [← Back to Mcp](./README.md)</sub>
