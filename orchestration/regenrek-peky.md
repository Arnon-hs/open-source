# regenrek/peky

[![Stars](https://img.shields.io/github/stars/regenrek/peky?style=flat-square&color=yellow)](https://github.com/regenrek/peky/stargazers) [![Forks](https://img.shields.io/github/forks/regenrek/peky?style=flat-square&color=blue)](https://github.com/regenrek/peky/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> All your AI Agents like Claude Code, Codex CLI in a single TUI to keep things organized.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 144 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | Go |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-coding` `ai-coding` `cli` `multi-agent` `project-manager` `tui`

## 🎯 Categories

Orchestration · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*rekek/peky* is a Go‑based terminal UI that consolidates multiple AI agents—such as Claude, Code, and Codex CLI—into a single, organized workspace. It lets developers stitch isolated prompts and tools together into repeatable, multi‑agent workflows, making it easier to coordinate tool‑use pipelines and maintain agent memory. With 144 ★ on GitHub and recent updates, it offers a lightweight orchestration layer for AI‑augmented development.

**Value**  
- **Unified interface:** Eliminates the context‑switching overhead of juggling separate CLIs or web UIs, letting teams manage prompts, responses, and tool calls from one TUI.  
- **Workflow repeatability:** By turning ad‑hoc prompt sequences into declarative pipelines, teams can version, share, and reuse agent patterns across projects.  
- **Extensibility:** The exposed API/SDK and language‑agnostic metadata make it straightforward to plug in additional models or custom tools, supporting complex multi‑agent orchestrations.

**Practical Adoption Path**  
1. **Prototype stage:** Clone the repo, run the provided binary, and connect your existing API keys (Claude, Codex, etc.) to validate the TUI workflow on a small code‑generation or analysis task.  
2. **Integration:** Wrap the CLI calls in scripts or CI jobs, or embed the SDK in internal tooling to automate repeatable pipelines (e.g., “lint → generate tests → review”).  
3. **Standardization:** Define a repository of shared workflow definitions (YAML/JSON) that teams can version‑control, and use *peky* as the canonical execution environment across dev, QA, and ops.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑05‑12) and has a modest but growing community (144 ★, 6 forks).  
- **Stability:** Core functionality (agent orchestration, TUI, API wrappers) appears stable, but production use should include a dependency audit (Go modules, third‑party SDKs) and security review of the bundled agents.  
- **Operational considerations:** Verify licensing compatibility, monitor upstream model API rate limits, and establish a process for updating the binary to incorporate security patches. With these checks in place, *peky* is well‑suited for internal prototypes and can be hardened for production‑grade AI‑driven pipelines.

### Русский

**regenrek/peky** — это TUI‑инструмент на Go, позволяющий объединять разрозненные AI‑агенты (Claude, Code, Codex CLI и др.) в единые, повторяемые рабочие процессы с поддержкой памяти, пайплайнов инструментов и оркестрации нескольких агентов. Типичный сценарий — построение прототипов или внутренних сервисов, где требуется координация multi‑agent‑workflow и стандартизация их взаимодействия. Проект находится на среднем уровне готовности: имеет 144 звёзд, активные обновления и достаточный набор API/SDK, но перед выводом в продакшн рекомендуется проверить лицензирование, безопасность зависимостей и наличие постоянных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
`regenrek/peky` 是一款基于终端 UI（TUI）的 AI Agent 管理平台，能够在同一个界面里统一调度 Claude、Code、Codex CLI 等多种大模型及工具。它把零散的 Prompt 与命令行工具封装成可复用的工作流，让多 Agent 协作变得直观且可组织。

**价值**  
- **工作流标准化**：将分散的 Prompt 与工具链包装成可重复执行的 Agent 流程，降低重复劳动。  
- **多 Agent 协同**：支持在同一 TUI 中编排多个模型的交互，适合复杂的代码生成、调试或数据处理场景。  
- **可视化记忆管理**：提供统一的 Agent “记忆”存储与查看，帮助保持上下文一致性。  

**典型接入方式**  
1. **CLI/SDK 调用**：项目直接提供可执行的 `peky` 二进制文件和 Go SDK，业务方可通过命令行或在 Go 代码中调用相应 API。  
2. **配置文件**：使用 YAML/JSON 定义 Agent、Prompt、工具链等元数据，`peky` 在启动时读取并构建工作流。  
3. **插件式扩展**：通过实现 `Agent` 接口或注册自定义工具，可快速把内部服务或第三方 API 纳入同一 TUI。  

**生产可用性**  
- **成熟度**：当前评分 69/100，适合作为原型或内部工具使用。  
- **活跃度**：最近一次更新在 2026‑05‑12，拥有 144 Stars、6 Forks，代码基于 Go，社区规模尚小。  
- **准备度**：依赖相对明确（Go 生态），但在投入生产前建议：  
  - 完成许可证合规检查（项目未明确声明）。  
  - 进行安全审计，尤其是对外部模型 API 的凭证管理。  
  - 评估维护者响应速度，必要时自行 fork 并承担后续维护。  

总体而言，`regenrek/peky` 是一款能够快速搭建多模型协作工作流的轻量级工具，适合在内部研发或原型阶段使用；在完成安全、合规和运维准备后，可逐步推广到生产环境。

## 🧭 Practical evaluation

**Value:** regenrek/peky helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 144 GitHub stars
- 6 forks
- updated 2026-05-12
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 46/100 |
| topics | 75/100 |
| outlook | 70/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/regenrek/peky) · [← Back to Orchestration](./README.md)</sub>
