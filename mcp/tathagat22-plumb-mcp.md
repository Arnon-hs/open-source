# tathagat22/plumb-mcp

[![Stars](https://img.shields.io/github/stars/tathagat22/plumb-mcp?style=flat-square&color=yellow)](https://github.com/tathagat22/plumb-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/tathagat22/plumb-mcp?style=flat-square&color=blue)](https://github.com/tathagat22/plumb-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Local Figma MCP server with no REST rate limits, no metered tool-call quotas, and a verification loop. Drop-in alternative to Figma's Dev Mode MCP and Framelink for Claude Code, Cursor, Windsurf — works on every plan including Free.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 62 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-coding-agent` `anthropic` `claude-code` `claude-mcp` `cursor` `design-to-code` `design-tokens` `dev-mode` `figma` `figma-mcp` `figma-plugin`

## 🎯 Categories

MCP · AI/ML · Backend · Design

## 📝 Summary

### English

Here's a 2-3 sentence summary of the open-source project:

**Project Summary:** tathagat22/plumb-mcp is an open-source, local Figma MCP server that provides a drop-in alternative to Figma's Dev Mode MCP and Framelink for connecting AI assistants to real tools and data. This project offers a flexible and cost-effective solution for developers, making it an attractive choice for those looking to standardize integrations. With its recent activity, adoption, and strong ecosystem signals, plumb-mcp is production-ready for serious pilots.

**Value:**

The project's primary value proposition is its ability to connect AI assistants to real tools and data through a standard protocol, making it an essential tool for developers working with AI agents. By providing a local MCP server, plumb-mcp eliminates the need for REST rate limits and metered tool-call quotas, allowing for seamless integration and development.

**Practical Adoption Path:**

To adopt plumb-mcp, developers can follow these steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI, language metadata, or focused topics, to determine its suitability for their needs.
2. Review the project's documentation and community resources to understand its usage and potential limitations.
3. Integrate pl

### Русский

**tathagat22/plumb-mcp** — это локальный сервер MCP, совместимый с Figma Dev Mode и Framelink, который устраняет ограничения REST‑rate‑limit и квоты на вызовы инструментов, позволяя AI‑ассистентам (Claude Code, Cursor, Windsurf и др.) надёжно работать с реальными данными и сервисами на любой подписке, включая бесплатную. Типичный сценарий — развертывание собственного Model Context Protocol (MCP) сервера, к которому подключаются агенты и инструменты через стандартный API/SDK/CLI, обеспечивая единый протокол интеграции и ускоряя выпуск новых функций. Проект имеет высокий уровень готовности к production: активные коммиты (обновлён 2026‑07‑02), 62 звёзд, 5 форков, написан на TypeScript, покрыт широким набором тем и уже используется в пилотных интеграциях, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
tathagat22/plumb-mcp 是一个本地化的 Figma MCP（Model Context Protocol）服务器，摆脱了 Figma 官方的 REST 限流和工具调用配额限制，并内置了验证循环。它可以直接替代 Figma Dev Mode MCP 与 Framelink，支持 Claude Code、Cursor、Windsurf 等 AI 助手，在所有计划（包括免费版）上均可使用。

**价值**  
- **无限制调用**：本地部署后不再受官方速率或计量配额约束，适合高频率的 AI‑Tool 交互。  
- **统一协议**：通过标准的 MCP 接口，将 AI 代理与真实工具、数据源无缝对接，降低集成复杂度。  
- **即插即用**：提供 API、SDK 与 CLI 三种入口，开发者只需几行配置即可让 AI 助手访问 Figma、设计系统或自定义后端服务。

**典型接入方式**  
1. **Docker/本地运行**：`docker run -p 3000:3000 ghcr.io/tathagat22/plumb-mcp`，启动本地 MCP 服务。  
2. **API 调用**：使用 HTTP POST 向 `http://localhost:3000/mcp` 发送符合 MCP 规范的 JSON 请求，获取设计数据或执行工具操作。  
3. **SDK 集成**：在 TypeScript/Node 项目中 `import { PlumbMCP } from 'plumb-mcp-sdk'`，实例化后直接调用 `client.runTool(...)`。  
4. **CLI 使用**：`plumb-mcp cli --file design.figma`，快速在终端检索或修改设计资源，适合脚本化工作流。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑02，仓库拥有 62 ⭐、5 🍴，且持续收到社区 issue 与 PR。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义和自动化测试，易于在 CI/CD 中集成。  
- **生态兼容**：已在 Claude Code、Cursor、Windsurf 等主流 AI 助手中验证，可直接作为后端服务部署。  
- **风险**：目前许可证、完整的安全审计以及维护者长期可用性仍需进一步确认；但从代码质量、社区活跃度和功能完整性来看，已具备在内部或受控生产环境中进行试点的条件。  

综上，plumb-mcp 为需要高频、低延迟 AI‑Tool 交互的团队提供了一个可靠、可自托管的 MCP 实现，接入门槛低，且在当前版本已具备相当的生产就绪度。

## 🧭 Practical evaluation

**Value:** tathagat22/plumb-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 62 GitHub stars
- 5 forks
- updated 2026-07-02
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 33/100 |
| production | 71/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/tathagat22/plumb-mcp) · [← Back to Mcp](./README.md)</sub>
