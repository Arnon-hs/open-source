# momoraul/Lupen

[![Stars](https://img.shields.io/github/stars/momoraul/Lupen?style=flat-square&color=yellow)](https://github.com/momoraul/Lupen/stargazers) [![Forks](https://img.shields.io/github/forks/momoraul/Lupen?style=flat-square&color=blue)](https://github.com/momoraul/Lupen/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Itemized cost receipts for Claude Code and Codex — by turn, verified, local.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 28 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Swift |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-coding` `anthropic` `claude` `claude-code` `cli` `codex` `cost-tracking` `developer-tools` `llm` `macos` `menubar`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Lupen (momoraul/Lupen) is a Swift‑based toolkit that generates itemized cost receipts for Claude Code and Codex calls, letting developers see exactly how much each turn, verification step, or local execution costs. It streamlines the addition of AI capabilities to a project without having to build a model stack from scratch, making it ideal for rapid prototyping of RAG pipelines, agent workflows, or model‑tooling evaluations.

**Value**  
- **Transparency:** By providing per‑turn cost breakdowns, Lupen lets teams budget AI usage accurately and spot inefficiencies early.  
- **Speed to market:** The library wraps the underlying Claude and Codex APIs, so developers can plug in AI features with just a few lines of Swift (or via the CLI/SDK) instead of writing their own instrumentation.  
- **Flexibility:** The receipts are language‑agnostic metadata, which can be consumed by monitoring dashboards, billing systems, or used to drive cost‑aware routing in multi‑model RAG or agent architectures.

**Practical Adoption Path**  
1. **Evaluation:** Clone the repo, run the provided CLI on a small test script, and verify that the receipt output matches expected API usage.  
2. **Integration:** Add Lupen as a Swift package (or invoke its CLI) in your existing codebase; replace direct Claude/Codex calls with Lupen‑wrapped calls.  
3. **Instrumentation:** Hook the receipt data into your observability stack (e.g., Prometheus, Grafana, or a custom billing dashboard).  
4. **Iterate:** Use the cost signals to fine‑tune prompts, batch requests, or switch to cheaper models where appropriate.  
5. **Scale:** Once the cost‑control loop is validated, promote the integration from a prototype repo to internal CI/CD pipelines.

**Production Readiness**  
- **Maturity:** Medium. The project has 28 stars, recent activity (last commit 2026‑06‑26), and a modest but active contributor base, indicating it is usable for internal prototypes.  
- **Dependencies:** Primarily Swift and standard HTTP client libraries; no heavyweight native bindings, which eases containerization.  
- **Risks:** The license, security posture, and long‑term maintainer commitment have not been fully vetted; a brief audit is recommended before production deployment.  
- **Recommendation:** Deploy Lupen in staging or internal tooling first, monitor for any breakage or licensing issues, and only promote to production once the audit and dependency lock‑in are completed.

### Русский

**momoraul/Lupen** — это open‑source библиотека на Swift, позволяющая получать детализированные расчётные чеки для Claude Code и Codex, проверяя их по‑очередно и локально. Она упрощает добавление AI‑функционала в прототипы и внутренние сервисы (RAG, агентные пайплайны, оценка инструментов), предоставляя готовый API/SDK/CLI и метаданные языка. Готовность к production — средняя: проект подходит для быстрых экспериментов, но перед развертыванием в продакшн требуется проверка лицензии, безопасности и поддержки зависимостей.

### 中文

**项目简介**  
momoraul/Lupen 是一款面向 Claude Code 与 Codex 的分项费用收据生成工具，能够在本地、逐轮（turn‑by‑turn）验证并输出详细的成本明细。它让开发者在不从零搭建模型堆栈的前提下，快速为 AI 功能添加计费可视化。

**价值主张**  
- **快速原型**：无需自行实现计费逻辑，直接获取每一次调用的细粒度费用，帮助团队评估 AI 功能的成本可行性。  
- **RAG/Agent 工作流支撑**：在检索增强生成（RAG）或智能体（Agent）场景中，能够实时追踪不同模块（检索、生成、工具调用等）的费用分摊。  
- **模型工具评估**：通过对比不同模型或不同 API 参数的费用，帮助产品和运营团队做出更具经济性的技术选型。

**典型接入方式**  
1. **SDK / API**：项目提供 Swift SDK 与 RESTful API，开发者可在 iOS/macOS 应用或服务器端直接调用 `recordTurn(costInfo:)` 等接口获取费用记录。  
2. **CLI 工具**：内置 `lupen` 命令行工具，可在 CI/CD 流程或本地调试时，使用 `lupen log --model=claude-code` 生成费用报告。  
3. **语言元数据**：通过项目的 `Package.swift` 暴露的元数据（如模型标识、参数配置），可在代码生成或自动化脚本中动态注入计费标签。

**生产可用性**  
- **成熟度**：当前评分 64/100，适合原型开发或内部工具使用。  
- **依赖与维护**：项目主要使用 Swift，拥有 28 个星标、4 个 fork，最近一次更新在 2026‑06‑26，代码活跃度尚可。上线前建议：  
  - 检查许可证兼容性（项目未明确声明）  
  - 评估第三方依赖的安全性（如网络请求库）  
  - 进行持续集成测试，确保费用记录在高并发场景下的准确性。  
- **生产建议**：在经过安全审计和依赖锁定后，可用于内部服务或面向特定客户的付费 AI 功能；若需对外大规模提供，建议额外实现故障回滚和费用上限控制机制。

## 🧭 Practical evaluation

**Value:** momoraul/Lupen helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 28 GitHub stars
- 4 forks
- updated 2026-06-26
- primary language: Swift
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 31/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 27/100 |
| production | 52/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/momoraul/Lupen) · [← Back to AI/ML](./README.md)</sub>
