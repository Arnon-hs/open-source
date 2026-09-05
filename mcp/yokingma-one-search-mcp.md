# yokingma/one-search-mcp

[![Stars](https://img.shields.io/github/stars/yokingma/one-search-mcp?style=flat-square&color=yellow)](https://github.com/yokingma/one-search-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/yokingma/one-search-mcp?style=flat-square&color=blue)](https://github.com/yokingma/one-search-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> 🚀 OneSearch MCP Server: Web Search & Scraper & Extract,  Support agent-browser, SearXNG, Tavily, DuckDuckGo, Bing, etc.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 121 |
| 🍴 **Forks** | 17 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-browser` `bing-mcp` `duckduckgo-mcp` `google-search-mcp` `mcp-server` `modelcontextprotocol` `searxng-mcp` `tavily-mcp`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
OneSearch MCP is a TypeScript‑based server that unifies web search, scraping, and data extraction across providers such as SearXNG, Tavily, DuckDuckGo, Bing, and more. It implements the Model Context Protocol (MCP), enabling AI assistants to invoke real‑world tools and retrieve up‑to‑date information through a single, standardized API.

**Value**  
By abstracting the heterogeneity of public search APIs, OneSearch MCP lets developers plug any MCP‑compatible AI agent into a reliable, extensible search backend without writing provider‑specific adapters. This reduces integration effort, accelerates feature rollout for conversational agents, and creates a reusable “search as a service” layer that can be shared across multiple products or teams.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or npm start script, and point your agent’s MCP client to the local endpoint.  
2. **Configure Providers** – Add API keys and optional query parameters for the desired search backends in the `config.yaml` file; the server will automatically route requests.  
3. **Integrate** – Use the generated OpenAPI spec or the built‑in SDK/CLI to call the `/search` endpoint from your AI workflow, handling the standardized JSON response.  
4. **Scale** – Deploy the server to a container orchestration platform (K8s, ECS, etc.) behind a load balancer, enable caching or rate‑limit middleware, and monitor health via the built‑in Prometheus metrics.

**Production Readiness**  
The project shows strong OSS maturity: 121 stars, recent commits (as of 2026‑06‑26), active issue handling, and a clear TypeScript codebase with an OpenAPI contract. Its modular architecture, Docker support, and existing integrations with major search engines make it suitable for pilot deployments and, after a brief security/license audit, for full‑scale production use.

### Русский

**OneSearch MCP** — это сервер‑прокси на TypeScript, который через единый протокол (Model Context Protocol) соединяет AI‑агентов с реальными веб‑инструментами (SearXNG, Tavily, DuckDuckGo, Bing и др.) для поиска, скрейпинга и извлечения данных. Типичный сценарий — интеграция в чат‑ботов или автопилотов, которым нужен быстрый доступ к актуальной информации без написания собственного парсера; достаточно развернуть сервер и подключить его к вашему агенту через API/SDK/CLI. Проект считается готовым к production: активные коммиты, 121 звезда, поддержка нескольких языков и хорошая экосистема, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介**  
OneSearch MCP Server（yokingma/one-search-mcp）是一套基于 Model Context Protocol（MCP）的统一搜索与抓取后端，内置对 SearXNG、Tavily、DuckDuckGo、Bing 等多家搜索引擎的适配，并提供网页抓取、内容抽取等能力，专为 AI 助手与真实工具/数据的对接而设计。

**价值点**  
- **统一协议**：通过标准的 MCP 接口，让各种 AI 代理（agent‑browser、ChatGPT‑插件等）无需关心底层搜索实现即可调用。  
- **多源搜索**：一次请求即可在多个搜索引擎之间切换或聚合结果，提升信息覆盖率与可靠性。  
- **即插即用**：提供 REST API、Node.js SDK 与 CLI 三种调用方式，适配大多数后端语言和部署环境。

**典型接入方式**  
1. **REST API**：在服务端或前端直接发 HTTP POST/GET 请求，携带 `model_context` 消息体，即可获得统一的搜索/抓取结果。  
2. **Node.js SDK**：`npm i one-search-mcp` 后，引入 `OneSearchClient`，在代码中调用 `search()`、`scrape()`、`extract()` 等方法，返回 Promise，适合在微服务或函数计算中使用。  
3. **CLI**：安装全局二进制 `npx one-search-mcp`，在命令行直接执行搜索或抓取，便于调试、脚本化或临时查询。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑26，GitHub ★121、Fork 17，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义和 OpenAPI 文档，易于集成和二次开发。  
- **生态兼容**：已对接多家主流搜索引擎，且实现了标准的 MCP 协议，能够快速对接现有 AI 助手框架（如 LangChain、AutoGPT）。  
- **风险**：目前许可证、长期维护者以及安全审计仍需进一步确认；在正式生产环境使用前建议进行内部安全评估并锁定依赖版本。

综合来看，OneSearch MCP Server 已具备较高的生产就绪度，适合作为 AI 助手的搜索/抓取后端，或作为模型上下文协议（MCP）服务的参考实现进行二次开发。

## 🧭 Practical evaluation

**Value:** yokingma/one-search-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 121 GitHub stars
- 17 forks
- updated 2026-06-26
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/yokingma/one-search-mcp) · [← Back to Mcp](./README.md)</sub>
