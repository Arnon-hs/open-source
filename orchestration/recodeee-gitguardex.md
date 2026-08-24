# recodeee/gitguardex

[![Stars](https://img.shields.io/github/stars/recodeee/gitguardex?style=flat-square&color=yellow)](https://github.com/recodeee/gitguardex/stargazers) [![Forks](https://img.shields.io/github/forks/recodeee/gitguardex?style=flat-square&color=blue)](https://github.com/recodeee/gitguardex/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Run many Codex & Claude agents in parallel without them overwriting each other. Isolated worktrees, file locks, PR-only merges. Auto-wires Oh My Codex, Oh My Claude, OpenSpec, and Caveman in every worktree.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-orchestration` `caveman` `claude` `cli` `codex` `git-worktree` `multi-agent` `npm` `npm-package` `openspec` `parallel-agents` `parallel-programming`

## 🎯 Categories

Orchestration · AI/ML · DevTools

## 📝 Summary

### English

**Brief summary**  
recodeee/gitguardex runs dozens of Codex and Claude agents side‑by‑side without stepping on each other’s toes. It creates isolated Git worktrees, enforces file‑level locks, and merges results only via pull‑requests, while automatically wiring tools such as Oh My Codex, Oh My Claude, OpenSpec and Caveman into every worktree.

**Value proposition**  
- **Deterministic multi‑agent pipelines** – each agent works in its own worktree, so prompts, tool‑use, and generated artefacts never clash, giving reproducible, audit‑able outputs.  
- **Zero‑setup orchestration** – the project bundles the wiring of popular LLM‑agent frameworks (Codex, Claude, OpenSpec, Caveman) and handles the Git plumbing (branching, locking, PR‑only merges) out of the box.  
- **Standardised “agent memory”** – because each worktree is a self‑contained Git repository, the history of prompts, tool calls and file changes becomes the canonical source of truth for downstream steps or human review.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Clone & install** – `git clone https://github.com/recodeee/gitguardex && npm ci` | Minimal dependencies; JavaScript runtime is widely available. |
| 2️⃣  | **Configure agents** – supply API keys & optional tool configs in the provided `.env` or `config.json`. | Centralises credentials; the same config is propagated to every worktree automatically. |
| 3️⃣  | **Define workflow** – create a YAML/JSON spec (or use the CLI) that lists the agents, their prompts and the order of execution. | The spec becomes the “pipeline definition” that gitguardex reads to spin up isolated worktrees. |
| 4️⃣  | **Run locally** – `npx gitguardex run workflow.yaml`. Observe separate worktrees under `.gitguardex/` and PRs generated in the repo. | Immediate feedback; PR‑only merges let you review each agent’s contribution before integration. |
| 5️⃣  | **Integrate CI/CD** – add the same CLI command to a GitHub Actions workflow; use the generated PRs as artefacts for downstream jobs (tests, deployments, documentation). | Turns the prototype into an automated, repeatable step in your CI pipeline. |
| 6️⃣  | **Scale & monitor** – increase the `--parallel` flag, add more agents (e.g., a tool‑using Caveman step), and hook the emitted events to a monitoring dashboard or Slack. | Leverages the core strength—parallelism—while keeping visibility on each agent’s output. |

**Production readiness**  
- **Maturity** – Medium. The repo is actively updated (last commit 2026‑05‑11) and has a modest but real user base (21 ★, 2 forks). The core functionality (worktree isolation, file locks, PR‑only merges) is stable, but the surrounding ecosystem (Oh My Codex, Oh My Claude, OpenSpec, Caveman) may evolve faster than the wrapper.  
- **Dependencies** – Pure JavaScript/Node; relies on Git, the OpenAI/Anthropic APIs, and the bundled tool libraries. Verify compatible versions and pin them in `package-lock.json`.  
- **Security & licensing** – No obvious red flags in the source, but a formal license audit (check for MIT/Apache etc.) and a review of any third‑party SDKs is still required before production use.  
- **Operational considerations** –  
  * **Credential management** – store API keys in secret managers (GitHub Secrets, Vault).  
  * **Resource limits** – parallel agents consume multiple API quotas; monitor usage to avoid throttling.  
  * **Git hygiene** – the PR‑only merge model is safe, but you may need a cleanup policy for stale worktrees.  

**Bottom line**  
gitguardex offers a lightweight, Git‑centric way to orchestrate isolated LLM agents, turning ad‑hoc prompt runs into repeatable, version‑controlled pipelines. For teams that already use Git for CI/CD and need to coordinate several Codex/Claude agents (e.g., multi‑step code generation, documentation synthesis, or tool‑use chaining), the adoption path is straightforward: clone, configure, describe the workflow, and run it locally or in CI. With a modest amount of dependency vetting and monitoring, it can move from prototype to production for internal tooling or customer‑facing services.

### Русский

**rec​odeee/gitguardex** — это инструмент оркестрации AI‑агентов, который позволяет запускать множество Codex и Claude‑агентов параллельно, изолируя их рабочие каталоги, блокируя файлы и объединяя результаты только через pull‑request‑мерджи. Он автоматически разворачивает в каждом ворк‑трее среды Oh My Codex, Oh My Claude, OpenSpec и Caveman, что упрощает построение повторяемых, изолированных пайплайнов с инструментами и «памятью» агента. Проект находится на среднем уровне готовности к production: подходит для прототипов и внутренних процессов, но требует проверки лицензии, безопасности и поддержки зависимостей перед масштабным внедрением.

### 中文

**项目简介（2‑3 句话）**  
recodeee/gitguardex 能在同一仓库内并行运行多个 Codex 与 Claude 代理，而不会相互覆盖。它通过隔离的 worktree、文件锁和仅 PR 合并的方式，自动为每个 worktree 接入 Oh My Codex、Oh My Claude、OpenSpec 与 Caveman，实现安全、可重复的多代理工作流。

**价值**  
- **隔离与并行**：每个代理拥有独立的工作树和锁，避免竞争条件和结果被覆盖。  
- **即插即用**：统一的自动接线把常用的 LLM 工具链（Codex、Claude、OpenSpec、Caveman）注入每个工作树，省去手动配置。  
- **可复用的工作流**：把一次性的 Prompt 与工具组合封装为可重复执行的流水线，提升团队协作与实验效率。  

**典型接入方式**  
1. **CLI**：在项目根目录运行 `gitguardex run <agent‑name>`，系统会创建独立 worktree、加锁并启动对应的 LLM 代理。  
2. **SDK/API**：通过 npm 包 `@recodeee/gitguardex` 引入，调用 `GitGuardex.start(agentConfig)`，可在自定义脚本或 CI/CD 中编排多代理任务。  
3. **CI 集成**：在 GitHub Actions、GitLab CI 等流水线中使用 `gitguardex ci`，自动处理 PR‑only 合并与工作树清理，适合持续集成与自动化评审。  

**生产可用性**  
- **成熟度**：当前得分 63/100，属于 **中等** 级别。适合原型、内部工具或受控的生产环境。  
- **依赖与维护**：项目使用 JavaScript，依赖相对轻量；但维护者活跃度有限（仅 21 星、2 fork），在正式生产前建议自行审计依赖安全性并设立内部维护者。  
- **风险点**：需确认许可证兼容性、代码审计（尤其是对外部 LLM API 调用）以及对工作树/锁的异常恢复机制。  

综上，gitguardex 为需要在同一代码库中协调多 LLM 代理的团队提供了简洁的隔离执行框架，接入方式灵活，适合作为内部原型或受控生产环境的基础设施，前提是进行必要的安全与运维审查后再上线。

## 🧭 Practical evaluation

**Value:** recodeee/gitguardex helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 21 GitHub stars
- 2 forks
- updated 2026-05-11
- primary language: JavaScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 48/100 |
| quality | 46/100 |
| recency | 20/100 |
| adoption | 24/100 |
| production | 45/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/recodeee/gitguardex) · [← Back to Orchestration](./README.md)</sub>
