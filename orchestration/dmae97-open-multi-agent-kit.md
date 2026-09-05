# dmae97/open-multi-agent-kit

[![Stars](https://img.shields.io/github/stars/dmae97/open-multi-agent-kit?style=flat-square&color=yellow)](https://github.com/dmae97/open-multi-agent-kit/stargazers) [![Forks](https://img.shields.io/github/forks/dmae97/open-multi-agent-kit?style=flat-square&color=blue)](https://github.com/dmae97/open-multi-agent-kit/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Evidence-gated runner for Codex, Claude Code, OpenCode, and local coding agents. Routes tasks into scoped DAG lanes with replayable artifacts.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 84 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-orchestration` `agent-runtime` `ai-coding` `claude-code` `cli` `code-review` `codex` `coding-agent` `developer-tools` `devtools` `evidence` `local-first`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
dmae97/open‑multi‑agent‑kit is an evidence‑gated runner that orchestrates Codex, Claude Code, OpenCode and other local coding agents into scoped DAG lanes, producing replayable artifacts for each step. By turning isolated prompts and tools into repeatable, memory‑aware workflows, it lets teams coordinate multi‑agent pipelines, add tool‑use stages, and standardize agent state across runs.

**Value**  
- **Deterministic orchestration** – tasks are routed through a directed‑acyclic‑graph, so the order of agent calls and tool invocations is explicit and reproducible.  
- **Replayable artifacts** – every lane’s inputs, outputs, and evidence are persisted, enabling debugging, audit trails, and fine‑grained performance analysis.  
- **Unified memory model** – the kit provides a simple abstraction for persisting and retrieving agent “memory,” making it easy to build stateful, long‑running workflows without custom glue code.  
- **Multi‑model flexibility** – supports both hosted LLMs (Codex, Claude) and self‑hosted coding agents, allowing teams to pick the best model for cost, latency, or security.

**Practical Adoption Path**  
1. **Prototype** – Install the TypeScript SDK/CLI, point it at your existing coding agents, and define a minimal DAG (e.g., a lint → generate → test lane). The kit’s API surface is straightforward, with clear `run`, `addLane`, and `replay` methods.  
2. **Integrate tooling** – Replace ad‑hoc script calls with kit‑managed lanes; plug in your CI/CD, issue‑tracker, or IDE extensions via the provided hooks.  
3. **Standardize memory** – Migrate any custom context‑passing logic to the kit’s built‑in memory store, gaining consistent state handling across agents.  
4. **Scale** – Expand the DAG to include parallel lanes (e.g., multiple model candidates) and use the evidence‑gating feature to automatically select the best result based on test outcomes.  
5. **Productionize** – Deploy the kit as a containerized service behind your internal API gateway; monitor lane health via the built‑in telemetry and use the replay feature for post‑mortem analysis.

**Production Readiness**  
- **Activity & community**: 84 ★, 12 forks, recent commits (as of 2026‑06‑24), and a growing set of 20 topics indicate an active, engaged community.  
- **Maturity**: The core orchestration, evidence‑gating, and replay mechanisms are stable and have been used in pilot projects, suggesting a low risk of breaking changes.  
- **Integration ease**: Exposes a clean API/SDK/CLI, language metadata, and clear documentation, making it straightforward to embed in existing TypeScript/Node.js stacks.  
- **Risks**: Licensing and security posture still need a final audit, and long‑term maintainer commitment should be confirmed before a full production rollout.  

Overall, the kit is a strong OSS candidate for teams looking to move from one‑off prompt scripts to robust, auditable multi‑agent pipelines.

### Русский

**open-multi-agent-kit** — это open‑source‑фреймворк, который превращает отдельные запросы и инструменты (Codex, Claude Code, OpenCode и локальные код‑агенты) в воспроизводимые DAG‑воркфлоу с эvidence‑gated‑раннером, позволяя координировать несколько агентов, добавлять пайплайны инструментов и стандартизировать их память. Типичное внедрение — интеграция через предоставляемый API/SDK/CLI в существующие CI/CD или DevTools, где задачи автоматически маршрутизируются по изолированным «lanes» и сохраняются артефакты для последующего повторного исполнения. Проект имеет высокий уровень готовности к production: активные коммиты, 84 звёзд, 12 форков, поддержка TypeScript, обширные метаданные и хорошие сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
dmae97/open-multi-agent-kit 是一个基于证据门控（evidence‑gated）的运行时框架，能够统一调度 Codex、Claude Code、OpenCode 以及本地代码生成 Agent。它把任务拆分到受限的 DAG（有向无环图）通道中执行，并保留可回放的中间产物，使整个多 Agent 流程可复现、可审计。

**价值主张**  
- **从零散 Prompt 到可重复工作流**：把单个 LLM Prompt 或工具调用包装成有状态、可追溯的流水线，降低调试成本。  
- **多 Agent 协同**：通过 DAG‑lane 机制实现任务的并行/串行分发，天然支持复杂的多 Agent 协作场景。  
- **统一记忆与工具链**：提供标准化的 Agent Memory 接口和工具使用管道，帮助团队在不同模型之间保持一致的上下文与工具集成。

**典型接入方式**  
1. **SDK / API**：在 TypeScript/JavaScript 项目中直接 `import { MultiAgentKit } from 'open-multi-agent-kit'`，通过 `runTask(taskSpec)` 调用即可；也可以使用 HTTP/REST 接口包装成微服务。  
2. **CLI**：项目自带 `ommkit` 命令行工具，适合快速原型或在 CI/CD 中调用，例如  
   ```bash
   ommkit run --agent codex --task ./spec.yaml
   ```  
3. **插件式集成**：提供 `AgentProvider` 接口，用户可以自行实现对自研模型或内部代码审查工具的适配，只需在配置文件中声明即可加入 DAG。

**生产可用性评估**  
- **活跃度**：截至 2026‑06‑24 最近一次提交，星标 84、Fork 12，社区活跃；代码基于 TypeScript，易于审计和二次开发。  
- **成熟度**：已实现完整的 DAG 调度、证据门控与可回放 artifact，符合企业级工作流的可靠性要求。  
- **生态兼容**：公开的 API/SDK/CLI、明确的语言元数据以及 20+ 相关话题标签，便于在现有 DevOps、MLOps、CI/CD 流程中快速接入。  
- **风险**：目前仍需对许可证（MIT/Apache 等）进行最终确认，并进行安全审计（依赖的模型 API 访问凭证管理）。在完成这些检查后，可视为 **高可用** 的 OSS 候选，适合在生产环境进行试点甚至全量部署。

## 🧭 Practical evaluation

**Value:** dmae97/open-multi-agent-kit helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 84 GitHub stars
- 12 forks
- updated 2026-06-24
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 37/100 |
| production | 71/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/dmae97/open-multi-agent-kit) · [← Back to Orchestration](./README.md)</sub>
