# jordanlyall/wc26-mcp

[![Stars](https://img.shields.io/github/stars/jordanlyall/wc26-mcp?style=flat-square&color=yellow)](https://github.com/jordanlyall/wc26-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/jordanlyall/wc26-mcp?style=flat-square&color=blue)](https://github.com/jordanlyall/wc26-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> AI companion for FIFA World Cup 2026 — 18 tools covering matches, teams, venues, city guides, fan zones, visa info, head-to-head records, and more. Works with Claude, ChatGPT, Cursor, and Telegram.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 33 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `chatgpt` `claude` `fifa-2026` `football` `mcp` `mcp-server` `model-context-protocol` `npx` `soccer` `telegram-bot` `typescript`

## 🎯 Categories

MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
jordanlyall/wc26-mcp is an open‑source Model Context Protocol (MCP) server that equips AI assistants—Claude, ChatGPT, Cursor, Telegram bots, etc.—with 18 ready‑made tools for the FIFA World Cup 2026, ranging from match schedules and team stats to venue guides, visa information, and fan‑zone details. Built in TypeScript, the project provides a standardized API/SDK/CLI layer that lets developers hook any LLM into real‑world data without writing custom integrations.

**Value**  
- **Standardized integration**: By exposing a common MCP interface, the project removes the friction of building bespoke connectors for each data source, letting teams reuse the same protocol across different LLM providers.  
- **Rich, domain‑specific toolkit**: The 18 pre‑packaged tools cover the full fan‑experience lifecycle, so developers can instantly add useful World‑Cup knowledge to chatbots, virtual assistants, or internal automation pipelines.  
- **Multi‑model support**: Compatibility with Claude, ChatGPT, Cursor, and Telegram means the same backend can serve diverse AI products, reducing duplication of effort.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the TypeScript server locally (or via Docker), and call the MCP endpoints from a test LLM prompt to verify tool responses.  
2. **Integration** – Add the provided SDK/CLI to your existing AI‑agent codebase; map the desired MCP calls to your agent’s action‑selection logic.  
3. **Deployment** – Containerize the server, configure API keys for any external data feeds, and expose it behind an internal gateway.  
4. **Scale** – Monitor usage, add caching or rate‑limiting as needed, and optionally extend the toolset with additional World‑Cup data sources.

**Production Readiness**  
- **Maturity**: Medium. The repo has 33 stars, 9 forks, recent updates (June 2026), and a clear TypeScript codebase, making it suitable for prototypes or internal tools.  
- **Dependencies**: Relies on standard Node/TS packages; a review of third‑party libraries and licensing is advisable before production use.  
- **Maintainability**: Limited community activity and a small maintainer pool mean you should plan for in‑house support and regular security audits.  
- **Risk**: No major metadata issues, but the license, security posture, and long‑term maintainer commitment need final verification.  

Overall, wc26-mcp offers a compelling shortcut for teams wanting to embed World Cup‑specific intelligence into AI assistants, with a clear path from sandbox testing to production—provided the organization performs the usual due‑diligence on security and maintenance.

### Русский

**jordanlyall/wc26-mcp** — это открытая платформа, позволяющая подключать любые AI‑ассистенты (Claude, ChatGPT, Cursor, Telegram‑боты) к реальному набору 18 инструментов, охватывающих матчи, команды, стадионы, городские гиды, фан‑зоны, визовую информацию и статистику. Типичный сценарий: разработчик разворачивает Model Context Protocol сервер, регистрирует API/SDK/CLI‑интерфейсы проекта и сразу получает готовый мост между моделью и данными, что ускоряет прототипирование и внутренние автоматизированные воркфлоу. Готовность к продакшн — средняя: проект стабилен для прототипов и ограниченных сервисов, но перед масштабным запуском требуется проверка лицензии, безопасности и поддержки зависимостей.

### 中文

**项目简介**  
jordanlyall/wc26-mcp 是面向 2026 年 FIFA 世界杯的 AI 助手平台，提供 18 套工具（赛程、球队、场馆、城市指南、粉丝区、签证信息、交锋记录等），并通过统一的 Model Context Protocol 与 Claude、ChatGPT、Cursor、Telegram 等多种大模型和聊天渠道对接。

**价值**  
- **标准化接入**：通过统一协议将 AI 助手快速绑定真实业务工具和数据，降低每次集成的成本。  
- **多模态覆盖**：一次部署即可为赛事信息、旅行指南、签证办理等多场景提供即时查询和自动化处理。  
- **生态兼容**：兼容主流大模型和即时通讯平台，方便在已有 AI 流程中直接复用。

**典型接入方式**  
1. **API/SDK**：项目提供 TypeScript SDK 与 RESTful API，开发者可在 Node.js、前端或后端服务中直接调用。  
2. **CLI**：通过 npm 安装的命令行工具，可在 CI/CD 或脚本中快速触发特定工具（如查询赛程）。  
3. **模型插件**：在 Claude、ChatGPT 等模型的插件系统中注册对应的协议端点，使模型在对话中自动调用对应功能。  
4. **Telegram Bot**：直接部署提供的 Telegram Bot，实现用户在 Telegram 中查询世界杯相关信息。

**生产可用性评估**  
- **成熟度**：项目已有 33 ⭐、9 fork，最近一次提交在 2026‑06‑25，代码以 TypeScript 为主，结构清晰，适合原型和内部工作流。  
- **依赖与维护**：依赖较为常规（Node.js、Express），但仍需自行检查第三方库的安全漏洞并确认维护者的活跃度。  
- **适配性**：协议实现完整，提供 API/SDK/CLI 三种入口，接入门槛低；但在大规模生产环境下，需要自行做高可用、限流和监控等包装。  
- **总体结论**：**中等**（Medium）可用性——适合作为原型、内部工具或 MVP 上线；在正式生产前建议进行安全审计、容错设计以及对关键依赖进行版本锁定。

## 🧭 Practical evaluation

**Value:** jordanlyall/wc26-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 33 GitHub stars
- 9 forks
- updated 2026-06-25
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 30/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/jordanlyall/wc26-mcp) · [← Back to Mcp](./README.md)</sub>
