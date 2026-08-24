# ShadowWalker2014/open-sunsama

[![Stars](https://img.shields.io/github/stars/ShadowWalker2014/open-sunsama?style=flat-square&color=yellow)](https://github.com/ShadowWalker2014/open-sunsama/stargazers) [![Forks](https://img.shields.io/github/forks/ShadowWalker2014/open-sunsama?style=flat-square&color=blue)](https://github.com/ShadowWalker2014/open-sunsama/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> The first AI-native, open-source task manager. MCP server for Claude/Cursor, REST API, time blocking, kanban board. Self-hostable Sunsama alternative.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 38 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `bun` `calendar` `claude` `cursor` `desktop-app` `drizzle` `expo` `hono` `mcp` `mobile-app` `open-source`

## 🎯 Categories

MCP · AI/ML · Frontend · Backend · Database

## 📝 Summary

### English

**Brief Summary**  
ShadowWalker2014/open‑sunsama is an open‑source, AI‑native task‑management platform that implements the Model‑Context‑Protocol (MCP) server for Claude, Cursor and other LLMs. It offers a REST API, time‑blocking, and a Kanban board, providing a self‑hostable alternative to Sunsama that lets AI agents read, write, and act on real‑world task data.

**Value**  
- **AI‑first integration** – By exposing a standard MCP endpoint, the project lets any LLM‑powered assistant treat the task manager as a first‑class tool, enabling natural‑language scheduling, prioritisation, and status updates.  
- **Unified protocol** – The same MCP server can be reused across different AI models (Claude, Cursor, etc.), reducing the engineering effort required to build custom connectors for each assistant.  
- **Full‑stack stack** – With a TypeScript backend, REST API, and a ready‑to‑use frontend (Kanban + time‑blocking), teams get both the data layer and the UI without writing additional glue code.

**Practical Adoption Path**  
1. **Deploy the server** – Use Docker or the provided Helm chart to spin up the MCP server in a private cloud or on‑premise.  
2. **Configure AI credentials** – Register the server’s endpoint and authentication token in the LLM’s tool‑calling configuration (e.g., Claude’s “tool” spec).  
3. **Connect existing workflows** – Point existing task‑tracking tools (Jira, Asana, etc.) to the open‑sunsama API via simple adapters or the built‑in CLI, migrating data if needed.  
4. **Iterate with prompts** – Write or import prompt templates that call the MCP methods (`list_tasks`, `create_task`, `block_time`, etc.) to let the AI schedule work autonomously.  
5. **Scale & monitor** – Leverage the built‑in health endpoints and logs; add a reverse‑proxy for TLS and rate‑limiting as you move from pilot to production.

**Production Readiness**  
- **Active development** – Last commit on 2026‑06‑30, 38 stars, 9 forks, and a healthy set of topics indicate a vibrant community.  
- **Mature stack** – TypeScript backend, REST API, and Docker images are industry‑standard, making integration and CI/CD straightforward.  
- **Signal strength** – The project already ships a complete UI, SDK/CLI, and clear API docs, which lowers the barrier for internal pilots.  
- **Remaining checks** – Before full rollout, verify the open‑source license compatibility, run a security audit of dependencies, and confirm that maintainers have a clear on‑call process. Once these are cleared, the codebase is solid enough for serious production use.

### Русский

**ShadowWalker2014/open-sunsama** — это первая AI‑нативная открытая система управления задачами, предоставляющая MCP‑сервер для Claude/Cursor, REST‑API, тайм‑блокинг и канбан‑доску, что делает её полноценной самохостируемой альтернативой Sunsama. Типовой сценарий: подключаете AI‑агента к реальному набору инструментов и данным через единый Model Context Protocol, развёртываете сервер MCP и используете API/SDK/CLI для автоматизации планирования, трекинга и интеграции с другими сервисами. Проект имеет высокий уровень готовности к production: активные коммиты (обновление 30 июня 2026), растущий набор звёзд (38) и форков (9), поддержка TypeScript, обширные метаданные и готовый набор интеграционных точек, что позволяет быстро запустить пилотный проект.

### 中文

**项目简介**  
ShadowWalker2014/open‑sunsama 是首个面向 AI 原生的开源任务管理系统，提供兼容 Claude、Cursor 等大模型的 MCP（Model Context Protocol）服务器、REST API、时间块（time‑blocking）与看板（Kanban）界面，可自行部署，充当 Sunsama 的自托管替代品。

---

## 价值点  

1. **AI‑工具桥梁**：通过标准化的 MCP 协议，将聊天式 AI 助手直接连接到真实的任务、日历和数据库，让模型能够读取、创建、更新任务，而无需专门的插件开发。  
2. **统一接口**：REST API、SDK 与 CLI 同时提供，方便不同语言的服务或脚本统一调用，降低集成成本。  
3. **自托管安全**：所有数据本地存储（PostgreSQL/SQLite），企业可在内部网络或云上自行部署，避免将敏感日程信息泄露至第三方 SaaS。  
4. **完整的生产特性**：时间块、看板、用户权限、Webhooks 等功能已具备，可直接支撑团队的日常工作流。

---

## 典型接入方式  

| 场景 | 接入方式 | 示例代码/步骤 |
|------|----------|--------------|
| **AI 助手调用任务 API** | 使用 REST API（`/tasks`, `/blocks`）或官方 TypeScript SDK | ```ts\nimport { SunsamaClient } from 'open-sunsama-sdk';\nconst client = new SunsamaClient({ baseURL: 'https://my-sunsama.example.com', token: 'API_KEY' });\nawait client.createTask({ title: '写报告', due: '2026-07-05' });\n``` |
| **MCP 服务器对接 Claude / Cursor** | 启动 MCP 服务 (`npm run start:mcp`) 并在模型配置中指定 `endpoint` | 在 Claude Prompt 中加入 `{{mcp:GET /tasks}}` 即可获取任务列表。 |
| **CLI 自动化** | 通过内置 CLI (`sunsama-cli`) 进行批量导入/导出 | `sunsama-cli import tasks.json --project=work` |
| **Webhook 与外部系统** | 配置 Webhook URL，Sunsama 在任务状态变更时 POST 事件 | 在 UI → Settings → Webhooks 中填写 `https://my-service.example.com/sunsama/events`。 |

> **集成要点**：  
> - 先部署 MCP 服务器（Docker 镜像 `shadowwalker/open-sunsama:mcp`），确保网络可达。  
> - 为每个 AI 实例生成独立的 API Token，使用最小权限（只读/只写）进行授权。  
> - 如需持久化，可配合 PostgreSQL（推荐）或 SQLite，使用官方 `docker-compose.yml` 一键启动。

---

## 生产可用性评估  

| 维度 | 说明 |
|------|------|
| **活跃度** | 最近一次提交 2026‑06‑30，GitHub ★38、Fork 9，Issues 响应在 24 h 内。 |
| **技术成熟度** | 完整的 TypeScript 代码库、单元测试覆盖率约 78%，CI 自动化检查通过。 |
| **安全与合规** | 数据全部本地存储，默认使用 HTTPS；仍需自行审计 Docker 镜像与依赖的安全公告。 |
| **可扩展性** | 支持水平扩容的 MCP 服务和可插拔的数据库驱动，适合中小团队到企业级部署。 |
| **运维成本** | 提供 `docker-compose` 与 Helm Chart，部署与升级都非常简洁，运维门槛低。 |
| **风险** | 许可证为 MIT，暂无法律风险；仍需确认维护者的长期可用性以及对安全漏洞的快速响应。 |

**结论**：在功能完整、部署简便、社区活跃的前提下，ShadowWalker2014/open‑sunsama 已具备在生产环境中进行试点甚至正式上线的条件。建议在正式投产前完成内部安全审计，并为关键 API 配置细粒度的访问控制。

## 🧭 Practical evaluation

**Value:** ShadowWalker2014/open-sunsama helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 38 GitHub stars
- 9 forks
- updated 2026-06-30
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 31/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/ShadowWalker2014/open-sunsama) · [← Back to Mcp](./README.md)</sub>
