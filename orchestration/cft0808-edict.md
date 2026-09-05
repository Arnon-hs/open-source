# cft0808/edict

[![Stars](https://img.shields.io/github/stars/cft0808/edict?style=flat-square&color=yellow)](https://github.com/cft0808/edict/stargazers) [![Forks](https://img.shields.io/github/forks/cft0808/edict?style=flat-square&color=blue)](https://github.com/cft0808/edict/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-82%2F100-brightgreen?style=flat-square)](#)

> 🏛️ 三省六部制 · OpenClaw Multi-Agent Orchestration System — 9 specialized AI agents with real-time dashboard, model config, and full audit trails

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 16.2k |
| 🍴 **Forks** | 1.7k |
| 💻 **Language** | Python |
| 📈 **Score** | 82/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-orchestration` `autonomous-agents` `claude` `dashboard` `kanban` `llm` `multi-agent` `openai` `openclaw` `orchestration` `python`

## 🎯 Categories

Orchestration · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary**  
cft0808/edict is an open‑source “OpenClaw” orchestration platform that lets you stitch together up to nine specialized AI agents into a single, real‑time workflow, complete with a dashboard, model‑configuration UI, and immutable audit logs. It turns ad‑hoc prompts and tool calls into repeatable, version‑controlled pipelines, making multi‑agent coordination, tool‑use pipelines, and persistent agent memory easy to standardize.  

**Value**  
- **From isolated prompts to production‑grade pipelines** – Edict abstracts each AI agent as a reusable micro‑service, so you can define, store, and re‑run complex interactions without rewriting prompt code.  
- **Visibility & compliance** – The built‑in dashboard shows live agent status, while the audit trail records every input, output, and configuration change, satisfying traceability requirements for regulated environments.  
- **Extensibility** – Because agents are defined in Python and exposed via a common API, you can plug in custom models, third‑party tools, or domain‑specific memory stores without touching the core engine.  

**Practical Adoption Path**  

| Step | Action | Why |
|------|--------|-----|
| 1️⃣ Quick‑start validation | Clone the repo, run the provided Docker Compose file, and follow the README tutorial to launch the demo dashboard. | Confirms the environment (Python 3.11, Docker) works on your infrastructure and gives a hands‑on feel for the UI and agent wiring. |
| 2️⃣ Proof‑of‑concept (PoC) | Implement a minimal workflow that mirrors a real business use case (e.g., “extract‑summarize‑store” using two agents). Keep the PoC to ≤ 3 agents and use the default SQLite memory backend. | Demonstrates that Edict can orchestrate your specific prompts and tools while keeping the scope manageable. |
| 3️⃣ Integration scaffolding | Replace the demo agents with your own models or APIs, add any required tool wrappers, and configure the model‑config UI to point to your production endpoints (e.g., Azure OpenAI, Anthropic). | Shows how to bring existing AI assets into Edict without rewriting core logic. |
| 4️⃣ Scaling & hardening | Switch the storage layer to PostgreSQL or a distributed KV store, enable TLS for the dashboard, and set up CI pipelines that run the audit‑log validation tests. | Moves the PoC from a sandbox to a production‑ready deployment. |
| 5️⃣ Governance rollout | Define role‑based access in the dashboard, lock down the configuration UI via environment variables, and integrate the audit logs with your SIEM. | Aligns the system with security and compliance policies. |

**Production Readiness**  
- **Activity & community** – 16 k+ stars, 1.7 k forks, and a recent commit (2026‑07‑06) indicate strong community momentum.  
- **Maturity** – The platform already ships a full UI, model config, and immutable logs; these are features that many enterprises build as separate services.  
- **Scalability** – Architecture is container‑first (Docker Compose / Kubernetes manifests in the repo), and the agent layer is language‑agnostic, allowing horizontal scaling of individual agents.  
- **Risks to address** – Final due‑diligence on the OSS license (MIT/Apache?), a security audit of third‑party dependencies, and confirmation that a core maintainer is actively responding to issues. Once these checks are completed, Edict is ready for a serious pilot in production environments.

### Русский

Резюме проекта cft0808/edict:

cft0808/edict — это открытый исходный код проект, предназначенный для управления и координации мульти-агентных потоков при помощи 9 специализированных AI-агентов с реал-time дашбордом и полным аудитом действий. Этот проект идеально подходит для реализации типового сценария внедрения, когда необходимо объединить изолированные команды и инструменты в повторяющиеся агентские потоки. cft0808/edict готов к production, поскольку имеет высокий уровень готовности (High) и сильные признаки активности, приёма и экосистемы.

### 中文

**项目简介**  
cft0808/edict 是基于 OpenClaw 的多智能体编排系统，提供 9 个专用 AI 代理、实时仪表盘、模型配置与完整审计链路，帮助将散落的 Prompt 与工具封装成可复用的工作流。

**价值**  
- **工作流标准化**：把零散的 Prompt、工具调用统一为可重复、可追踪的多代理流程。  
- **可观测性与审计**：实时仪表盘展示每个代理的状态、输入输出，所有交互都有审计记录，便于调试与合规。  
- **灵活的模型配置**：支持为不同代理指定模型、温度、上下文长度等参数，满足多场景需求。

**典型接入方式**  
1. **阅读 README 与示例**，确认系统依赖（Python ≥3.9、Docker）并完成本地快速启动。  
2. **定义 Agent 配置**（JSON/YAML），指定每个代理的模型、工具链和记忆策略。  
3. **在现有业务中嵌入 SDK**：通过 `edict.run_workflow(workflow_id, inputs)` 调用编排好的工作流，或使用 HTTP API 与仪表盘交互。  
4. **小范围 PoC**：先在单机或测试环境跑一个简化的 workflow，验证工具调用、记忆同步和审计日志是否满足预期。  

**生产可用性**  
- **活跃度高**：截至 2026‑07‑06 最近一次提交，星标 16 157、Fork 1 701，社区活跃。  
- **技术成熟**：核心使用 Python 实现，配套 Docker 镜像，易于容器化部署与弹性扩容。  
- **风险点**：仍需最终确认许可证兼容性、依赖安全审计以及维护者响应速度。总体而言，已具备 OSS 级别的生产候选资质，适合在内部或受控环境中做正式上线前的试点。

## 🧭 Practical evaluation

**Value:** cft0808/edict helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 16157 GitHub stars
- 1701 forks
- updated 2026-07-06
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 81/100 |
| stars | 90/100 |
| topics | 100/100 |
| outlook | 90/100 |
| quality | 89/100 |
| recency | 80/100 |
| adoption | 87/100 |
| production | 75/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/cft0808/edict) · [← Back to Orchestration](./README.md)</sub>
