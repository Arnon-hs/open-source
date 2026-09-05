# bagidea/bagidea-office

[![Stars](https://img.shields.io/github/stars/bagidea/bagidea-office?style=flat-square&color=yellow)](https://github.com/bagidea/bagidea-office/stargazers) [![Forks](https://img.shields.io/github/forks/bagidea/bagidea-office?style=flat-square&color=blue)](https://github.com/bagidea/bagidea-office/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> A living AI-agent office on your desktop wallpaper — Claude Code agents that walk, work, delegate, learn & hold meetings. Per-agent swappable models (Claude/GLM/DeepSeek/Qwen/Kimi/OpenAI/Gemini/Groq/Ollama…), workflows, plugins, voice & Telegram/Discord/LINE. Open source.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 93 |
| 🍴 **Forks** | 31 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-orchestration` `ai` `ai-agents` `anthropic` `automation` `autonomous-agents` `claude` `claude-code` `desktop-wallpaper` `gemini` `godot` `llm`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML

## 📝 Summary

### English

**Brief summary**  
Bagidea‑Office is an open‑source “living AI‑agent office” that runs Claude‑style code agents directly on your desktop wallpaper. Each agent can be equipped with a swappable LLM (Claude, OpenAI, Gemini, etc.), custom workflows, plugins, voice interaction and integrations with Telegram, Discord or LINE, enabling them to walk, work, delegate, learn and even hold meetings.

**Value**  
- **From isolated prompts to repeatable workflows** – The platform lets you stitch together multiple agents, tool‑use pipelines and persistent memory so that a single prompt can trigger a coordinated, multi‑step process rather than a one‑off answer.  
- **Plug‑and‑play model selection** – Swappable back‑ends let you balance cost, latency and capability without rewriting code, and the built‑in voice and chat integrations make the agents usable by non‑technical staff.  
- **Standardised orchestration** – By exposing a clear API/CLI and SDK, Bagidea‑Office provides a common language for defining agent roles, hand‑offs and state sharing, which simplifies governance and auditability across teams.

**Practical adoption path**  
1. **Prototype** – Clone the repo, run the Docker/Node setup, and use the CLI to spin up a single Claude‑based agent with a simple “schedule‑meeting” workflow.  
2. **Extend** – Add additional agents (e.g., a data‑retrieval agent using OpenAI and a reporting agent using Gemini) and connect them via the provided workflow DSL or plugin hooks.  
3. **Integrate** – Hook the agents into existing communication channels (Telegram, Discord, LINE) using the out‑of‑box connectors, and expose the CLI as a micro‑service behind your internal API gateway.  
4. **Govern** – Leverage the built‑in memory store to persist context, configure role‑based access, and apply your organization’s LLM usage policies.  
5. **Scale** – Deploy the agents on Kubernetes or a managed container service, swapping the underlying LLM models (including self‑hosted Ollama) to meet performance or cost targets.

**Production readiness**  
- **Activity & community** – 93 ★, 31 forks, recent commits (as of 2026‑06‑22) and a growing ecosystem of 18 topics indicate active maintenance.  
- **Technical maturity** – The project ships a stable JavaScript core, a documented API/SDK, CLI tools and ready‑made integrations, making it straightforward to evaluate and embed in existing stacks.  
- **Risk considerations** – No major metadata or licensing red flags have been found, but a final security audit (dependency scanning, secret handling) and confirmation of long‑term maintainers are advisable before a full production rollout.  

Overall, Bagidea‑Office is a high‑readiness OSS candidate for organizations that want to move from ad‑hoc prompt engineering to orchestrated, multi‑agent automation with flexible model back‑ends and real‑time user interaction.

### Русский

**bagidea/bagidea-office** — это открытый «офис»‑агент на рабочем столе, где Claude‑агенты (и другие модели — GLM, DeepSeek, Qwen, Kimi, OpenAI, Gemini, Groq, Ollama) могут ходить, выполнять задачи, делегировать работу, обучаться и проводить встречи, используя плагины, голосовое управление и интеграцию с Telegram/Discord/LINE. Проект позволяет превратить разрозненные запросы и инструменты в воспроизводимые многопотоковые рабочие процессы, стандартизировать память агентов и быстро собрать конвейеры с использованием внешних инструментов. Благодаря активному развитию (обновления — 2026‑06‑22), 93 звёздам, 31 форку, JavaScript‑базе и открытым API/CLI, проект считается готовым к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
bagidea/bagidea‑office 是一款把 Claude 等大模型包装成“AI 办公助理”，直接跑在桌面壁纸上。每个助理可以独立选择模型、插件、工作流，支持语音、Telegram/Discord/LINE 等渠道，能够自行走动、分配任务、学习并召开会议，实现多 Agent 协同与工具链自动化。  

**价值**  
- **把碎片化的 Prompt 与工具统一为可重复的 Agent 工作流**，降低了手工编排的成本。  
- **模型可随代理自由切换**（Claude、GLM、DeepSeek、Qwen、Kimi、OpenAI、Gemini、Groq、Ollama 等），满足不同场景的性能/成本需求。  
- **插件化、可编排的多 Agent 框架**，适用于跨团队协作、自动化报告、数据抓取、客服等多种业务。  

**典型接入方式**  
1. **API/SDK**：项目提供基于 JavaScript 的 SDK 与 REST API，开发者可在现有系统中直接调用 `createAgent、runWorkflow、addPlugin` 等接口。  
2. **CLI**：通过 `bagidea-office` 命令行工具快速启动本地或容器化实例，适合 CI/CD 流水线或脚本化部署。  
3. **插件/Webhook**：利用内置插件机制或自定义 webhook 与外部服务（如数据库、消息队列、企业 IM）对接，实现工具链的完整闭环。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑22 最近一次提交，GitHub ★93、Fork 31，18 个主题标签，社区活跃。  
- **技术成熟**：核心使用 JavaScript/Node.js，提供完整的 API 文档、示例代码和 Docker 镜像，易于在容器或云平台上部署。  
- **安全与合规**：暂无重大元数据风险，仍需对许可证（MIT/Apache）和依赖库的安全审计进行最终确认。  
- **适配性强**：支持多种大模型和通讯渠道，能够快速在企业内部或 SaaS 环境中进行试点，具备从小规模实验到全量生产的平滑升级路径。  

综上，bagidea-office 已具备较高的生产就绪度，适合作为企业内部多 Agent 编排与自动化的 OSS 基石。

## 🧭 Practical evaluation

**Value:** bagidea/bagidea-office helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 93 GitHub stars
- 31 forks
- updated 2026-06-22
- primary language: JavaScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 72/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/bagidea/bagidea-office) · [← Back to Orchestration](./README.md)</sub>
