# QuintinShaw/pi-dynamic-workflows

[![Stars](https://img.shields.io/github/stars/QuintinShaw/pi-dynamic-workflows?style=flat-square&color=yellow)](https://github.com/QuintinShaw/pi-dynamic-workflows/stargazers) [![Forks](https://img.shields.io/github/forks/QuintinShaw/pi-dynamic-workflows?style=flat-square&color=blue)](https://github.com/QuintinShaw/pi-dynamic-workflows/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Claude Code–style dynamic workflows for Pi: code-mode subagents with real model routing, journaled resume, git-worktree isolation, cost accounting, an interactive /workflows TUI, an /ultracode standing opt-in, and deep research.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 61 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-workflows` `claude-code` `coding-agent` `deep-research` `dynamic-workflows` `llm` `multi-agent` `pi` `pi-package` `subagents` `typescript` `ultracode`

## 🎯 Categories

Orchestration · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
QuintinShaw/pi‑dynamic‑workflows is an open‑source TypeScript framework that lets you compose “Claude‑style” AI sub‑agents into repeatable, dynamically‑routed workflows. It provides journaled resumability, git‑worktree isolation, cost accounting, a TUI for managing `/workflows`, and an optional “/ultracode” mode for deeper research‑grade interactions.

**Value**  
- **Turn ad‑hoc prompts into reusable pipelines** – By treating each prompt or tool as a sub‑agent, teams can standardise memory handling, tool‑use sequencing, and error recovery.  
- **Visibility & control** – The interactive TUI, journalling, and cost accounting give operators real‑time insight into execution paths and budget impact, which is rare in pure LLM wrappers.  
- **Safe experimentation** – Git‑worktree isolation lets you spin up sandboxed branches for new workflow versions without contaminating production state.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the built‑in `/workflows` TUI on a small test prompt set to verify the routing and journalling features.  
2. **Integrate via README examples** – Follow the quick‑start guide to wrap an existing tool (e.g., a retrieval API) as a sub‑agent and add it to a workflow definition file.  
3. **Iterate & version** – Use the git‑worktree isolation to branch workflow changes, run automated tests, and merge only after cost‑accounting checks pass.  
4. **Scale** – Deploy the TUI or its headless API behind your internal orchestration layer, and enable the `/ultracode` opt‑in for research‑intensive tasks where deeper model reasoning is required.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑06‑23) and has modest community traction (≈60 ★, 15 forks).  
- **Strengths:** Clear modular design, built‑in cost tracking, and a usable UI for ops teams.  
- **Caveats:** Requires a review of the license, security posture, and long‑term maintainer commitment before a production rollout. Dependency health (Node/TS ecosystem) and CI/CD integration should be validated.  
- **Recommendation:** Suitable for internal prototypes or controlled‑release pipelines; proceed to production after a small pilot, a security audit, and establishing a maintenance plan.

### Русский

QuintinShaw/pi‑dynamic‑workflows — это open‑source‑фреймворк, позволяющий превратить разрозненные подсказки и инструменты в воспроизводимые агентные пайплайны с реальным роутингом моделей, журналированием, учётом затрат и изоляцией через git‑worktree. Типичное внедрение начинается с небольшого proof‑of‑concept: подключаем TUI /workflows, настраиваем один‑два суб‑агента и проверяем работу через README, после чего можно масштабировать процесс координации многопользовательских или инструментальных workflow‑ов. Готовность к production — средняя: проект подходит для прототипов и внутренних систем, но требует проверки лицензии, безопасности и поддерживаемости зависимостей перед запуском в продакшн.

### 中文

**项目简介**  
QuintinShaw/pi‑dynamic‑workflows 为 Pi 提供 Claude Code 风格的动态工作流框架，支持代码模式子代理、真实模型路由、日志化恢复、git‑worktree 隔离、费用统计、交互式 `/workflows` TUI、可选的 `/ultracode` 模式以及深度研究功能。

**价值**  
- 将零散的提示词和工具包装成可复用、可追溯的代理工作流，提升团队协作和研发效率。  
- 通过模型路由和费用统计实现精细成本控制；git‑worktree 隔离保证不同工作流之间互不干扰。  
- 交互式 TUI 与 ultracode 选项让开发者既能快速调试，又能在代码层面深度定制。

**典型接入方式**  
1. **快速试验**：克隆仓库 → `npm install` → 参考 `README` 中的最小示例，使用 `pi run <workflow>` 启动一个简单的多代理流程。  
2. **工具链集成**：在已有的 CI/CD 或内部平台中添加 `pi-dynamic-workflows` 作为子进程或 npm 包，引入 `WorkflowEngine` API，配置模型路由和工具插件即可。  
3. **生产化**：结合 git‑worktree 将每个工作流版本化，使用内置的成本记账模块监控费用，配合日志恢复机制实现容错与回滚。

**生产可用性**  
- **成熟度**：Medium。项目已拥有 61 星、15 Fork，最近一次更新在 2026‑06‑23，代码基于 TypeScript，适合作为原型或内部业务的基础设施。  
- **准备工作**：在生产环境部署前建议完成以下检查：  
  1. **许可证与合规**：确认项目使用的开源许可证（MIT/Apache 等）符合企业政策。  
  2. **安全审计**：运行 `npm audit` 并审查依赖的安全报告。  
  3. **维护者沟通**：联系仓库维护者确认长期维护计划或自行承担维护。  
  4. **依赖锁定**：使用 lockfile（`package-lock.json`）或 `pnpm`/`yarn` 的锁定机制，防止意外升级。  
- **可行性**：适合作为原型、内部工具或实验性产品的工作流编排层；在完成上述审计和监控后，可逐步推广到生产环境。  

总体而言，QuintinShaw/pi-dynamic-workflows 为多代理、工具链驱动的 AI 应用提供了一套灵活且可追溯的工作流框架，只要做好安全与运维准备，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** QuintinShaw/pi-dynamic-workflows helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 61 GitHub stars
- 15 forks
- updated 2026-06-23
- primary language: TypeScript
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 36/100 |
| production | 53/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/QuintinShaw/pi-dynamic-workflows) · [← Back to Orchestration](./README.md)</sub>
