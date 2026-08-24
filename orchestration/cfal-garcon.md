# cfal/garcon

[![Stars](https://img.shields.io/github/stars/cfal/garcon?style=flat-square&color=yellow)](https://github.com/cfal/garcon/stargazers) [![Forks](https://img.shields.io/github/forks/cfal/garcon?style=flat-square&color=blue)](https://github.com/cfal/garcon/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Self-hosted browser workspace to run coding agents in parallel, steer work as it runs, review diffs, and ship.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 36 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-harness` `agent-orchestration` `agentic-ai` `ai-agents` `ai-coding` `ampcode` `claude-code` `code-review` `codex` `coding-agent` `coding-agents` `cursor-ai`

## 🎯 Categories

Orchestration · AI/ML · Frontend · DevTools

## 📝 Summary

### English

**Brief Summary**  
Garçon (cfal/garcon) is a self‑hosted, TypeScript‑based web workspace that lets you run multiple coding agents in parallel, steer their execution in real time, review generated diffs, and ship the results. It turns ad‑hoc prompts and tool calls into repeatable, orchestrated agent pipelines, making multi‑agent workflows easier to build, test, and iterate.

**Value**  
- **Workflow orchestration** – Garçon provides a UI‑driven control plane for coordinating several AI agents, letting you define sequences, branch logic, and shared memory without writing custom glue code.  
- **Rapid prototyping** – By visualising agent actions and diffs live, developers can debug and refine prompts or tool integrations much faster than with pure CLI scripts.  
- **Standardisation** – The platform encourages reusable “agent‑as‑a‑service” components, helping teams enforce consistent tool‑use patterns and auditability across projects.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the Docker compose (or `npm run dev`) and follow the README to launch the UI locally. Use a simple two‑agent example (e.g., a code‑generator + linter) to validate the orchestration model.  
2. **Integration** – Wrap existing internal tools (linters, test runners, CI steps) as Garçon “tools” and expose them via the provided API. Incrementally replace script‑based pipelines with Garçon workflows.  
3. **Team rollout** – Add the workspace to a shared internal network, configure SSO/OAuth for access control, and create a library of vetted agent templates that developers can clone and customise.  

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last update 2026‑07‑12) and has modest community traction (36 stars, 5 forks). Core functionality (parallel execution, diff review) works, but the ecosystem of plugins and monitoring tools is still limited.  
- **Dependencies** – Built on Node/TypeScript and a few browser‑based UI libraries; ensure compatible versions with your internal stack and audit third‑party packages for security.  
- **Operational considerations** – Deploy behind a firewall or VPN, enable TLS, and set resource limits for the agent containers to avoid runaway compute. Conduct a small‑scale pilot to assess latency and scalability before expanding to production workloads.  

Overall, Garçon is a solid choice for internal prototyping or as a stepping stone toward a fully managed agent orchestration platform, provided you perform a brief security/license audit and start with a limited, well‑monitored proof‑of‑concept.

### Русский

**cfal/garcon** — это self‑hosted рабочее пространство в браузере, позволяющее запускать несколько кодирующих агентов параллельно, управлять их процессом в реальном времени, просматривать диффы и сразу готовить релиз. Типичный сценарий внедрения — небольшое proof‑of‑concept, в котором агентные подсистемы (память, инструменты, пайплайны) стандартизируются и координируются, после чего интеграция расширяется на более крупные внутренние или прототипные проекты. Готовность к production — средняя: проект подходит для прототипов и внутренних воркфлоу, но перед выпуском в продакшн требуется проверка лицензии, безопасности и стабильности зависимостей.

### 中文

**项目简介（2‑3 句）**  
cfal/garcon 是一个自托管的浏览器工作空间，能够并行运行多代码代理、实时调度任务、审阅代码差异并直接发布。它把零散的 Prompt 与工具封装成可复用的 Agent 工作流，让开发者可以像使用本地 IDE 一样管理 AI 编程代理。

**价值**  
- **工作流可编排**：把多个 AI 代理、工具链和记忆模块串联，形成端到端的自动化编程流水线。  
- **即时可视化**：在浏览器中实时查看任务进度、调度指令和代码 diff，降低调试成本。  
- **重复使用**：一次配置的 Prompt+Tool 组合可以保存为模板，供后续项目快速复用，提升团队协作效率。

**典型接入方式**  
1. **快速 PoC**：克隆仓库，运行 `docker compose up`（或 `npm install && npm run dev`）启动本地 UI。  
2. **集成到 CI/CD**：通过提供的 REST/WS 接口在 CI 脚本中创建、调度 Agent 任务，完成代码生成后自动提交 PR。  
3. **自定义插件**：在 `src/plugins` 目录添加自定义工具或记忆实现，随后在 UI 中配置对应的 Agent 流程。  

**生产可用性**  
- **成熟度**：Medium。当前适合原型开发、内部工具或受控环境的自动化编程；在生产环境使用前需完成依赖审计、版本锁定和安全加固。  
- **社区与维护**：GitHub 36 星、5 Fork，最近一次提交为 2026‑07‑12，活跃度一般。建议在正式上线前与维护者确认长期维护计划。  
- **风险**：许可证、依赖安全和维护者活跃度仍需进一步评估；若满足这些前置条件，可在内部部署后逐步扩展到生产。

## 🧭 Practical evaluation

**Value:** cfal/garcon helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 36 GitHub stars
- 5 forks
- updated 2026-07-12
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 29/100 |
| production | 52/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/cfal/garcon) · [← Back to Orchestration](./README.md)</sub>
