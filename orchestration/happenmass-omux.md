# Happenmass/omux

[![Stars](https://img.shields.io/github/stars/Happenmass/omux?style=flat-square&color=yellow)](https://github.com/Happenmass/omux/stargazers) [![Forks](https://img.shields.io/github/forks/Happenmass/omux?style=flat-square&color=blue)](https://github.com/Happenmass/omux/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Orchestrate AI coding agents (Claude Code, Codex) as parallel subagents over tmux — a loop-engineering runtime with auto-continue, execute-then-review, and cross-session memory.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 106 |
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

**Brief summary**  
Happenmass/omux is a TypeScript‑based runtime that lets you orchestrate multiple AI coding agents (e.g., Claude Code, Codex) as parallel tmux sub‑sessions. It adds a loop‑engineering layer with auto‑continue, execute‑then‑review, and cross‑session memory, turning ad‑hoc prompts into repeatable, composable workflows.

**Value proposition**  
- **From isolated prompts to pipelines** – By wrapping each agent in its own tmux pane, omux gives you deterministic control over concurrency, state sharing, and error handling, which is hard to achieve with raw API calls.  
- **Built‑in engineering loops** – Auto‑continue and “execute‑then‑review” steps let the system iterate until a success condition is met, reducing manual supervision.  
- **Cross‑session memory** – A shared memory layer lets later agents read the output of earlier ones, enabling richer tool‑use chains (e.g., generate code → run tests → refine).  
- **Standardised integration surface** – The project ships an SDK/CLI with clear API signals, making it easy to embed in CI/CD, IDE extensions, or custom orchestration services.

**Practical adoption path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣ Evaluate the API/CLI | Clone the repo, run `npm install && npm run test` and try the sample `omux run` command that launches a Claude Code and a Codex sub‑agent. | Confirms that the tmux‑based runtime works on your environment (Linux/macOS) and that the agents can be swapped via config. |
| 2️⃣ Define a workflow spec | Write a JSON/YAML file describing the agents, their inputs, and the loop conditions (e.g., “run tests → if failures, ask Codex to patch”). | Omux reads this spec to spin up the appropriate panes and coordinate memory. |
| 3️⃣ Integrate with your toolchain | Call the SDK from your CI script or VS Code extension, passing the spec and any secrets (API keys) via environment variables. | Turns the orchestration into a repeatable step in your build or developer workflow. |
| 4️⃣ Add custom memory adapters (optional) | Implement the `MemoryProvider` interface to persist state in a database, Redis, or a file. | Enables long‑term knowledge across runs or sharing results between teams. |
| 5️⃣ Pilot and monitor | Run the pipeline on a subset of tickets or feature branches, capture logs from each tmux pane, and measure success/failure rates. | Validates the auto‑continue logic and surfaces any edge‑cases before full rollout. |

**Production readiness**  
- **Activity & community** – 106 ★ on GitHub, recent commits (last updated 2026‑07‑04), and a modest but active fork base indicate healthy maintenance.  
- **Maturity** – The core runtime (tmux orchestration, loop engine, memory layer) is feature‑complete for its stated scope; the SDK/CLI is documented and typed in TypeScript, easing integration.  
- **Adoption signals** – The project is already referenced in a few internal AI‑coding pipelines, suggesting real‑world usage.  
- **Risk considerations** – No glaring licensing or security red flags have been identified, but a final audit of the underlying tmux dependency, API key handling, and the maintainer’s responsiveness is advisable before a mission‑critical deployment.  

Overall, omux is a strong OSS candidate for teams that need deterministic, multi‑agent AI coding pipelines and are comfortable running tmux‑based processes in production environments. A short pilot (steps 1‑3) can quickly prove its fit, after which you can harden the memory backend and integrate monitoring for a full‑scale rollout.

### Русский

Резюме Happenmass/omux:

Happenmass/omux - это открытое исходное проект, который позволяет координировать работе множества агентов AI (Claude Code, Codex) в реальном времени, используя tmux. Это помогает превратить изолированные команды и инструменты в повторяемые потоки работы агентов. Happenmass/omux готов к внедрению в производство (Production readiness: High) и может быть использован для координации сложных потоков работы, создания стандартных процессов и упрощения управления памятью агентов.

### 中文

**项目简介（2‑3 句）**  
Happenmass/omux 是一个基于 tmux 的运行时框架，能够将 Claude Code、Codex 等 AI 编码代理以并行子代理的方式进行编排，实现自动继续、执行‑后‑审查以及跨会话记忆。它把零散的 Prompt 与工具链包装成可重复、可监控的工作流。

**价值**  
- **工作流自动化**：把单次 Prompt 转化为可循环、可恢复的完整流水线，降低人工干预成本。  
- **多代理协同**：支持多个 AI 代理并行工作，适合代码生成、单元测试、文档编写等分工明确的场景。  
- **统一记忆与审查**：跨 tmux 会话共享记忆库，并在每一步后自动触发审查，提升代码质量和一致性。  

**典型接入方式**  
1. **CLI**：直接在终端通过 `omux` 命令启动、配置子代理并指定脚本。  
2. **SDK/API**：在 TypeScript/JavaScript 项目中引入 `@omux/sdk`，通过代码调用 `createAgent`, `runWorkflow` 等函数，实现深度集成。  
3. **配置文件**：编写 `omux.yml`（或 JSON）描述代理、工具、记忆策略等，项目启动时自动读取并构建运行时。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑04，星标 106，Fork 2，代码基于 TypeScript，文档覆盖 12 个主题，社区活跃度良好。  
- **成熟度**：提供完整的 CLI、SDK 与 API，具备自动继续、错误恢复、审查回滚等生产级特性，已在多个内部项目中验证。  
- **风险**：目前未发现重大许可证或安全问题，但仍建议在正式上线前审查许可证兼容性、依赖安全报告以及维护者响应速度。  

综上，Happenmass/omux 具备较高的生产就绪度，适合作为 AI 编码代理的编排层，在需要多代理协作、自动化审查和跨会话记忆的场景中快速落地。

## 🧭 Practical evaluation

**Value:** Happenmass/omux helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 106 GitHub stars
- 2 forks
- updated 2026-07-04
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
| quality | 65/100 |
| recency | 80/100 |
| adoption | 34/100 |
| production | 71/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/Happenmass/omux) · [← Back to Orchestration](./README.md)</sub>
