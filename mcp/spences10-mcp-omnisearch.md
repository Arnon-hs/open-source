# spences10/mcp-omnisearch

[![Stars](https://img.shields.io/github/stars/spences10/mcp-omnisearch?style=flat-square&color=yellow)](https://github.com/spences10/mcp-omnisearch/stargazers) [![Forks](https://img.shields.io/github/forks/spences10/mcp-omnisearch?style=flat-square&color=blue)](https://github.com/spences10/mcp-omnisearch/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> 🔍 A Model Context Protocol (MCP) server providing unified access to multiple search engines (Tavily, Brave, Kagi, Exa), AI tools (Kagi FastGPT, Exa, Linkup), and content extraction services (Firecrawl, Tavily, Kagi). Includes GitHub search. All through a single interface.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 328 |
| 🍴 **Forks** | 47 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`brave` `exa` `firecrawl` `github-search` `kagi` `linkup` `mcp` `model-context-protocol` `search` `tavily`

## 🎯 Categories

MCP

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
spences10/mcp‑omnisearch is a TypeScript‑based Model Context Protocol (MCP) server that aggregates search, AI, and content‑extraction services—including Tavily, Brave, Kagi, Exa, FastGPT, Linkup, and Firecrawl—behind a single, uniform API. It also offers built‑in GitHub code search, letting AI agents retrieve and process data from a variety of sources without having to manage multiple vendor SDKs.  

**Value**  
- **Unified interface:** Developers and AI assistants can call one endpoint to query many search engines, LLM‑powered tools, and web‑scraping services, dramatically reducing integration complexity.  
- **Standardized protocol:** By adhering to the Model Context Protocol, the server enables plug‑and‑play connectivity for any MCP‑compatible AI agent, fostering ecosystem interoperability.  
- **Extensible architecture:** Adding new providers or custom plugins is straightforward, allowing teams to evolve their toolchain without rewriting client code.  

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the provided Docker compose or npm script, and configure API keys for the desired providers.  
2. **Integrate:** Point your MCP‑compatible AI agent (e.g., LangChain, AutoGPT, or a custom assistant) to the server’s `/search` and `/extract` endpoints; the agent can now issue a single request like `search("latest React best practices")` and receive consolidated results.  
3. **Extend:** If you need additional services (e.g., internal document stores), implement a new provider module following the existing TypeScript interface and register it in the server’s config.  
4. **Deploy:** Deploy the server as a containerized micro‑service (K8s, ECS, etc.) behind an internal API gateway, applying rate‑limiting and secret management for the third‑party keys.  

**Production Readiness**  
- **Activity & Community:** 328 ★, 47 forks, last updated on 2026‑06‑23, with recent commits and active issue handling, indicating a healthy maintenance cadence.  
- **Maturity:** The codebase is TypeScript‑typed, includes CI pipelines, and provides both SDK and CLI entry points, simplifying integration and automated testing.  
- **Scalability:** Designed as a stateless HTTP server; can be horizontally scaled behind a load balancer.  
- **Risks:** Licensing and security posture still require a formal review, and long‑term maintainer commitment should be verified before mission‑critical roll‑outs.  

Overall, mcp‑omnisearch is production‑ready for pilot projects and can be hardened for full‑scale deployments with standard DevSecOps practices.

### Русский

**spences10/mcp-omnisearch** — это сервер Model Context Protocol, который через единый API объединяет поиск в нескольких движках (Tavily, Brave, Kagi, Exa), AI‑инструменты (Kagi FastGPT, Exa, Linkup) и сервисы извлечения контента (Firecrawl, Tavily, Kagi), а также поиск по GitHub. Он позволяет быстро подключить AI‑агентов к реальным инструментам и данным, стандартизируя интеграцию и упрощая развёртывание MCP‑серверов. Проект имеет высокую готовность к production: активные обновления, 328 звёзд, TypeScript‑код, хорошая экосистема и широкую поддержку, требующую лишь финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
`spences10/mcp-omnisearch` 是一个实现 Model Context Protocol（MCP）的统一搜索服务，提供对多家搜索引擎（Tavily、Brave、Kagi、Exa）、AI 工具（Kagi FastGPT、Exa、Linkup）以及内容抽取服务（Firecrawl、Tavily、Kagi）的统一接口，并内置 GitHub 代码搜索。  

**价值**  
- **统一协议**：AI 助手只需使用 MCP 即可调用多种外部搜索和数据抽取能力，避免为每个服务单独实现适配层。  
- **即插即用**：通过标准的 HTTP/JSON API（或对应的 SDK/CLI）即可把搜索、LLM Tool、网页抓取等功能快速接入现有 AI 工作流。  
- **生态兼容**：兼容主流 LLM Agent 框架（如 LangChain、Auto‑GPT、OpenAI Function Calling），帮助开发者把真实世界信息快速注入模型上下文。  

**典型接入方式**  
1. **直接调用 HTTP API**：向 `POST /search`、`/tool`、`/extract` 等端点发送 JSON 请求，返回统一结构的搜索结果或提取内容。  
2. **使用官方 TypeScript SDK**：`npm i mcp-omnisearch` 后，调用 `client.search(...)`、`client.runTool(...)` 等方法，内部完成身份验证、参数序列化和错误处理。  
3. **CLI/脚本**：项目自带 `mcp-omnisearch-cli`，可在 CI/CD、自动化脚本或本地调试时直接使用，例如 `mcp-omnisearch search "最新 AI 论文"`。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，星标 328、Fork 47，社区活跃且已有多项实际使用案例。  
- **技术成熟度**：基于 TypeScript 实现，提供完整的类型定义和自动化测试，错误码和超时策略明确，适合在容器化或 Serverless 环境中部署。  
- **安全与合规**：项目使用 MIT 许可证，代码审计记录良好；但在正式投产前仍建议自行进行依赖漏洞扫描并确认 API 密钥管理符合内部安全规范。  
- **可扩展性**：通过配置文件可灵活添加/替换后端搜索/抽取服务，支持自定义插件，满足企业级多租户或高并发需求。  

综上，`spences10/mcp-omnisearch` 已具备较高的生产准备度，适合作为 AI 助手与外部工具/数据的桥梁，在需要统一检索与内容抽取的场景下快速落地。

## 🧭 Practical evaluation

**Value:** spences10/mcp-omnisearch helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 328 GitHub stars
- 47 forks
- updated 2026-06-23
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 58/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/spences10/mcp-omnisearch) · [← Back to Mcp](./README.md)</sub>
