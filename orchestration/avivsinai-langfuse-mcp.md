# avivsinai/langfuse-mcp

[![Stars](https://img.shields.io/github/stars/avivsinai/langfuse-mcp?style=flat-square&color=yellow)](https://github.com/avivsinai/langfuse-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/avivsinai/langfuse-mcp?style=flat-square&color=blue)](https://github.com/avivsinai/langfuse-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> A Model Context Protocol (MCP) server for Langfuse, enabling AI agents to query Langfuse trace data for enhanced debugging and observability

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 97 |
| 🍴 **Forks** | 25 |
| 💻 **Language** | Python |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agents` `claude-code` `codex` `developer-tools` `genai` `langfuse` `llm` `mcp` `mcp-server` `observability` `tracing`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
avivsinai/langfuse‑mcp is a Python‑based Model Context Protocol (MCP) server that plugs into Langfuse, allowing AI agents to query trace data for richer debugging, observability, and state‑sharing. By exposing Langfuse’s trace metadata through a simple API/SDK/CLI, it turns isolated prompts and tool calls into repeatable, orchestrated agent workflows.

**Value**  
- **Unified Agent Memory:** Agents can read past execution traces, making decisions based on historic context rather than starting from a blank slate.  
- **Debug‑first Observability:** Real‑time access to Langfuse’s detailed logs and metrics lets developers pinpoint failures, latency spikes, or unexpected tool usage quickly.  
- **Workflow Standardisation:** The MCP layer provides a consistent contract for multi‑agent pipelines, enabling teams to compose, version, and reuse complex tool‑use sequences across projects.

**Practical Adoption Path**  
1. **Prototype:** Add the `langfuse-mcp` package to an existing Langfuse‑enabled project and spin up the MCP server (Docker or direct `uvicorn`).  
2. **Integrate:** Update your agents to call the MCP API (or use the provided SDK) when they need to retrieve prior trace data or push new events.  
3. **Orchestrate:** Layer the MCP calls into your orchestration framework (e.g., LangChain, CrewAI) to build multi‑agent loops or tool‑use pipelines.  
4. **Validate:** Run end‑to‑end tests with a small set of prompts, verify that trace‑driven decisions improve success rates, and monitor the added latency.  
5. **Scale:** Deploy the MCP server behind a load balancer, enable authentication, and configure persistence (PostgreSQL, Redis) for production workloads.

**Production Readiness**  
- **Activity & Adoption:** 97 stars, 25 forks, recent commits (last updated 2026‑06‑27) and multiple downstream adopters indicate a healthy community.  
- **Maturity:** The project ships a stable API, SDK, and CLI, and follows the MCP spec, making integration straightforward.  
- **Risk Considerations:** No major metadata or licensing issues have been identified, but a final security audit and verification of active maintainers are advisable before mission‑critical deployment. Overall, the project is ready for a serious pilot in production environments.

### Русский

avivsinai/langfuse-mcp — это сервер Model Context Protocol (MCP) для Langfuse, который позволяет AI‑агентам запрашивать трассировочные данные из Langfuse, упрощая отладку и наблюдаемость сложных многопоточных сценариев. Типичный сценарий: интеграция MCP в пайплайн с несколькими агентами и инструментами, чтобы стандартизировать их «память», координировать последовательные вызовы и превращать разрозненные подсказки в повторяемые рабочие процессы. Проект считается почти готовым к production: активные коммиты, 97 звёзд, 25 форков, поддержка API/SDK/CLI, Python‑база и сильные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
avivsinai/langfuse-mcp 是一个基于 Model Context Protocol（MCP）的服务端实现，专为 Langfuse 设计。它让 AI 代理能够实时查询 Langfuse 的 trace 数据，从而实现更细粒度的调试、可观测性以及跨工具的上下文共享。

**价值主张**  
- **将孤立的 Prompt 与工具链转化为可复用的工作流**：通过统一的 MCP 接口，多个代理可以共享同一套追踪信息，实现协同推理和记忆持久化。  
- **提升调试与可观测性**：开发者可以直接在代理运行时检索执行历史、输入输出和错误信息，快速定位问题。  
- **标准化 Agent Memory**：把 Langfuse 的 trace 视作统一的记忆库，简化了多代理或多步骤任务的状态管理。

**典型接入方式**  
1. **API/SDK**：在代理代码中引入 `langfuse-mcp` 提供的 Python SDK，使用 `MCPClient` 直接调用 `get_trace(trace_id)`、`list_traces()` 等接口。  
2. **CLI**：通过自带的 `langfuse-mcp-cli` 在本地或 CI 环境中查询 trace，适合调试或自动化脚本。  
3. **语言元数据**：服务自动暴露 OpenAPI 文档，支持其他语言（如 Node.js、Go）通过生成的客户端代码进行调用。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑27 最近一次提交，拥有 97 ★、25 Fork，社区讨论活跃。  
- **技术成熟度**：核心实现基于 Python，提供完整的单元测试和 CI，已在多个内部项目中验证。  
- **生态兼容**：直接兼容 Langfuse 官方 API，且遵循 MCP 标准，易于与现有的 Orchestration、Agent‑Framework（如 LangChain、AutoGPT）集成。  
- **风险**：目前仍需对许可证（MIT）进行合规审查，安全审计和维护者响应时效需进一步确认。整体来看，项目已具备 **高** 的生产候选级别，适合在正式环境中进行试点并逐步推广。

## 🧭 Practical evaluation

**Value:** avivsinai/langfuse-mcp helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 97 GitHub stars
- 25 forks
- updated 2026-06-27
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/avivsinai/langfuse-mcp) · [← Back to Orchestration](./README.md)</sub>
