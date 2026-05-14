# alexei-led/ccgram

[![Stars](https://img.shields.io/github/stars/alexei-led/ccgram?style=flat-square&color=yellow)](https://github.com/alexei-led/ccgram/stargazers) [![Forks](https://img.shields.io/github/forks/alexei-led/ccgram?style=flat-square&color=blue)](https://github.com/alexei-led/ccgram/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Telegram ↔ tmux bridge for Claude Code, Codex CLI, and Gemini CLI. Monitor output, respond to prompts, manage parallel sessions.  Control AI coding agents from your phone.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 129 |
| 🍴 **Forks** | 37 |
| 💻 **Language** | Python |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-coding` `claude-code` `cli` `codex` `codex-cli` `developer-tools` `gemini` `gemini-cli` `pi-agent` `python` `telegram` `telegram-bot`

## 🎯 Categories

Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`alexei-led/ccgram` is a Python‑based bridge that lets you control Claude Code, Codex CLI, and Gemini CLI from Telegram, forwarding tmux sessions to your phone. It monitors AI‑generated output, auto‑responds to prompts, and orchestrates parallel coding agents, turning repetitive command‑line tasks into a mobile‑friendly workflow. The project scores 78/100 and is positioned as an automation‑focused dev‑tool.

**Value**  
- **Hands‑free AI coding**: Developers can start, stop, and query AI coding agents without leaving their phone, eliminating context switches.  
- **Repeatable flows**: By exposing API/CLI hooks, ccgram enables scripted pipelines (e.g., “run lint → generate code → test”) that can be triggered from Telegram or integrated into CI/CD.  
- **Parallel session management**: tmux integration lets multiple AI agents run side‑by‑side, with real‑time monitoring and selective response handling, reducing manual copy‑paste and supervision.

**Practical Adoption Path**  
1. **Clone & install** – `pip install -r requirements.txt` and

### Русский

**alexei-led/ccgram** — это открытый Python‑мост между Telegram и tmux, позволяющий управлять AI‑кодерами (Claude Code, Codex CLI, Gemini CLI) прямо со смартфона: мониторить вывод, отвечать на запросы и запускать параллельные сессии. Типичный сценарий — автоматизация рутинных операций разработки (например, запуск тестов, генерация кода и планирование задач) через чат‑бота, что упрощает построение повторяемых рабочих потоков без постоянного переключения между терминалом и IDE. Проект считается почти готовым к production: активные коммиты, 129 звёзд, 37 форков, поддержка API/CLI, а также сильные сигналы экосистемы делают его надёжным кандидатом для пилотного внедрения, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
alexei-led/ccgram 是一个 Telegram ↔ tmux 桥接工具，能够在手机上实时监控 Claude Code、Codex CLI、Gemini CLI 的输出、响应提示并管理并行会话，让 AI 编码代理的控制变得像聊天一样便捷。

**价值**  
- **自动化重复操作**：把手动的代码生成、调试、任务调度等步骤搬到 Telegram，省去键盘敲击和窗口切换。  
- **统一工作流**：可将多个 AI 编码后端（Claude、Codex、Gemini）统一接入，同步监控并行会话，形成可复用的流水线。  
- **随时随地控制**：在手机上即可启动、停止、查看 AI 生成的代码，提升远程或移动办公的灵活性。

**典型接入方式**  
1. **部署 tmux 会话**：在服务器或本地机器上启动 tmux，并运行目标 CLI（如 `claude-code`、`codex`、`gemini`）。  
2. **运行 ccgram**：通过 Python 包或 Docker 镜像启动 ccgram，配置 Telegram Bot Token 与对应的 tmux 会话 ID。  
3. **使用 Telegram**：向 Bot 发送指令（如 `/run`, `/status`, `/stop`），Bot 会把指令转发到 tmux，返回的输出会实时回推到聊天窗口。  
4. **脚本化**：利用 ccgram 暴露的 CLI/API，将其嵌入 CI/CD、Cron 或自定义调度脚本，实现全自动化的 AI 编码任务。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑14，星标 129、fork 37，社区活跃。  
- **技术成熟度**：核心实现基于 Python，依赖明确（tmux、Telegram Bot API），易于审计和容器化。  
- **可评估性**：提供明确的 API/CLI 接口和语言元数据，便于快速 PoC 并集成到现有 DevOps 流程。  
- **风险**：许可证、完整的安全审计以及维护者的长期可用性仍需进一步确认，但整体信号表明该项目已具备在生产环境中试点的条件。

## 🧭 Practical evaluation

**Value:** alexei-led/ccgram helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 129 GitHub stars
- 37 forks
- updated 2026-05-14
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 86/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 43/100 |
| production | 77/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/alexei-led/ccgram) · [← Back to Automation](./README.md)</sub>
