# alicicek/tale-mode

[![Stars](https://img.shields.io/github/stars/alicicek/tale-mode?style=flat-square&color=yellow)](https://github.com/alicicek/tale-mode/stargazers) [![Forks](https://img.shields.io/github/forks/alicicek/tale-mode?style=flat-square&color=blue)](https://github.com/alicicek/tale-mode/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> A discipline plugin for Claude Code + OpenAI Codex — plan first, verify against the real code, receipts on every decision, independent adversarial review, and a self-armed loop that keeps going until a real check passes. Built by Fable to make any Claude work like a careful senior engineer.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 33 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Shell |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agents` `claude` `claude-code` `claude-code-plugin` `code-quality` `developer-tools` `hooks` `llm` `openai-codex`

## 🎯 Categories

Orchestration · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
tale‑mode is an open‑source “discipline” plugin that wraps Claude Code and OpenAI Codex in a structured workflow: it forces a planning step, validates generated code against the real codebase, records decision receipts, and runs an adversarial review loop until the code passes real checks. Built by Fable, it lets any Claude model behave like a careful senior engineer, turning ad‑hoc prompts into repeatable, auditable agent pipelines.

**Value**  
- **Reliability & Auditing** – By mandating a plan, verification, and receipt generation, tale‑mode adds traceability and reduces the risk of hallucinated or unsafe code.  
- **Workflow Orchestration** – It converts isolated LLM calls into coordinated multi‑agent pipelines, making it easy to add tool‑use steps (e.g., linting, testing, deployment) and to standardize agent memory across runs.  
- **Low‑Barrier Integration** – Exposes simple API/CLI hooks and language‑agnostic signals, so existing CI/CD or DevOps scripts can invoke the disciplined loop without major refactoring.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Shell‑based CLI against a sandbox repo, and observe the generated plan/receipt logs.  
2. **Integration** – Wrap the CLI or SDK calls in your build or CI pipeline (e.g., GitHub Actions, Jenkins) to replace raw Claude/Codex calls.  
3. **Customization** – Extend the adversarial review step with internal static‑analysis tools or security scanners; configure the “real‑check” criteria (unit tests, integration tests, code‑review approvals).  
4. **Pilot** – Deploy on a non‑critical microservice or internal tool, collect metrics on pass‑rate, cycle time, and audit logs.  
5. **Scale** – Once the pilot meets reliability targets, roll out to broader codebases and embed the plugin in your standard developer tooling (IDE extensions, internal bots).

**Production Readiness**  
- **Maturity**: Medium. The project is functional for prototypes and internal workflows but lacks extensive production‑grade testing, formal CI, and a large maintainer community.  
- **Signals**: 33 GitHub stars, 2 forks, recent update (2026‑07‑03), primary language Shell, modest topic coverage.  
- **Risks**: License compliance, security posture of the wrapper scripts, and the need for an active maintainer to address bugs or dependency updates.  
- **Recommendation**: Suitable for internal or staged roll‑outs after a security audit and a small “maintenance contract” (e.g., assigning a team member to monitor upstream changes). For mission‑critical production, consider adding additional safeguards (redundant testing, code‑review gating) and possibly forking the repo to ensure long‑term support.

### Русский

Резюме проекта alicicek/tale-mode:

Алисике/тейл-мод (alicicek/tale-mode) - это плагин для дисциплины, построенный на основе Claude Code и OpenAI Codex. Он позволяет создавать повторяемые агентские потоки, координируя работу множества агентов и добавляя в них инструментальные пайплайны. Это идеальное решение для прототипирования и внутренних потоков, но требует тщательного осмотрения и проверки перед внедрением в производство.

Типовым сценарием внедрения является интеграция Aлисике/тейл-мод в существующие агентские системы, чтобы повысить их эффективность и повторяемость. Это может быть особенно полезно в сценариях, когда требуется координация работы множества агентов и добавление инструментальных пайплайнов.

Уровень готовности к production: средний. Плагин можно использовать для прототипирования и внутренних потоков, но требует тщательного осмотрения и проверки перед внедрением в

### 中文

**项目简介**  
**alicicek/tale-mode** 是一个面向 Claude Code 与 OpenAI Codex 的纪律插件。它通过“先规划‑后验证‑收据记录‑对抗审查‑自我循环”的工作流，把任何 Claude 变成像资深工程师一样审慎、可追溯的代码生成助手。

**价值**  
- **把零散的 Prompt 与工具链转化为可复用的 Agent 流程**，实现多 Agent 协同、工具调用流水线和统一的记忆管理。  
- **全程留痕**：每一步决策都有收据（receipt），便于审计、回溯和对抗性审查。  
- **自我强化循环**：在真实代码校验通过前，持续迭代直至满足要求，提升生成代码的可靠性。

**典型接入方式**  
1. **CLI/SDK**：项目提供 Shell 脚本入口，可直接在 CI/CD 中调用，也可通过包装的 Python/Node SDK 与现有工具链集成。  
2. **API 信号**：暴露统一的 JSON‑API（或 OpenAI‑style 调用），支持传入 “计划” 与 “验证” 请求，返回决策收据和状态码。  
3. **语言/主题元数据**：通过项目自带的 `metadata.yaml`（或类似文件）声明支持的语言、工具和主题，便于在 Orchestration 平台（如 Fable、Airflow）中自动发现并编排。

**生产可用性**  
- **成熟度**：Score 67，GitHub 33 ★、2 Fork，最近一次更新为 2026‑07‑03，代码主要为 Shell。整体功能已可用于原型和内部工作流。  
- **准备度**：**中等**。在生产环境使用前建议：  
  1. **依赖审计**：确认所有外部 CLI、SDK 与 OpenAI/Claude 接口的版本兼容性。  
  2. **安全审查**：检查许可证（MIT/Apache 等）以及执行的 shell 脚本是否存在潜在代码注入风险。  
  3. **运维监控**：为自我循环的迭代次数设置上限，并记录收据日志以便故障排查。  
- **适用场景**：原型验证、内部代码生成平台、需要严格审计的高合规项目。若完成上述依赖与安全检查，可直接在生产 CI/CD 中作为代码审查/生成的前置步骤使用。

## 🧭 Practical evaluation

**Value:** alicicek/tale-mode helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 33 GitHub stars
- 2 forks
- updated 2026-07-03
- primary language: Shell
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 27/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/alicicek/tale-mode) · [← Back to Orchestration](./README.md)</sub>
