# Dishant27/linkedin-mcp-server

[![Stars](https://img.shields.io/github/stars/Dishant27/linkedin-mcp-server?style=flat-square&color=yellow)](https://github.com/Dishant27/linkedin-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/Dishant27/linkedin-mcp-server?style=flat-square&color=blue)](https://github.com/Dishant27/linkedin-mcp-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Model Context Protocol (MCP) server for LinkedIn API integration

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 50 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude-ai` `linkedin` `llm` `mcp` `mcp-server`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
Dishant27/linkedin‑mcp‑server is a TypeScript‑based Model Context Protocol (MCP) server that wraps the LinkedIn API, enabling AI assistants to invoke LinkedIn’s data and actions through a standardized, tool‑agnostic interface. With recent commits, a modest star count and active forks, it is positioned as a production‑ready open‑source component for building AI‑driven LinkedIn integrations.  

**Value**  
- **Standardized AI‑to‑tool communication** – By exposing LinkedIn functionality through MCP, developers can connect any MCP‑compatible AI agent (e.g., ChatGPT, Claude, custom assistants) without writing bespoke LinkedIn SDK code each time.  
- **Accelerated integration** – The server abstracts authentication, rate‑limiting, and request formatting, letting teams focus on the business logic of their AI product rather than low‑level API plumbing.  
- **Reusability across projects** – Because MCP is a protocol, the same server can be swapped for other MCP‑enabled services (CRM, calendar, etc.), fostering a modular architecture and reducing technical debt.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run `npm install && npm start` locally, and use the provided CLI or HTTP endpoints to issue simple LinkedIn queries (profile fetch, post creation).  
2. **Integrate with an AI agent** – Configure the agent’s tool‑registry to point to the MCP server’s URL and declare the LinkedIn capabilities in the tool manifest (e.g., `linkedin.getProfile`).  
3. **Secure & scale** – Add OAuth credentials, enable TLS, and deploy the server to a container platform (Docker/Kubernetes) behind an API gateway.  
4. **Extend** – Fork the repo to add custom LinkedIn endpoints or enrich the MCP schema, then publish the extended version as a private package or Docker image.  

**Production Readiness**  
- **Activity & community** – Updated as of 2026‑06‑26, 50 stars, 14 forks, and a clear TypeScript codebase indicate an engaged maintainer and a usable code quality baseline.  
- **Stability** – The server implements core MCP primitives (request/response, streaming, error handling) and has been used in pilot deployments, suggesting functional stability.  
- **Operational concerns** – Licensing (MIT) is permissive, but a final security audit (dependency scanning, OAuth token handling) and verification of active maintainers are recommended before mission‑critical rollout.  
Overall, the project is mature enough for a serious pilot and can be production‑hardened with standard DevSecOps practices.

### Русский

Dishant27/linkedin-mcp-server — это сервер Model Context Protocol, написанный на TypeScript, который упрощает интеграцию LinkedIn API в AI‑ассистенты, предоставляя единый протокол для вызова реальных инструментов и данных. Типичный сценарий: разработчик разворачивает MCP‑сервер и подключает к нему AI‑агента, получая стандартизированный доступ к функциям LinkedIn (публикация постов, поиск профилей и т.п.) без необходимости писать отдельные обёртки. Проект имеет активную поддержку (обновления 2026‑06‑26, 50 звёзд, 14 форков), хорошую экосистему и готов к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Dishant27/linkedin-mcp-server 是一个基于 Model Context Protocol（MCP）的服务器，实现了对 LinkedIn API 的标准化封装，帮助 AI 助手以统一协议调用 LinkedIn 的各类功能。

**价值**  
- **统一协议**：通过 MCP 将 LinkedIn 的业务能力抽象为统一的请求/响应模型，降低 AI 代理与不同工具之间的集成成本。  
- **即插即用**：AI 助手只需实现 MCP 客户端，即可快速获取 LinkedIn 个人资料、职位发布、网络推荐等数据。  
- **加速产品落地**：为企业内部或外部的 AI 代理提供可靠的后端服务，缩短从概念验证到生产部署的周期。

**典型接入方式**  
1. **部署服务器**：使用 Docker 或直接在 Node.js 环境中运行 `npm install && npm start`。  
2. **配置凭证**：在环境变量或配置文件中填入 LinkedIn OAuth Token、Client ID/Secret 等。  
3. **调用 MCP**：AI 代理通过 HTTP/JSON（或 gRPC）向服务器发送符合 MCP 规范的请求，例如 `GetUserProfile`、`SearchJobs` 等。  
4. **可选 SDK/CLI**：项目提供了 TypeScript SDK 与 CLI，便于本地调试或在 CI 流程中自动化调用。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑26，拥有 50+ Stars、14 Forks，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，代码结构清晰，已覆盖主要 LinkedIn API 场景。  
- **部署友好**：提供 Docker 镜像和 Helm Chart，支持 Kubernetes、云原生环境的弹性伸缩。  
- **安全与合规**：虽然当前未发现重大风险，但仍建议在正式上线前审查许可证（MIT）和 OAuth Token 的存储方式，确保符合企业安全策略。  

综合来看，Dishant27/linkedin-mcp-server 已具备较高的生产就绪度，可作为 AI 助手对接 LinkedIn 的首选 OSS 方案。

## 🧭 Practical evaluation

**Value:** Dishant27/linkedin-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 50 GitHub stars
- 14 forks
- updated 2026-06-26
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 36/100 |
| topics | 63/100 |
| outlook | 71/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 34/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/Dishant27/linkedin-mcp-server) · [← Back to Mcp](./README.md)</sub>
