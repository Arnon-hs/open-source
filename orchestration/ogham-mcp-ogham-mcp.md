# ogham-mcp/ogham-mcp

[![Stars](https://img.shields.io/github/stars/ogham-mcp/ogham-mcp?style=flat-square&color=yellow)](https://github.com/ogham-mcp/ogham-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/ogham-mcp/ogham-mcp?style=flat-square&color=blue)](https://github.com/ogham-mcp/ogham-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Shared memory MCP server — persistent, searchable, cross-client Claude, Opencode

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 110 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Python |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `ai-memory` `claude` `codex` `llm` `llm-tools` `mcp` `memory` `model-context-protocol` `opencode` `persistent-memory` `pgvector`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Database

## 📝 Summary

### English

**Project Summary**

Ogham-MCP is an open-source, shared memory server that enables the creation of repeatable agent workflows by connecting isolated prompts and tools. This project facilitates the coordination of multi-agent workflows, standardizes agent memory, and allows for the addition of tool-use pipelines. With its high production readiness and strong ecosystem signals, Ogham-MCP is suitable for serious pilots.

**Value Proposition**

The value of Ogham-MCP lies in its ability to turn isolated prompts and tools into repeatable agent workflows, making it easier to manage complex tasks and workflows. By providing a shared memory server, Ogham-MCP enables the connection of disparate tools and agents, allowing for more efficient and standardized workflows.

**Practical Adoption Path**

To adopt Ogham-MCP, users can start by evaluating its API, SDK, and CLI implementation signals. They can then explore its language metadata and focused topics to determine its suitability for their specific use cases. With its high production readiness, users can confidently pilot Ogham-MCP in their environments and integrate it with their existing tools and workflows.

**Production Readiness**

Ogham-MCP has demonstrated high production readiness, with recent activity, adoption, and ecosystem signals indicating a strong and stable project. Its recent update (202

### Русский

**ogham-mcp** — это open‑source сервер совместного доступа к памяти (MCP), позволяющий сохранять, индексировать и искать контекстные данные между разными клиентами Claude/Opencode. Он упрощает построение повторяемых агентных пайплайнов: координатор может хранить результаты работы одного агента и передавать их другим, добавлять цепочки инструментов и стандартизировать общую память для RAG‑сценариев. Проект готов к production‑использованию: активные коммиты, 110 звёзд, 21 форк, поддержка API/SDK/CLI на Python и хорошая экосистема, требующая лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
ogham‑mcp 是一个基于共享内存的 Multi‑Client Protocol（MCP）服务器，提供持久化、可搜索的跨客户端记忆层。它能够把零散的 Prompt 与工具包装成可重复、可编排的智能体工作流，帮助开发者快速构建多代理协作、工具调用流水线以及统一的记忆管理。

**价值点**  
- **工作流复用**：将一次性 Prompt 转化为可重复调用的 Agent 流程，降低重复开发成本。  
- **跨客户端记忆**：持久化、全文搜索的共享记忆，使不同 Agent 能够在同一上下文中协同工作。  
- **易于编排**：提供统一的 API/SDK/CLI 接口，方便在 Orchestration 平台（如 Airflow、Prefect）或自研调度系统中嵌入。  

**典型接入方式**  
1. **API 调用**：通过 HTTP/REST 或 gRPC 接口提交 Prompt、查询记忆或触发工具链。  
2. **Python SDK**：`pip install ogham-mcp` 后使用 `ogham_mcp.Client` 直接在代码中创建、查询、更新记忆。  
3. **CLI**：`ogham-mcp run --config config.yaml` 可在本地或容器中启动服务，适合快速验证。  
4. **语言元数据**：项目自带的 OpenAPI/Swagger 文档以及 Python 类型提示，便于自动生成客户端代码。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑03 最近一次提交，星标 110、Fork 21，代码基于 Python，社区活跃。  
- **成熟度**：提供完整的 API、SDK 与 CLI，具备持久化存储（可选 SQLite、PostgreSQL）和全文检索，已在多个内部项目中验证。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式投产前完成一次安全审计并确认维护者的长期可用性。  

综合来看，ogham‑mcp 已具备在生产环境中进行试点的条件，适合作为多 Agent 协作与工具链编排的记忆与调度底层。

## 🧭 Practical evaluation

**Value:** ogham-mcp/ogham-mcp helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 110 GitHub stars
- 21 forks
- updated 2026-07-03
- primary language: Python
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 41/100 |
| production | 59/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/ogham-mcp/ogham-mcp) · [← Back to Orchestration](./README.md)</sub>
