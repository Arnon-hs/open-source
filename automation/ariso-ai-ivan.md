# ariso-ai/ivan

[![Stars](https://img.shields.io/github/stars/ariso-ai/ivan?style=flat-square&color=yellow)](https://github.com/ariso-ai/ivan/stargazers) [![Forks](https://img.shields.io/github/forks/ariso-ai/ivan?style=flat-square&color=blue)](https://github.com/ariso-ai/ivan/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> 🤖 Ivan: AI-Powered Development Assistant - Breaks down complex tasks, implements them with Claude Code, creates PRs with smart commits, orchestrates AI code reviews, and automatically addresses PR comments

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 42 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `automation` `claude` `cli` `code-review` `development` `git` `pull-requests`

## 🎯 Categories

Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Ivan (ariso‑ai/ivan) is an AI‑powered development assistant that decomposes complex feature requests, writes the code using Claude, opens pull requests with intelligent commit messages, runs AI‑driven code reviews, and automatically resolves review comments. By automating these repetitive steps, it turns a manual development workflow into a repeatable, low‑effort pipeline.

**Value**  
- **Time savings:** Eliminates the back‑and‑forth of writing, reviewing, and revising code, letting developers focus on design and higher‑level problems.  
- **Consistency:** Standardised commit messages and review feedback reduce human error and enforce team conventions.  
- **Scalability:** The same AI‑driven flow can be applied to many tickets or micro‑tasks, making it easy to scale internal tooling or prototype new features quickly.

**Practical Adoption Path**  
1. **Pilot:** Clone the repo, install the TypeScript CLI/SDK, and connect it to your existing version‑control and CI system (GitHub, GitLab, etc.).  
2. **Configure:** Supply API keys for Claude (or another LLM) and define the “implementation signals” (e.g., issue templates, language metadata) that tell Ivan how to parse tasks.  
3. **Run a sandbox:** Execute a few low‑risk tickets (bug‑fixes, docs updates) and review the generated PRs and AI comments.  
4. **Iterate:** Fine‑tune prompts, add custom hooks (e.g., linting, test runners), and integrate with your task‑tracking tool (Jira, Linear).  
5. **Roll‑out:** Expand to larger feature branches or a dedicated “AI‑assistant” queue, monitoring success metrics (cycle time, review turnaround) before wider team adoption.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑07‑01), written in TypeScript, and has modest community traction (42 stars, 2 forks).  
- **Strengths:** Clear API/CLI surface, well‑defined integration points, and a focused use‑case that fits internal tooling or prototype pipelines.  
- **Caveats:**  
  * Dependency health and long‑term maintainer commitment need verification.  
  * Security and licensing reviews are still pending.  
  * For mission‑critical production use, add safeguards (e.g., manual PR approval gates, automated security scans) and monitor LLM usage costs.  

In short, Ivan is a promising automation layer for development workflows; it can be safely trialled in a sandbox, refined, and then promoted to production once the dependency, security, and governance checks are completed.

### Русский

**ariso‑ai/ivan** — это AI‑ассистент разработки, который автоматически разбивает сложные задачи, генерирует код через Claude, создает pull‑request‑ы с осмысленными коммитами, проводит AI‑ревью и обрабатывает комментарии к PR. Он подходит для автоматизации повторяющихся операций в конвейерах CI/CD: от планирования задач до их реализации и проверки, позволяя интегрировать инструменты в единый, повторяемый workflow. Проект находится на среднем уровне готовности — пригоден для прототипов и внутренних процессов, но требует дополнительной проверки лицензии, безопасности и поддержки перед развертыванием в продакшн.

### 中文

**项目简介**  
🤖 **Ivan** 是一款 AI 驱动的开发助理，能够把复杂需求拆解成可执行的子任务，利用 Claude Code 自动生成实现代码、提交智能化的 PR，并在 PR 评审阶段进行 AI 辅助审查、自动处理评审意见。  

**价值**  
- **消除重复劳动**：代码生成、PR 创建、审查回复等环节全自动化，显著降低开发人员的手工操作时间。  
- **提升交付效率**：通过 AI 快速实现功能点并生成高质量提交，缩短从需求到合并的周期。  
- **可编排的工作流**：提供统一的 API/SDK/CLI，便于将其嵌入 CI/CD、任务调度或自定义脚本，实现端到端的自动化流程。  

**典型接入方式**  
1. **API/SDK**：在项目的构建脚本或 CI 流水线中调用 Ivan 的 TypeScript SDK，提交任务描述，获取代码实现和 PR 信息。  
2. **CLI**：通过 `ivan-cli` 在本地或 CI 环境直接运行，如 `ivan run "实现用户登录"`，自动生成代码并创建 PR。  
3. **Webhook/插件**：结合 GitHub Actions 或 GitLab CI，在代码推送后触发 Ivan 自动进行代码审查和评论处理。  

**生产可用性**  
- **成熟度**：目前评分 67/100，适合作为原型或内部工具使用。  
- **依赖与维护**：项目使用 TypeScript，依赖相对轻量；但仍需自行审查其安全性、许可证合规性以及维护者活跃度后再用于生产。  
- **准备度**：具备基本的 API/CLI 接口，易于评估和集成；在正式上线前建议进行安全审计、性能基准测试以及对关键依赖的版本锁定。  

总体而言，Ivan 能显著降低开发过程中的手动工作量，适合作为内部自动化工具快速验证或在受控环境中逐步推广到生产。

## 🧭 Practical evaluation

**Value:** ariso-ai/ivan helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 42 GitHub stars
- 2 forks
- updated 2026-07-01
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 28/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/ariso-ai/ivan) · [← Back to Automation](./README.md)</sub>
