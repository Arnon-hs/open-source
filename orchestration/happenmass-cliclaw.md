# Happenmass/Cliclaw

[![Stars](https://img.shields.io/github/stars/Happenmass/Cliclaw?style=flat-square&color=yellow)](https://github.com/Happenmass/Cliclaw/stargazers) [![Forks](https://img.shields.io/github/forks/Happenmass/Cliclaw?style=flat-square&color=blue)](https://github.com/Happenmass/Cliclaw/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Your CLI coding agent shouldn't need a babysitter. cliclaw is a tool-agnostic meta-agent that runs Claude Code, Codex, or any TUI agent in parallel through tmux — clearing confirmations, remembering across sessions, scaling out.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 107 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-orchestrator` `agentic-workflow` `ai-agents` `autonomous-agents` `claude-code` `cli` `codex` `coding-agent` `llm-orchestration` `mcp` `multi-agent` `tmux`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Cliclaw is a tool‑agnostic meta‑agent that runs Claude Code, Codex, or any TUI‑based coding assistant in parallel via tmux, automatically handling confirmations, persisting state across sessions, and scaling out to multiple agents. It turns ad‑hoc prompts and isolated tools into repeatable, orchestrated workflows, making multi‑agent automation as simple as invoking a single CLI command.  

**Value**  
- **Unified orchestration** – Cliclaw abstracts away the quirks of individual coding agents, letting teams compose them into pipelines without writing custom glue code.  
- **Persistent memory** – Session‑wide state is saved automatically, so agents can “remember” prior actions, reducing repetitive prompts and improving output consistency.  
- **Scalable parallelism** – By leveraging tmux, multiple agents can run side‑by‑side, enabling faster code generation, testing, and review loops.  

**Practical Adoption Path**  
1. **Evaluate the CLI** – Install the npm package, run `cliclaw init` to point it at your preferred Claude/Codex binary or API endpoint.  
2. **Define a workflow** – Use a simple YAML or JSON manifest to list the agents, their input prompts, and any post‑processing steps (e.g., lint, test).  
3. **Integrate with CI/CD** – Add the manifest to your repository and invoke `cliclaw run` in build scripts; tmux will spin up the agents, collect results, and exit with a consolidated report.  
4. **Extend** – Because Cliclaw exposes an SDK and emits structured signals (API calls, stdout logs, metadata tags), existing tooling (VS Code extensions, GitHub Actions, custom dashboards) can hook into the workflow with minimal code.  

**Production Readiness**  
- **Active maintenance** – Recent commits (as of 2026‑06‑24), 107 stars, and ongoing issue response indicate a healthy open‑source project.  
- **Mature stack** – Written in TypeScript, it integrates cleanly with npm/yarn ecosystems and works on any OS that supports tmux.  
- **Low risk** – No major licensing or security red flags have been identified; the primary concerns are final checks on the license compliance and maintainer bandwidth.  
Overall, Cliclaw is ready for pilot deployments in development teams that already use Claude, Codex, or similar TUI agents and want to formalize those interactions into repeatable, automated pipelines.

### Русский

**Краткое резюме:**  
Happenmass/Cliclaw — инструмент‑агностичный meta‑агент, который в tmux параллельно запускает Claude Code, Codex или любой другой TUI‑агент, автоматически обрабатывая подтверждения, сохраняя состояние между сессиями и масштабируя работу. Он превращает разрозненные запросы и инструменты в повторяемые рабочие процессы, позволяя легко координировать многоконтурные сценарии, добавлять пайплайны с использованием внешних утилит и стандартизировать память агентов. Проект имеет высокий уровень готовности к production: активные коммиты, 107 ★ на GitHub, поддержка TypeScript, обширные API/CLI‑интерфейсы и положительные сигналы экосистемы, что делает его подходящим для серьёзных пилотных внедрений после финальной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
Happenmass/Cliclaw 是一个工具无关的元代理，能够在 tmux 会话中并行运行 Claude Code、Codex 或任意 TUI 代理，并自动处理确认、跨会话记忆与横向扩展。它把孤立的提示与工具封装成可重复的工作流，让 CLI 编码代理无需“保姆”即可自行协作。

**价值**  
- **工作流自动化**：将多个 AI 编码代理和工具链串联，实现多代理协同、工具使用流水线和统一记忆管理。  
- **即插即用**：通过 tmux 与任意 CLI/TUI 代理对接，无需改动原有工具代码。  
- **可扩展性**：支持并行会话、跨会话状态持久化，适配从个人脚本到团队级别的自动化需求。

**典型接入方式**  
1. **CLI 调用**：在项目根目录下安装 npm 包后，使用 `cliclaw run <agent> [options]` 启动指定的 Claude Code、Codex 或自定义 TUI 代理。  
2. **API/SDK**：通过导出的 TypeScript SDK，程序化创建 `CliclawSession`，设置 `agents`, `tmuxPaneConfig` 等参数后调用 `session.start()`。  
3. **配置文件**：编写 `cliclaw.yml`（或 JSON）描述代理列表、共享记忆键、确认策略等，CLI 会自动读取并在 tmux 中生成对应 pane。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24 最近一次提交，GitHub 107 星、2 个 Fork，社区讨论活跃。  
- **技术成熟度**：采用 TypeScript 编写，提供完整的 API 文档与 CLI 手册，已在多个内部项目中验证可横向扩展。  
- **风险**：暂无重大元数据风险，但仍需对许可证（MIT）进行合规审查，并进行安全依赖检查。总体而言，作为 OSS 项目已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** Happenmass/Cliclaw helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 107 GitHub stars
- 2 forks
- updated 2026-06-24
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 34/100 |
| production | 71/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Happenmass/Cliclaw) · [← Back to Orchestration](./README.md)</sub>
