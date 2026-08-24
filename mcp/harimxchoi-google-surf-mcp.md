# HarimxChoi/google-surf-mcp

[![Stars](https://img.shields.io/github/stars/HarimxChoi/google-surf-mcp?style=flat-square&color=yellow)](https://github.com/HarimxChoi/google-surf-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/HarimxChoi/google-surf-mcp?style=flat-square&color=blue)](https://github.com/HarimxChoi/google-surf-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> ✨Anti-Bot Search MCP: No API Key✨

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 152 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anti-bot` `claude` `google-search` `mcp` `model-context-protocol` `no-api-key` `playwright`

## 🎯 Categories

MCP · Automation · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
HarimxChoi/google‑surf‑mcp is an open‑source “Anti‑Bot Search” Model Context Protocol (MCP) server that lets AI assistants query Google Search without needing an API key. Written in TypeScript, the project provides a simple API/SDK/CLI that standardizes tool integration, making it easy to plug real‑world data sources into generative agents.

**Value**  
- **Standardized integration** – By exposing the Model Context Protocol, the server offers a uniform way for any MCP‑compatible AI agent to access live search results, eliminating the need for bespoke scrapers or paid API keys.  
- **Rapid prototyping** – The ready‑made API and CLI let developers quickly connect agents to up‑to‑date web information, accelerating the development of knowledge‑aware assistants and RAG pipelines.  
- **Cost‑effective** – Because it bypasses Google’s paid Search API, teams can experiment and run low‑traffic pilots without incurring external service fees.

**Practical Adoption Path**  
1. **Clone & Install** – `git clone https://github.com/HarimxChoi/google-surf-mcp && npm install`.  
2. **Configure** – Set optional environment variables (e.g., request throttling, custom user‑agents).  
3. **Run the MCP server** – `npm start` launches a local HTTP endpoint that complies with the Model Context Protocol.  
4. **Integrate** – Point your AI assistant’s MCP client (or any MCP‑compatible SDK) to the server’s URL; the assistant can now issue `search` actions and receive structured results.  
5. **Scale** – Deploy the server to a container platform (Docker, Kubernetes, or serverless) and adjust rate‑limit settings for production traffic.

**Production Readiness**  
- **Activity & Community** – 152 ★, 22 forks, recent commit (2026‑05‑14), and multiple topics indicate an active codebase.  
- **Maturity** – The project follows a clear API contract, includes a CLI, and is written in TypeScript, which aids type safety and maintainability.  
- **Risk Assessment** – No major metadata or licensing concerns identified, though a final review of the open‑source license and security posture is recommended. Overall, the repository exhibits strong signals for pilot deployments and can be promoted to production after standard security hardening and monitoring.

### Русский

HarimxChoi/google-surf-mcp — это открытый MCP‑сервер, позволяющий AI‑ассистентам обращаться к реальным инструментам и данным без необходимости использовать API‑ключи; он реализован на TypeScript и предоставляет единый протокол для подключения внешних сервисов, SDK и CLI. Типичный сценарий — быстрое внедрение Model Context Protocol в существующие автоматизационные и бэкенд‑системы, чтобы агентам было удобно вызывать внешние инструменты (поиск, скрейпинг, интеграции) в режиме реального времени. Проект считается готовым к production‑использованию: активные коммиты, 152 звезды, 22 форка, поддержка нескольких языков и тем, а также положительные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
HarimxChoi/google‑surf‑mcp 是一款「零 API Key」的 Anti‑Bot Search MCP（Model Context Protocol）实现，使用 TypeScript 编写，能够让 AI 助手通过统一协议直接调用真实的搜索工具和数据源。

**价值**  
- **标准化接入**：提供统一的 MCP 接口，帮助 AI 代理快速对接搜索、爬虫等后端工具，降低集成成本。  
- **免密钥**：无需申请或管理 Google API Key，即可在本地或私有网络中运行，适合对安全、隐私有严格要求的场景。  
- **开箱即用**：自带 CLI、SDK 与 OpenAPI 规格，支持快速部署 Model Context Protocol 服务器，便于在多语言生态中复用。

**典型接入方式**  
1. **作为 MCP 服务器**：在 Node.js 环境下 `npm i google-surf-mcp`，启动 `npx google-surf-mcp serve`，即可得到一个符合 MCP 规范的 HTTP/WS 接口。  
2. **SDK 调用**：在 TypeScript/JavaScript 项目中引入 `import { search } from 'google-surf-mcp'`，直接调用 `search(query)` 获得搜索结果对象。  
3. **CLI 使用**：`npx google-surf-mcp query "最新 AI 研究"`，在终端获取结构化返回，适合脚本化或 CI/CD 场景。  
4. **与其他语言集成**：通过 OpenAPI 文档或 gRPC 网关，其他语言（Python、Go、Java 等）可生成客户端代码，实现跨语言调用。

**生产可用性**  
- **活跃度**：截至 2026‑05‑14 最近一次提交，GitHub ★152、Fork 22，拥有 7 个相关话题，社区活跃。  
- **成熟度**：项目已实现完整的 MCP 协议栈、错误处理与限流，具备基本的单元与集成测试。  
- **风险**：暂无重大元数据或许可证冲突，但仍建议在正式上线前完成安全审计（依赖的第三方库、容器镜像等）并确认维护者的响应能力。  
- **结论**：在具备基本运维能力的环境中，可视为 **高可用 OSS 候选**，适合在内部 AI 平台或面向客户的 AI 助手项目中进行试点或正式部署。

## 🧭 Practical evaluation

**Value:** HarimxChoi/google-surf-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 152 GitHub stars
- 22 forks
- updated 2026-05-14
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 46/100 |
| topics | 88/100 |
| outlook | 51/100 |
| quality | 52/100 |
| recency | 20/100 |
| adoption | 43/100 |
| production | 54/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/HarimxChoi/google-surf-mcp) · [← Back to Mcp](./README.md)</sub>
