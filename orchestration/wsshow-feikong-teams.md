# wsshow/feikong-teams

[![Stars](https://img.shields.io/github/stars/wsshow/feikong-teams?style=flat-square&color=yellow)](https://github.com/wsshow/feikong-teams/stargazers) [![Forks](https://img.shields.io/github/forks/wsshow/feikong-teams?style=flat-square&color=blue)](https://github.com/wsshow/feikong-teams/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> 一个基于多智能体协作的 AI 助手，支持命令行和Web界面，提供团队模式、自定义会议模式和多智能体讨论模式（圆桌会议模式）三种工作方式，通过多个专业智能体协同工作来完成复杂的编程和系统任务。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 121 |
| 🍴 **Forks** | 28 |
| 💻 **Language** | Go |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai` `auto` `chatbot` `chatgpt` `cli` `cowork` `eino` `fkteams` `mcp` `multiagent` `skills`

## 🎯 Categories

Orchestration · MCP · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
feikong‑teams is an open‑source AI assistant built on multi‑agent collaboration, offering a CLI and a web UI with three work modes—team mode, custom meeting mode, and round‑table discussion mode. By orchestrating specialized agents, it can tackle complex programming and system‑integration tasks that would be cumbersome for a single prompt‑based model.

**Value**  
The platform turns ad‑hoc prompts and isolated tools into repeatable, orchestrated workflows, enabling teams to coordinate multiple agents, embed tool‑use pipelines, and maintain consistent agent memory. This reduces the overhead of manually chaining LLM calls, improves reliability for complex tasks, and provides a structured environment for collaborative AI‑driven development.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repository, run the provided Docker/CLI starter, and experiment with the built‑in team and meeting modes on a small code‑base.  
2. **Integration** – Use the exposed Go SDK or REST API to embed feikong‑teams into existing CI/CD pipelines or internal dev‑tools, customizing agents for your domain‑specific tasks.  
3. **Scaling** – Deploy the web UI behind an internal gateway, configure persistent storage for agent memory, and add custom tool plugins (e.g., code linters, cloud APIs) to extend the workflow.  

**Production Readiness**  
With recent commits (as of 2026‑06‑26), 121 stars, 28 forks, and active issue handling, the project shows strong community momentum. Its Go codebase, clear CLI/API surface, and modular architecture make it straightforward to containerize and monitor in production. While a final review of licensing, security hardening, and maintainer commitment is advisable, the overall signals indicate that feikong‑teams is mature enough for pilot deployments and can be hardened for enterprise use.

### Русский

**wsshow/feikong‑teams** — это open‑source платформа на Go, позволяющая собрать несколько специализированных AI‑агентов в единую рабочую команду, доступную как через CLI, так и через веб‑интерфейс. Она поддерживает три режима — командный, пользовательский конференционный и «круглый стол», что упрощает построение повторяемых многопоточных пайплайнов для сложных программных и системных задач (координация агентов, интеграция инструментов, унификация памяти). Проект имеет высокий уровень готовности к production: свежие коммиты, активное сообщество (121 звезда, 28 форков), хорошая документация и открытый API/SDK, что делает его подходящим для пилотных внедрений в рамках автоматизации и оркестрации многопользовательских AI‑процессов.

### 中文

**项目简介**  
wsshow/feikong‑teams 是一个基于多智能体协作的 AI 助手，提供命令行和 Web 界面，支持团队模式、自定义会议模式以及圆桌会议（多智能体讨论）三种工作方式。通过多个专业化的智能体协同工作，能够完成复杂的编程、系统集成和自动化任务。

**价值体现**  
- **把零散的 Prompt 与工具串联成可复用的工作流**，实现跨工具、跨语言的自动化编排。  
- **多智能体协同** 能够在同一任务中分工（如代码生成、单元测试、部署验证），显著提升任务完成的效率和可靠性。  
- **统一的记忆与状态管理**，让不同会话和不同智能体之间共享上下文，避免信息丢失和重复劳动。

**典型接入方式**  
1. **CLI**：直接在终端调用 `feikong-teams`，适合 CI/CD、脚本化任务以及本地开发调试。  
2. **Web UI**：通过浏览器访问提供的前端页面，适合团队协作、会议式交互以及可视化监控。  
3. **SDK/API**：项目公开了 Go 语言的库以及 HTTP API，其他语言（如 Python、Node）可通过 REST 调用或生成对应的客户端，实现深度集成到现有平台或服务中。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，GitHub 上 121 ★、28 Fork，社区活跃，Issue 响应及时。  
- **技术成熟度**：核心实现使用 Go，具备高并发、低资源占用的特性，适合在容器化或云原生环境中部署。  
- **生态兼容**：提供标准化的 API/SDK，易于与现有 CI/CD、监控、身份认证体系对接。  
- **风险**：目前尚需进一步审查许可证细节、依赖安全性以及维护者的长期投入，但整体信号表明项目已具备在正式生产环境中进行试点的条件。

综上，wsshow/feikong‑teams 能帮助组织把分散的 AI Prompt 与工具链统一为可重复、可监控的多智能体工作流，接入方式灵活，且已具备较高的生产就绪度。

## 🧭 Practical evaluation

**Value:** wsshow/feikong-teams helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 121 GitHub stars
- 28 forks
- updated 2026-06-26
- primary language: Go
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/wsshow/feikong-teams) · [← Back to Orchestration](./README.md)</sub>
