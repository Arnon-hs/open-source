# standardagents/dmux

[![Stars](https://img.shields.io/github/stars/standardagents/dmux?style=flat-square&color=yellow)](https://github.com/standardagents/dmux/stargazers) [![Forks](https://img.shields.io/github/forks/standardagents/dmux?style=flat-square&color=blue)](https://github.com/standardagents/dmux/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> A dev agent multiplexer for git worktrees and coding agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 118 |
| 💻 **Language** | HTML |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-workflow` `ai` `ai-agents` `cli` `coding-agents` `coordinator` `orchestration`

## 🎯 Categories

Orchestration · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
standardagents/dmux is an open‑source “dev‑agent” multiplexer that lets you stitch together isolated prompts, tools, and coding agents into repeatable, coordinated workflows using Git worktrees. It provides a simple API/SDK/CLI for orchestrating multi‑agent pipelines, standardising agent memory, and adding tool‑use stages, making it easy to turn ad‑hoc scripts into production‑grade automation.  

**Value**  
- **Workflow composability** – Turn disparate prompts and utilities into a single, version‑controlled pipeline, reducing duplication and manual hand‑offs.  
- **Agent memory & state sharing** – Built‑in mechanisms keep context consistent across agents, improving reliability for complex coding tasks.  
- **Tool‑use integration** – Seamlessly attach external tools (linters, test runners, CI hooks) as first‑class steps in the workflow.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI against a small Git worktree, and experiment with a simple two‑agent flow (e.g., code generation → lint → commit).  
2. **Integrate** – Wrap the CLI or SDK calls in your CI/CD scripts or VS Code extensions, using the exposed API to feed prompts and retrieve results.  
3. **Scale** – Define reusable workflow definitions (YAML/JSON) for common patterns (code review, dependency bumping, feature scaffolding) and store them alongside your codebase for versioned reuse.  

**Production Readiness**  
- **Activity & community** – 1,552 stars, 118 forks, recent commits (as of 2026‑05‑13) and active issue discussions indicate a healthy project.  
- **Ease of evaluation** – Clear API/SDK/CLI surface, language‑agnostic metadata, and focused topics make it straightforward to test in a sandbox environment.  
- **Risks** – License compliance, security posture, and maintainer continuity still need a final check, but no major red flags have been identified. Overall, dmux is mature enough for a serious pilot in production settings.

### Русский

standardagents/dmux — это мультиплексор‑агент для разработки, позволяющий объединять изолированные подсказки и инструменты в повторяемые рабочие процессы с поддержкой git‑worktree и многопоточными агентами. Его типичное применение — построение цепочек из нескольких агентов (например, код‑генератор + тест‑раннер + анализатор), стандартизация памяти агентов и создание инструментальных пайплайнов. Проект считается почти готовым к production: активные коммиты, 1552 звёзд, широкое принятие и готовый API/CLI, требующие лишь финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
standardagents/dmux 是一个面向 Git worktree 与代码生成代理的多路复用器，能够把单独的 Prompt 与工具包装成可重复执行的 Agent 工作流。

**价值主张**  
- **统一工作流**：把分散的提示、工具和记忆统一在同一管道中，降低跨 Agent 协作的复杂度。  
- **可复用与可组合**：通过声明式的 API/SDK/CLI，快速搭建多 Agent 协同、工具调用链路，实现“一次定义、处处复用”。  
- **提升可靠性**：标准化的记忆管理与状态持久化，让 Agent 在长时间运行或多轮交互中保持上下文一致。

**典型接入方式**  
1. **CLI**：直接在终端使用 `dmux` 命令启动或管理工作树/Agent 流程。  
2. **SDK / API**：在 Python、Node.js 等语言中引入 `dmux` 包，调用 `createWorkflow()、addAgent()、run()` 等函数，实现代码层面的深度集成。  
3. **配置文件**：通过 YAML/JSON 描述工作流拓扑，配合 CLI 或 SDK 自动生成对应的执行图，适合 CI/CD 或 DevOps 场景。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目最近一次提交，拥有 1552 星、118 叉，社区活跃。  
- **生态兼容**：提供标准化的接口（REST‑like API、CLI、语言 SDK），易与现有 Git、CI、LLM 平台对接。  
- **成熟度**：代码库结构清晰、文档完备，已被若干内部项目用于多 Agent 编排，具备在生产环境中进行试点的条件。  
- **风险提示**：仍需进一步审查许可证、依赖安全性以及维护者响应速度，但整体风险较低，适合作为 OSS 方案进入正式生产。

## 🧭 Practical evaluation

**Value:** standardagents/dmux helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1552 GitHub stars
- 118 forks
- updated 2026-05-13
- primary language: HTML
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 68/100 |
| topics | 88/100 |
| outlook | 88/100 |
| quality | 82/100 |
| recency | 100/100 |
| adoption | 63/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/standardagents/dmux) · [← Back to Orchestration](./README.md)</sub>
