# the-open-engine/zeroshot

[![Stars](https://img.shields.io/github/stars/the-open-engine/zeroshot?style=flat-square&color=yellow)](https://github.com/the-open-engine/zeroshot/stargazers) [![Forks](https://img.shields.io/github/forks/the-open-engine/zeroshot?style=flat-square&color=blue)](https://github.com/the-open-engine/zeroshot/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Your autonomous engineering team in a CLI. The agent loop produces senior-level code that you can actually trust in prod because of non-negotiable feedback from independent reviewers. Supports Claude Code, OpenAI Codex, OpenCode, and Gemini CLI with trivial setup.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 132 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-orchestration` `agentic-workflow` `ai-agent` `ai-agents` `autonomous-agents` `claude` `cli` `codex` `coding-assistant` `developer-tools` `gemini` `generative-ai`

## 🎯 Categories

Orchestration · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Zeroshot is an open‑source CLI that turns isolated LLM prompts into autonomous, senior‑level engineering agents. By enforcing non‑negotiable feedback from independent reviewers, it delivers production‑ready code while supporting Claude, OpenAI Codex, OpenCode, and Gemini back‑ends with minimal setup.  

**Value**  
- **Reliability through review** – Every generated artifact must pass an independent reviewer loop, giving teams the confidence to ship AI‑produced code in production.  
- **Unified orchestration** – It stitches together prompt execution, tool use, memory handling, and multi‑agent coordination into repeatable workflows, eliminating the ad‑hoc glue code that typically surrounds LLM integrations.  
- **Broad model support** – One CLI works with the major code‑generation models, letting teams experiment or migrate without re‑architecting their pipelines.  

**Practical Adoption Path**  
1. **Quick onboarding** – Install the CLI (npm/yarn) and configure API keys for the desired model(s).  
2. **Pilot a single workflow** – Define a modest “agent loop” (e.g., generate a microservice scaffold, run reviewer feedback, commit) using the provided YAML/JSON schema.  
3. **Scale to multi‑agent pipelines** – Add tool‑use steps (e.g., linting, testing, containerization) and enable shared memory to coordinate several agents.  
4. **Integrate with CI/CD** – Wrap the CLI in your build scripts or GitHub Actions to enforce the reviewer checkpoint automatically on every PR.  

**Production Readiness**  
- **High**: The project shows strong OSS signals—1,542 stars, 132 forks, recent commits (June 2026), active issue/PR activity, and a clear JavaScript codebase.  
- **Ecosystem fit**: Exposes a clean API/SDK and CLI, making integration with existing dev‑toolchains straightforward.  
- **Remaining checks**: Verify the license compatibility, perform a security audit of the dependencies, and confirm that the core maintainers are still responsive before a full‑scale rollout.  

Overall, Zeroshot offers a mature, well‑documented foundation for turning LLM‑driven code generation into a trustworthy, production‑grade engineering workflow.

### Русский

**the-open-engine/zeroshot** — это CLI‑инструмент, который превращает отдельные запросы и инструменты в повторяемые агентные рабочие процессы: он оркестрирует несколько AI‑агентов (Claude, OpenAI Codex, OpenCode, Gemini) и обеспечивает «неготовый к компромиссам» фидбек от независимых ревьюеров, что позволяет генерировать продакшн‑готовый, senior‑уровневый код. Типичный сценарий — автоматизация сложных DevOps‑ и CI/CD‑потоков, где требуется координация мульти‑агентных задач, добавление пайплайнов с использованием внешних инструментов и стандартизация памяти агентов. Проект уже имеет высокий уровень готовности к production (активные коммиты, 1542 звёзд, 132 форка, поддержка JavaScript‑SDK/CLI), что делает его надёжным кандидатом для пилотного внедрения в реальных проектах.

### 中文

**项目简介（2‑3 句话）**  
the-open-engine/zeroshot 是一个在命令行中运行的自主工程团队，能够通过循环式 Agent 生成可直接投产的高级代码，并通过独立评审者的强制反馈确保质量。它即插即用，支持 Claude Code、OpenAI Codex、OpenCode 与 Gemini CLI，配置极其简洁。

**价值主张**  
- 将零散的 Prompt 与工具封装为可重复、可追踪的 Agent 工作流，帮助团队实现 **多 Agent 协同、工具链自动化、统一记忆库** 等高级用例。  
- 通过独立评审者的非妥协反馈，显著提升生成代码的可靠性和可维护性，降低在生产环境中出现 bug 的风险。

**典型接入方式**  
1. **CLI 直接使用**：安装 NPM 包后，使用 `zeroshot run <prompt>` 即可启动 Agent 循环。  
2. **SDK/API 调用**：项目暴露了 `runWorkflow`、`addTool`、`setMemory` 等函数，支持在自研脚本或 CI/CD 流水线中以 JavaScript/TypeScript 调用。  
3. **与现有 CI/CD 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 中加入一步 `zeroshot exec`，即可把生成的代码自动提交、审查并部署。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑22 最近一次提交，星标 1542、Fork 132，社区讨论活跃。  
- **技术成熟度**：核心实现使用 JavaScript，提供完整的 API、CLI 与语言元数据，易于在现有 DevOps 环境中评估。  
- **风险**：暂无重大元数据风险，但仍需在正式使用前完成许可证合规、依赖安全审计以及维护者响应速度的最终确认。  

综合来看，zeroshot 已具备高可用的 OSS 基础，适合作为 **生产级** 的 AI‑驱动代码生成与自动化编排平台进行试点。

## 🧭 Practical evaluation

**Value:** the-open-engine/zeroshot helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1542 GitHub stars
- 132 forks
- updated 2026-06-22
- primary language: JavaScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 68/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 64/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/the-open-engine/zeroshot) · [← Back to Orchestration](./README.md)</sub>
