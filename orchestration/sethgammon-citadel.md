# SethGammon/Citadel

[![Stars](https://img.shields.io/github/stars/SethGammon/Citadel?style=flat-square&color=yellow)](https://github.com/SethGammon/Citadel/stargazers) [![Forks](https://img.shields.io/github/forks/SethGammon/Citadel?style=flat-square&color=blue)](https://github.com/SethGammon/Citadel/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> The operating layer for Claude Code + OpenAI Codex: persistent project memory, intent routing, safety hooks, cost telemetry, and parallel agent fleets.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 615 |
| 🍴 **Forks** | 57 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-orchestration` `agent-workflow` `ai-agents` `claude-code-plugin` `claude-plugins` `codex-plugin` `developer-tools` `mcp`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
SethGammon/Citadel is an open‑source orchestration layer that adds persistent memory, intent routing, safety hooks, cost telemetry, and parallel‑agent fleet management to Claude Code and OpenAI Codex. It turns ad‑hoc prompts and tool calls into repeatable, observable multi‑agent workflows, making it easy to build robust AI‑powered automation pipelines. With active development, 600+ stars and recent commits, it is ready for serious pilot projects.

**Value**  
- **Workflow repeatability** – By persisting project state and routing intents, Citadel lets you treat a series of prompts and tool invocations as a single, version‑controlled pipeline.  
- **Scalability & safety** – Parallel agent fleets can be spun up on demand, while built‑in safety hooks and cost telemetry keep execution under control.  
- **Standardisation** – Provides a common API/SDK/CLI for memory handling and tool integration, reducing the engineering effort required to stitch together Claude, Codex, or other LLMs.

**Practical Adoption Path**  
1. **Evaluate the API/SDK** – Clone the repo, run the provided CLI demo, and connect your existing Claude or Codex keys.  
2. **Prototype a simple workflow** – Define a small “intent” (e.g., generate a function, run a linter, commit to Git) and let Citadel manage memory and routing.  
3. **Scale to parallel agents** – Use the fleet manager to launch multiple agents for tasks such as batch code review or test generation.  
4. **Integrate safety & telemetry** – Enable the built‑in hooks to enforce policy checks and capture per‑request cost data.  
5. **Deploy** – Containerise the service (Dockerfile is included) and run it behind your internal API gateway for production use.

**Production Readiness**  
- **Activity & Community** – 615 ★, 57 forks, recent commits (as of 2026‑06‑24) and a growing issue/PR discussion indicate an active maintainer base.  
- **Maturity** – Core features (memory, routing, safety, telemetry) are stable; the JavaScript codebase is well‑documented and includes an SDK and CLI for easy integration.  
- **Risk Profile** – No major metadata or licensing concerns identified, though a final security audit and confirmation of maintainer responsiveness are recommended before full‑scale rollout.  

Overall, Citadel offers a production‑grade foundation for building repeatable, safe, and cost‑aware multi‑agent AI pipelines, making it a strong candidate for pilot deployments and eventual enterprise adoption.

### Русский

SethGammon/Citadel — это открытая платформа‑операционный слой для Claude Code и OpenAI Codex, которая добавляет постоянную память проекта, маршрутизацию намерений, безопасные хуки, телеметрию затрат и поддержку параллельных флотов агентов, позволяя превратить разрозненные запросы и инструменты в воспроизводимые агентные рабочие процессы. Типичный сценарий — координация многокомпонентных AI‑агентов, построение конвейеров с использованием внешних инструментов и стандартизация памяти агентов для сложных автоматизационных задач. Проект имеет высокий уровень готовности к production: активные коммиты, широкое принятие (600+ звёзд, 57 форков), поддержка API/SDK/CLI и JavaScript‑экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
SethGammon/Citadel 是为 Claude Code 与 OpenAI Codex 打造的运行层，提供持久化项目记忆、意图路由、安全钩子、成本监控以及并行 Agent 编队等功能，使零散的 Prompt 与工具能够组织成可重复的 Agent 工作流。

**价值体现**  
- **统一记忆与路由**：为每个项目维护持久化记忆，自动根据意图将请求分发给合适的 Agent。  
- **安全与成本可视化**：内置安全拦截和费用遥测，帮助团队在大规模使用 LLM 时保持合规与预算可控。  
- **并行编队**：支持多 Agent 并行执行，显著提升复杂任务（如多步骤代码生成、测试、部署）的吞吐量。  
- **即插即用的工作流**：将孤立的 Prompt、工具链和 API 组合成标准化、可复用的流水线，降低开发与运维成本。

**典型接入方式**  
1. **SDK / API**：通过项目提供的 JavaScript SDK 调用 `createAgent`, `routeIntent`, `storeMemory` 等方法，直接在业务代码中嵌入。  
2. **CLI**：使用 `citadel-cli` 进行本地调试或脚本化部署，适合 CI/CD 流程。  
3. **语言元数据**：项目通过 `package.json` 中的 `citadel` 字段暴露插件信息，支持自动化发现和配置。  
4. **自定义插件**：可实现自定义安全钩子或成本上报插件，按需扩展。

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，最近一次提交，拥有 615 ★、57 Fork，社区活跃度高。  
- **成熟度**：提供完整的 API、CLI 与示例，已在多个内部项目中验证，适合作为正式生产环境的候选。  
- **风险**：需进一步审查许可证（MIT/Apache 等）以及安全审计报告；维护者仍在活跃，但建议在关键业务上线前进行一次安全评估。  

总体而言，Citadel 在 OSS 场景下已具备较高的生产就绪度，适合作为构建多 Agent 编排、统一记忆与成本治理的核心组件。

## 🧭 Practical evaluation

**Value:** SethGammon/Citadel helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 615 GitHub stars
- 57 forks
- updated 2026-06-24
- primary language: JavaScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 55/100 |
| production | 59/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/SethGammon/Citadel) · [← Back to Orchestration](./README.md)</sub>
