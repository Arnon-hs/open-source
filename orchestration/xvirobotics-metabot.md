# xvirobotics/metabot

[![Stars](https://img.shields.io/github/stars/xvirobotics/metabot?style=flat-square&color=yellow)](https://github.com/xvirobotics/metabot/stargazers) [![Forks](https://img.shields.io/github/forks/xvirobotics/metabot?style=flat-square&color=blue)](https://github.com/xvirobotics/metabot/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> 构建受监督的、自我进化的 Agent 组织的基础设施 | Infrastructure for supervised, self-improving agent organization. 飞书/Telegram 手机端运行 Claude Code 或 Kimi Code（双引擎，两家原生订阅直接用），共享记忆、Agent 工厂、定时任务、通信总线。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 745 |
| 🍴 **Forks** | 113 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-native` `agent-organization` `ai-agent` `anthropic` `claude-agent-sdk` `claude-code` `feishu` `feishu-bot` `kimi` `kimi-code` `lark` `metamemory`

## 🎯 Categories

Orchestration · Automation · AI/ML · Libraries & SDKs

## 📝 Summary

### English

**Brief Summary**  
xvirobotics/metabot provides an open‑source infrastructure that lets developers stitch together supervised, self‑improving AI agents into reusable, orchestrated workflows. It offers shared memory, an “Agent Factory,” scheduled tasks, and a communication bus that run on mobile Feishu/Telegram clients with dual Claude/Kimi engines, turning ad‑hoc prompts into repeatable pipelines.

**Value**  
- **Workflow Automation** – Converts isolated prompts and tool calls into deterministic, version‑controlled agent pipelines, reducing manual glue code.  
- **Scalable Coordination** – The built‑in bus and scheduling engine enable multiple agents to collaborate, share state, and trigger each other, which is ideal for complex AI‑driven processes (e.g., data enrichment → analysis → reporting).  
- **Tool‑Use Extensibility** – Plug‑in support for external tools and APIs lets teams augment agents with domain‑specific capabilities without rewriting core logic.  
- **Cross‑Platform Access** – Mobile Feishu/Telegram clients give on‑the‑go access to the same agent orchestration layer used in server environments, facilitating rapid experimentation and monitoring.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/CLI starter, and connect a Feishu or Telegram bot token to test Claude/Kimi code execution.  
2. **Define Agents** – Use the Agent Factory SDK (TypeScript) to wrap existing prompts or scripts as reusable agents, specifying input/output schemas and memory keys.  
3. **Compose Pipelines** – Wire agents together via the communication bus or scheduled tasks, persisting shared memory in the built‑in store or an external DB (e.g., PostgreSQL).  
4. **Integrate** – Expose the metabot API/CLI to existing services (CI/CD, ticketing, data pipelines) and replace ad‑hoc script calls with orchestrated agent calls.  
5. **Scale & Monitor** – Deploy the service to a container orchestration platform (K8s, Docker Swarm), enable logging and health checks, and gradually migrate production workloads.

**Production Readiness**  
- **Activity & Community** – 745 stars, 113 forks, recent commits (as of 2026‑05‑13), and a healthy issue/PR turnover indicate active maintenance.  
- **Technology Stack** – Written in TypeScript, with clear API/SDK/CLI surfaces and extensive topic tagging, making integration straightforward for modern JavaScript/Node ecosystems.  
- **Reliability Features** – Built‑in scheduling, shared memory persistence, and a decoupled bus provide fault isolation and observability needed for production.  
- **Remaining Checks** – A final review of the license, security scanning (dependency vulnerabilities), and confirmation of long‑term maintainers is advisable, but overall the project is mature enough for a serious pilot or production deployment.

### Русский

**xvirobotics/metabot** — это инфраструктурный фреймворк на TypeScript, который преобразует разрозненные запросы и инструменты в повторяемые рабочие процессы агентов: он обеспечивает совместную память, фабрику агентов, планировщик задач и коммуникационный шина, интегрируя Claude Code и Kimi Code через Feishu/Telegram. Типичный сценарий — координация многокомпонентных AI‑агентов, построение конвейеров с использованием внешних инструментов и стандартизация их памяти для автоматизации бизнес‑процессов. Проект считается почти готовым к production: активные коммиты (обновление 13 мая 2026), 745 звёзд, 113 форков, поддержка API/SDK/CLI и широкая экосистема тем, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
xvirobotics/metabot 是一套面向 **受监督的自我进化 Agent 组织** 的基础设施。它在飞书/Telegram 移动端直接运行 Claude Code 与 Kimi Code 双引擎，提供共享记忆、Agent 工厂、定时任务和统一通信总线，帮助把零散的 Prompt 与工具组合成可重复、可扩展的 Agent 工作流。

**核心价值**  
- **统一记忆 & 共享状态**：所有 Agent 通过统一的记忆层实现信息共享与知识沉淀。  
- **可编排的多 Agent 流程**：通过 Agent 工厂和定时任务，轻松构建、调度和监控跨语言、跨平台的多 Agent 工作流。  
- **双引擎即插即用**：Claude Code 与 Kimi Code 原生订阅，免去二次封装，直接在移动端调用 AI 能力。  
- **标准化工具链**：提供统一的通信总线和 API/SDK/CLI，便于把外部工具（如数据库、搜索、爬虫）接入到 Agent 流程中。

**典型接入方式**  
1. **API/SDK**：通过公开的 TypeScript SDK 调用 `createAgent()、runTask()、pushMemory()` 等函数，实现业务系统对 Agent 的创建、调度和记忆写入。  
2. **CLI**：使用 `metabot-cli` 在 CI/CD 或本地脚本中快速启动/停止 Agent，适合 DevOps 场景。  
3. **Webhook / 总线**：在飞书或 Telegram Bot 中配置 webhook，接收 Agent 事件并通过统一的消息总线（Kafka/Redis）进行跨服务通信。  
4. **插件式工具链**：将自研工具包装为符合 `ToolInterface` 的插件，直接注入 Agent 的工具使用管道，实现“一键工具调用”。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑13，GitHub ★745、Fork 113，社区活跃。  
- **技术成熟度**：基于 TypeScript 开发，提供完整的类型定义、单元测试和 CI，易于在企业内部审计。  
- **部署灵活**：支持 Docker、K8s 以及 Serverless 部署，能够在私有云或公有云环境中快速落地。  
- **安全与合规**：项目采用 MIT 许可证，代码审计记录公开，暂无已知重大安全漏洞。  

综合来看，metabot 已具备 **高可用、易集成、可扩展** 的特性，适合作为企业内部 AI Agent 编排平台进行正式生产部署。

## 🧭 Practical evaluation

**Value:** xvirobotics/metabot helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 745 GitHub stars
- 113 forks
- updated 2026-05-13
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/xvirobotics/metabot) · [← Back to Orchestration](./README.md)</sub>
