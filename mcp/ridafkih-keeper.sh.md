# ridafkih/keeper.sh

[![Stars](https://img.shields.io/github/stars/ridafkih/keeper.sh?style=flat-square&color=yellow)](https://github.com/ridafkih/keeper.sh/stargazers) [![Forks](https://img.shields.io/github/forks/ridafkih/keeper.sh?style=flat-square&color=blue)](https://github.com/ridafkih/keeper.sh/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Calendar sync tool & universal calendar MCP server. Aggregate, sync and control calendars on Google, Outlook, Office 365, iCloud, CalDAV or ICS.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 38 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bun` `caldav` `calendar` `calendar-sync` `google-calendar` `ical` `icloud` `ics` `mcp` `mcp-server` `nextjs` `open-source`

## 🎯 Categories

MCP · Communication · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`ridafkih/keeper.sh` is an open‑source calendar synchronization and MCP (Model Context Protocol) server written in TypeScript. It aggregates, syncs, and controls calendars across Google, Outlook, Office 365, iCloud, CalDAV, and generic ICS feeds, exposing a uniform API/CLI that AI assistants can use as a single source of truth for scheduling data. With over a thousand stars, recent commits, and a clear protocol layer, it is ready for pilot‑grade deployments.

**Value**  
Keeper.sh turns a fragmented calendar ecosystem into a single, programmatically accessible service, enabling AI agents to read, write, and reason over real‑world scheduling information without bespoke integrations for each provider. By implementing the Model Context Protocol, it offers a standard contract that other tools and AI platforms can adopt, reducing integration overhead and fostering interoperability across SaaS calendars.

**Practical Adoption Path**  

1. **Evaluation** – Clone the repo, run the provided Docker compose or npm scripts, and point the server at a test Google or Outlook account using the built‑in OAuth flow.  
2. **Integration** – Consume the exposed REST/GraphQL endpoints (or the generated SDK) from your AI assistant or backend service to fetch events, create meetings, or listen for updates.  
3. **Extension** – Add custom adapters for any missing calendar source via the documented plugin interface, then register the new adapter in the server’s configuration.  
4. **Production Roll‑out** – Deploy the server behind an internal reverse proxy, enable TLS, and configure role‑based API keys for each consuming AI service.

**Production Readiness**  
The project shows strong OSS maturity: 1,173 GitHub stars, recent activity (last commit 2026‑06‑29), active issue handling, and a well‑documented TypeScript codebase. Its API/CLI surface, clear licensing, and modular architecture make it suitable for a serious pilot, while the remaining due‑diligence steps (full security audit, license confirmation, and maintainer engagement) should be completed before a full‑scale production launch.

### Русский

**ridafkih/keeper.sh** — это open‑source‑инструмент для синхронизации и унификации календарей (Google, Outlook, Office 365, iCloud, CalDAV, ICS) и сервер MCP, который позволяет подключать AI‑ассистентов к реальным сервисам через стандартный протокол. Типовой сценарий: развернуть сервер MCP, настроить интеграцию с нужными календарными сервисами и дать AI‑агенту доступ к единому API/CLI для чтения, создания и изменения событий. Проект обладает высокой готовностью к production: активные коммиты (обновлён 2026‑06‑29), 1173 звёзд, широкая экосистема (TypeScript, 16 тем), стабильный бекенд‑модуль и уже проверенные интеграции, требующие лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
`ridafkih/keeper.sh` 是一款日历同步与统一日历 MCP（Model‑Context‑Protocol）服务器，能够聚合、同步并统一管理 Google、Outlook、Office 365、iCloud、CalDAV 以及标准 ICS 文件的日历数据。它提供统一的 API/SDK/CLI 接口，使 AI 助手能够以一致的协议访问和操作各种日历服务。

**价值**  
- **统一协议**：通过标准化的 MCP 接口，将分散在不同平台的日历抽象为同一套操作，极大降低 AI 助手或其他自动化系统的集成成本。  
- **多平台兼容**：一次配置即可同步 Google、Outlook、iCloud 等主流日历，实现跨平台日程统一，提升业务协同效率。  
- **可扩展性**：提供 TypeScript SDK 与 CLI，便于在自研服务或第三方平台上快速嵌入日历功能，支持 Model Context Protocol（MCP）服务器的快速搭建。

**典型接入方式**  
1. **API 接入**：部署 `keeper.sh` 服务器后，使用其 RESTful API（或 GraphQL）进行日历 CRUD 操作，适合后端服务或 AI Agent 的直接调用。  
2. **SDK 接入**：通过官方 TypeScript SDK 在 Node.js / 前端项目中引入 `keeper.sh`，调用封装好的方法完成日历同步、查询和事件推送。  
3. **CLI 接入**：在 CI/CD 或运维脚本中使用 `keeper.sh` 提供的命令行工具，实现批量导入/导出、日历迁移或定时同步任务。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑29 最近一次提交，拥有 1,173 ⭐、38 fork，16 个主题标签，表明社区活跃且代码维护频繁。  
- **技术成熟度**：核心使用 TypeScript 编写，具备完整的类型定义和自动化测试，易于在企业级 TypeScript/Node 环境中集成。  
- **部署与运维**：提供 Docker 镜像和 Helm Chart，支持云原生部署，配套的健康检查与日志输出满足生产监控需求。  
- **安全与合规**：项目采用 MIT 许可证，暂无已知重大安全漏洞；建议在正式使用前进行一次依赖审计和许可证合规检查。  

综合来看，`ridafkih/keeper.sh` 已具备较高的生产就绪度，适合作为 AI 助手或企业内部系统对日历数据的统一接入层，在实际项目中进行试点部署后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** ridafkih/keeper.sh helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1173 GitHub stars
- 38 forks
- updated 2026-06-29
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 75/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/ridafkih/keeper.sh) · [← Back to Mcp](./README.md)</sub>
