# JeiKeiLim/tenet

[![Stars](https://img.shields.io/github/stars/JeiKeiLim/tenet?style=flat-square&color=yellow)](https://github.com/JeiKeiLim/tenet/stargazers) [![Forks](https://img.shields.io/github/forks/JeiKeiLim/tenet?style=flat-square&color=blue)](https://github.com/JeiKeiLim/tenet/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Cross-platform AI agent harness for 12+ hour autonomous development cycles. Spec-driven, DAG-orchestrated, with a 3-critic evaluation pipeline. Works with Claude Code, OpenCode, and Codex.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 41 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-driven-development` `claude` `codex` `harness` `harness-engineering` `opencode` `spec-driven-development`

## 🎯 Categories

Automation · AI/ML

## 📝 Summary

### English

**Brief Summary**  
JeiKeiLim/tenet is a TypeScript‑based, cross‑platform AI‑agent framework that automates long‑running development cycles (12+ hours) by orchestrating spec‑driven DAGs and a three‑critic evaluation pipeline. It integrates with Claude Code, OpenCode, and Codex, letting teams replace repetitive manual steps with repeatable, scheduled workflows.

**Value**  
- **Automation of tedious tasks** – Tenet abstracts the “glue” work of stitching together LLM‑generated code, testing, and refinement, freeing engineers to focus on higher‑level design.  
- **Spec‑driven, DAG orchestration** – Workflows are expressed as declarative specifications, enabling deterministic execution, easy versioning, and clear dependency tracking.  
- **Robust quality gate** – The built‑in three‑critic pipeline (syntactic, semantic, and performance checks) raises confidence in generated artifacts before they are merged or deployed.  
- **Multi‑model support** – By working with Claude Code, OpenCode, and Codex, teams can pick the model that best fits cost, latency, or licensing constraints without rewriting orchestration logic.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided README examples, and connect a single LLM (e.g., Claude Code) to a small, self‑contained task such as generating a utility script.  
2. **Incremental Integration** – Replace an existing manual step in your CI/CD pipeline with a Tenet node, using the spec DSL to define inputs/outputs. Validate the three‑critic feedback loop on this isolated piece.  
3. **Workflow Expansion** – Gradually add more nodes to build a full DAG that covers code generation, unit‑test creation, and deployment verification. Leverage Tenet’s scheduling features to run the pipeline nightly or on‑demand.  
4. **Monitoring & Governance** – Hook Tenet’s evaluation results into your observability stack (e.g., Grafana, Slack) and enforce policy checks (e.g., security linting) before promoting to production.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑25) and functional for prototypes or internal tooling, but it has modest community adoption (41 stars, 1 fork) and limited real‑world case studies.  
- **Dependencies**: Built on TypeScript and standard Node.js packages; verify compatibility with your runtime and audit third‑party libraries for security vulnerabilities.  
- **Operational Considerations**:  
  - *License & security*: Conduct a final review of the repository’s license and run a security scan (e.g., Snyk) before internal rollout.  
  - *Maintainability*: Assign an owner to keep the DAG specs and critic configurations in sync with evolving LLM APIs.  
  - *Scalability*: For large‑scale use, consider containerizing Tenet and scaling the critic services horizontally.  

In short, Tenet offers a compelling way to automate long‑duration AI‑driven development cycles, but organizations should start with a small PoC, perform due‑diligence on dependencies and licensing, and only promote to production once the three‑critic pipeline and orchestration have been validated in a controlled environment.

### Русский

**JeiKeiLim/tenet** — кроссплатформенный фреймворк‑агент для автономных AI‑разработок (12 + часовых циклов), который управляет задачами через DAG‑ориентированную спецификацию и трёхкритериальную оценку, поддерживая Claude Code, OpenCode и Codex. Он позволяет автоматизировать повторяющиеся ручные операции, связывать инструменты в воспроизводимые потоки и планировать периодические задачи, что делает его подходящим для прототипов и внутренних рабочих процессов; однако перед вводом в production рекомендуется начать с небольшого proof‑of‑concept, проверить README и провести аудит лицензий, безопасности и зависимостей. В текущем состоянии проект имеет среднюю готовность к продакшну (многообещающие возможности, но требуется дополнительная проверка поддержки и обслуживания).

### 中文

**价值**  
JeiKeiLim/tenet 通过 **Spec‑driven、DAG 编排 + 3‑critic 评估** 的方式，把 Claude Code、OpenCode、Codex 等大模型包装成可长时间（12 小时以上）自行运行的 AI 代理。它能够把手工的代码生成、测试、部署、监控等环节自动化，显著降低重复性劳动，让研发团队把精力放在业务创新上。

**典型接入方式**  
1. **阅读并运行 README**：先在本地或 CI 环境执行项目自带的快速示例，确认依赖（Node ≥ 18、TypeScript、对应模型的 API Key）能够正常工作。  
2. **定义 Spec & DAG**：在项目根目录编写 JSON/YAML 规格文件，描述任务节点、输入/输出以及依赖关系（DAG）。  
3. **接入模型凭证**：在 `.env` 中配置 Claude、OpenAI（Codex）或 OpenCode 的访问令牌。  
4. **启动调度器**：`npm run start`（或 `ts-node src/engine.ts`）启动调度器，系统会依据 DAG 自动调度各节点并走 3‑critic 评审流程。  
5. **监控与扩展**：通过内置的日志/Prometheus 指标或自定义 webhook，将结果回写至自家 CI/CD、Issue Tracker 或数据库，实现端到端的可视化工作流。

**生产可用性**  
- **成熟度**：当前得分 60/100，适合作为原型或内部工具使用。  
- **依赖与维护**：TypeScript 代码库较小（41 Stars、1 Fork），最近一次提交在 2026‑06‑25，说明仍在活跃维护，但仍需自行审计依赖安全性和许可证兼容性。  
- **部署建议**：先在沙箱或小规模 PoC 环境验证 Spec 与模型调用是否符合预期；确认 3‑critic 评审的阈值与业务容忍度后，再考虑在生产环境（K8s、Docker Swarm 等）以容器化方式部署，并加入监控/限流。  

综上，JeiKeiLim/tenet 能显著削减手工编程与运维工作，接入成本相对低（只要配置 Spec 与模型凭证），但在正式生产前建议完成安全审计、依赖锁定以及容错/回滚机制的验证。

## 🧭 Practical evaluation

**Value:** JeiKeiLim/tenet helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 41 GitHub stars
- 1 forks
- updated 2026-06-25
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 27/100 |
| production | 65/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/JeiKeiLim/tenet) · [← Back to Automation](./README.md)</sub>
