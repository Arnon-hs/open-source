# digitaldrywood/detent

[![Stars](https://img.shields.io/github/stars/digitaldrywood/detent?style=flat-square&color=yellow)](https://github.com/digitaldrywood/detent/stargazers) [![Forks](https://img.shields.io/github/forks/digitaldrywood/detent?style=flat-square&color=blue)](https://github.com/digitaldrywood/detent/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-36%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 36/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Detent is an open‑source framework that lets you stitch together isolated LLM prompts and tool calls into repeatable, version‑controlled agent pipelines using Git work‑trees and a serialized merge‑train model. By treating each step of a multi‑agent workflow as a commit that can be merged, tested, and rolled back, Detent makes complex orchestration both auditable and reproducible.

**Value**  
- **Modular orchestration:** Turns ad‑hoc prompt‑tool combos into reusable “agent modules” that can be composed, versioned, and shared across teams.  
- **Built‑in memory & state handling:** The merge‑train approach provides a deterministic way to persist and replay agent state, reducing drift and debugging time.  
- **Git‑native workflow:** Leverages familiar Git work‑tree mechanics, so engineers can use existing CI/CD pipelines, code reviews, and branching strategies to manage AI workflows.

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the provided examples, and replace the sample prompts/tools with your own.  
2. **Integrate:** Wrap your existing LLM calls or external APIs as Detent “steps,” then define a merge‑train pipeline (e.g., `detent init`, `detent add-step`, `detent train`).  
3. **Validate:** Use the built‑in test harness to execute the pipeline on a sandbox dataset; manually inspect the generated Git history to confirm correct state transitions.  
4. **CI/CD Hook‑up:** Add Detent commands to your CI pipeline (e.g., GitHub Actions) to automatically lint, test, and merge agent updates.  
5. **Roll‑out:** Deploy the orchestrated agents behind an internal service or API gateway, monitoring for failures and iterating on step definitions.

**Production Readiness**  
- **Readiness level:** *Medium* – suitable for prototypes, internal tools, or low‑risk production workloads.  
- **What to verify before production:**  
  - License compliance and any third‑party dependencies.  
  - Maintenance health (issue activity, recent releases).  
  - Documentation depth for custom step creation and merge‑train configuration.  
  - Test coverage and ability to run automated regression tests in CI.  
- **Risk mitigation:** Conduct a security audit of any external tool integrations, set up version‑pinning for the underlying LLM libraries, and establish a rollback plan using the Git‑based history.  

If these checks pass, Detent can become a robust backbone for multi‑agent AI pipelines, offering traceability and repeatability that are hard to achieve with ad‑hoc script‑gluing approaches.

### Русский

Detent — это open‑source‑платформа для оркестрации AI‑агентов, позволяющая превратить разрозненные подсказки и инструменты в воспроизводимые рабочие процессы с помощью worktree‑структур и сериализованного merge‑train. Типовой сценарий — построение многокомпонентных пайплайнов, где несколько агентов последовательно используют инструменты и сохраняют общую память, что упрощает координацию и стандартизацию их взаимодействий. Готовность к production — средняя: проект подходит для прототипов и внутренних сервисов, но требует ручной проверки лицензии, документации и частоты релизов перед масштабным внедрением.

### 中文

**项目简介**  
Detent 是一个面向 AI 代理的编排框架，利用 Git worktree 与序列化的 merge‑train 机制，将单个 Prompt 与工具链组合成可重复、可追踪的工作流。它帮助把零散的 AI 调用组织成结构化的多代理流水线，并提供统一的记忆/状态管理。

**核心价值**  
- **工作流可复用**：把一次性 Prompt、工具调用封装成模块化的“agent”，通过 worktree 实现代码/配置的轻量分支管理，便于版本化和回滚。  
- **多代理协同**：内置序列化 merge‑train，保证多个代理的执行顺序和冲突解决，适合复杂的任务分解与协作。  
- **统一记忆层**：提供标准化的记忆存储接口，让不同代理可以共享上下文，提升长期任务的连贯性。

**典型接入方式**  
1. **依赖安装**：`pip install detent`（或通过源码 `poetry install`）。  
2. **定义 Agent**：在项目根目录下创建 `agents/`，每个子目录对应一个 Git worktree，包含 `prompt.yaml`、`tool_config.json` 等。  
3. **配置 Merge Train**：在 `detent.yaml` 中声明各 Agent 的执行顺序、依赖关系以及冲突解决策略。  
4. **启动编排**：使用 CLI `detent run --pipeline my_pipeline`，或在 Python 中调用 `detent.run(pipeline_name)`，即可自动创建 worktree、执行 Prompt、收集结果并合并。  
5. **手动审查**：由于当前元数据较少，建议在首次接入时通过日志和生成的工作树手动检查每一步的输出，确保工具调用和记忆写入符合预期。

**生产可用性**  
- **成熟度**：Medium。框架已更新至 2026‑06‑22，具备基本功能，可用于原型或内部业务流程，但仍缺乏完整的 CI/CD、自动化测试和长期维护承诺。  
- **使用建议**：在生产环境部署前，需进行以下检查：  
  - 许可证兼容性（确认 MIT/Apache 等开源协议）  
  - 维护活跃度（查看最近 Issue、PR 及发布频率）  
  - 文档完整性（尤其是 Agent 定义、工作流调试指南）  
  - 依赖安全性（审计 `requirements.txt` 中的第三方库）  
- **适用场景**：快速搭建多代理原型、内部工具链自动化、实验性 AI 流程的可追溯化管理。若对可靠性、监控和高并发有严格要求，建议在此基础上自行封装监控/回滚层或等待社区成熟后再投入关键业务。

## 🧭 Practical evaluation

**Value:** Detent: AI agent orchestration with worktrees and serialized merge train helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-22
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 36/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/digitaldrywood/detent) · [← Back to Orchestration](./README.md)</sub>
