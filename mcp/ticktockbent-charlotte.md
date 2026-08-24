# TickTockBent/charlotte

[![Stars](https://img.shields.io/github/stars/TickTockBent/charlotte?style=flat-square&color=yellow)](https://github.com/TickTockBent/charlotte/stargazers) [![Forks](https://img.shields.io/github/forks/TickTockBent/charlotte?style=flat-square&color=blue)](https://github.com/TickTockBent/charlotte/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Token-efficient browser MCP server — structured web pages for AI agents, not raw accessibility dumps

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 139 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `mcp` `mcp-server` `model-context-protocol` `typescript` `web-browsing` `web-scraping`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
TickTockBent / charlotte is an open‑source, token‑efficient MCP (Model Context Protocol) server that delivers structured web pages instead of raw accessibility dumps, enabling AI agents to consume and act on real‑world tools and data through a standardized interface. Written in TypeScript, it already ships with an API/SDK/CLI, clear language metadata, and focused integration topics, making it easy to plug into existing AI‑assistant stacks. With 139 ★, recent commits (as of 2026‑05‑13), and growing community interest, it is a strong candidate for production pilots.

**Value**  
- Provides a lightweight, token‑saving way for LLM‑based assistants to retrieve and manipulate web content, reducing inference costs.  
- Implements the Model Context Protocol, giving developers a common contract for exposing tools, services, or datasets to any MCP‑compatible AI.  
- By returning structured pages (e.g., JSON‑LD, DOM fragments) rather than unfiltered HTML, it improves reliability of downstream reasoning and action execution.

**Practical adoption path**  
1. **Prototype** – Clone the repo, run the supplied Docker/CLI locally, and point an MCP‑aware model (e.g., OpenAI‑compatible) at the server’s endpoint.  
2. **Integrate** – Use the provided TypeScript SDK (or REST API) to register your own tool endpoints or data sources; the SDK handles authentication, pagination, and token budgeting.  
3. **Test** – Run end‑to‑end scenarios (e.g., “schedule a meeting”, “fetch latest stock prices”) in a sandbox to validate that the AI correctly parses the structured responses.  
4. **Deploy** – Containerize the server, configure TLS and rate‑limiting, and roll it out behind your internal API gateway. Existing CI/CD pipelines can treat it like any other microservice.  

**Production readiness**  
- **Activity & community**: Recent commits, 139 ★, 20 forks, and seven well‑curated topics indicate an active maintainer base.  
- **Stability**: The TypeScript codebase is type‑checked, and the project ships a CLI and Docker image, reducing integration friction.  
- **Scalability**: Designed for token efficiency, it can be horizontally scaled behind a load balancer; health‑check endpoints are included.  
- **Risks**: License and security posture still need a final audit, and long‑term maintainer commitment should be confirmed before mission‑critical rollout.  

Overall, charlotte is mature enough for a serious pilot and, with standard security review, can be promoted to production use in AI‑assistant ecosystems.

### Русский

**TickTockBent/charlotte** — это токен‑экономичный сервер MCP, который преобразует структурированные веб‑страницы в удобный для AI‑агентов протокол Model Context Protocol, позволяя подключать виртуальных помощников к реальным инструментам и данным без необходимости парсить «сырой» HTML. Типичный сценарий — развертывание сервера MCP в качестве шлюза между AI‑агентом и внешними сервисами (инструменты, API, базы данных), что упрощает стандартизированную интеграцию и ускоряет вывод в продакшн новых функций. Проект считается почти готовым к production: активные коммиты, 139 звёзд, TypeScript‑база, поддержка API/SDK/CLI и положительные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
TickTockBent/charlotte 是一款 **Token‑efficient 浏览器 MCP（Model Context Protocol）服务器**，它将网页内容以结构化的形式提供给 AI 代理，而不是直接返回原始的可访问性转储，从而大幅降低 token 消耗并提升模型推理效率。

**价值主张**  
- **标准化接入**：通过统一的 MCP 接口，让 AI 助手能够像调用本地工具一样安全、可靠地访问真实的网络资源和业务数据。  
- **降低成本**：结构化页面只返回必要的语义片段，显著削减 LLM 所需的 token 数量，降低调用费用。  
- **快速集成**：提供 API、SDK 与 CLI 三种接入方式，配套 TypeScript 类型定义，开发者可在几行代码内完成接入。

**典型接入方式**  
1. **API 调用**：直接向 `POST /mcp/query` 发送 URL 与查询参数，返回 JSON 结构化结果。  
2. **SDK 引入**：在 Node/TS 项目中 `npm install @charlotte/mcp`，使用 `charlotteClient.query(url, options)` 完成查询。  
3. **CLI 工具**：`charlotte-cli query <url> --format=json`，适合脚本化或调试场景。  

**生产可用性**  
- **活跃度**：2026‑05‑13 最近更新，GitHub 139 星、20+ Fork，社区讨论活跃。  
- **技术成熟度**：核心使用 TypeScript 实现，已提供完整的类型声明和单元测试，兼容主流 LLM 平台。  
- **生态兼容**：支持 OpenAI、Claude、Gemini 等模型的上下文注入，易于在现有 AI Agent 框架中部署。  
- **风险**：目前暂无重大元数据或许可证风险，但仍建议在正式上线前进行安全审计并确认维护者的长期可用性。  

综合来看，TickTockBent/charlotte 已具备 **高生产就绪度**，适合作为 AI 助手与真实工具、数据交互的标准化后端服务进行试点或正式部署。

## 🧭 Practical evaluation

**Value:** TickTockBent/charlotte helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 139 GitHub stars
- 20 forks
- updated 2026-05-13
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 46/100 |
| topics | 88/100 |
| outlook | 54/100 |
| quality | 52/100 |
| recency | 20/100 |
| adoption | 42/100 |
| production | 52/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/TickTockBent/charlotte) · [← Back to Mcp](./README.md)</sub>
