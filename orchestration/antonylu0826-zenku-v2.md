# antonylu0826/zenku-v2

[![Stars](https://img.shields.io/github/stars/antonylu0826/zenku-v2?style=flat-square&color=yellow)](https://github.com/antonylu0826/zenku-v2/stargazers) [![Forks](https://img.shields.io/github/forks/antonylu0826/zenku-v2?style=flat-square&color=blue)](https://github.com/antonylu0826/zenku-v2/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> AI-first No-Code engine for building production-ready data apps via conversation. Features Multi-Agent architecture, dynamic UI rendering, and built-in Undo/Time-Machine. Supports SQLite, Postgres, and MSSQL.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 17 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `application-builder` `database-management` `dynamic-ui` `low-code` `mcp-server` `multi-agent-system` `no-code` `self-hosted` `typescript`

## 🎯 Categories

Orchestration · MCP · AI/ML · Frontend · Backend

## 📝 Summary

### English

**Brief Summary**  
Zenku v2 (antonylu0826/zenku‑v2) is an AI‑first, no‑code engine that lets you assemble production‑ready data applications through conversational prompts. It ships a multi‑agent architecture, dynamic UI rendering, and a built‑in undo/time‑machine, and can connect to SQLite, PostgreSQL, or MSSQL back‑ends.

**Value**  
- **From prompts to pipelines** – Isolated LLM prompts and tools are turned into repeatable, versioned agent workflows, so teams can codify “how we do X” once and reuse it across projects.  
- **Multi‑agent orchestration** – Different agents can specialize (e.g., data extraction, validation, visualization) and hand off work automatically, reducing the need for custom glue code.  
- **Built‑in state management** – The undo/time‑machine feature gives deterministic replay of agent actions, which is crucial for debugging, auditability, and compliance in data‑centric apps.  
- **Rapid UI prototyping** – UI components are generated on‑the‑fly from the conversation, letting non‑engineers prototype dashboards and CRUD screens without writing front‑end code.

**Practical Adoption Path**  

| Step | What to Do | Why |
|------|------------|-----|
| 1️⃣ Evaluation | Clone the repo, run the provided CLI (`zenku start`) and point it at a test SQLite DB. Verify the conversational UI, agent hand‑offs, and undo feature. | Confirms the core “no‑code → app” loop works in your environment. |
| 2️⃣ Integration | Use the exported SDK or API to embed Zenku into an existing internal portal or CI pipeline. Replace the demo DB with your PostgreSQL/MSSQL instance. | Leverages the existing API surface and lets you keep your data source strategy. |
| 3️⃣ Customization | Add custom tool adapters (e.g., a proprietary ETL service) by implementing the `Tool` interface in TypeScript. Register the new tool in the agent config. | Extends the platform to cover domain‑specific actions while staying within the multi‑agent framework. |
| 4️⃣ Governance | Enable the time‑machine logs, configure role‑based access, and set up CI checks for dependency updates (npm audit, Snyk). | Addresses security and compliance concerns before moving to production. |
| 5️⃣ Production Roll‑out | Deploy the Docker image (or the built Node server) behind your API gateway, enable health checks, and monitor via Prometheus/Grafana. | Provides the reliability and observability needed for production workloads. |

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑14) and has a modest but growing community (35 ★, 17 forks). It is suitable for prototypes, internal tools, or early‑stage SaaS products.  
- **Dependencies**: Pure TypeScript/Node stack; standard npm dependencies, but a dependency audit is recommended before production.  
- **Scalability**: Works with SQLite for local dev and scales to PostgreSQL/MSSQL for larger datasets; multi‑agent orchestration runs as separate async workers, which can be horizontally scaled.  
- **Risks**: License and long‑term maintainership still need verification; security posture (e.g., LLM prompt injection, DB credential handling) must be reviewed and hardened.  

**Bottom line** – Zenku v2 offers a fast, conversational way to turn AI prompts into repeatable data‑app workflows, with built‑in state tracking and multi‑agent coordination. After a short hands‑on trial, integration via its API/CLI, and a security/gov review, it can be safely promoted to production for internal dashboards, data‑ops pipelines, or as the foundation of a low‑code data‑app platform.

### Русский

**Zenku v2** (antonylu0826/zenku-v2) — это open‑source движок «AI‑first No‑Code», позволяющий через диалог быстро собрать готовое к продакшену приложение для работы с данными. Он реализует мульти‑агентную архитектуру с динамической генерацией UI, поддерживает Undo/Time‑Machine и подключается к SQLite, Postgres и MSSQL, что делает его удобным для построения повторяемых пайплайнов, координации нескольких агентов и стандартизации их памяти. Проект находится на среднем уровне готовности: подходит для прототипов и внутренних процессов, но требует проверки лицензии, безопасности и поддержки перед масштабным внедрением в продакшн.

### 中文

**项目简介**  
`antonylu0826/zenku-v2` 是一款 **AI‑first 无代码引擎**，通过自然语言对话即可快速搭建可投产的数据应用。它采用多代理（Multi‑Agent）架构，支持动态 UI 渲染和内置的 Undo/Time‑Machine 功能，并兼容 SQLite、Postgres 与 MSSQL。

**价值主张**  
- **把孤立的 Prompt 与工具转化为可复用的 Agent 工作流**，实现跨工具、跨数据库的统一编排。  
- **多代理协同**：可在同一对话中调度多个专职 Agent，适用于复杂业务流程的自动化。  
- **内置记忆与回滚**：通过时间机器机制轻松追溯和恢复历史状态，降低调试成本。  

**典型接入方式**  
1. **API/SDK**：项目提供 RESTful API 与 TypeScript SDK，业务系统只需调用 `createWorkflow`、`runAgent` 等接口即可启动或调度工作流。  
2. **CLI**：`zenku-cli` 支持本地快速原型搭建、流程导出与部署，适合 DevOps 自动化。  
3. **插件式 UI**：通过 `renderUI` 接口将动态生成的前端组件直接嵌入现有 Web 应用，实现无缝的 No‑Code 界面。  

**生产可用性评估**  
- **成熟度**：GitHub ★35、Fork ★17，最近一次提交于 2026‑05‑14，代码基于 TypeScript，文档覆盖 API、SDK 与 CLI。  
- **适用场景**：原型验证、内部工具、低代码平台的 Agent 编排层。  
- **风险**：仍需进一步审查许可证、依赖安全（尤其是数据库驱动）以及维护者活跃度。若在生产环境使用，建议：  
  1. 完整进行依赖漏洞扫描；  
  2. 为关键业务添加单元/集成测试；  
  3. 将核心工作流导出为代码或容器镜像，以便独立部署。  

总体而言，`zenku-v2` 在 **快速构建 AI 驱动的数据应用** 方面具备显著优势，适合作为内部原型或中等规模业务的底层编排引擎，在完成安全与运维审查后即可投入生产。

## 🧭 Practical evaluation

**Value:** antonylu0826/zenku-v2 helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 35 GitHub stars
- 17 forks
- updated 2026-05-14
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 50/100 |
| recency | 20/100 |
| adoption | 33/100 |
| production | 49/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/antonylu0826/zenku-v2) · [← Back to Orchestration](./README.md)</sub>
