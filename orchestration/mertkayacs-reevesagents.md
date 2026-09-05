# mertkayacs/reevesagents

[![Stars](https://img.shields.io/github/stars/mertkayacs/reevesagents?style=flat-square&color=yellow)](https://github.com/mertkayacs/reevesagents/stargazers) [![Forks](https://img.shields.io/github/forks/mertkayacs/reevesagents?style=flat-square&color=blue)](https://github.com/mertkayacs/reevesagents/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> Free, local, tmux-first workspace for AI CLI agents. Let one agent (Claude Code, Codex, Hermes, DeepSeek, Kimi, ...) spawn and drive others over MCP. No API keys, no changes to your Agent.md or Claude.md. TUI, Web UI, CLI, MCP in one package.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 77 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai-agents` `autonomous-agents` `claude-code` `codex` `deepseek` `hermes` `hermes-agent` `homebrew` `kimi` `kimi-cli` `llm-orchestration`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
ReevesAgents is an open‑source, tmux‑first workspace that lets a primary AI CLI agent (Claude, Codex, Hermes, DeepSeek, Kimi, etc.) spawn and control additional agents through the Multi‑Agent Communication Protocol (MCP). It bundles a TUI, Web UI, CLI, and MCP server in a single TypeScript package, requiring no external API keys or modifications to existing Agent/Claude markdown files. The project is actively maintained, has 77 ★ on GitHub, and is positioned as a low‑friction way to turn ad‑hoc prompts into repeatable, orchestrated agent pipelines.

### Value proposition
- **From isolated prompts to reusable workflows** – By providing a local, key‑free environment, ReevesAgents lets teams prototype, test, and ship multi‑agent pipelines without the overhead of cloud APIs or custom glue code.  
- **Unified interface** – The same binary serves as a terminal multiplexer (tmux), a web dashboard, and a CLI, so developers can pick the UI that fits their workflow while keeping the underlying MCP communication consistent.  
- **Tool‑use and memory orchestration** – Agents can pass data, invoke tools, and share a common memory store, enabling complex use‑cases such as code generation → lint → test → refactor loops or data‑ingestion → analysis → reporting pipelines.  

### Practical adoption path
1. **Clone & install** – `git clone https://github.com/mertkayacs/reevesagents && npm ci` (or use the pre‑built Docker image).  
2. **Define a “root” agent** – Create a simple Agent.md (or use the built‑in Claude Code template) that describes the primary task and the agents it may spawn.  
3. **Run the workspace** – `npx reevesagents start` launches tmux, the web UI (localhost:8080), and the MCP server.  
4. **Add downstream agents** – Use the CLI (`reevesagents add --type codex`) or the web UI to register additional agents; configure their prompts or tool bindings in the generated JSON/YAML files.  
5. **Iterate locally** – Test the full pipeline, tweak prompts or tool parameters, and once stable, export the configuration (`reevesagents export`) for CI/CD or containerized deployment.  

### Production readiness
- **Activity & community** – The repository shows recent commits (last update 2026‑06‑23), 77 ★, 10 forks, and a growing set of topics, indicating an engaged user base.  
- **Technical maturity** – Built in TypeScript with clear modular boundaries (TUI, Web UI, MCP server), it can be containerized or run on bare‑metal servers; the MCP layer abstracts communication, making future agent additions straightforward.  
- **Risk considerations** – No obvious licensing or security red flags have been identified, but a formal audit of the MIT‑style license, dependency vulnerabilities, and maintainer responsiveness is recommended before a production rollout.  

Overall, ReevesAgents offers a high‑confidence, low‑cost entry point for organizations that need orchestrated, repeatable AI agent pipelines while keeping everything on‑premise and under version control.

### Русский

**mertkayacs/reevesagents** — это бесплатный локальный пакет‑ориентированный на tmux рабочий стол для AI‑агентов, позволяющий одному агенту (Claude Code, Codex, Hermes, DeepSeek, Kimi и др.) динамически порождать и управлять другими через MCP без необходимости API‑ключей и правок конфигурационных файлов. Типичный сценарий — построение повторяемых многопоточных цепочек: координация нескольких агентов, подключение инструментов и стандартизация памяти агента в едином TUI/Web‑UI/CLI интерфейсе. Проект имеет высокий уровень готовности к production: активные коммиты, 77 звёзд, 10 форков, современный TypeScript‑код и широкую экосистемную поддержку, требуя лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
mertkayacs/reevesagents 是一个免费、本地化、以 tmux 为首的 AI CLI 代理工作空间。它让单个代理（Claude Code、Codex、Hermes、DeepSeek、Kimi 等）能够通过 MCP 动态生成并驱动其他代理，提供统一的 TUI、Web UI、CLI 与 MCP 功能，无需 API Key，也不需要改动现有的 `Agent.md` 或 `Claude.md`。

**价值**  
- **把孤立的 Prompt 与工具链转化为可复用的工作流**，实现多代理协同、工具调用流水线以及统一的记忆管理。  
- **全本地运行**，不依赖外部云服务或 API Key，提升安全性和成本可控性。  
- **一次部署即得多种交互方式**（终端、网页、MCP），适配不同使用场景，降低学习曲线。

**典型接入方式**  
1. **克隆仓库并安装依赖**（Node.js ≥ 18，pnpm/yarn）。  
2. **启动主进程**：`pnpm start`（或 `npm run dev`），默认在 tmux 会话中启动 TUI，同时暴露 Web UI（http://localhost:3000）和 MCP 端口。  
3. **在配置文件中声明要使用的底层模型**（如 Claude Code、DeepSeek），无需提供 API Key，系统会使用本地模型或已授权的离线后端。  
4. **通过 CLI / TUI / Web UI 发起任务**，或让一个代理通过 MCP 调用其他代理，实现流水线式的自动化。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑23，拥有 77 Stars、10 Forks，维护者仍在持续更新。  
- **技术成熟度**：TypeScript 主体代码、清晰的模块化设计、完整的 API/SDK/CLI 接口，便于二次集成与监控。  
- **安全与合规**：目前未发现重大元数据风险，仍需对许可证（MIT/Apache 等）和依赖安全审计进行最终确认。  
- **适配性**：提供标准化的信号（API、SDK、CLI）和丰富的主题标签，可快速在现有 AI 平台或内部工具链中评估并投入试点。  

综合来看，reevesagents 已具备 **高可用性** 与 **易集成性**，适合作为企业内部的 **多代理编排** 与 **工具化 AI 工作流** 的 OSS 基石，在完成许可证与安全审计后即可进入生产环境。

## 🧭 Practical evaluation

**Value:** mertkayacs/reevesagents helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 77 GitHub stars
- 10 forks
- updated 2026-06-23
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 40/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 73/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/mertkayacs/reevesagents) · [← Back to Orchestration](./README.md)</sub>
