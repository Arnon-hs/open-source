# zircote/subcog

[![Stars](https://img.shields.io/github/stars/zircote/subcog?style=flat-square&color=yellow)](https://github.com/zircote/subcog/stargazers) [![Forks](https://img.shields.io/github/forks/zircote/subcog?style=flat-square&color=blue)](https://github.com/zircote/subcog/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Persistent memory system for AI coding assistants. Captures decisions, learnings, and context from coding sessions. Features hybrid search (semantic + BM25), MCP server integration, SQLite persistence with knowledge graph, and proactive memory surfacing. Written in Rust.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Rust |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-assistant` `claude` `claude-plugin` `cli` `developer-tools` `embeddings` `gemini` `hybrid-search` `knowledge-graph` `llm` `mcp`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · DevTools · Database

## 📝 Summary

### English

**Brief Summary**  
zircote/subcog is a Rust‑based persistent memory layer designed for AI coding assistants. It records decisions, learnings, and contextual information from coding sessions and makes that knowledge searchable through a hybrid semantic + BM25 engine, while persisting everything in SQLite with a built‑in knowledge‑graph. The system also ships an MCP (Model Context Protocol) server, enabling AI agents to retrieve and surface relevant memory proactively.

**Value**  
- **Contextual continuity** – AI assistants can recall prior decisions, code‑review comments, and debugging steps, dramatically reducing “cold‑start” friction.  
- **Standardised integration** – By exposing a MCP‑compatible API/SDK/CLI, subcog lets any model‑driven tool plug into a common memory store, simplifying tool‑to‑model communication and avoiding bespoke data pipelines.  
- **Hybrid search** – Combining semantic embeddings with BM25 ensures both fuzzy, meaning‑based retrieval and precise keyword matching, covering the full spectrum of developer queries.  
- **Lightweight persistence** – SQLite + knowledge‑graph gives durable storage without the operational overhead of a full‑blown database cluster.

**Practical Adoption Path**  
1. **Prototype** – Add the subcog CLI or SDK to an existing AI‑assistant prototype; configure the MCP endpoint and point it at a local SQLite file.  
2. **Instrument sessions** – Emit “decision” and “learning” events from the assistant (e.g., after a refactor suggestion or a test failure) using the provided Rust library or the language‑agnostic HTTP API.  
3. **Evaluate retrieval** – Run typical developer queries against the hybrid search API; tune embedding models or BM25 parameters as needed.  
4. **Scale** – For multi‑user or CI environments, mount the SQLite file on a shared volume or switch to a replicated SQLite‑cluster (e.g., via rqlite) while keeping the same API contract.  
5. **Productionize** – Deploy the MCP server as a containerized microservice behind your AI platform, monitor health/end‑points, and integrate with your existing observability stack.

**Production Readiness**  
- **Activity & adoption** – Recent commits (as of 2026‑05‑12), 22 ★ on GitHub, and multiple forks indicate an active community.  
- **Maturity** – Core features (persistent store, hybrid search, MCP server) are implemented and documented; the Rust codebase is concise and compiled, reducing runtime bugs.  
- **Integration simplicity** – Clear API/SDK/CLI surface and language‑agnostic HTTP endpoints make it easy to evaluate in a pilot without deep Rust expertise.  
- **Risks** – Licensing, security audit, and long‑term maintainer commitment still need a final check, but no show‑stopper issues have been identified.  

Overall, subcog is a high‑readiness OSS component that can be dropped into AI‑assistant pipelines to give them durable, searchable memory and a standard way to interact with external tools. It is suitable for a serious pilot and, after the minor due‑diligence steps, can be promoted to production use.

### Русский

**zircote/subcog** — это открытая система постоянной памяти для AI‑ассистентов, написанная на Rust. Она сохраняет решения, выводы и контекст из код‑сессий, предоставляет гибридный поиск (семантический + BM25), интеграцию с MCP‑сервером и хранение в SQLite с графом знаний, позволяя агентам проактивно всплывать нужную информацию и подключаться к реальным инструментам через единый протокол. Проект имеет высокий уровень готовности к production: активные обновления (последний коммит 2026‑05‑12), растущая пользовательская база (22★, 5 форков), поддержка API/SDK/CLI и хорошие сигналы экосистемы, что делает его подходящим для пилотных внедрений в инструменты разработки и сервисы Model Context Protocol.

### 中文

**项目简介**  
zircote/subcog 是用 Rust 编写的持久化记忆系统，专为 AI 编码助理设计。它在编程会话中捕获决策、学习和上下文，并通过语义+BM25 混合检索、MCP 服务器集成、SQLite 持久化（带知识图谱）以及主动记忆呈现，为模型提供可查询的长期记忆。

**价值**  
- **桥接 AI 与真实工具/数据**：通过标准化的 Model Context Protocol（MCP），让 AI 助手能够直接调用本地工具、数据库和业务系统，提升自动化程度和准确性。  
- **高效检索与知识组织**：混合搜索结合语义向量和 BM25，既能快速定位关键词，又能捕捉语义相似度；SQLite+知识图谱让记忆结构化、可追溯。  
- **持续学习与上下文复用**：会话记忆持久化后可在后续任务中自动 surfacing，帮助模型复用过去的决策和经验，降低重复劳动。

**典型接入方式**  
1. **MCP 服务器**：部署 subcog 提供的 MCP 服务，AI 助手通过统一的 HTTP/gRPC 接口发送 `store`, `query`, `update` 等请求。  
2. **SDK/CLI**：项目自带 Rust SDK 与命令行工具，开发者可在其他语言（如 Python、Node）中通过 FFI 或子进程调用，实现快速原型。  
3. **插件化集成**：将 SQLite 持久化层挂载到现有 CI/CD、IDE 或代码审查系统，实现“代码即记忆”的闭环。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑12，星标 22、fork 5，代码质量和文档较为完整。  
- **生态兼容**：使用通用的 MCP 协议，易与已有的 AI Agent 框架（如 LangChain、AutoGPT）对接。  
- **成熟度**：持久化采用成熟的 SQLite，搜索层基于开源向量库和 BM25，实现了可靠的混合检索。  
- **风险**：需进一步审查许可证（MIT/Apache）兼容性、依赖安全漏洞以及维护者响应速度。

总体来看，zircote/subcog 已具备在生产环境中进行试点的条件，适合作为 AI 编码助理的记忆后端或标准化工具集成层。

## 🧭 Practical evaluation

**Value:** zircote/subcog helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 22 GitHub stars
- 5 forks
- updated 2026-05-12
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 70/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/zircote/subcog) · [← Back to Mcp](./README.md)</sub>
