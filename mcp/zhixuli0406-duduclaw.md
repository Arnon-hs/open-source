# zhixuli0406/DuDuClaw

[![Stars](https://img.shields.io/github/stars/zhixuli0406/DuDuClaw?style=flat-square&color=yellow)](https://github.com/zhixuli0406/DuDuClaw/stargazers) [![Forks](https://img.shields.io/github/forks/zhixuli0406/DuDuClaw?style=flat-square&color=blue)](https://github.com/zhixuli0406/DuDuClaw/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Open-source AI Agent platform — 80+ MCP tools, 7 channels (Slack/Discord/LINE/Telegram), Rust + Python. Self-hostable Claude/GPT alternative for production multi-LLM systems.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 43 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Rust |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-platform` `agentic-ai` `ai-agent` `claude` `gemini` `llm` `llm-agent` `mcp` `mcp-server` `model-context-protocol` `multi-llm` `openai`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
DuDuClaw is an open‑source AI‑agent platform that implements the Model Context Protocol (MCP) with more than 80 ready‑to‑use tool integrations and seven communication channels (Slack, Discord, LINE, Telegram, etc.). Built in Rust with a Python SDK, it can be self‑hosted as a Claude‑ or GPT‑style multi‑LLM backend for production‑grade workflows.  

**Value**  
- **Unified tool access** – By exposing a standard MCP API, DuDuClaw lets any LLM‑powered assistant invoke real‑world tools (databases, web services, messaging platforms) without custom glue code.  
- **Multi‑channel reach** – The built‑in connectors for popular chat apps enable seamless deployment of agents where users already communicate.  
- **Performance & safety** – Rust’s low‑level efficiency and the ability to run the stack entirely on‑premise give organizations control over latency, data residency, and cost, while the Python SDK makes rapid prototyping easy.  

**Practical Adoption Path**  
1. **Prototype** – Use the Python SDK/CLI to spin up a local MCP server, connect a few of the 80+ pre‑bundled tools, and test agent prompts in a sandbox.  
2. **Integrate** – Replace the prototype’s stub endpoints with your own services (e.g., internal CRM, data warehouse) by implementing the MCP interface; the existing channel adapters (Slack, Discord, etc.) can be enabled with minimal configuration.  
3. **Self‑host** – Deploy the Rust server in a container orchestration platform (Docker/K8s) behind your firewall, configure TLS and authentication, and point your LLM provider (Claude, GPT‑4, open‑source models) to the MCP endpoint.  
4. **Scale & Monitor** – Leverage the built‑in logging and health‑check endpoints, add rate‑limiting or circuit‑breaker middleware, and integrate with your observability stack.  

**Production Readiness**  
- **Maturity**: Medium. The project has 43 stars, recent updates (June 2026), and a modest fork count, indicating active but still small‑scale community involvement.  
- **Stability**: Core MCP server is written in Rust, which offers strong type safety and performance; the Python SDK is well‑documented for rapid iteration.  
- **Dependencies**: Relatively self‑contained, but you’ll need to audit third‑party tool adapters and ensure they meet your security policies.  
- **Operational considerations**: Requires in‑house expertise to maintain the Rust service, manage TLS/auth, and keep the tool adapters up‑to‑date; no out‑of‑the‑box monitoring or auto‑scaling features.  

Overall, DuDuClaw is a solid foundation for building production‑grade, multi‑LLM agents that need reliable access to external tools and chat channels, provided you allocate resources for security review, dependency management, and operational tooling.

### Русский

DuDuClaw — это открытая платформа AI‑агентов, реализованная на Rust и Python, предоставляющая более 80 MCP‑инструментов и 7 каналов (Slack, Discord, LINE, Telegram и др.) через единый протокол Model Context Protocol, что упрощает подключение LLM‑моделей к реальным инструментам и данным. Типичный сценарий — развертывание собственного сервера‑агента (альтернатива Claude/GPT) для интеграции с корпоративными сервисами, построения прототипов и внутренних рабочих процессов, а также публикация готовых MCP‑серверов. Готовность к production оценивается как средняя: проект уже стабилен и активно обновляется (43 звёзд, 5 форков, последний коммит 2026‑06‑25), но перед запуском в продакшн рекомендуется проверить лицензирование, безопасность и долгосрочную поддержку зависимостей.

### 中文

**项目简介**  
DuDuClaw 是一个开源的 AI Agent 平台，提供 80+ MCP（Model Context Protocol）工具和 7 条主流聊天渠道（Slack、Discord、LINE、Telegram 等），核心实现基于 Rust 与 Python，可自托管并作为 Claude / GPT 的替代方案，适用于多模型生产环境。

**价值**  
- **统一协议**：通过标准化的 MCP 将 AI 助手与真实工具、数据库、业务系统快速对接，降低集成成本。  
- **多渠道输出**：一次部署即可在多种即时通讯平台上提供同质化的 AI 服务，提升触达率。  
- **语言多样**：Rust 提供高性能、低资源占用，Python SDK/CLI 让快速原型和脚本化调用变得轻松。  

**典型接入方式**  
1. **部署 MCP Server**：使用 Docker 或直接编译 Rust 二进制，启动 Model Context Protocol 服务。  
2. **注册渠道**：在平台后台配置 Slack、Discord、LINE、Telegram 等 webhook/Token，即可让 AI Agent 收发消息。  
3. **调用工具**：通过平台提供的 REST API、Python SDK 或 CLI，向已注册的 MCP 工具（如搜索、数据库查询、代码执行等）发送请求，返回结果自动注入对话上下文。  

**生产可用性**  
- **成熟度**：目前在 GitHub 上拥有 43 星、5 个 Fork，最近一次提交在 2026‑06‑25，代码以 Rust 为主，具备较好的性能基准。  
- **适用场景**：适合内部原型、业务流程自动化或中小规模的生产部署；在大流量、跨地域的高可用需求下仍需进行依赖审计、容灾设计和安全加固。  
- **风险点**：许可证、长期维护者活跃度以及安全审计尚未完成，需要在正式投产前进行评估。  

总体而言，DuDuClaw 为企业提供了一套 **“AI + 工具 + 渠道”** 的完整解决方案，能够在保持灵活性的同时，加速 AI 助手在真实业务环境中的落地。

## 🧭 Practical evaluation

**Value:** zhixuli0406/DuDuClaw helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 43 GitHub stars
- 5 forks
- updated 2026-06-25
- primary language: Rust
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 31/100 |
| production | 55/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/zhixuli0406/DuDuClaw) · [← Back to Mcp](./README.md)</sub>
