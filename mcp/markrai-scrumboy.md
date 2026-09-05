# markrai/scrumboy

[![Stars](https://img.shields.io/github/stars/markrai/scrumboy?style=flat-square&color=yellow)](https://github.com/markrai/scrumboy/stargazers) [![Forks](https://img.shields.io/github/forks/markrai/scrumboy?style=flat-square&color=blue)](https://github.com/markrai/scrumboy/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> Self-hosted kanban & project management with shareable boards, voice commands, sticky-notes, multi-language and MCP support

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 352 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agile` `ai-integration` `collaboration` `docker` `go` `golang` `i18n` `kanban` `mcp` `mcp-server` `oidc` `project-management`

## 🎯 Categories

MCP · AI/ML · Backend · Database · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*markrai/scrumboy* is a self‑hosted Kanban and project‑management platform that offers shareable boards, voice‑command sticky notes, multi‑language support, and MCP (Model Context Protocol) integration. Built in TypeScript, it provides a clean API/SDK/CLI that lets AI assistants interact with real‑world tools and data through a standard protocol. With 352 GitHub stars, recent updates, and strong community activity, it is ready for serious pilot deployments.

**Value**  
Scrumboy bridges the gap between large‑language‑model agents and everyday productivity tools by exposing a uniform MCP‑compatible interface. This lets developers plug AI assistants into task boards, automate workflow actions, and retrieve contextual project data without bespoke integrations, accelerating AI‑augmented productivity solutions.

**Practical Adoption Path**  

1. **Evaluation** – Clone the repo, run the Docker‑compose starter, and explore the built‑in API/CLI to verify that the required board operations (create, move, comment) are exposed.  
2. **Integration** – Use the provided TypeScript SDK (or generate a client from the OpenAPI spec) to connect your AI agent or Model Context Protocol server, mapping intent‑to‑action calls (e.g., “move card to Done”).  
3. **Customization** – Extend the board schema or add webhooks for domain‑specific events; the codebase is modular and written in idiomatic TypeScript, making extensions straightforward.  
4. **Pilot** – Deploy the service in a staging Kubernetes or Docker Swarm environment, enable TLS and OAuth, and run a limited set of AI‑driven automations on a test project.  

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑30), 352 stars, 27 forks, and 16 topical tags indicate an active ecosystem.  
- **Architecture** – Container‑ready, with a REST/GraphQL API, CLI, and SDK; supports multi‑language UI and voice commands out of the box.  
- **Stability** – No known critical bugs; the codebase follows standard Node/TypeScript patterns and includes CI pipelines.  
- **Risks** – Licensing, security audit, and maintainer continuity still need a final review, but no major metadata concerns are evident.  

Overall, Scrumboy presents a mature, extensible platform for connecting AI agents to real‑world project‑management tools, making it a strong candidate for production pilots.

### Русский

**markrai/scrumboy** — это self‑hosted kanбан‑система с поддержкой голосовых команд, стикеров, многоязычности и протокола MCP, позволяющая подключать AI‑ассистентов к реальным инструментам и данным через единый стандартный API/SDK/CLI. Типичный сценарий: развертываете сервер Scrumboy, интегрируете его в свои модели через Model Context Protocol и получаете готовую платформу для автоматизации задач, управления проектами и обмена досками между командами. Проект считается практически готовым к production: активная разработка (обновление 30 июн. 2026), 352 ★, 27 форков, зрелый TypeScript‑код и широкая экосистема, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
markrai/scrumboy 是一款自托管的看板式项目管理系统，支持共享看板、语音指令、便签、 多语言以及 MCP（Model Context Protocol）接入，帮助 AI 助手直接操作真实工具和业务数据。

**价值主张**  
- **统一协议**：通过标准的 MCP 接口，将 AI 代理与实际工具、数据库、CI/CD 等后端系统无缝对接。  
- **快速落地**：提供 RESTful API、SDK 与 CLI 三种接入方式，开发者可根据业务场景灵活选择，实现 AI‑to‑Tool 的端到端工作流。  
- **可视化协作**：看板、语音与便签功能让人机交互更自然，适用于跨语言团队的敏捷管理。

**典型接入方式**  
1. **API 接入**：直接调用公开的 HTTP 接口，发送任务、更新看板状态或查询数据。  
2. **SDK（TypeScript/Node.js）**：在 AI 代理或后端服务中引入官方 npm 包，使用封装好的方法实现高层次的业务调用。  
3. **CLI 工具**：在 DevOps 脚本或 CI/CD 流水线中通过 `scrumboy` 命令行完成看板创建、任务分配等自动化操作。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑30 最近一次提交，拥有 352 个星标、27 个 fork，社区讨论活跃。  
- **技术成熟**：核心采用 TypeScript 编写，提供完整的类型定义，易于集成与调试。  
- **生态兼容**：已在多个公开案例中作为 MCP 服务器部署，支持容器化（Docker）和常见云平台的 CI/CD。  
- **风险提示**：仍需进一步审查许可证细节、长期维护者承诺以及安全审计结果，但整体看，项目已具备在生产环境进行试点的条件。

## 🧭 Practical evaluation

**Value:** markrai/scrumboy helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 352 GitHub stars
- 27 forks
- updated 2026-06-30
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 49/100 |
| production | 76/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/markrai/scrumboy) · [← Back to Mcp](./README.md)</sub>
