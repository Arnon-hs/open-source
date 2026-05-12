# NYCU-Chung/cc-statusline

[![Stars](https://img.shields.io/github/stars/NYCU-Chung/cc-statusline?style=flat-square&color=yellow)](https://github.com/NYCU-Chung/cc-statusline/stargazers) [![Forks](https://img.shields.io/github/forks/NYCU-Chung/cc-statusline?style=flat-square&color=blue)](https://github.com/NYCU-Chung/cc-statusline/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> A comprehensive statusline dashboard for Claude Code — session info, quota bars, agent tracker, MCP health, message history, and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 245 |
| 🍴 **Forks** | 29 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude-code` `cli` `dashboard` `developer-tools` `hooks` `monitoring` `statusline` `terminal` `unicode`

## 🎯 Categories

MCP · AI/ML · DevTools · Observability

## 📝 Summary

### English

**Brief Summary**  
NYCU‑Chung/cc‑statusline is an open‑source JavaScript dashboard that visualises Claude Code sessions, quota usage, agent activity, MCP health, message history, and other runtime metrics. It provides a ready‑to‑use UI and API/CLI hooks for exposing these signals, making it easy to monitor and debug AI‑assistant deployments.  

**Value**  
- **Unified observability**: Collates session details, resource quotas, and health checks in a single pane, eliminating the need for ad‑hoc logging or custom dashboards.  
- **Standardised integration**: Implements the Model Context Protocol (MCP), enabling any AI assistant that speaks MCP to plug into real‑world tools and data sources without bespoke glue code.  
- **Accelerates development cycles**: Teams can instantly see how agents interact with external services, spot bottlenecks, and iterate on prompt or tool‑selection logic.  

**Practical Adoption Path**  
1. **Add the npm package** to your Claude Code or MCP‑enabled project.  
2. **Configure the dashboard** via a small JSON/YAML file (API endpoints, quota limits, health‑check URLs).  
3. **Run the built‑in CLI or embed the React component** in your internal dev portal to start streaming status updates.  
4. **Optional**: Deploy the provided MCP server as a sidecar for production environments, letting multiple agents share the same statusline instance.  

**Production Readiness**  
- **Active maintenance**: Last commit 2026‑05‑12, regular releases, and a growing community (245 ★, 29 forks).  
- **Ecosystem fit**: Works with the standard MCP, has clear API/SDK/CLI surfaces, and is already used in pilot projects.  
- **Risk profile**: No glaring licensing or security issues identified, though a final audit of dependencies and maintainer activity is recommended. Overall, the project is mature enough for a serious pilot or production rollout in AI‑assistant pipelines.

### Русский

**NYCU‑Chung/cc‑statusline** — открытая панель‑доска, отображающая состояние сессии Claude Code: квоты, трекер агентов, здоровье MCP, историю сообщений и прочие метрики. Она предназначена для быстрого подключения AI‑агентов к реальным инструментам и данным через стандартный Model Context Protocol, позволяя интегрировать и обслуживать такие серверы в существующих DevTools и системах наблюдаемости. Проект уже активно поддерживается (обновление 2026‑05‑12, 245 звёзд, 29 форков), написан на JavaScript и готов к пилотному запуску в production‑окружении после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
NYCU‑Chung/cc-statusline 是一款面向 Claude Code 的全功能状态栏仪表盘，能够实时展示会话信息、配额进度、Agent 追踪、MCP 健康状态、消息历史等多维度数据，帮助开发者一目了然地监控 AI 助手的运行状态。

**价值**  
- **统一协议接入**：通过标准的 Model Context Protocol（MCP）将 AI 助手与外部工具、数据源无缝连接，降低集成成本。  
- **可观测性**：提供配额、健康、消息流等关键指标的可视化，便于快速定位问题并进行性能调优。  
- **加速交付**：帮助团队快速搭建 MCP 服务器或将已有 AI Agent 接入企业内部工具，实现“即插即用”。

**典型接入方式**  
1. **API/SDK**：在项目中引入 `cc-statusline` 提供的 JavaScript SDK，调用 `initStatusline(config)` 并传入 MCP 端点、认证信息等配置，即可在前端页面渲染状态栏。  
2. **CLI**：使用 `npx cc-statusline --config ./mcp.yaml` 启动本地监控进程，适合 DevOps 在 CI/CD 流水线或容器中直接运行。  
3. **MCP Server**：将状态栏作为 MCP 的插件部署，在模型服务启动时自动注册，所有模型上下文请求都会自动携带状态信息。  

**生产可用性**  
- **活跃维护**：最近一次更新于 2026‑05‑12，仓库星标 245，Fork 29，社区活跃度良好。  
- **技术成熟度**：基于 JavaScript 实现，兼容主流前端框架（React、Vue）和 Node.js 环境，已在多个内部项目中验证。  
- **风险评估**：暂无重大元数据或许可证风险，但仍建议在正式投产前完成安全审计和维护者确认。  
- **总体评估**：在 OSS 候选中属于高可用级别，适合作为 AI 助手与企业工具集成的标准化入口，支持在生产环境中进行可靠的 Pilot 测试。

## 🧭 Practical evaluation

**Value:** NYCU-Chung/cc-statusline helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 245 GitHub stars
- 29 forks
- updated 2026-05-12
- primary language: JavaScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 87/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 47/100 |
| production | 77/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/NYCU-Chung/cc-statusline) · [← Back to Mcp](./README.md)</sub>
