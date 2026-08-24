# basilisk-labs/agentplane

[![Stars](https://img.shields.io/github/stars/basilisk-labs/agentplane?style=flat-square&color=yellow)](https://github.com/basilisk-labs/agentplane/stargazers) [![Forks](https://img.shields.io/github/forks/basilisk-labs/agentplane?style=flat-square&color=blue)](https://github.com/basilisk-labs/agentplane/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> 🛩️ Git-native workflow control for coding agents: approved plans, verification, and reviewable evidence for Claude Code, Codex, Cursor, and Aider.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 48 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-change-record` `agentic-coding` `agentplane` `ai-agents` `ai-code-review` `aider` `audit-trail` `claude-code` `cli` `codex` `coding-agents` `cursor`

## 🎯 Categories

Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Agentplane (basilisk‑labs/agentplane) is a TypeScript‑based, Git‑native framework that orchestrates coding agents such as Claude Code, Codex, Cursor, and Aider. It automates plan approval, verification, and evidence‑review steps, turning ad‑hoc AI‑assisted development into repeatable, auditable pipelines.  

**Value**  
- **Automation of repetitive tasks** – eliminates manual hand‑offs (plan creation, execution, validation) by embedding them in the Git workflow, freeing developers to focus on higher‑level design.  
- **Traceable, reviewable output** – every agent action is recorded as a commit or PR, providing an immutable audit trail that satisfies compliance and code‑review requirements.  
- **Tool‑agnostic orchestration** – a single declarative interface can chain together multiple AI coding agents, making it easy to switch or combine models without rewriting glue code.  

**Practical Adoption Path**  
1. **Pilot the CLI/SDK** – clone the repo, install the npm package, and run the provided example pipelines on a small feature branch.  
2. **Integrate with existing CI/CD** – add the `agentplane` step to your GitHub Actions or GitLab CI file to automatically trigger plan generation, execution, and verification on PRs.  
3. **Extend with custom agents** – use the TypeScript SDK to wrap any internal or third‑party AI tool, then declare the new agent in the `agentplane.yml` configuration.  
4. **Scale to production** – roll the pipeline out to all repos, enforce the “approved‑plan‑only” policy via branch protection rules, and monitor the generated evidence logs for compliance.  

**Production Readiness**  
- **Active development** – last commit on 2026‑05‑13, 48 stars, 6 forks, and a healthy set of 19 topics indicate a vibrant community.  
- **Strong ecosystem fit** – exposes clear API/CLI hooks, language metadata, and integrates directly with Git, making evaluation straightforward.  
- **Risk profile** – no major licensing or security red flags have been identified, though a final review of the license and maintainer activity is advisable. Overall, Agentplane is mature enough for a serious pilot and can be promoted to production once the minor compliance checks are completed.

### Русский

**basilisk-labs/agentplane** – это open‑source‑инструмент, который автоматизирует повторяющиеся шаги в работе кодирующих агентов (Claude Code, Codex, Cursor, Aider) через Git‑native workflow: планирование, проверка и документирование результатов. Типичный сценарий — создание однородных конвейеров, где план генерируется автоматически, проходит верификацию и сохраняется в репозитории, а затем планируется или запускается по расписанию, устраняя ручные операции. Проект имеет высокий уровень готовности к production: активные коммиты, 48 звёзд, 6 форков, поддержка API/SDK/CLI, TypeScript‑база и широкие интеграционные возможности, требующие лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
basilisk-labs/agentplane 是一款 Git 原生的工作流控制框架，专为 Claude Code、Codex、Cursor、Aider 等编码助手设计。它通过“批准的计划 → 自动验证 → 可审查证据”三步链路，把重复的手动操作转化为可编排、可追溯的自动化流程。

**价值**  
- **消除重复劳动**：把代码审查、计划批准、结果验证等繁琐环节自动化，显著提升研发效率。  
- **可组合的工具桥梁**：提供统一的 API/SDK/CLI，能够把不同的 AI 编码工具、CI/CD、任务调度器等轻松串联成可重复执行的流水线。  
- **可审计的证据链**：所有自动化步骤都会生成可回溯的审计记录，方便事后审查和合规。

**典型接入方式**  
1. **CLI**：在 CI 脚本或本地终端直接调用 `agentplane` 命令，提交计划、触发验证、获取审计报告。  
2. **SDK（TypeScript/JavaScript）**：在自研插件或内部平台中引入 `@agentplane/sdk`，通过代码调用 `createPlan → approvePlan → verify → getEvidence` 等函数，实现深度集成。  
3. **REST API**：部署的 AgentPlane 服务暴露 HTTP 接口，其他语言（Python、Go 等）通过标准的 `POST /plans`、`GET /evidence` 等路径进行交互，适合跨语言生态。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑13，星标 48、Fork 6，社区讨论活跃，具备持续维护的迹象。  
- **技术成熟度**：采用 TypeScript 编写，提供完整的类型定义和丰富的 GitHub topics，易于审查和二次开发。  
- **安全与合规**：暂无重大元数据风险，但仍需在正式投产前完成许可证（MIT/Apache 等）和安全审计的最终确认。  
- **适配度**：已对 Claude Code、Codex、Cursor、Aider 等主流编码助手提供原生适配，接入成本低，适合作为内部研发流程的自动化核心组件。

综上，AgentPlane 在消除手工编码工作、构建可审计的 AI 编码流水线方面具备明确价值，接入方式灵活，且已具备较高的生产就绪度，可作为企业级研发自动化的可靠 OSS 选项进行试点。

## 🧭 Practical evaluation

**Value:** basilisk-labs/agentplane helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 48 GitHub stars
- 6 forks
- updated 2026-05-13
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 36/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 32/100 |
| production | 51/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/basilisk-labs/agentplane) · [← Back to Automation](./README.md)</sub>
