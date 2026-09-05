# Jeffrey0117/ClaudeBot

[![Stars](https://img.shields.io/github/stars/Jeffrey0117/ClaudeBot?style=flat-square&color=yellow)](https://github.com/Jeffrey0117/ClaudeBot/stargazers) [![Forks](https://img.shields.io/github/forks/Jeffrey0117/ClaudeBot?style=flat-square&color=blue)](https://github.com/Jeffrey0117/ClaudeBot/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Not a pipe to Claude. A command center on your phone. — Telegram bot for Claude Code CLI with plugin system, multi-bot, queue, streaming, and hot-reload.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 62 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bot` `claude` `claude-code` `telegram` `telegram-bot` `typescript`

## 🎯 Categories

Orchestration · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Jeffrey0117/ClaudeBot is a TypeScript‑based Telegram bot that turns your phone into a command center for Claude’s Code CLI, offering a plugin system, multi‑bot support, request queuing, streaming responses, and hot‑reload of code. It automates repetitive tasks by letting you invoke Claude operations, chain tools, and schedule workflows directly from Telegram, eliminating the need for manual CLI work.

**Value**  
- **Automation of manual steps** – Developers can trigger Claude code generation, run scripts, or invoke other services with a simple chat command, turning ad‑hoc CLI usage into repeatable, auditable actions.  
- **Extensible plugin architecture** – Custom plugins let teams integrate internal tools (CI pipelines, ticketing systems, monitoring alerts) without modifying the core bot.  
- **Multi‑bot & queuing** – Parallel bots can handle different projects or environments, while the built‑in queue prevents race conditions and ensures orderly execution.  
- **Streaming & hot‑reload** – Real‑time response streaming gives immediate feedback, and hot‑reloading lets you update plugins or bot logic on‑the‑fly without downtime.

**Practical Adoption Path**  
1. **Pilot Setup** – Clone the repo, configure the required Claude API token and Telegram bot token, and run the Docker compose or `npm start` locally.  
2. **Define Plugins** – Use the provided SDK to write simple TypeScript plugins that wrap existing internal scripts or APIs (e.g., trigger a build, post a Jira ticket).  
3. **Integrate with Existing CI/CD** – Deploy the bot to a staging environment (Kubernetes, Fly.io, or a managed VM) and expose the Telegram webhook.  
4. **User Training** – Provide a short cheat‑sheet of bot commands to developers and ops staff; enable role‑based access via Telegram usernames.  
5. **Scale to Production** – Add persistence (Redis/PostgreSQL) for queue state, enable TLS for the webhook, and monitor logs with Prometheus/Grafana.  

**Production Readiness**  
- **Activity & Community** – The project shows recent commits (as of 2026‑06‑27), 62 stars, 13 forks, and a clear TypeScript codebase, indicating an active maintainer and community interest.  
- **Architecture** – Built on well‑known components (Telegram Bot API, Claude CLI, Node.js), with a modular plugin system that isolates custom logic, making it easier to audit and secure.  
- **Scalability** – Supports multiple bots and a request queue, which can be backed by external stores for horizontal scaling.  
- **Risks** – Licensing, security posture, and long‑term maintainer commitment still need a final review, but no major metadata issues were found. Overall, the project is mature enough for a serious pilot and can be hardened for production with standard DevOps practices.

### Русский

Jeffrey0117/ClaudeBot is a Telegram bot for Claude Code CLI with plugin system, multi-bot Jeffrey0117/ClaudeBot** — это Telegram‑бот, который превращает Claude Code CLI в мобильный командный центр с системой плагинов, очередью, потоковой передачей и горячей перезагрузкой, позволяя автоматизировать рутинные операции и соединять инструменты в повторяемые потоки. Типовый сценарий внедрения — подключение бота к рабочему чату команды, где разработчики запускают скрипты, планируют задачи и управляют CI/CD‑процессами без выхода из мессенджера. Благодаря недавней активности, растущему числу звёзд и форков, а также чёткой документации API/CLI, проект демонстрирует высокий уровень готовности к продакшену и подходит для пилотного использования в продакшн‑средах.

### 中文

**项目简介**  
Jeffrey0117/ClaudeBot 是一个运行在 Telegram 上的 Claude Code CLI 控制中心，内置插件系统、支持多机器人、任务队列、流式输出与热重载，帮助你把手动操作转化为可编排的自动化流程。

**价值**  
- **消除重复劳动**：通过 Telegram 指令即可触发 Claude 的代码生成、调试等功能，省去在本地或网页上反复点击的步骤。  
- **可组合的工作流**：插件机制让不同工具（CI、监控、数据库等）能够在同一个聊天窗口里串联，实现“一键”执行的业务流。  
- **即时反馈 & 热更新**：支持流式返回结果并可在运行时热重载插件，提升调试效率和响应速度。

**典型接入方式**  
1. **创建 Telegram Bot**：在 BotFather 中获取 Bot Token。  
2. **部署 ClaudeBot**：克隆仓库，使用 Docker 或直接 `npm install && npm run start` 启动，配置环境变量 `TELEGRAM_TOKEN`、`CLAUDE_API_KEY` 等。  
3. **插件开发**：在 `plugins/` 目录编写 TypeScript 插件，导出符合 `IPlugin` 接口的函数，即可在聊天中通过 `/pluginName` 调用。  
4. **调用 Claude**：在 Telegram 中发送指令（如 `/run your-code`），ClaudeBot 将通过 Claude Code CLI 执行并返回结果，支持队列和流式输出。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑27，星标 62、fork 13，社区已有一定使用基础。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的 API/CLI 接口，插件系统清晰，易于二次开发。  
- **风险**：许可证、长期维护者以及安全审计仍需进一步确认，但整体代码质量和更新频率足以支撑正式业务的试点部署。  

综上，ClaudeBot 具备较高的生产就绪度，适合作为自动化、DevOps 场景下的“指令中心”，快速将手工操作转为可重复、可监控的工作流。

## 🧭 Practical evaluation

**Value:** Jeffrey0117/ClaudeBot helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 62 GitHub stars
- 13 forks
- updated 2026-06-27
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 38/100 |
| topics | 75/100 |
| outlook | 66/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Jeffrey0117/ClaudeBot) · [← Back to Orchestration](./README.md)</sub>
