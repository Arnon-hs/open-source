# kevinelliott/agentpipe

[![Stars](https://img.shields.io/github/stars/kevinelliott/agentpipe?style=flat-square&color=yellow)](https://github.com/kevinelliott/agentpipe/stargazers) [![Forks](https://img.shields.io/github/forks/kevinelliott/agentpipe?style=flat-square&color=blue)](https://github.com/kevinelliott/agentpipe/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> A CLI/TUI app that orchestrates multi-agent conversations by enabling different AI CLI tools (Claude Code, Gemini, Qwen, etc.) to communicate in shared rooms.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 136 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | Go |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `ai-agents-automation` `ai-agents-cli` `claude-code` `cli-app` `cursor-ai` `factory-ai` `gemini-cli` `grok` `qwen-code` `tui-app`

## 🎯 Categories

Orchestration · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
*agentpipe* is a Go‑based CLI/TUI that lets multiple AI agents (Claude Code, Gemini, Qwen, etc.) converse in shared “rooms,” turning ad‑hoc prompts into repeatable, orchestrated workflows. By wiring together disparate AI‑CLI tools, it provides a lightweight orchestration layer for multi‑agent coordination, tool‑use pipelines, and persistent agent memory.

**Value**  
- **Workflow unification** – Isolated AI tools become collaborative agents that can pass messages, results, and context to one another without writing custom glue code.  
- **Repeatability & standardisation** – Defined rooms act as reusable “conversation scripts,” making it easy to version, test, and share complex agent pipelines across teams.  
- **Rapid prototyping** – The TUI gives immediate visual feedback on message flow, helping developers iterate on multi‑agent designs faster than building bespoke APIs.

**Practical Adoption Path**  
1. **Pilot the CLI** – Install the binary (`go install github.com/kevinelliott/agentpipe@latest`) and spin up a test room with two agents (e.g., Claude and Gemini) to verify basic messaging.  
2. **Integrate existing AI‑CLI tools** – Add the required agent executables to the `agentpipe` config (JSON/YAML). Because the tool works through standard input/output, most AI‑CLI wrappers can be dropped in with minimal adaptation.  
3. **Define reusable pipelines** – Encode common sequences (e.g., “code generation → static analysis → refactor”) as room scripts or shell wrappers, committing them to a repository for team consumption.  
4. **Persist memory** – Enable the built‑in memory store or hook an external KV store (Redis, SQLite) to keep context across sessions, then promote the setup to a staging environment.  
5. **Scale to production** – Containerise the agentpipe process, expose its API/CLI via a sidecar or internal service, and integrate with CI/CD pipelines for automated execution of agent workflows.

**Production Readiness**  
- **Activity & community** – 136 ★, 23 forks, recent commits (last updated 2026‑06‑27), and a Go codebase make the project easy to audit and extend.  
- **Ecosystem fit** – The tool exposes clear API/SDK/CLI signals, works with any language‑agnostic AI CLI, and already supports multiple major models, reducing integration friction.  
- **Stability** – The core orchestration logic is small and self‑contained; the primary risk areas are licensing verification, security hardening of the underlying AI binaries, and ensuring maintainers remain active.  
- **Readiness level** – High for an OSS candidate; it is mature enough for a serious pilot in internal tooling or a production‑adjacent service, provided the final security and license review is completed.

### Русский

Резюме проекта kevinelliott/agentpipe:

**Польза проекта**: kevinelliott/agentpipe позволяет координировать работу нескольких агентов AI, объединив их в общую систему, что позволяет создавать повторяемые потоки работы агентов.

**Типовой сценарий внедрения**: проект может быть использован для координации мульти-агентных потоков, добавления пайплайнов для использования инструментов и стандартизации памяти агентов.

**Уровень готовности к production**: проект имеет высокий уровень готовности к production, что подтверждается его частотой обновлений, количеством звезд на GitHub и активностью сообщества.

### 中文

**项目简介（2‑3 句）**  
kevinelliott/agentpipe 是一款基于 Go 的 CLI/TUI 工具，能够在同一个“房间”里让多种 AI CLI（如 Claude Code、Gemini、Qwen 等）相互对话并协同工作。它把原本孤立的提示和工具串联成可重复的多代理工作流，从而实现复杂的自动化与编排。

**价值**  
- **统一编排**：将不同模型和工具的交互抽象为“代理”，在共享空间中自由通信，极大降低多模型协作的集成成本。  
- **可复用工作流**：一次配置的对话脚本可以保存、版本化并在不同环境中重复执行，适合 CI/CD、数据处理或研发辅助等场景。  
- **标准化记忆与工具使用**：内置 agent memory 和工具调用管道，帮助保持上下文一致性并实现自动化工具链（如代码生成 → 编译 → 测试）。

**典型接入方式**  
1. **CLI 直接调用**：在终端或脚本中使用 `agentpipe run <room-id> --agent claude --agent gemini …` 启动多代理会话。  
2. **SDK/API**：项目提供 Go 包（`github.com/kevinelliott/agentpipe/pkg`），可在自研服务中嵌入 `NewRoom()`、`AddAgent()`、`SendMessage()` 等函数，实现程序化编排。  
3. **TUI 交互**：通过 `agentpipe tui` 启动基于终端的图形界面，适合调试和手动演示。  
4. **容器化部署**：官方 Dockerfile 可直接构建镜像，配合 Kubernetes Job 或 CronJob 在生产环境中以批处理方式运行预定义工作流。

**生产可用性**  
- **活跃度**：截至 2026‑06‑27，项目最近一次提交，拥有 136 星、23 Fork，且主要语言为 Go，社区活跃度良好。  
- **成熟度**：实现了完整的 API/CLI、插件化的 Agent 接口以及持久化记忆模块，具备高可测性和可扩展性。  
- **风险**：目前未发现重大元数据或许可证冲突；仍需对依赖的 AI 服务（Claude、Gemini、Qwen 等）的访问凭证、配额以及安全审计进行最终确认。  
- **适配度**：由于提供标准化的信号（API、SDK、CLI）以及明确的主题标签，评估与现有 CI/CD、微服务或内部研发平台的集成成本相对低，已可作为 OSS 候选进入正式生产试点。

## 🧭 Practical evaluation

**Value:** kevinelliott/agentpipe helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 136 GitHub stars
- 23 forks
- updated 2026-06-27
- primary language: Go
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 42/100 |
| production | 57/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/kevinelliott/agentpipe) · [← Back to Orchestration](./README.md)</sub>
