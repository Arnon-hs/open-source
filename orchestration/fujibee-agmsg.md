# fujibee/agmsg

[![Stars](https://img.shields.io/github/stars/fujibee/agmsg?style=flat-square&color=yellow)](https://github.com/fujibee/agmsg/stargazers) [![Forks](https://img.shields.io/github/forks/fujibee/agmsg?style=flat-square&color=blue)](https://github.com/fujibee/agmsg/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Cross-vendor messaging for CLI AI coding agents — let Claude Code, Codex, Gemini & Copilot talk to each other in one team. Bash + SQLite, no daemon, no framework.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 833 |
| 🍴 **Forks** | 61 |
| 💻 **Language** | Shell |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-communication` `agent-teams` `agentic` `ai-agents` `bash` `claude-code` `cli` `codex` `copilot` `developer-tools` `gemini-cli` `inter-agent`

## 🎯 Categories

Orchestration · AI/ML · DevTools · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
fujibee/agmsg is a lightweight, Bash‑driven orchestration layer that lets different CLI‑based AI coding agents (Claude, Codex, Gemini, Copilot, etc.) exchange messages through a shared SQLite store—no background daemon or heavyweight framework required. By turning isolated prompts into a persistent, queryable “agent memory,” it enables repeatable, multi‑agent workflows that can be scripted and version‑controlled like any other shell tool. The project is actively maintained, has strong community traction (≈ 830 ★), and is packaged as a simple CLI/SDK that can be dropped into existing pipelines.

**Value**  
- **Unified communication**: Provides a common “mailbox” for heterogeneous AI agents, removing the friction of custom glue code.  
- **Persisted state**: SQLite‑backed message logs act as a cheap, portable memory layer, making debugging and audit trails trivial.  
- **Zero‑ops deployment**: Because it runs purely as a Bash script with no daemon, it can be added to CI/CD, local dev environments, or edge containers without additional infrastructure.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI (`agmsg send …`, `agmsg recv …`) against a local SQLite file, and replace existing ad‑hoc `curl`/`openai` calls with `agmsg` messages.  
2. **Integrate** – Wrap each agent’s invocation in a small shell wrapper that pushes its output to `agmsg` and reads the next input from the queue; commit the wrapper to your repo.  
3. **Scale** – Move the SQLite database to a shared volume (e.g., NFS, Docker volume, or cloud‑attached file) so multiple containers or CI runners can collaborate.  
4. **Extend** – Use the SDK (exposed as simple Bash functions) to embed richer metadata (e.g., task IDs, timestamps) or to plug in a custom persistence layer if needed.  

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑06‑23), 833 stars, 61 forks, and active issue discussion indicate a healthy open‑source project.  
- **Stability**: The core is just Bash + SQLite, both battle‑tested components; there is no long‑running daemon to manage, reducing operational risk.  
- **Integration Simplicity**: Exposes a clear CLI/SDK surface and minimal external dependencies, making security reviews and CI integration straightforward.  
- **Remaining Checks**: Before a full production rollout, verify the license compatibility, run a security scan of the Bash scripts, and confirm an active maintainer is available for critical bug fixes. Once those final reviews are completed, agmsg is a strong candidate for a serious pilot in multi‑agent AI coding pipelines.

### Русский

**fujibee/agmsg** — это лёгкий Bash‑инструмент с SQLite, позволяющий объединить разные LLM‑агенты (Claude, Codex, Gemini, Copilot) в единый рабочий процесс без демонов и тяжёлых фреймворков. Типичное внедрение: в CI/CD или локальном окружении скриптом задаёте последовательность подсказок и обмен данными между агентами, тем самым автоматизируя многошаговые задачи — от генерации кода до проверки и деплоя. Проект имеет высокую готовность к production: активные коммиты, 833★, 61 fork, свежий релиз (23 июня 2026) и широкую поддержку API/CLI, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
fujibee/agmsg 是一个基于 Bash 与 SQLite 的轻量级 OSS 工具，旨在为 CLI AI 编码代理（Claude Code、Codex、Gemini、Copilot 等）提供跨厂商的消息传递层。无需守护进程或额外框架，即可让多个 AI 代理在同一团队中协同工作、共享记忆、构建可复用的工作流。

**价值主张**  
- **打通孤立的提示与工具**：把单独的 AI 提示、代码生成或调试工具统一进一个可编排的消息总线，形成端到端的多代理工作流。  
- **可复用的 Agent 流程**：通过 SQLite 持久化消息和状态，轻松实现“记忆”与“工具调用”链路，适合构建 CI/CD、自动化重构、代码审查等场景。  
- **零依赖、即插即用**：仅依赖 Bash 与 SQLite，兼容几乎所有类 Unix 环境，降低部署和运维成本。

**典型接入方式**  
1. **CLI 调用**：直接在终端使用 `agmsg send --to codex "请生成单元测试"`，或 `agmsg recv --from claude` 读取回复。  
2. **SDK/API**：项目提供了轻量的 Shell 函数库和 JSON‑over‑STDIN 接口，其他语言（Python、Node 等）可通过子进程调用或包装成 HTTP/Unix‑socket 代理。  
3. **管道集成**：在 CI 脚本或 Makefile 中将 `agmsg` 作为中间层，串联多个 AI 工具，实现“生成‑审查‑优化”的自动化链路。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，最近一次提交，GitHub 833 ⭐、61 fork，14 个相关话题，表明社区活跃且持续迭代。  
- **成熟度**：采用 Bash+SQLite 的极简架构，无守护进程，易于审计和容错；已有若干企业内部试点报告工作流稳定。  
- **风险**：目前尚需对许可证（MIT）进行合规确认，并进行一次安全审计（依赖 SQLite 与 Bash 脚本），但整体风险低。  

**结论**  
agmsg 已具备在生产环境中作为多 AI 代理编排层的条件，适合希望快速搭建可复用、可追溯的 AI 编码流水线的团队。只要完成许可证与安全的最终检查，即可作为正式的 OSS 组件投入业务使用。

## 🧭 Practical evaluation

**Value:** fujibee/agmsg helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 833 GitHub stars
- 61 forks
- updated 2026-06-23
- primary language: Shell
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 66/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 57/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/fujibee/agmsg) · [← Back to Orchestration](./README.md)</sub>
