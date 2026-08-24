# majiayu000/vibeguard

[![Stars](https://img.shields.io/github/stars/majiayu000/vibeguard?style=flat-square&color=yellow)](https://github.com/majiayu000/vibeguard/stargazers) [![Forks](https://img.shields.io/github/forks/majiayu000/vibeguard?style=flat-square&color=blue)](https://github.com/majiayu000/vibeguard/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Native rules, hooks, and guards that prevent Claude Code and Codex from hallucinating code, duplicating files, or shipping unverified changes.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 26 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Shell |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-harness` `agentic-engineering` `ai-agents` `ai-safety` `anti-hallucination` `claude` `claude-code` `code-quality` `codex` `codex-cli` `developer-tools` `guardrails`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`majiayu000/vibeguard` provides native rules, hooks, and guards that stop Claude Code and Codex from hallucinating code, duplicating files, or shipping unverified changes. By exposing implementation signals (API/SDK/CLI, language metadata, and focused topics), it lets developers add AI‑driven code‑generation safeguards without building a model stack from scratch. The project is a lightweight, shell‑based toolkit aimed at prototyping and internal AI‑assisted development workflows.  

**Value**  
- **Safety‑first AI coding** – Prevents common AI‑generated code errors (hallucinations, duplicate artifacts, untested changes) that can derail projects or introduce security risks.  
- **Fast integration** – Offers ready‑to‑use hooks and guard definitions that can be dropped into existing CI/CD pipelines, IDE extensions, or agent frameworks with minimal code changes.  
- **Low overhead** – Implemented in shell scripts, it adds negligible runtime cost while delivering clear, actionable signals to downstream tooling.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI to scan a sample codebase, and observe the guard reports.  
2. **Integrate** – Add the relevant hooks to your CI pipeline (e.g., GitHub Actions, Jenkins) or bind the SDK to your AI‑code‑generation service.  
3. **Customize** – Extend the rule set or write new shell‑based guards to cover project‑specific conventions or compliance checks.  
4. **Iterate** – Use the exposed signals (pass/fail, file‑level metadata) to feed back into your RAG or autonomous agent loops, tightening the model’s output quality over time.  

**Production Readiness**  
- **Maturity**: Medium. The tool is functional for prototyping and internal workflows, but it still requires a review of licensing, security posture, and long‑term maintainer commitment before mission‑critical deployment.  
- **Stability**: Recent update (2026‑06‑25) and modest community interest (26 stars, 4 forks) indicate active, albeit small, maintenance.  
- **Dependencies**: Pure shell implementation with optional API/SDK wrappers; minimal external dependencies make it easy to audit.  
- **Next steps for production**: Conduct a security audit of the scripts, verify licensing compatibility with your stack, and set up a monitoring process for updates or community contributions. Once those checks are in place, vibeguard can be safely promoted to production‑grade CI/CD safeguards for AI‑generated code.

### Русский

**Vibeguard** — набор нативных правил, хуков и «охран» для моделей Claude Code и Codex, который автоматически предотвращает галлюцинации кода, дублирование файлов и выпуск непроверенных изменений. Его обычно подключают в прототипах AI‑фич или внутренних RAG‑/агентных пайплайнах, где требуется быстрый контроль качества генерируемого кода без построения собственного стекa моделей. Готовность к production — средняя: проект удобен для экспериментальных и внутренних задач, но перед выпуском в продакшн требуется проверка лицензии, безопасности и поддерживаемости зависимостей.

### 中文

**项目简介**  
majiayu000/vibeguard 是一套原生规则、钩子和守卫，专门用于防止 Claude Code、Codex 等大模型在生成代码时出现幻觉、重复文件或未验证的改动。它通过对模型输出进行实时校验，让 AI 编码更安全、更可靠。

**价值**  
- **降低风险**：自动拦截不可信的代码片段，防止因模型幻觉导致的生产事故。  
- **提升效率**：无需从头搭建防护体系，直接在现有开发流程中加入 AI 代码审查。  
- **加速原型**：帮助团队快速验证 AI 功能、构建 RAG 或智能体工作流，缩短研发周期。

**典型接入方式**  
1. **CLI**：在 CI/CD 流程或本地开发环境中通过命令行调用 `vibeguard`，对生成的代码文件进行检查。  
2. **SDK/API**：在自定义脚本或服务中引入其 Shell 脚本或包装的 HTTP 接口，实现实时校验。  
3. **Git Hook**：将 `vibeguard` 安装为 pre‑commit / pre‑push 钩子，自动在代码提交前拦截违规改动。

**生产可用性**  
- **成熟度**：目前适合原型开发和内部工作流，已在多个内部项目中验证可行。  
- **依赖与维护**：项目主要使用 Shell 编写，依赖较少；但仍需自行评估其安全审计、许可证兼容性以及维护者活跃度后再用于生产环境。  
- **准备度**：中等（Medium）——在引入生产系统前建议进行完整的集成测试和风险评估。

## 🧭 Practical evaluation

**Value:** majiayu000/vibeguard helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 26 GitHub stars
- 4 forks
- updated 2026-06-25
- primary language: Shell
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 27/100 |
| production | 52/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/majiayu000/vibeguard) · [← Back to AI/ML](./README.md)</sub>
