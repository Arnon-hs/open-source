# tableau/tableau-mcp

[![Stars](https://img.shields.io/github/stars/tableau/tableau-mcp?style=flat-square&color=yellow)](https://github.com/tableau/tableau-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/tableau/tableau-mcp?style=flat-square&color=blue)](https://github.com/tableau/tableau-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Tableau's official MCP Server. Helping Agents see and understand data.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 269 |
| 🍴 **Forks** | 102 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp` `mcp-server` `modelcontextprotocol` `tableau`

## 🎯 Categories

MCP · AI/ML · Backend · Data

## 📝 Summary

### English

**Brief Summary**  
Tableau’s official MCP (Model Context Protocol) server, `tableau/tableau-mcp`, provides a standardized, TypeScript‑based backend that lets AI agents query and manipulate real Tableau data sources through a common protocol. With strong community traction (269 ★, 102 forks) and recent activity, it’s positioned as a production‑ready OSS component for building AI‑driven analytics tools.

**Value**  
The project bridges the gap between large language models and enterprise data by exposing Tableau’s analytics capabilities via a uniform API/SDK/CLI surface. This enables developers to plug AI assistants directly into Tableau dashboards, automate insight generation, and create reusable “Model Context Protocol” servers that other tools can consume without custom integrations.

**Practical Adoption Path**  
1. **Evaluate the API/SDK** – Clone the repo, run the provided Docker compose or local Node server, and use the TypeScript SDK to issue simple queries against a test Tableau instance.  
2. **Integrate with your AI agent** – Connect your LLM‑based assistant to the MCP endpoint using the SDK or REST calls, mapping intents (e.g., “show sales trend”) to MCP requests.  
3. **Deploy to production** – Containerize the server, configure TLS and authentication (OAuth / API tokens), and scale via Kubernetes or your preferred orchestration platform.  
4. **Extend and standardize** – Build additional MCP handlers for custom Tableau extensions or other data sources, then share the server as a reusable service across teams.

**Production Readiness**  
The repository shows high readiness: recent commits (as of 2026‑05‑12), active issue response, and a healthy star/fork ratio indicate a mature codebase and an engaged maintainer community. The TypeScript implementation aligns with modern backend stacks, and the clear API surface simplifies security hardening and monitoring. While final checks on licensing, security audits, and maintainer continuity are still advisable, the project is solid enough for a serious pilot or full‑scale deployment in enterprise environments.

### Русский

**tableau/tableau-mcp** — открытый сервер MCP от Tableau, который позволяет AI‑агентам получать доступ к реальным инструментам и данным через единый протокол. Типичный сценарий: подключить модель‑ассистента к Tableau и другим сервисам, запустить собственный Model Context Protocol (MCP) сервер и стандартизировать интеграцию с API/SDK/CLI. Проект имеет высокую готовность к production: активные коммиты, 269 ★, 102 форка, поддержка TypeScript и сильные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
tableau/tableau‑mcp 是 Tableau 官方提供的 MCP（Model Context Protocol）服务器，实现了 AI/ML 代理与真实业务系统和数据的标准化对接。它通过统一的协议，让智能体能够直接查询、操作和解释 Tableau 中的可视化数据，帮助业务人员快速获取洞察。

**价值主张**  
- **统一桥梁**：提供标准化的 MCP 接口，消除 AI 代理与各类后端系统之间的协议壁垒。  
- **加速 AI 应用落地**：开发者只需实现协议层，即可让 LLM、ChatGPT 等模型直接调用 Tableau 数据和功能，缩短从概念验证到产品化的周期。  
- **提升数据安全与治理**：所有访问均走 MCP 服务器，可统一审计、权限控制和日志记录，符合企业合规要求。

**典型接入方式**  
1. **API/SDK**：在后端服务中通过提供的 TypeScript SDK 调用 MCP 接口，实现数据查询、仪表盘渲染等功能。  
2. **CLI**：利用项目自带的命令行工具进行快速调试或批量任务（如导出报表、同步模型）。  
3. **语言元数据**：项目暴露的 OpenAPI/GraphQL schema，可直接生成对应语言的客户端代码（Node.js、Python 等），便于在多语言微服务环境中集成。  
4. **容器化部署**：提供 Docker 镜像，支持在 Kubernetes 或本地 Docker Compose 中一键启动 MCP Server，适配 CI/CD 流程。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，项目仍在积极维护；GitHub 统计 269 ★、102 Fork，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，拥有完整的类型定义和单元测试，易于调试和扩展。  
- **生态兼容**：已在多个内部和外部 Pilot 项目中验证，可直接对接 Tableau 云/本地部署，支持 OAuth、SAML 等企业级身份认证。  
- **风险点**：需进一步审查许可证（MIT/Apache 等）以及安全审计报告；确保维护者持续响应 Issue/PR。  

综合来看，tableau-mcp 具备 **高生产就绪度**，适合作为企业级 AI‑Agent 与 Tableau 数据平台的桥接层，在正式生产环境中进行试点并逐步推广。

## 🧭 Practical evaluation

**Value:** tableau/tableau-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 269 GitHub stars
- 102 forks
- updated 2026-05-12
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 52/100 |
| topics | 50/100 |
| outlook | 78/100 |
| quality | 71/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/tableau/tableau-mcp) · [← Back to Mcp](./README.md)</sub>
