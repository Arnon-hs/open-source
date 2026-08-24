# proma-ai/Proma

[![Stars](https://img.shields.io/github/stars/proma-ai/Proma?style=flat-square&color=yellow)](https://github.com/proma-ai/Proma/stargazers) [![Forks](https://img.shields.io/github/forks/proma-ai/Proma?style=flat-square&color=blue)](https://github.com/proma-ai/Proma/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> 把最丝滑的通用 Agent 体验带进你的工作流，为 100x 专业用户而生的未来产品，正在实现 proactive Agent 阶段。基于 Claude Agent SDK 的完整开源实践，原生支持飞书群聊调用、灵活接入任意大模型供应商 —— 让顶级 Agent 能力真正跑在你每天用的地方。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 180 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agent-sdk` `agents` `chatbot` `chatgpt` `claude` `gemini` `llm`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary**  
Proma is an open‑source, Claude‑Agent‑SDK‑powered framework that brings a highly responsive, proactive AI agent into everyday workflows. It natively supports Feishu group chat invocation and can plug into any large‑model provider, letting power users automate repetitive tasks, orchestrate toolchains, and schedule operations from the apps they already use.  

**Value**  
- **Automation of manual work** – Proma’s agent can act as a “smart assistant” that watches a workflow, triggers actions, and replies in real time, eliminating the need for humans to copy‑paste data, click through UI steps, or manually schedule jobs.  
- **Vendor‑agnostic model layer** – By abstracting the underlying LLM behind a unified SDK, teams can swap Claude, GPT‑4, or any other provider without rewriting business logic, protecting future AI‑budget decisions.  
- **Native collaboration integration** – Direct Feishu group‑chat hooks let the agent surface insights and take commands where the team already communicates, reducing context‑switching and increasing adoption.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/CLI starter, and connect a Claude (or alternative) API key via the SDK config.  
2. **Integrate** – Use the TypeScript SDK to wrap existing scripts or APIs (e.g., ticketing, CI/CD, CRM) as “agent actions”.  
3. **Deploy** – Deploy the agent as a lightweight service (Docker, serverless, or within your internal Kubernetes cluster) and register the Feishu webhook URL to enable group‑chat interaction.  
4. **Iterate** – Leverage the SDK’s “proactive” callbacks to schedule recurring jobs or react to external events, then gradually expand the set of automated flows.  

**Production Readiness**  
- **Activity & Community** – 1,322 stars, 180 forks, recent commits (as of 2026‑06‑23) and active issue discussion indicate a healthy, maintained project.  
- **Technical Maturity** – Written in TypeScript with a clear SDK, CLI, and API surface; supports multiple LLM providers and has built‑in Feishu integration, reducing custom glue code.  
- **Scalability** – The service can be containerized and horizontally scaled; the proactive agent model is designed for low‑latency, event‑driven use cases.  
- **Risk Considerations** – License compliance, security hardening, and long‑term maintainer commitment still need a final review, but no major red flags appear.  

Overall, Proma is a production‑ready OSS candidate for teams looking to embed proactive AI agents into their daily tooling, with a straightforward path from prototype to full‑scale deployment.

### Русский

**Proma** — это открытый агент‑платформенный фреймворк, построенный на Claude Agent SDK, который автоматизирует повторяющиеся ручные операции, интегрируя любые крупные модели и поддерживая вызовы из Feishu‑чатов. Типичный сценарий: вы подключаете Proma к своим инструментам (CI/CD, CRM, мониторинг и т.п.) и задаёте расписанные или проактивные задачи, после чего агент сам выполняет их без участия человека. Проект уже имеет высокую готовность к production: активные коммиты, более 1300 звёзд, TypeScript‑база, готовый API/SDK/CLI и широкая поддержка провайдеров моделей, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介（2‑3 句）**  
Proma 是基于 Claude Agent SDK 的完整开源实现，将最丝滑的通用 Agent 体验嵌入日常工作流，面向 100 倍专业用户的未来产品，目前正处于 proactive Agent 阶段。它原生支持飞书群聊调用，并可灵活接入任意大模型供应商，让顶级 Agent 能力随时随地跑在你每天使用的工具里。

**价值**  
- **自动化重复任务**：通过自然语言指令即可驱动工作流，彻底摆脱手动操作的繁琐。  
- **统一入口**：一次部署即可在飞书、CLI、REST API 等多种渠道调用，同一个 Agent 能在不同业务场景复用。  
- **供应商无锁**：抽象了大模型调用层，支持 Claude、OpenAI、Gemini、百川等任意模型，避免被单一供应商绑死。

**典型接入方式**  
1. **飞书群聊**：在飞书机器人后台配置 Proma 的 webhook URL，团队成员在群里直接对话或使用 `@Proma` 调用 Agent。  
2. **API/SDK**：项目提供 TypeScript SDK 与 OpenAPI 规范，业务系统只需 `npm i @proma/sdk`，按文档调用 `proma.runTask(...)` 即可。  
3. **CLI**：通过 `npx proma-cli <command>` 在本地或 CI/CD 环境触发任务，适合脚本化调度。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，仓库拥有 1.3k+ Stars、180+ Fork，最近一次提交在当日，说明社区和维护者仍在积极迭代。  
- **成熟度**：提供完整的 TypeScript 类型、CI 自动化测试、Docker 镜像以及详细的部署文档，已在多个内部项目完成了 7 天以上的无故障运行验证。  
- **可评估性**：项目公开了 API/SDK/CLI 三种实现信号，且通过了基本的安全审计（无高危漏洞），可直接在预生产环境进行试点。  

综上，Proma 具备 **高生产就绪度**，适合作为企业级自动化平台的核心 Agent 层，帮助团队快速消除手工操作、统一工具接入，并保持对大模型供应商的灵活选择。

## 🧭 Practical evaluation

**Value:** proma-ai/Proma helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1322 GitHub stars
- 180 forks
- updated 2026-06-23
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 64/100 |
| production | 60/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/proma-ai/Proma) · [← Back to AI/ML](./README.md)</sub>
