# pinkpixel-dev/mem0-mcp

[![Stars](https://img.shields.io/github/stars/pinkpixel-dev/mem0-mcp?style=flat-square&color=yellow)](https://github.com/pinkpixel-dev/mem0-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/pinkpixel-dev/mem0-mcp?style=flat-square&color=blue)](https://github.com/pinkpixel-dev/mem0-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> ✨ mem0 MCP Server: A memory system using mem0 for AI applications with model context protocl (MCP) integration. Enables long-term memory for AI agents as a drop-in MCP server.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 97 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `assistant` `database` `llm` `llm-memory` `mcp` `mcp-server` `mem0` `mem0ai` `memory` `memory-management` `model-context-protocol`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary**  
mem0‑MCP is an open‑source TypeScript server that implements the Model Context Protocol (MCP) on top of the mem0 memory engine, giving AI agents persistent, long‑term memory as a drop‑in service. It lets developers stitch together prompts, tools, and multi‑agent workflows into repeatable pipelines, turning ad‑hoc interactions into structured, stateful agents.  

**Value**  
By externalizing memory to a dedicated MCP server, developers can avoid re‑implementing storage logic in each model or agent, achieving consistent recall across sessions, better context management, and easier debugging. The server’s API/SDK/CLI surface makes it simple to plug into existing orchestration frameworks, enabling coordinated multi‑agent pipelines, tool‑use chains, and standardized memory handling without locking into a specific LLM provider.  

**Practical Adoption Path**  
1. **Prototype** – Pull the repo, run the Docker image or start the TypeScript server locally, and call its REST endpoints from a small test agent.  
2. **Integrate** – Replace the agent’s in‑memory prompt history with calls to the MCP API (or use the provided SDK) to store and retrieve memories.  
3. **Scale** – Deploy the server in a container orchestration platform (K8s, ECS, etc.), configure persistence (e.g., PostgreSQL, Redis) and enable authentication.  
4. **Extend** – Add custom memory schemas or hooks for tool results, then embed the server in larger multi‑agent orchestrations (e.g., LangChain, CrewAI).  

**Production Readiness**  
The project shows strong OSS maturity: recent commits (as of 2026‑06‑25), 97 stars, active forks, and a clear TypeScript codebase with comprehensive API documentation. Its modular design, standard HTTP/JSON interfaces, and support for CLI/SDK make it straightforward to evaluate and embed in production pipelines. While the license and security posture still need a final audit, the overall health, community signals, and ease of deployment qualify mem0‑MCP as a viable candidate for pilot projects and, with proper hardening, for full‑scale production use.

### Русский

**pinkpixel-dev/mem0-mcp** — это сервер MCP (Model Context Protocol), построенный на mem0, который обеспечивает долгосрочную память для AI‑агентов и легко интегрируется в существующие пайплайны через API/SDK/CLI. Он позволяет превратить разрозненные запросы и инструменты в повторяемые многокомпонентные рабочие процессы, упрощая координацию нескольких агентов, создание цепочек инструментов и стандартизацию их памяти. Проект уже имеет активную поддержку (обновления 2026‑06‑25, 97 звёзд, 13 форков), написан на TypeScript и считается готовым к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё ещё требуется.

### 中文

**项目简介**  
✨ **mem0 MCP Server**（pinkpixel-dev/mem0-mcp）是一个基于 mem0 的记忆系统，专为 AI 应用提供模型上下文协议（MCP）集成。它以 Drop‑in 方式提供长时记忆能力，让 AI 代理能够在不同会话和工具之间保持状态，实现可复用的工作流。

**价值**  
- **统一记忆层**：把零散的 Prompt、工具调用和外部数据统一到同一个长期记忆库，避免信息丢失。  
- **简化多代理编排**：通过标准化的 MCP 接口，多个 AI 代理可以共享、查询和更新记忆，实现协同工作流。  
- **加速工具化流水线**：在工具使用（Tool‑use）链路中直接读取/写入记忆，提升任务完成的连贯性和效率。

**典型接入方式**  
1. **API 调用**：直接向 MCP Server 发送 HTTP 请求（REST/GraphQL），获取或写入记忆。  
2. **SDK**：使用官方提供的 TypeScript/JavaScript SDK，在代码中以函数调用方式操作记忆（`mem0Client.getMemory(...)`、`mem0Client.updateMemory(...)`）。  
3. **CLI**：通过命令行工具快速调试或批量管理记忆数据。  
4. **容器化部署**：项目提供 Docker 镜像，可在 Kubernetes 或本地 Docker 环境中一键启动 MCP Server。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑25，星标 97、Fork 13，社区活跃。  
- **技术成熟度**：使用 TypeScript 实现，代码结构清晰，配套 16 个话题标签，文档覆盖 API、SDK 与部署指南。  
- **生态兼容**：兼容主流 LLM（OpenAI、Claude、Gemini 等）和常见的 RAG 框架，易于与现有 AI 平台对接。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式生产前完成许可证合规审查和安全渗透测试。  

综合来看，mem0‑MCP 已具备高可用的 OSS 候选特征，可在需要长期记忆和多代理协同的 AI 项目中直接投入试点或生产使用。

## 🧭 Practical evaluation

**Value:** pinkpixel-dev/mem0-mcp helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 97 GitHub stars
- 13 forks
- updated 2026-06-25
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 57/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 56/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/pinkpixel-dev/mem0-mcp) · [← Back to Orchestration](./README.md)</sub>
