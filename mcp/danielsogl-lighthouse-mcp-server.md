# danielsogl/lighthouse-mcp-server

[![Stars](https://img.shields.io/github/stars/danielsogl/lighthouse-mcp-server?style=flat-square&color=yellow)](https://github.com/danielsogl/lighthouse-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/danielsogl/lighthouse-mcp-server?style=flat-square&color=blue)](https://github.com/danielsogl/lighthouse-mcp-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> MCP server that enables AI agents to perform comprehensive web audits using Google Lighthouse with 13+ tools for performance, accessibility, SEO, and security analysis.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 58 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`lighthouse` `lighthouse-audits` `lighthouse-score` `mcp` `mcp-server`

## 🎯 Categories

MCP · AI/ML · Backend · Database · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *lighthouse-mcp-server* is an open‑source Model Context Protocol (MCP) service that lets AI agents invoke Google Lighthouse to run full‑stack web audits—covering performance, accessibility, SEO, and security—through a standardized API. Built in TypeScript, it ships with a ready‑to‑use CLI/SDK and can be deployed as a lightweight backend that returns Lighthouse reports in a machine‑readable format. With active maintenance, 58 ⭐ on GitHub and recent updates, it’s a solid candidate for production pilots that need AI‑driven site quality checks.

**Value**  
- **Bridge AI and real tools** – By exposing Lighthouse via MCP, developers can let LLMs or autonomous agents call a trusted, industry‑standard audit engine without writing custom scraping or analysis code.  
- **One‑stop audit** – The server aggregates 13+ Lighthouse modules, delivering performance, accessibility, SEO, and security metrics in a single request, which simplifies pipelines that would otherwise stitch together multiple tools.  
- **Standardized integration** – Using MCP means the same request/response schema works across different AI platforms, reducing vendor lock‑in and accelerating the rollout of AI‑assisted observability features.

**Practical Adoption Path**  
1. **Run locally or in a container** – Clone the repo, install dependencies (`npm ci`), and start the server (`npm start`) or use the provided Dockerfile for isolated deployment.  
2. **Connect your AI agent** – Configure the agent’s tool‑calling module to point to the MCP endpoint (`/run-lighthouse`) and pass a URL payload; the server returns a JSON report that the agent can parse and act upon.  
3. **Scale as needed** – For higher throughput, deploy the service behind a load balancer or Kubernetes, optionally enabling caching of recent audit results to reduce duplicate runs.  
4. **Extend or customize** – Since the codebase is TypeScript, you can add custom Lighthouse plugins or additional output formats (e.g., HTML, CSV) without breaking the MCP contract.

**Production Readiness**  
- **Activity & Community** – Recent commit (2026‑05‑11), 58 stars, 10 forks, and active issue discussion indicate a healthy open‑source project.  
- **Stability** – The server follows a clear MCP schema, includes both CLI and SDK entry points, and has minimal external dependencies, making it easy to containerize and monitor.  
- **Security** – Lighthouse itself is maintained by Google; the server merely forwards URLs to it, but you should still enforce URL whitelisting and rate limiting to mitigate abuse.  
- **Maintainability** – Written in TypeScript with well‑defined interfaces, the codebase is approachable for teams familiar with Node.js.  

Overall, *lighthouse-mcp-server* offers a production‑grade, low‑friction way to empower AI agents with authoritative web‑audit capabilities, and it can be piloted quickly in any environment that supports Node/Docker.

### Русский

**danielsogl/lighthouse-mcp-server** — это open‑source MCP‑сервер на TypeScript, который через Model Context Protocol позволяет AI‑агентам запускать полные аудиты сайтов с помощью Google Lighthouse и более 13 встроенных инструментов для оценки производительности, доступности, SEO и безопасности. Типичный сценарий — подключить вашего чат‑бота или другую AI‑систему к реальному набору аналитических инструментов, используя единый API/SDK/CLI, что ускоряет разработку и стандартизирует интеграцию. Проект имеет высокий уровень готовности к production: активные коммиты, 58 звёзд, 10 форков, недавнее обновление (2026‑05‑11) и сильные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё рекомендуется.

### 中文

**项目简介**  
danielsogl/lighthouse-mcp-server 是一款基于 Model Context Protocol（MCP）的后端服务，能够让 AI 代理调用 Google Lighthouse 完成网页的性能、可访问性、SEO 与安全等 13 项以上的综合审计。

**价值**  
- **标准化接入**：通过 MCP 为 AI 助手提供统一的 API/SDK/CLI 接口，使它们可以像调用本地函数一样调用 Lighthouse，降低了 AI 与真实工具之间的集成成本。  
- **多维度质量洞察**：一次审计即可获得性能、可访问性、最佳实践、SEO 与安全等多维度指标，为 AI 驱动的自动化优化、监控和报告提供可靠数据来源。  
- **可复用的服务层**：作为独立的 MCP 服务器，可在不同项目、团队或云环境中复用，支持模型上下文的实时查询与结果返回。

**典型接入方式**  
1. **API 调用**：在 AI 模型的提示或函数调用中指定 MCP 方法（如 `lighthouse.runAudit(url)`），服务器返回 JSON 格式的审计报告。  
2. **SDK/CLI**：项目中引入 TypeScript/Node.js SDK 或直接使用提供的 CLI，适合批量审计或 CI/CD 流水线集成。  
3. **MCP 桥接**：将服务器注册到现有的 Model Context Protocol 生态（如 LangChain、OpenAI Function Calls），即可在任意支持 MCP 的大模型中直接使用。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑11，星标 58、fork 10，代码基于 TypeScript，维护频率稳定。  
- **生态兼容**：提供完整的 OpenAPI 文档、Docker 镜像以及 npm 包，易于在容器化或无服务器环境中部署。  
- **安全与合规**：项目本身不包含敏感数据，主要风险在于 Lighthouse 运行时的浏览器沙箱安全，需要在生产环境中做好容器隔离和资源限制。  
- **适配度**：已被多个开源 AI 框架用于实验性集成，具备“高”级别的生产候选（OSS‑candidate）资格，适合在内部 pilot 或面向客户的 SaaS 场景中直接使用。  

综上，danielsogl/lighthouse-mcp-server 为 AI 与真实网页审计工具之间搭建了可靠、标准化的桥梁，接入简便且具备足够的成熟度可用于生产环境。

## 🧭 Practical evaluation

**Value:** danielsogl/lighthouse-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 58 GitHub stars
- 10 forks
- updated 2026-05-11
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 38/100 |
| topics | 63/100 |
| outlook | 78/100 |
| quality | 65/100 |
| recency | 100/100 |
| adoption | 34/100 |
| production | 75/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/danielsogl/lighthouse-mcp-server) · [← Back to Mcp](./README.md)</sub>
