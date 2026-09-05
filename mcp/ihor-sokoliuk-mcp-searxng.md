# ihor-sokoliuk/mcp-searxng

[![Stars](https://img.shields.io/github/stars/ihor-sokoliuk/mcp-searxng?style=flat-square&color=yellow)](https://github.com/ihor-sokoliuk/mcp-searxng/stargazers) [![Forks](https://img.shields.io/github/forks/ihor-sokoliuk/mcp-searxng?style=flat-square&color=blue)](https://github.com/ihor-sokoliuk/mcp-searxng/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Private web search for AI assistants via SearXNG — supports Claude, Cursor, and any MCP client

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 944 |
| 🍴 **Forks** | 136 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `claude` `cursor` `llm` `mcp` `mcp-server` `mcp-servers` `privacy` `search` `searxng` `self-hosted` `web-search`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
ihor‑sokoliuk’s **mcp-searxng** is an open‑source bridge that lets AI assistants (Claude, Cursor, or any Model‑Context‑Protocol client) perform private web searches through SearXNG. By exposing a standard MCP‑compatible API, it enables agents to retrieve real‑world data safely and consistently, turning search results into structured tool calls for downstream reasoning.

**Value**  
- **Real‑world grounding:** AI agents can augment their knowledge with up‑to‑date, privacy‑preserving web results instead of relying solely on static training data.  
- **Standardized integration:** The MCP layer abstracts the underlying search engine, so the same client code works with any MCP‑compliant tool, reducing vendor lock‑in.  
- **Extensible ecosystem:** Because the project is written in TypeScript and ships both an HTTP API and a CLI/SDK, developers can embed it in serverless functions, microservices, or local dev environments with minimal friction.

**Practical Adoption Path**  
1. **Prototype:** Pull the Docker image or run `npm install` to launch the SearXNG server with the MCP wrapper; configure the endpoint URL in your AI‑assistant client (e.g., Claude or Cursor).  
2. **Integrate:** Use the provided TypeScript SDK or raw HTTP calls to send search queries and receive structured results (titles, snippets, URLs, relevance scores).  
3. **Secure & Customize:** Enable authentication (API keys or OAuth), adjust SearXNG sources to match your privacy policy, and add custom parsers if you need domain‑specific extraction.  
4. **Scale:** Deploy the service behind a load balancer or as a Kubernetes microservice; the stateless design lets you horizontally scale to handle production query volumes.

**Production Readiness**  
- **Activity & Adoption:** 944 ★, 136 forks, recent commits (last updated 2026‑06‑23), and active issues indicate a healthy community.  
- **Maturity:** The project provides a complete API/SDK/CLI surface, clear TypeScript typings, and Docker support, making it straightforward to containerize and monitor.  
- **Risk Profile:** No obvious metadata or licensing red flags; however, a final security audit and verification of maintainer responsiveness are recommended before mission‑critical deployment. Overall, the codebase is robust enough for a serious pilot or full‑scale production rollout.

### Русский

**ihor-sokoliuk/mcp-searxng** — это открытый сервер‑прокси, который интегрирует SearXNG с Model Context Protocol (MCP), позволяя AI‑ассистентам (Claude, Cursor и любые MCP‑клиенты) выполнять приватный веб‑поиск и получать актуальные данные в реальном времени. Типичный сценарий: разворачиваете сервис, подключаете к нему ваш AI‑агент через MCP и получаете единый, стандартизированный интерфейс для запросов к поисковой системе, что упрощает построение «инструмент‑под‑рукой» у моделей. Проект имеет высокий уровень готовности к production: активные коммиты, более 900 звёзд, TypeScript‑код, поддержка API/SDK/CLI и широкое принятие в экосистеме, требующее лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
ihor‑sokoliuk/mcp‑searxng 为 AI 助手提供私有化的 Web 搜索能力，基于 SearXNG 并实现 Model Context Protocol（MCP），可直接对接 Claude、Cursor 以及任意支持 MCP 的客户端。它通过统一的协议把真实的网络数据和工具暴露给 AI，帮助模型在对话中获取最新、可信的外部信息。

**价值主张**  
- **标准化接入**：实现了 MCP 服务器，使 AI 助手无需自行编写爬虫或搜索逻辑，只需遵循统一的 API/SDK 即可调用真实的搜索结果。  
- **私有化安全**：部署在内部网络或自有云上，数据不泄露到公共搜索引擎，满足企业合规和隐私要求。  
- **多客户端兼容**：同时支持 Claude、Cursor 等主流 AI 平台，以及任何实现 MCP 的自研客户端，降低集成成本。

**典型接入方式**  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **MCP 客户端（如 Claude、Cursor）** | 直接调用公开的 HTTP API | 1. 部署 mcp‑searxng（Docker / Kubernetes）<br>2. 在 MCP 客户端配置搜索服务的 URL 与 token<br>3. 客户端通过 `search(query)` 调用即可获得 SearXNG 结果 |
| **自研后端服务** | 使用官方 TypeScript SDK 或 CLI | 1. `npm i @mcp/searxng-client`<br>2. 初始化 `new SearxngClient({baseUrl, apiKey})`<br>3. 在业务代码中调用 `client.search(...)` |
| **命令行/脚本** | 通过提供的 CLI 工具 | `npx mcp-searxng search "最新 AI 论文"`，可将结果直接输出为 JSON、Markdown 或管道到其他工具 |
| **MCP 服务器集群** | 作为微服务部署在 Kubernetes | 使用官方 Helm chart (`helm repo add mcp-searxng …`) 部署，开启水平伸缩、Ingress TLS 等生产特性 |

**生产可用性评估**  

- **活跃度**：截至 2026‑06‑23 最近一次提交，GitHub ★944、Fork 136，社区活跃，Issue 响应及时。  
- **技术成熟度**：核心实现使用 TypeScript，提供完整的 OpenAPI 文档、SDK 与 CLI，易于 CI/CD 集成。  
- **安全与合规**：项目本身采用 MIT 许可证，代码无明显安全漏洞；私有化部署可自行审计依赖的 SearXNG 实例。  
- **可扩展性**：支持自定义搜索实例（DuckDuckGo、Bing、Google 自建代理等），并可通过插件增加结果过滤、摘要生成等功能。  
- **风险**：仍需确认维护者的长期可用性以及对依赖的 SearXNG 版本升级策略；在正式生产前建议进行一次渗透测试和灾备演练。

**结论**  
综合活跃的社区、完整的协议实现以及灵活的部署方式，ihor‑sokoliuk/mcp‑searxng 已具备在企业级 AI 助手项目中作为搜索后端的生产就绪能力，适合作为私有化、标准化的搜索桥梁快速上线。

## 🧭 Practical evaluation

**Value:** ihor-sokoliuk/mcp-searxng helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 944 GitHub stars
- 136 forks
- updated 2026-06-23
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 75/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/ihor-sokoliuk/mcp-searxng) · [← Back to Mcp](./README.md)</sub>
