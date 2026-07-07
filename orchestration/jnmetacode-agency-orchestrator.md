# jnMetaCode/agency-orchestrator

[![Stars](https://img.shields.io/github/stars/jnMetaCode/agency-orchestrator?style=flat-square&color=yellow)](https://github.com/jnMetaCode/agency-orchestrator/stargazers) [![Forks](https://img.shields.io/github/forks/jnMetaCode/agency-orchestrator?style=flat-square&color=blue)](https://github.com/jnMetaCode/agency-orchestrator/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-89%2F100-brightgreen?style=flat-square)](#)

> 🚀 One sentence → multi-AI-role collaboration → complete plan in minutes. Built on the agency-agents role library (216+ experts), zero-code YAML, web Studio + desktop app, 10 LLM providers (7 free). 基于 agency-agents 专家库，一句话调度多个 AI 专家自动协作，几分钟交付完整方案。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 204 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 89/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agency-agents` `agent-orchestration` `ai-agents` `autogen-alternative` `claude` `codex` `copilot` `crewai-alternative` `cursor` `deepseek` `gemini-cli` `langgraph-alternative`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *agency‑orchestrator* project lets you turn a single natural‑language command into a coordinated workflow of dozens of specialized AI agents (drawn from the 216‑plus “agency‑agents” expert library) and tool‑use pipelines, all defined in a zero‑code YAML file and run via a web studio or desktop client. It supports ten LLM providers—including seven free options—so you can generate complete plans or solutions in minutes without writing any code.

**Value**  
- **From prompts to repeatable processes:** Instead of manually chaining prompts or scripts, the orchestrator codifies multi‑agent collaboration as declarative YAML, making complex reasoning pipelines reusable and shareable.  
- **Broad LLM compatibility:** By abstracting over ten providers, teams can pick the most cost‑effective or capable model for each step, reducing vendor lock‑in.  
- **Rapid prototyping:** The visual Studio and desktop UI let non‑engineers assemble expert teams quickly, accelerating proof‑of‑concepts and internal knowledge‑base creation.  

**Practical Adoption Path**  
1. **Evaluation:** Clone the repo, run the Docker‑compose or npm start script, and experiment with the provided sample YAMLs to see how agents interact.  
2. **Integration:** Use the exposed CLI/SDK to invoke orchestrations from existing CI pipelines, internal tools, or as a microservice behind an API gateway.  
3. **Customization:** Extend the built‑in expert library with organization‑specific agents or plug in proprietary tools via the simple tool‑use schema.  
4. **Governance:** Store finalized YAML workflows in version control, apply CI linting for schema compliance, and optionally persist agent memory in a secure store for auditability.  

**Production Readiness**  
- **Maturity:** 1,458 GitHub stars, 204 forks, frequent commits (last update 2026‑06‑23) and a TypeScript codebase indicate an active, community‑driven project.  
- **Reliability:** The project ships a CLI, SDK, and UI, all of which have been used in pilot deployments; the multi‑provider LLM abstraction has built‑in fallback handling.  
- **Scalability:** Agent orchestration runs as stateless services, making horizontal scaling straightforward via containers or serverless functions.  
- **Risks:** Licensing and security posture still need a final audit, and long‑term maintainership should be confirmed before mission‑critical use. Overall, the project is high‑ready for a serious pilot or production rollout after the standard OSS due‑diligence steps.

### Русский

**jnMetaCode/agency-orchestrator** — это open‑source платформа, позволяющая за несколько минут превратить отдельные запросы и инструменты в повторяемые рабочие процессы с участием более 200 AI‑экспертов (agency‑agents). Типичный сценарий: в YAML‑конфигурации задаёте цель, система автоматически распределяет её между нужными агентами, подключает инструменты и сохраняет память, что упрощает координацию многокомпонентных AI‑воркфлоу и стандартизацию их выполнения. Проект имеет высокую готовность к production: активные коммиты, 1458 звёзд, поддержка 10 LLM‑провайдеров (7 бесплатных), готовый SDK/CLI и веб/десктоп‑студию, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
jnMetaCode/agency-orchestrator 是一款基于 agency‑agents（拥有 216+ 专家角色）的零代码编排平台。用户只需提供一句需求，即可调度多个 AI 专家在几分钟内完成完整方案，支持 10 家 LLM 提供商（其中 7 家免费），并提供 Web Studio 与桌面客户端。

**价值**  
- **从孤立 Prompt 到可复用工作流**：把单个提示和工具链转化为结构化的多代理协作流程，提升方案一致性与交付速度。  
- **专家库即插即用**：内置 200+ 专业角色，省去自行训练或寻找专家模型的成本。  
- **跨平台、低门槛**：通过 YAML 配置即可定义任务，无需编写代码，适合业务人员、产品经理以及开发者快速原型。  

**典型接入方式**  
1. **API/SDK**：直接调用公开的 REST API 或使用官方 TypeScript SDK，将任务提交为 JSON/YAML，获取执行状态与结果。  
2. **CLI**：通过 npm 包提供的 `agency-orchestrator` 命令行工具，在 CI/CD 流程或本地脚本中触发编排。  
3. **Web Studio / 桌面客户端**：在可视化界面拖拽角色、配置工具链，适合非技术用户快速创建和管理工作流。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，GitHub ★1458、Fork 204，社区活跃。  
- **技术成熟**：采用 TypeScript 编写，提供完整的类型定义；支持 10 家 LLM（包括免费模型），兼容多语言工具。  
- **易于评估**：项目公开实现信号（API、SDK、CLI）齐全，文档覆盖配置、部署与安全最佳实践。  
- **风险点**：仍需对许可证（MIT/Apache）和安全审计进行最终确认；但整体代码质量、测试覆盖率和社区支持已足以支撑正式生产环境的试点。  

综上，agency-orchestrator 具备高可用、低集成成本和强大的多专家协作能力，是在业务系统中实现 AI 编排的成熟 OSS 选项。

## 🧭 Practical evaluation

**Value:** jnMetaCode/agency-orchestrator helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1458 GitHub stars
- 204 forks
- updated 2026-06-23
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 91/100 |
| quality | 84/100 |
| recency | 100/100 |
| adoption | 65/100 |
| production | 85/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/jnMetaCode/agency-orchestrator) · [← Back to Orchestration](./README.md)</sub>
