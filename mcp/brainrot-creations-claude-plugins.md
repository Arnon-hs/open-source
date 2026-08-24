# Brainrot-Creations/claude-plugins

[![Stars](https://img.shields.io/github/stars/Brainrot-Creations/claude-plugins?style=flat-square&color=yellow)](https://github.com/Brainrot-Creations/claude-plugins/stargazers) [![Forks](https://img.shields.io/github/forks/Brainrot-Creations/claude-plugins?style=flat-square&color=blue)](https://github.com/Brainrot-Creations/claude-plugins/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Official Claude Code plugin marketplace for Brainrot Creations

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `anthropic` `brainrot-creations` `browser-automation` `claude-code` `claude-code-plugin` `hive` `mcp` `model-context-protocol` `plugin-marketplace`

## 🎯 Categories

MCP · Automation · AI/ML

## 📝 Summary

### English

**Project Summary:**
Brainrot-Creations/claude-plugins is an open-source project that facilitates the connection of AI assistants to real tools and data through the Model Context Protocol (MCP). This plugin marketplace enables users to integrate AI agents with various tools and data sources, streamlining the automation process. With its standard protocol, users can easily connect their AI assistants to a wide range of applications.

**Value Proposition:**
The Brainrot-Creations/claude-plugins project offers a standardized way to integrate AI assistants with real tools and data, making it easier to automate tasks and workflows. By providing a common protocol, users can connect their AI agents to various tools and data sources, increasing the efficiency and productivity of their workflows.

**Practical Adoption Path:**
To adopt Brainrot-Creations/claude-plugins, users can start by evaluating the project's implementation signals, such as API/SDK/CLI, language metadata, or focused topics. They can then connect their AI agents to the plugin marketplace and start integrating with various tools and data sources. For a smooth adoption process, users should ensure they have a good understanding of the project's documentation and community support.

**Production Readiness:**
The production readiness of Brainrot-Creations/claude-plugins is medium, making

### Русский

**Brainrot‑Creations/claude-plugins** — открытый маркетплейс плагинов для Claude, позволяющий быстро подключать AI‑ассистентов к реальным инструментам и данным через единый протокол Model Context Protocol. Типичный сценарий — разработка прототипов или внутренних рабочих процессов, где требуется интеграция AI‑агентов с внешними API/SDK/CLI (например, автоматизация задач, доступ к фирменным сервисам). Готовность к production средняя: проект пригоден для прототипов, но перед развёртыванием в продакшн требуется проверка лицензии, безопасности и поддерживаемости зависимостей.

### 中文

**项目简介（2‑3 句）**  
Brainrot‑Creations/claude-plugins 是官方的 Claude Code 插件市场，提供一套统一的 Model Context Protocol（MCP），帮助开发者快速为 Claude AI 助手接入真实工具、服务和数据。通过该仓库，用户可以发布、发现并使用标准化的插件，实现 AI 与外部系统的无缝交互。

**价值**  
- **统一协议**：基于 MCP，消除不同插件之间的协议差异，降低集成成本。  
- **快速连接**：只需几行代码即可让 Claude 调用外部 API、CLI、SDK 等，实现“AI + 工具”的即插即用。  
- **生态共享**：插件以 marketplace 形式发布，社区可复用、二次开发，提升研发效率。

**典型接入方式**  
1. **API/SDK 接入**：在项目中引入 `@brainrot/claude-plugin-sdk`（JavaScript），使用 `registerPlugin()` 注册插件并提供 `execute()` 实现业务逻辑。  
2. **CLI/脚本调用**：通过仓库提供的 CLI (`claude-plugin-cli`) 直接在终端注册、调试插件，适合 CI/CD 或运维自动化场景。  
3. **MCP 服务器**：部署 `mcp-server`（Docker 镜像或 Node.js），作为统一的插件路由层，Claude 通过标准 HTTP 接口访问所有已注册插件。  

**生产可用性**  
- **成熟度**：当前评分 71/100，适合作为原型或内部工作流的实验平台。  
- **代码质量**：22 Stars、2 Forks，最近一次提交在 2026‑06‑27，使用 JavaScript，文档覆盖基本 API 与部署指南。  
- **风险与准备**：  
  - 需要进一步审查许可证、依赖安全（尤其是第三方 API 调用）以及维护者活跃度。  
  - 在生产环境部署前，建议进行安全审计、单元/集成测试，并对 MCP 服务器做高可用、限流与监控配置。  

综上，Brainrot‑Creations/claude-plugins 为 Claude AI 与外部工具的集成提供了便利的标准化入口，适合快速原型和内部系统集成；在完成安全与运维检查后，可逐步提升至生产使用。

## 🧭 Practical evaluation

**Value:** Brainrot-Creations/claude-plugins helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 2 forks
- updated 2026-06-27
- primary language: JavaScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 24/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Brainrot-Creations/claude-plugins) · [← Back to Mcp](./README.md)</sub>
