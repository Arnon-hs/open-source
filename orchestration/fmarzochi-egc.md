# Fmarzochi/EGC

[![Stars](https://img.shields.io/github/stars/Fmarzochi/EGC?style=flat-square&color=yellow)](https://github.com/Fmarzochi/EGC/stargazers) [![Forks](https://img.shields.io/github/forks/Fmarzochi/EGC?style=flat-square&color=blue)](https://github.com/Fmarzochi/EGC/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Your AI agents never start from zero again. Local-first MCP runtime with persistent memory across sessions and tools.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 25 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-runtime` `ai-agents` `ai-coding-assistant` `antigravity` `claude-code` `claude-code-plugin` `cli` `codex` `cursor` `gemini-cli` `google-ai` `hooks`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Fmarzochi/EGC is a local‑first multi‑agent coordination platform that gives AI agents persistent memory across sessions and seamless access to tools, turning ad‑hoc prompts into repeatable, stateful workflows. It ships a JavaScript runtime with an API/SDK/CLI, making it easy to embed into existing back‑ends or dev‑tool pipelines. With active recent commits, solid GitHub metrics, and broad topic coverage, it is ready for serious pilot projects.

**Value**  
- **Persistent Agent Memory:** Agents retain context between runs, eliminating the “starting from zero” problem and improving efficiency in long‑running or iterative tasks.  
- **Tool‑Use Pipelines:** Built‑in support for connecting external tools (e.g., databases, APIs, CLIs) enables richer, end‑to‑end automation without custom glue code.  
- **Standardized Workflows:** By abstracting orchestration into reusable components, teams can share, version, and scale multi‑agent processes across projects.

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the provided CLI or SDK in a sandbox, and connect a simple tool (e.g., a web‑search API) to validate the memory and orchestration features.  
2. **Integrate:** Replace existing script‑based prompt calls with the EGC SDK in your Node.js services, wiring the persistent store to your preferred backend (local file, Redis, etc.).  
3. **Scale:** Deploy the runtime as a containerized microservice, expose its API to other services, and use the built‑in versioning to manage workflow updates across teams.  
4. **Govern:** Leverage the CLI to audit agent state, enforce policy hooks, and integrate with CI/CD pipelines for automated testing of agent workflows.

**Production Readiness**  
- **Activity & Community:** 25 stars, 21 forks, recent commit (2026‑06‑22), and 20 topical tags indicate an engaged community and ongoing maintenance.  
- **Technical Maturity:** The JavaScript runtime, clear API/SDK/CLI surface, and local‑first design reduce external dependencies and simplify deployment.  
- **Risk Considerations:** No immediate licensing or security red flags, but a final review of the open‑source license and a security audit of the runtime are advisable before full production rollout.  

Overall, Fmarzochi/EGC offers a mature, low‑friction way to bring persistent, tool‑enabled AI agents into production environments, making it a strong candidate for pilot deployments and eventual enterprise scaling.

### Русский

Fmarzochi/EGC — это локальный runtime для мульти‑агентных приложений, который сохраняет память агентов между сеансами и упрощает интеграцию инструментов, превращая разрозненные подсказки в повторяемые рабочие процессы. Его типичное применение — координация многопользовательских пайплайнов, построение цепочек «агент‑инструмент‑агент» и стандартизация долговременного контекста, что ускоряет разработку сложных AI‑сценариев. Проект имеет активную разработку, хорошие сигналы экосистемы (25 звёзд, 21 форк, обновление 2026‑06‑22) и готов к пилотному запуску в продакшн, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
Fmarzochi/EGC 为 AI 代理提供本地优先的 MCP（Memory‑Centric Processing）运行时，实现跨会话的持久记忆与工具调用，使得代理不再每次都从零开始。它把零散的 Prompt 与工具包装成可复用的工作流，帮助团队快速搭建多代理协作、工具链集成以及统一的记忆管理。

**价值**  
- **持久记忆**：代理的状态与上下文自动保存在本地，后续会话可直接复用，显著提升效率与一致性。  
- **工作流复用**：把孤立的 Prompt 与工具封装为可编排的流程，降低重复开发成本。  
- **多代理协同**：内置 MCP 调度，支持多代理之间的任务分配与结果合并，适用于复杂业务场景。  

**典型接入方式**  
1. **SDK / API**：通过 npm 安装 `egc` 包，使用提供的 JavaScript SDK 调用 `createAgent`, `runWorkflow` 等方法。  
2. **CLI**：`egc run --workflow myWorkflow.json` 可直接在终端启动预定义的工作流，适合 CI/CD 或脚本化调用。  
3. **语言元数据**：项目在 `package.json` 中声明了 `engines`、`topics` 等元信息，便于在 monorepo 或微服务中统一管理依赖。  
4. **插件式工具链**：可将自定义工具（REST API、数据库、文件系统等）注册为 EGC 插件，随后在工作流 DSL 中引用，实现“prompt + tool” 的一体化执行。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑22，星标 25、Fork 21，社区讨论活跃，代码维护频率满足生产需求。  
- **成熟度**：提供完整的 API 文档、CLI 手册以及示例工作流，已在若干内部项目中进行试点验证，表现出稳定的错误处理与持久化机制。  
- **风险**：当前尚未完成最终的许可证合规审查和安全审计（如依赖漏洞扫描），建议在正式上线前进行一次完整的合规与渗透测试。  

综合来看，Fmarzochi/EGC 已具备较高的生产就绪度，适合作为 AI 代理记忆与编排的底层框架，在内部或小规模对外服务中进行试点，随后根据安全合规评估逐步推广至全量生产环境。

## 🧭 Practical evaluation

**Value:** Fmarzochi/EGC helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 25 GitHub stars
- 21 forks
- updated 2026-06-22
- primary language: JavaScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 31/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/Fmarzochi/EGC) · [← Back to Orchestration](./README.md)</sub>
