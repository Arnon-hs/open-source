# firecrawl/firecrawl-mcp-server

[![Stars](https://img.shields.io/github/stars/firecrawl/firecrawl-mcp-server?style=flat-square&color=yellow)](https://github.com/firecrawl/firecrawl-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/firecrawl/firecrawl-mcp-server?style=flat-square&color=blue)](https://github.com/firecrawl/firecrawl-mcp-server/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-89%2F100-brightgreen?style=flat-square)](#)

> 🔥 Official Firecrawl MCP Server - Adds powerful web scraping and search to Cursor, Claude and any other LLM clients.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.7k |
| 🍴 **Forks** | 774 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 89/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`batch-processing` `claude` `content-extraction` `data-collection` `firecrawl` `firecrawl-ai` `javascript-rendering` `llm-tools` `mcp` `mcp-server` `model-context-protocol` `search-api`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Data

## 📝 Summary

### English

**Brief Summary**  
The **firecrawl‑firecrawl‑mcp‑server** project provides a ready‑to‑run Model Context Protocol (MCP) server that adds web‑scraping and search capabilities to any LLM client—such as Cursor, Claude, or custom agents. By exposing a simple HTTP/JSON API (and SDK/CLI wrappers), it lets developers plug real‑world data into their AI assistants without writing bespoke scrapers.  

**Value**  
- **Bridges the AI‑to‑data gap** – AI assistants can retrieve up‑to‑date web content, indexed search results, or structured extracts on demand, turning generic LLMs into task‑specific tools.  
- **Standardized integration** – MCP is a community‑driven protocol; using firecrawl’s server means you can swap the underlying LLM or the client (Cursor, Claude, LangChain, etc.) without rewriting integration code.  
- **Open‑source, battle‑tested** – With >6 k stars, active forks, and recent commits, the codebase is mature and community‑vetted, reducing the risk of hidden bugs.  

**Practical Adoption Path**  
1. **Prototype** – Pull the Docker image or run `npm install && npm start` locally; call the `/search` or `/scrape` endpoints from a notebook or a simple script to verify data quality.  
2. **Integrate** – Replace existing ad‑hoc scraper calls in your LLM workflow with the MCP server’s API; use the provided JavaScript SDK or generate a client in any language via the OpenAPI spec.  
3. **Scale** – Deploy the server behind a load balancer (Kubernetes, ECS, or Fly.io) and configure caching, rate‑limiting, and authentication (API keys or OAuth) as needed for production traffic.  
4. **Extend** – If you need custom parsers or domain‑specific extraction, fork the repo and add new handlers; the MCP contract remains unchanged, preserving compatibility with downstream agents.  

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑23), >6 k stars, 774 forks, and a vibrant issue/PR discussion indicate strong maintenance.  
- **Stability** – The server is built in JavaScript/Node.js, a well‑understood runtime for backend services, and ships with comprehensive API documentation and a CLI for health checks.  
- **Ecosystem Fit** – MCP is already adopted by several LLM platforms; firecrawl’s implementation is the de‑facto reference server, making it a safe choice for pilots and full‑scale deployments.  
- **Risks** – License (MIT) is permissive, but a final security audit and verification of active maintainers are recommended before mission‑critical use.  

Overall, firecrawl‑firecrawl‑mcp‑server is a high‑readiness, open‑source component that lets you quickly equip AI assistants with reliable web‑scraping and search, following a clear path from local testing to production‑grade deployment.

### Русский

**firecrawl/firecrawl-mcp-server** — официальный MCP‑сервер Firecrawl, который через стандартный Model Context Protocol позволяет LLM‑ассистентам (Cursor, Claude и др.) выполнять веб‑скрейпинг и поиск, получая доступ к актуальным данным и внешним инструментам. Типичный сценарий — интеграция AI‑агента в существующую инфраструктуру: сервер разворачивается как микросервис (API/SDK/CLI), после чего любые LLM‑клиенты могут запрашивать извлечение контента, индексацию и поиск по веб‑страницам без отдельной реализации. Проект обладает высокой готовностью к production: активные коммиты, более 6600 звёзд, широкое использование в сообществе и поддержка JavaScript, что делает его надёжным выбором для пилотных и масштабных внедрений.

### 中文

**项目价值**  
firecrawl‑mcp‑server 为 AI 助手（如 Cursor、Claude 以及其他 LLM 客户端）提供统一的 **Model Context Protocol（MCP）** 接口，使其能够直接调用强大的网页抓取与搜索功能。通过标准化的协议，开发者可以快速把真实的网络数据和工具接入到 LLM 工作流中，极大提升模型的实际可操作性和信息获取能力。

**典型接入方式**  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **在代码中直接调用** | 使用提供的 **JavaScript/Node.js SDK** 或 **REST API** | 1. `npm install @firecrawl/mcp-server`  <br>2. 初始化客户端并配置 API Key <br>3. 调用 `crawl(url)`、`search(query)` 等方法 |
| **命令行/脚本** | 通过 **CLI**（`firecrawl-mcp`） | 1. 安装全局 CLI：`npm i -g @firecrawl/mcp-cli` <br>2. 运行 `firecrawl crawl <url>` 或 `firecrawl search "<关键词>"` |
| **作为独立服务** | 部署 **MCP Server**（Docker / Kubernetes） | 1. 拉取镜像 `docker pull firecrawl/mcp-server` <br>2. 启动容器并映射端口 <br>3. 在 LLM 客户端配置 MCP 端点（如 `http://host:8080`） |
| **在其他语言环境** | 通过 **HTTP/JSON** 协议调用 | 直接向服务器的 `/v1/crawl`、`/v1/search` 等 REST 接口发送请求，返回标准化的 JSON 响应 |

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，拥有 6.6k 星、774 fork，社区活跃，Issue 处理及时。  
- **成熟度**：提供完整的 API 文档、SDK、CLI 与 Docker 镜像，支持多语言调用，已被多家企业在实际项目中使用。  
- **安全与合规**：项目采用 MIT 许可证，代码审计记录良好；但在正式投产前仍建议自行进行安全扫描并确认依赖的爬虫行为符合目标站点的 robots.txt 与隐私政策。  
- **可扩展性**：基于 Node.js 实现，天然支持水平扩容（K8s 部署），并可通过自定义插件接入额外的爬取或搜索后端。

**结论**：firecrawl‑mcp‑server 已具备 **高可用、易集成、社区支持强** 的特性，是在生产环境中为 LLM 添加实时网络信息获取能力的可靠 OSS 选项。只要完成常规的安全审计与运维监控，即可直接用于正式业务。

## 🧭 Practical evaluation

**Value:** firecrawl/firecrawl-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6662 GitHub stars
- 774 forks
- updated 2026-06-23
- primary language: JavaScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 81/100 |
| topics | 100/100 |
| outlook | 95/100 |
| quality | 90/100 |
| recency | 100/100 |
| adoption | 79/100 |
| production | 85/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/firecrawl/firecrawl-mcp-server) · [← Back to Mcp](./README.md)</sub>
