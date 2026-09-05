# easecloudio/mcp-metabase-server

[![Stars](https://img.shields.io/github/stars/easecloudio/mcp-metabase-server?style=flat-square&color=yellow)](https://github.com/easecloudio/mcp-metabase-server/stargazers) [![Forks](https://img.shields.io/github/forks/easecloudio/mcp-metabase-server?style=flat-square&color=blue)](https://github.com/easecloudio/mcp-metabase-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> A comprehensive MCP server for Metabase with 70+ tools.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 75 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp` `mcp-server` `metabase`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **easecloudio/mcp‑metabase‑server** is a TypeScript‑based MCP (Model Context Protocol) server that wraps Metabase, exposing more than 70 ready‑to‑use tools and data queries through a uniform API. It enables AI assistants and other agents to invoke Metabase dashboards, reports, and data‑driven actions as if they were native functions, simplifying the bridge between large language models and enterprise analytics.  

**Value**  
- **Standardized Integration**: By speaking the MCP, developers can connect any AI agent to Metabase without writing custom connectors for each endpoint.  
- **Rich Toolset**: Over 70 pre‑built Metabase operations (queries, visualizations, alerts, etc.) accelerate the creation of data‑aware assistants.  
- **Rapid Prototyping**: The server abstracts authentication, query building, and result formatting, letting teams focus on the AI logic rather than low‑level API details.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the Docker compose (or npm start) against a test Metabase instance, and use the provided README examples to call a few MCP endpoints.  
2. **Integration Layer** – Wrap the MCP calls in your AI‑assistant framework (e.g., LangChain, AutoGPT) and map the desired tools to agent actions.  
3. **Security & Governance Review** – Verify licensing, add authentication/authorization (OAuth, API keys), and run static‑code/security scans.  
4. **Pilot Deployment** – Deploy the server in a staging environment, monitor latency and error rates, and iterate on tool selection.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑05‑14), has 75 stars and 20 forks, and its TypeScript codebase is relatively clean, making it suitable for prototypes and internal workflows.  
- **Considerations**: Before production use, perform a thorough security audit, confirm the license aligns with your organization’s policy, and establish a maintenance plan for dependency updates. With those checks in place, the server can serve as a reliable backbone for AI‑driven analytics services.

### Русский

**easecloudio/mcp-metabase-server** — это открытый MCP‑сервер для Metabase, включающий более 70 готовых инструментов и реализующий стандартный протокол Model Context Protocol, позволяющий быстро подключать AI‑ассистентов к реальным данным и сервисам. Типичный сценарий — запуск небольшого proof‑of‑concept: установить сервер, настроить соединение с Metabase и начать использовать готовые интеграции для автоматизации запросов и аналитики, а затем масштабировать решение до внутреннего или клиентского продукта. Готовность к production — средняя: проект подходит для прототипов и внутренних workflow, но перед выводом в продакшн требуется проверка лицензии, безопасности и стабильности зависимостей.

### 中文

**项目简介**  
easecloudio/mcp-metabase-server 是一套基于 Model Context Protocol（MCP）的完整 Metabase 后端实现，内置 70+ 常用工具，帮助 AI 助手通过统一协议安全、快速地访问真实的数据和业务功能。

**价值体现**  
- **标准化接口**：使用 MCP 统一协议，AI 代理无需了解具体 API 即可调用 Metabase 的查询、仪表盘、报表等功能。  
- **快速集成**：提供即插即用的 TypeScript 服务器，降低将 AI 与业务数据对接的开发成本。  
- **可扩展工具库**：自带 70 多个预置工具（查询、导出、通知等），满足大多数企业内部工作流的需求。

**典型接入方式**  
1. **阅读 README**，确认运行环境（Node.js、TypeScript）并完成依赖安装。  
2. **启动本地实例**（`npm run start`），通过配置文件指向已有的 Metabase 实例和数据库。  
3. **在 AI 助手侧**，使用 MCP 客户端库（如 `@mcp/client`）连接到该服务器，按协议调用所需工具即可。  
4. **小规模 PoC**：先在测试环境中调用几个关键工具（如 `query_dashboard`），验证数据返回与权限控制，随后逐步扩展到完整工作流。

**生产可用性**  
- **成熟度**：当前评分 66/100，GitHub 75 星、20 Fork，活跃更新至 2026‑05‑14，代码以 TypeScript 编写，结构清晰。  
- **适用场景**：适合原型开发、内部业务自动化或作为 MCP 生态的参考实现；在正式投产前建议进行：  
  - 依赖安全审计（第三方库的许可证与漏洞扫描）  
  - 性能压测（并发查询、超时控制）  
  - 运维监控（日志、健康检查）  
- **总体评估**：**中等**（Medium）——可在内部或受控环境中投入使用，完成上述检查后即可考虑在生产环境部署。

## 🧭 Practical evaluation

**Value:** easecloudio/mcp-metabase-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 75 GitHub stars
- 20 forks
- updated 2026-05-14
- primary language: TypeScript
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 40/100 |
| topics | 38/100 |
| outlook | 66/100 |
| quality | 58/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 66/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/easecloudio/mcp-metabase-server) · [← Back to Mcp](./README.md)</sub>
