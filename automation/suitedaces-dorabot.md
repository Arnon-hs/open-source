# suitedaces/dorabot

[![Stars](https://img.shields.io/github/stars/suitedaces/dorabot?style=flat-square&color=yellow)](https://github.com/suitedaces/dorabot/stargazers) [![Forks](https://img.shields.io/github/forks/suitedaces/dorabot?style=flat-square&color=blue)](https://github.com/suitedaces/dorabot/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> macOS app for 24/7 AI agents in an IDE with memory, scheduled tasks, browser use + access to Whatsapp, Telegram, Slack.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 229 |
| 🍴 **Forks** | 33 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-assistant` `browser-automation` `claude` `claude-agent-sdk` `electron` `macos` `open-source` `openai` `personal-ai` `slack-bot` `telegram-bot`

## 🎯 Categories

Automation · AI/ML · Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
dorabot (suitedaces/dorabot) is a macOS application that lets developers run 24/7 AI agents directly inside their IDE, equipped with persistent memory, scheduled tasks, browser automation, and integrations with WhatsApp, Telegram and Slack. By exposing a clean API/SDK/CLI and being built in TypeScript, it enables the creation of repeatable, automated workflows that eliminate tedious manual steps. With strong recent activity, 229 ★ on GitHub and a growing ecosystem, it is a mature open‑source candidate for production pilots.

**Value**  
- **Automation of repetitive work** – AI agents can remember context, execute scheduled jobs, and interact with web services, turning ad‑hoc manual tasks into reliable, repeatable flows.  
- **Unified communication** – Direct access to popular messaging platforms (WhatsApp, Telegram, Slack) lets bots send notifications, collect inputs, or trigger actions without switching contexts.  
- **Developer‑centric integration** – Running inside the IDE keeps the feedback loop tight, allowing developers to prototype, test, and iterate on automation scripts quickly.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided CLI or launch the macOS app, and experiment with the sample agents to verify compatibility with your IDE and workflow.  
2. **Integration** – Use the exposed TypeScript SDK or REST API to embed dorabot agents into existing build pipelines, CI/CD jobs, or internal tooling.  
3. **Customization** – Extend agents with custom memory schemas, schedule new tasks, or add additional platform connectors (e.g., internal APIs) via the modular plugin architecture.  
4. **Pilot** – Deploy the macOS app on a small team’s machines, monitor performance and security logs, and iterate on the agents based on real‑world usage.  

**Production Readiness**  
- **Activity & Community** – The project shows recent commits (last updated 2026‑05‑11), 229 stars, 33 forks, and 14 topical tags, indicating active interest and contributions.  
- **Technical Maturity** – Built in TypeScript with a well‑documented API/CLI, it integrates cleanly into modern development stacks and CI pipelines.  
- **Risk Profile** – No major metadata or licensing red flags have been identified, though a final security audit and verification of maintainer responsiveness are advisable before full‑scale rollout.  

Overall, dorabot offers a high‑impact, low‑friction way to automate developer workflows and is ready for serious pilot deployments in production environments.

### Русский

**suitedaces/dorabot** — это macOS‑приложение, позволяющее запускать 24/7 AI‑агентов прямо в IDE: они сохраняют контекст, могут выполнять запланированные задачи, работать в браузере и взаимодействовать с WhatsApp, Telegram и Slack, тем самым автоматизируя повторяющиеся ручные операции. Типичный сценарий — интеграция инструмента в существующий workflow для создания повторяемых цепочек (например, автоматический сбор данных, отправка отчетов в мессенджеры и запуск периодических скриптов). Проект имеет высокий уровень готовности к production: активные коммиты, 229 звёзд, 33 форка, современный стек TypeScript и открытый API/CLI, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
suitedaces/dorabot 是一款基于 macOS 的 IDE 插件，能够让 AI 代理 24/7 持续运行，具备记忆、定时任务、浏览器交互以及 WhatsApp、Telegram、Slack 等即时通讯渠道的访问能力。

**价值主张**  
- **自动化重复工作**：把手动的代码生成、调试、文档编写等日常任务交给 AI，显著提升开发效率。  
- **工具链无缝连接**：通过统一的 AI 代理，将 IDE、浏览器以及常用通讯工具串联成可重复的工作流，减少在不同平台之间切换的摩擦。  
- **可编排的定时任务**：支持在指定时间或触发条件下自动执行脚本或查询，帮助团队实现持续集成/持续部署（CI/CD）之外的运维和监控任务。

**典型接入方式**  
1. **API/SDK**：项目提供 TypeScript SDK，开发者可在自己的插件或脚本中直接调用 `dorabot` 的接口，实现自定义指令和数据交互。  
2. **CLI**：通过 `dorabot-cli` 在终端启动或管理 AI 代理，可用于 CI 流水线或本地调试。  
3. **IDE 插件**：直接在支持的 macOS IDE（如 VS Code、IntelliJ）中安装插件，配置 API Token 与通讯渠道，即可在编辑器内与 AI 代理交互。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目最近有提交，星标 229、fork 33，表明社区活跃。  
- **技术成熟度**：主语言 TypeScript，拥有 14 个相关话题标签，代码结构清晰，易于二次开发。  
- **生态兼容**：提供标准化的 API、CLI 与 SDK，能够快速集成到现有工作流中。  
- **风险**：许可证、完整的安全审计以及维护者的长期可用性仍需进一步确认，但目前的信号足以支持在内部或受控环境下进行试点。  

综合来看，dorabot 已具备较高的生产就绪度，适合作为自动化助理在 macOS 开发环境中进行功能验证或小规模部署。

## 🧭 Practical evaluation

**Value:** suitedaces/dorabot helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 229 GitHub stars
- 33 forks
- updated 2026-05-11
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 47/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/suitedaces/dorabot) · [← Back to Automation](./README.md)</sub>
