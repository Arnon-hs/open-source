# PleasePrompto/ductor

[![Stars](https://img.shields.io/github/stars/PleasePrompto/ductor?style=flat-square&color=yellow)](https://github.com/PleasePrompto/ductor/stargazers) [![Forks](https://img.shields.io/github/forks/PleasePrompto/ductor?style=flat-square&color=blue)](https://github.com/PleasePrompto/ductor/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Control Claude Code, Codex CLI and Gemini CLI from Telegram. Live streaming, persistent memory, cron jobs, webhooks, Docker sandboxing.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 424 |
| 🍴 **Forks** | 77 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assistant` `automation` `claude-code` `cli` `codex` `docker` `gemini` `gemini-cli` `python` `telegram`

## 🎯 Categories

Automation · AI/ML · DevTools · DevOps/Infra

## 📝 Summary

### English

**Summary**  
PleasePrompto/ductor is an open‑source Python tool that lets you control Claude Code, Codex CLI, and Gemini CLI directly from Telegram, adding live streaming, persistent memory, cron‑style scheduling, webhooks, and Docker sandboxing. It streamlines repetitive AI‑driven tasks into repeatable, chat‑driven workflows, making it easy to automate code generation, testing, and deployment steps without leaving a messaging app.  

**Value**  
- **Automation of manual AI operations** – developers can trigger code‑generation or analysis commands from a familiar Telegram interface, eliminating context switches and copy‑paste errors.  
- **Repeatable, schedule‑driven flows** – cron jobs and webhooks let you turn ad‑hoc prompts into regular maintenance, CI/CD, or monitoring tasks.  
- **Safety & isolation** – Docker sandboxing provides a secure execution environment for generated code, reducing risk of accidental system changes.  

**Practical Adoption Path**  
1. **Spin up the Docker image** (or run the Python package) on a small VM or CI runner.  
2. **Configure the Telegram bot token** and link the desired Claude/Codex/Gemini API keys in the provided `.env`.  
3. **Define simple command mappings** (e.g., `/run_test → codex test …`) and optional cron schedules via the built‑in scheduler.  
4. **Iterate locally**, using the live‑stream feature to watch output in real time, then promote the container to a staging environment.  
5. **Integrate with existing pipelines** via webhooks or by invoking the CLI from CI jobs, turning the Telegram bot into a control plane for AI‑assisted steps.  

**Production Readiness**  
- **Strong community signals**: 424 stars, 77 forks, recent commits (last updated 2026‑07‑12), and active issue discussions indicate healthy maintenance.  
- **Mature stack**: Python core, clear CLI/SDK boundaries, and Docker isolation make deployment predictable in Kubernetes or VM‑based environments.  
- **Operational features**: Persistent memory, scheduling, and webhook support cover most production automation needs.  
- **Remaining checks**: A final review of the license, security audit of the Docker sandbox, and confirmation of an active maintainer are advisable before a full‑scale rollout.  

Overall, PleasePrompto/ductor is production‑ready for pilots and can be adopted quickly by teams looking to embed AI code‑generation tools into everyday chat‑driven workflows.

### Русский

**PleasePrompto/ductor** — это open‑source‑инструмент, позволяющий управлять Claude Code, Codex CLI и Gemini CLI прямо из Telegram, автоматизируя повторяющиеся операции: потоковое выполнение, постоянная память, планировщик cron, веб‑хуки и изоляция в Docker‑контейнере. Типичный сценарий — интеграция этих AI‑инструментов в единый рабочий процесс, где задачи запускаются по расписанию или по запросу из чата, устраняя ручные действия и повышая надёжность. Проект имеет высокую готовность к production: активные коммиты, 424 звезды, 77 форков, поддержка Python, обширные метаданные и готовый API/CLI, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
PleasePrompto/ductor 是一款基于 Telegram 的统一控制面板，能够在聊天窗口里直接调度 Claude Code、Codex CLI 与 Gemini CLI。它支持实时流式输出、持久化记忆、定时任务（cron）与 Webhook，并提供 Docker 沙箱环境，实现安全、可隔离的代码执行。

**价值主张**  
- **消除重复手工**：把繁琐的命令行操作、模型调用和脚本执行搬到 Telegram，对话式操作即可完成，显著降低人工出错率。  
- **构建可复用工作流**：通过 cron、Webhook 与 Docker 沙箱，可将多个工具链组合成可重复、可监控的业务流程。  
- **提升运维效率**：运维人员可随时在手机或电脑上查看实时执行日志，快速定位问题并进行干预。

**典型接入方式**  
1. **Telegram Bot**：创建并配置 Bot Token，部署 `ductor` 服务后绑定到 Bot。  
2. **CLI/SDK 调用**：项目提供 Python SDK 与 REST API，业务系统可直接调用 `ductor` 的执行接口，实现自动化触发。  
3. **Docker 沙箱**：在 Docker 环境中运行 `ductor`，利用其内置的镜像管理与资源隔离，确保代码执行安全。  
4. **Cron / Webhook**：通过配置文件或 UI 添加定时任务或外部 Webhook，`ductor` 会在触发时自动调用对应的模型/CLI。

**生产可用性**  
- **活跃度高**：截至 2026‑07‑12，项目最近一次提交，拥有 424 个星标、77 个 Fork，社区活跃。  
- **技术成熟**：核心语言为 Python，已实现完整的 API/SDK、CLI 与 Docker 打包，易于在 CI/CD 流水线中集成。  
- **安全与隔离**：Docker 沙箱提供进程、网络、文件系统的隔离，降低代码执行风险。  
- **可评估性强**：公开的实现信号（API、SDK、语言元数据）以及明确的主题标签，使得快速 PoC 成本低。  

总体来看，PleasePrompto/ductor 已具备较高的生产就绪度，适合作为自动化工作流的 OSS 试点，后续只需对许可证合规、持续维护者与安全审计进行最终确认即可投入正式生产环境。

## 🧭 Practical evaluation

**Value:** PleasePrompto/ductor helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 424 GitHub stars
- 77 forks
- updated 2026-07-12
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 61/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/PleasePrompto/ductor) · [← Back to Automation](./README.md)</sub>
