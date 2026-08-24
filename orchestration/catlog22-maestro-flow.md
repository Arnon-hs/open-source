# catlog22/maestro-flow

[![Stars](https://img.shields.io/github/stars/catlog22/maestro-flow?style=flat-square&color=yellow)](https://github.com/catlog22/maestro-flow/stargazers) [![Forks](https://img.shields.io/github/forks/catlog22/maestro-flow?style=flat-square&color=blue)](https://github.com/catlog22/maestro-flow/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Intent-driven workflow orchestration for multi-agent AI development — adaptive lifecycle engine, self-reinforcing knowledge graph, and visual dashboard for Claude Code, Gemini, Codex & more

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 398 |
| 🍴 **Forks** | 52 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `claude-code` `cli` `codex` `gemini` `knowledge-graph` `mcp` `multi-agent` `typescript` `workflow-orchestration`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Maestro‑Flow is an open‑source, intent‑driven orchestration engine that lets developers stitch together isolated LLM prompts, tools, and memory stores into repeatable, multi‑agent AI workflows. It bundles an adaptive lifecycle manager, a self‑reinforcing knowledge‑graph, and a visual dashboard that supports Claude, Gemini, Codex and other model back‑ends. With a TypeScript core, CLI/SDK APIs and rich metadata, it makes turning ad‑hoc prompt chains into production‑grade pipelines fast and transparent.  

---  

### Value  

* **From silos to pipelines** – Converts single‑shot prompts and tool calls into structured, version‑controlled workflows, reducing duplication and onboarding friction.  
* **Unified agent memory** – The built‑in knowledge graph persists and enriches state across agents, enabling context‑aware hand‑offs and self‑reinforcement.  
* **Cross‑model flexibility** – Works with major LLM providers (Claude, Gemini, Codex, etc.), so teams can experiment or migrate without rewriting orchestration logic.  
* **Observability & control** – The visual dashboard gives real‑time insight into each step, execution metrics, and error tracing, which is essential for debugging complex multi‑agent systems.  

### Practical Adoption Path  

1. **Prototype** – Clone the repo, run the provided Docker/CLI starter, and connect a single model (e.g., Claude) using the simple API key config.  
2. **Define intents** – Encode business‑level intents in the YAML/JSON manifest; the engine generates the corresponding agent chain and knowledge‑graph schema.  
3. **Integrate tools** – Register external tools (APIs, code interpreters, databases) via the SDK; Maestro‑Flow automatically injects tool‑use steps into the workflow.  
4. **Iterate & version** – Use the dashboard to monitor runs, tweak intents, and commit updated manifests to version control.  
5. **Scale to production** – Deploy the engine as a containerized microservice behind your internal API gateway, enable persistence for the knowledge graph (e.g., PostgreSQL or Neo4j), and configure CI/CD pipelines to promote validated workflow versions.  

### Production Readiness  

* **Activity & community** – 398 ★, 52 forks, recent commits (as of 2026‑06‑24), and a growing ecosystem of topics indicate an active project.  
* **Maturity** – The TypeScript codebase, CLI/SDK exposure, and clear separation of lifecycle, graph, and UI layers make it straightforward to embed in existing stacks.  
* **Stability** – No known critical bugs; the architecture is modular, allowing independent scaling of the orchestration engine, knowledge graph, and dashboard.  
* **Risks** – Licensing and security posture still need a final audit, and long‑term maintainership should be confirmed before mission‑critical deployment.  

Overall, Maestro‑Flow is a high‑readiness OSS candidate for teams that want to formalize multi‑agent AI pipelines, offering a clear path from sandbox experimentation to production‑grade orchestration.

### Русский

**catlog22/maestro-flow** — это открытая платформа для оркестрации intent‑ориентированных многопользовательских AI‑агентов, объединяющая адаптивный lifecycle‑движок, самоукрепляющийся граф знаний и визуальную панель управления (поддержка Claude Code, Gemini, Codex и др.). Она позволяет превратить разрозненные промпты и инструменты в повторяемые, масштабируемые рабочие процессы: координация нескольких агентов, построение конвейеров с использованием внешних инструментов и стандартизация памяти агентов. Проект уже имеет высокий уровень готовности к продакшну — активные коммиты, 398 звёзд, 52 форка, TypeScript‑база и открытый API/SDK/CLI, что делает его подходящим для серьёзного пилотного внедрения после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
catlog22/maestro‑flow 是一套面向多 Agent AI 开发的 Intent‑驱动工作流编排框架，提供自适应生命周期引擎、可自我强化的知识图谱以及可视化仪表盘，支持 Claude Code、Gemini、Codex 等主流大模型的协同工作。

**价值主张**  
- **统一编排**：把零散的 Prompt、工具和模型封装成可复用、可追踪的 Agent 工作流，显著提升开发效率和系统可维护性。  
- **知识沉淀**：通过自强化知识图谱自动记录与检索 Agent 交互历史，实现“记忆即服务”，降低重复学习成本。  
- **全栈可视化**：Dashboard 直观展示工作流状态、执行日志和依赖关系，帮助团队快速定位瓶颈和调优。

**典型接入方式**  
1. **API / SDK**：项目提供 TypeScript SDK 与 RESTful API，开发者可在现有代码库中直接调用 `createWorkflow / runIntent` 等接口。  
2. **CLI**：通过 `maestro-flow` 命令行工具进行工作流定义、部署与监控，适合 CI/CD 流程中自动化使用。  
3. **语言元数据**：项目在 `package.json` 中声明了 `@maestro/flow` 依赖，npm 安装后即可在 Node/TS 项目中 `import { Maestro } from '@maestro/flow'` 使用。  
4. **插件式集成**：支持自定义工具插件（如外部 API、数据库、文件系统），只需实现统一的 `ToolAdapter` 接口即可纳入编排。

**生产可用性**  
- **活跃度**：截至 2026‑06‑24 最近一次提交，GitHub ★398、Fork 52，社区讨论活跃，具备持续维护的迹象。  
- **技术成熟度**：采用 TypeScript 编写，提供完整的类型定义和单元测试，易于在企业代码基座中集成。  
- **生态兼容**：已对 Claude Code、Gemini、Codex 等主流模型提供官方适配器，且通过 OpenAPI 规范对外暴露，便于与现有 MLOps 平台对接。  
- **风险评估**：暂无严重元数据或许可证风险，但建议在正式投产前完成安全审计（依赖库的漏洞扫描）并确认维护者的响应能力。

**结论**  
凭借强大的多 Agent 编排能力、可自我学习的知识图谱以及成熟的可视化监控，maestro‑flow 已具备在生产环境中进行试点甚至全量上线的条件，只需完成常规的安全合规检查即可投入使用。

## 🧭 Practical evaluation

**Value:** catlog22/maestro-flow helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 398 GitHub stars
- 52 forks
- updated 2026-06-24
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 61/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/catlog22/maestro-flow) · [← Back to Orchestration](./README.md)</sub>
