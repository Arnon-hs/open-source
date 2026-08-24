# project-nomos/nomos

[![Stars](https://img.shields.io/github/stars/project-nomos/nomos?style=flat-square&color=yellow)](https://github.com/project-nomos/nomos/stargazers) [![Forks](https://img.shields.io/github/forks/project-nomos/nomos?style=flat-square&color=blue)](https://github.com/project-nomos/nomos/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Your AI digital clone — learns who you are, acts on your behalf, remembers everything. Persistent vector memory, multi-agent teams, 60+ skills, smart model routing. Self-hosted, encrypted, multi-provider (Claude/Ollama/OpenRouter). Deploy to Slack, Discord, Telegram, WhatsApp & more in minutes.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `agent-skills` `agentic-ai` `ai-agents` `ai-assistant` `autonomous-agents` `claude` `claude-ai` `claude-code` `claude-skills` `digital-clone` `llm`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Nomos (project‑nomos/nomos) is a self‑hosted AI “digital twin” that learns a user’s preferences, retains a persistent vector memory, and can act autonomously across chat platforms (Slack, Discord, Telegram, WhatsApp, etc.). It stitches together large‑language‑model (LLM) providers (Claude, Ollama, OpenRouter) with a multi‑agent orchestration engine that offers 60+ built‑in skills, smart model routing, and encrypted storage, making it easy to turn ad‑hoc prompts into repeatable, memory‑backed workflows.

**Value Proposition**  
- **From isolated prompts to reusable agents** – Nomos captures context and tool‑use patterns in a vector store, so the same “knowledge” can be re‑invoked across sessions and teams.  
- **Multi‑agent teamwork** – Developers can compose agents that specialize (e.g., data extraction, summarisation, ticket routing) and let Nomos coordinate them automatically, dramatically reducing the glue‑code needed for complex pipelines.  
- **Provider‑agnostic and secure** – By abstracting over Claude, Ollama, OpenRouter, etc., teams can pick the most cost‑effective or privacy‑focused model while all data remains encrypted on‑premise.

**Practical Adoption Path**  
1. **Pilot Setup** – Clone the TypeScript repo, run the provided Docker compose file, and generate an API key. The out‑of‑the‑box CLI/SDK lets you spin up a test agent in minutes.  
2. **Connect a Channel** – Use the built‑in Slack/Discord/Telegram integration wizard to register a bot token; Nomos will automatically register the agent as a webhook endpoint.  
3. **Define Skills & Memory** – Add or enable any of the 60+ pre‑packaged skills (e.g., “search‑web”, “summarise‑pdf”) via the YAML‑based skill catalog, and configure a persistent vector store (e.g., Qdrant, Pinecone) for long‑term memory.  
4. **Iterate & Refine** – Leverage the smart model‑routing API to experiment with different LLM back‑ends, monitor token usage, and fine‑tune prompts using the built‑in telemetry dashboard.  
5. **Productionize** – Harden the deployment with TLS, RBAC, and secret management (Vault, Docker secrets). Add health checks and autoscaling rules to the orchestrator (Kubernetes or Docker Swarm) and integrate CI/CD pipelines for skill‑catalog updates.

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑06‑22), has 22 GitHub stars and a small but functional community. Core features (vector memory, multi‑agent orchestration, multi‑provider support) are usable for internal tools and prototypes.  
- **Dependencies** – Relies on external vector DBs and LLM APIs; you’ll need to audit version compatibility and licensing for each provider.  
- **Security** – Encryption is built‑in, but a formal security audit and review of the open‑source license are still required before exposing the service externally.  
- **Operational Overhead** – Requires container orchestration, secret management, and monitoring of LLM quota usage. Once those basics are in place, scaling to production workloads is straightforward.  

Overall, Nomos offers a compelling way to institutionalise AI‑driven workflows, with a clear path from a quick sandbox deployment to a hardened, production‑grade service—provided you perform the usual due‑diligence on security, licensing, and dependency management.

### Русский

**project‑nomos/nomos** — это open‑source платформа, превращающая разрозненные запросы и инструменты в повторяемые агентные воркфлоу: она хранит контекст в векторной памяти, объединяет несколько агентов с более чем 60 навыками и автоматически маршрутизирует запросы к лучшей модели (Claude, Ollama, OpenRouter). Типичный сценарий — быстрое развертывание в Slack, Discord, Telegram или WhatsApp, где несколько агентов совместно решают задачи, используют внешние инструменты и сохраняют историю взаимодействий. Готовность к production — средний уровень: проект уже стабильно работает в прототипах и внутренних процессах, но перед запуском в продакшн требуется проверка лицензии, безопасности и обеспечение поддержки зависимостей.

### 中文

**项目简介（2‑3 句）**  
project‑nomos/nomos 是一个自托管的 AI 数字克隆平台，能够通过持久化向量记忆和多代理团队为用户学习行为、代为行动并完整记忆交互。它提供 60 多种技能、智能模型路由以及对 Claude、Ollama、OpenRouter 等多家大模型的加密多供应商支持，可在几分钟内部署至 Slack、Discord、Telegram、WhatsApp 等主流渠道。

**价值**  
- **把碎片化 Prompt 与工具统一为可复用的工作流**，让团队可以像编排业务流程一样调度 AI 代理。  
- **持久记忆与多代理协作**，实现跨会话、跨渠道的上下文保持和复杂任务分解。  
- **多模型、多渠道、一键部署**，降低技术门槛，快速在内部或面向用户的产品中嵌入 AI 助手。

**典型接入方式**  
1. **API / SDK**：项目提供 RESTful API 与 TypeScript SDK，直接在现有业务代码中调用 `createAgent`, `runWorkflow` 等接口。  
2. **CLI**：通过 `nomos-cli` 可在本地或 CI/CD 环境快速创建、测试、部署工作流。  
3. **渠道插件**：内置 Slack、Discord、Telegram、WhatsApp 等 Bot 插件，只需配置对应的 webhook / token，即可把数字克隆挂载到聊天平台。  

**生产可用性**  
- **成熟度**：目前评分 71/100，适合作为原型或内部自动化工具使用；代码基于 TypeScript，结构清晰，易于二次开发。  
- **依赖与维护**：依赖大模型服务（Claude、Ollama、OpenRouter）以及向量数据库（如 Milvus/PGVector），需自行监控这些外部组件的可用性和费用。  
- **安全与合规**：提供端到端加密和自托管部署，适合对数据隐私有严格要求的场景，但仍需自行审查许可证（MIT）以及潜在的第三方库安全风险。  
- **运维准备**：建议在生产环境加入容器化部署（Docker/K8s），并配合健康检查、日志聚合和滚动更新，以降低单点故障风险。  

总体而言，project‑nomos/nomos 在 **快速搭建可复用的 AI 工作流** 方面表现突出，适合作为内部工具或面向特定用户的 AI 助手的技术基座；在正式上线前需完成依赖监控、容错设计以及安全审计。

## 🧭 Practical evaluation

**Value:** project-nomos/nomos helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 4 forks
- updated 2026-06-22
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 26/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/project-nomos/nomos) · [← Back to Orchestration](./README.md)</sub>
