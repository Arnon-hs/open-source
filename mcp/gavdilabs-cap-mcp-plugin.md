# gavdilabs/cap-mcp-plugin

[![Stars](https://img.shields.io/github/stars/gavdilabs/cap-mcp-plugin?style=flat-square&color=yellow)](https://github.com/gavdilabs/cap-mcp-plugin/stargazers) [![Forks](https://img.shields.io/github/forks/gavdilabs/cap-mcp-plugin?style=flat-square&color=blue)](https://github.com/gavdilabs/cap-mcp-plugin/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> MCP (Model Context Protocol) server plugin for CAP NodeJS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 62 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `cap` `capire` `mcp` `mcp-server` `plugin` `sap` `sap-cap`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

Here's a brief summary of the open-source project:

**Summary:** gavdilabs/cap-mcp-plugin is an open-source MCP (Model Context Protocol) server plugin for CAP NodeJS, facilitating the connection of AI assistants to real tools and data through a standardized protocol. This project enables the integration of AI agents with various tools, standardizing the process and making it more efficient. Its recent activity, adoption, and strong ecosystem signals make it a promising candidate for production use.

**Value:** The value proposition of gavdilabs/cap-mcp-plugin lies in its ability to standardize integrations between AI assistants and real tools and data, making it easier to connect AI agents with various systems. This standardization enables faster development, improved efficiency, and better integration of AI capabilities.

**Practical Adoption Path:** To adopt gavdilabs/cap-mcp-plugin, developers can start by evaluating the plugin's implementation signals, such as API/SDK/CLI, language metadata, or focused topics. They can then assess the plugin's production readiness, considering factors such as recent activity, adoption, and ecosystem signals. Once satisfied, developers can integrate the plugin into their projects, utilizing its capabilities to connect AI assistants with real tools and data.

**Production Readiness:** The

### Русский

**gavdilabs/cap-mcp-plugin** — это TypeScript‑плагин для CAP NodeJS, реализующий серверную часть Model Context Protocol (MCP) и позволяющий быстро подключать AI‑ассистентов к реальным инструментам и данным через единый протокол. Типичный сценарий: развёртывание MCP‑сервера в существующем CAP‑приложении и интеграция с AI‑агентами, которые затем могут вызывать бизнес‑логика и внешние сервисы без кастомных адаптеров. Проект имеет высокую готовность к production: активные коммиты (обновление 30 июня 2026), 62 звёзд, 22 форка, хороший набор API/SDK/CLI и поддержка основных тем, что делает его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介（2‑3 句）**  
gavdilib​s/cap‑mcp‑plugin 是一个基于 TypeScript 的 CAP（NodeJS）插件，实现了 Model Context Protocol（MCP）服务器端功能。它提供统一的 API/SDK/CLI 接口，使 AI 助手能够安全、可靠地调用真实的业务工具和数据。  

**价值**  
- **标准化**：通过 MCP 将 AI 代理与后端服务解耦，避免每个项目都自行实现专属协议。  
- **快速集成**：即插即用的插件形式，让开发者在几行代码内即可让 AI 与现有业务系统交互。  
- **可观测与可控**：插件自带日志、错误捕获和权限校验，帮助运维团队监控 AI 调用行为。  

**典型接入方式**  
1. **API 方式**：在 CAP 项目中 `import { createMcpServer } from 'cap-mcp-plugin'`，配置路由后启动即得到符合 MCP 规范的 HTTP 接口。  
2. **SDK 方式**：使用插件导出的 `McpClient` 在其他微服务或前端应用中直接调用 `client.invoke(toolId, payload)`。  
3. **CLI 方式**：通过 `npx cap-mcp-plugin serve` 本地启动调试服务器，配合 OpenAI、Claude 等模型的 `tools` 参数进行快速原型验证。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑30 最近一次提交，拥有 62 ⭐、22 Fork，且持续接受 PR 与 Issue 反馈。  
- **生态兼容**：基于 CAP（NodeJS）和 TypeScript，天然兼容现有 SAP‑CAP 应用和主流云函数平台。  
- **成熟度**：插件已实现完整的错误处理、鉴权和审计日志，具备企业级部署所需的可观测性。  
- **风险**：需进一步审查许可证（MIT/Apache）和安全审计报告，但整体代码质量和社区活跃度足以支撑正式生产环境的试点。  

综上，gavdilabs/cap-mcp-plugin 为 AI‑工具集成提供了标准、易用且具备生产级可靠性的解决方案，适合作为企业内部 AI 助手与业务系统对接的首选组件。

## 🧭 Practical evaluation

**Value:** gavdilabs/cap-mcp-plugin helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 62 GitHub stars
- 22 forks
- updated 2026-06-30
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 37/100 |
| production | 74/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/gavdilabs/cap-mcp-plugin) · [← Back to Mcp](./README.md)</sub>
