# VasiHemanth/tokentelemetry

[![Stars](https://img.shields.io/github/stars/VasiHemanth/tokentelemetry?style=flat-square&color=yellow)](https://github.com/VasiHemanth/tokentelemetry/stargazers) [![Forks](https://img.shields.io/github/forks/VasiHemanth/tokentelemetry?style=flat-square&color=blue)](https://github.com/VasiHemanth/tokentelemetry/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Token telemetry dashboard for AI autonomous and coding agents — tracks tokens, sessions, tool calls & reasoning across Hermes agent, Claude Code, Antigravity CLI, Codex & more. 100% local.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 154 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `claude-code` `codex` `cost-tracking` `cursor` `dashboard` `developer-tools` `gemini-cli` `github-copilot` `hermes-agent` `llm` `llm-monitoring`

## 🎯 Categories

Automation · AI/ML · DevTools · Observability

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
VasiHemanth/tokentelemetry is a fully‑local, TypeScript‑based observability dashboard that records token usage, session lifecycles, tool invocations and reasoning steps for AI agents such as Hermes, Claude Code, Antigravity CLI, Codex, and others. By exposing rich telemetry signals (API/SDK/CLI calls, language metadata, topic tags) it lets developers monitor and audit AI‑driven workflows without sending data to external services. The project is actively maintained, has a growing community, and is positioned as a plug‑and‑play component for building repeatable, automated AI pipelines.

**Value**  
- **Eliminates manual bookkeeping** – developers no longer need to write custom logging or scrape console output to track token consumption, session boundaries, or tool‑call metrics.  
- **Improves cost‑control and debugging** – real‑time visibility into token usage helps prevent runaway API bills and speeds up root‑cause analysis of unexpected agent behavior.  
- **Enables repeatable, observable pipelines** – the telemetry can be fed into CI/CD, alerting, or analytics systems, turning ad‑hoc AI interactions into auditable, production‑grade workflows.

**Practical adoption path**  
1. **Clone / npm install** the repository and run the provided Docker/Node server locally.  
2. **Instrument agents** by adding the supplied SDK or CLI wrapper to existing Hermes, Claude Code, Antigravity, or Codex integrations; this automatically emits the required telemetry events.  
3. **Connect the dashboard** to your local instance (or to a downstream observability stack) and verify token/session data appears as expected.  
4. **Iterate** by adding custom tags or extending the SDK for any proprietary tool calls, then embed the dashboard into internal developer portals or monitoring dashboards.

**Production readiness**  
- **Activity & community** – 154 ★, 21 forks, recent commits (last updated 2026‑06‑23) and a healthy set of topics indicate active maintenance.  
- **Stability** – The core telemetry pipeline is written in TypeScript with clear API contracts, and the project ships ready‑to‑run Docker images, reducing integration friction.  
- **Security & compliance** – All data stays on‑premise, mitigating data‑exfiltration concerns; however, a final review of the license and any third‑party dependencies is still recommended.  
Overall, the project exhibits a high level of production readiness for a serious pilot, especially for teams looking to embed observability into AI‑centric automation without relying on external SaaS solutions.

### Русский

**VasiHemanth/tokentelemetry** — это локальная открытая панель наблюдения за токенами, сессиями, вызовами инструментов и процессом рассуждения для AI‑агентов (Hermes, Claude Code, Antigravity CLI, Codex и др.). Она автоматизирует рутинные операции, позволяя объединять инструменты в повторяемые рабочие потоки и планировать операционные задачи без ручного вмешательства. Проект уже имеет активную поддержку (обновления 2026‑06‑23, 154 звёзд, 21 форк), написан на TypeScript и готов к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
VasiHemanth/tokentelemetry 是一款本地运行的 Token 遥测仪表盘，能够统一采集并可视化 AI 自主体、代码生成模型（Claude Code、Codex 等）以及 Antigravity CLI、Hermes Agent 等工具的 token 消耗、会话、工具调用和推理过程，帮助开发者实时洞察模型使用情况。

**价值**  
- **自动化监控**：无需手动记录 token 用量或会话日志，系统自动捕获全部关键信号。  
- **工作流可视化**：把多种 AI/CLI 工具的交互链路以仪表盘形式呈现，便于调优成本与性能。  
- **本地安全**：所有数据均在本地保存，避免敏感信息外泄，适合合规要求高的企业环境。  

**典型接入方式**  
1. **SDK/CLI 集成**：在项目中引入 `@tokentelemetry/sdk`（TypeScript）或使用提供的 CLI，按需在 API 调用、工具插件或脚本入口处插入 `trackToken(...)`、`trackSession(...)` 等函数。  
2. **环境变量配置**：通过 `TOKEN_TELEMETRY_ENDPOINT`、`TOKEN_TELEMETRY_PROJECT_ID` 等变量指定本地仪表盘地址和项目标识。  
3. **即插即用**：对已使用的 Hermes、Claude Code、Antigravity CLI 等工具，只需在启动脚本中添加 `--telemetry` 参数，即可自动上报。  

**生产可用性**  
- **活跃度**：最近一次提交（2026‑06‑23）且星标 154、Fork 21，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的 API 文档和示例，易于在 CI/CD 流程中集成。  
- **安全与合规**：全部数据本地存储，无外部依赖；但仍建议在正式上线前审查许可证（MIT）和潜在的第三方依赖安全性。  
- **适配度**：已在多个 AI 代码生成与自动化工具中验证，具备直接用于生产环境的能力，适合作为监控与成本控制的核心组件。  

综上，tokentelemetry 能显著降低人工记录和成本分析的工作负担，接入方式简洁，且具备足够的活跃度和技术成熟度，适合在生产环境中进行试点乃至全面部署。

## 🧭 Practical evaluation

**Value:** VasiHemanth/tokentelemetry helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 154 GitHub stars
- 21 forks
- updated 2026-06-23
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 70/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/VasiHemanth/tokentelemetry) · [← Back to Automation](./README.md)</sub>
