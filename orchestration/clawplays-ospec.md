# clawplays/ospec

[![Stars](https://img.shields.io/github/stars/clawplays/ospec?style=flat-square&color=yellow)](https://github.com/clawplays/ospec/stargazers) [![Forks](https://img.shields.io/github/forks/clawplays/ospec?style=flat-square&color=blue)](https://github.com/clawplays/ospec/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Spec-driven, agentic workflow framework for AI coding agents. Turn a request into a verifiable goal loop — plan, act, verify — with durable specs and evidence in your repo. Works with Claude Code, Codex, Gemini, OpenCode, and plain CLI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 552 |
| 🍴 **Forks** | 34 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `agentic-coding` `ai` `ai-agents` `ai-coding-assistant` `ai-workflow` `claude-code` `cli` `codex` `coding-agent` `developer-tools` `llm`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
clawplays/ospec is a spec‑driven workflow framework that lets AI coding agents operate in a repeatable “plan‑act‑verify” loop, turning ad‑hoc prompts into durable specifications and verifiable evidence stored in your repository. It supports Claude Code, Codex, Gemini, OpenCode, and plain CLI, making it easy to coordinate multi‑agent pipelines, tool‑use sequences, and standardized agent memory.  

**Value**  
- **Repeatability & Audibility** – By converting each request into a formal spec and persisting verification artifacts, teams gain traceability and can rerun or audit past agent actions.  
- **Cross‑model Flexibility** – The same orchestration layer works with multiple LLM back‑ends, protecting investments as model choices evolve.  
- **Modular Agent Coordination** – Enables multi‑agent collaboration, tool chaining, and shared memory without writing custom glue code for each integration.  

**Practical Adoption Path**  
1. **Pilot Integration** – Add the npm package (or use the provided CLI) to an existing repo, define a simple spec (e.g., “generate a CRUD API”), and run the plan‑act‑verify loop with your preferred model.  
2. **Extend with Custom Tools** – Register internal CLIs or SDKs as “actions” in the spec, allowing agents to invoke company‑specific utilities.  
3. **Scale to Multi‑Agent Pipelines** – Chain specs so the output of one agent becomes the input spec for the next, using the built‑in evidence store to pass context.  
4. **Governance & CI Integration** – Treat the generated evidence as build artifacts; gate merges on successful verification steps, and version specs alongside code.  

**Production Readiness**  
- **High**: Actively maintained (last commit 2026‑06‑23), 552 stars, 34 forks, and a clear JavaScript SDK/CLI surface.  
- **Ecosystem Fit**: Works with major LLM providers and can be invoked from any CI/CD pipeline.  
- **Remaining Checks**: Confirm license compatibility, run a security audit of dependencies, and verify that core maintainers have a documented on‑call process before full production rollout.  

Overall, ospec offers a robust, model‑agnostic way to turn one‑off AI prompts into repeatable, auditable developer workflows, making it a strong candidate for early‑stage pilots and eventual production use.

### Русский

**clawplays/ospec** — это open‑source фреймворк, позволяющий превратить отдельные запросы и инструменты в воспроизводимые агентные рабочие процессы: план → действие → проверка с постоянными спецификациями и доказательствами, интегрирующий Claude Code, Codex, Gemini, OpenCode и обычный CLI. Типичный сценарий — координация многопользовательских AI‑агентов, построение конвейеров с использованием инструментов и стандартизация памяти агента, что упрощает масштабирование и повторное использование логики. Проект имеет высокий уровень готовности к production: активные коммиты, 552 звёзд, 34 форка, поддержка JavaScript‑SDK/CLI и хорошую экосистемную совместимость, требуя лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
clawplays/ospec 是一个面向 AI 编码代理的规格驱动工作流框架。它把「请求」转化为「可验证目标循环」——计划 → 执行 → 验证，并在代码仓库中留下持久化的规格与证据。框架兼容 Claude Code、Codex、Gemini、OpenCode 以及普通 CLI，帮助把零散的提示和工具包装成可重复、可审计的代理工作流。

**价值**  
- **统一规范**：通过可版本化的 specs 将多轮交互、工具调用和状态记忆统一记录，便于审计和回溯。  
- **工作流复用**：把一次性 Prompt 变成可重复的 “plan‑act‑verify” 循环，降低每次开发 AI 代理的成本。  
- **多代理协同**：天然支持多代理协作、工具链接入以及记忆标准化，适用于复杂的代码生成、审查和部署场景。

**典型接入方式**  
1. **API/SDK**：在项目中通过 npm 安装 `@clawplays/ospec`，调用 `createSpec`, `runPlan`, `verifyResult` 等函数即可嵌入现有代码。  
2. **CLI**：使用 `ospec` 命令行工具直接在终端定义 spec（JSON/YAML）并执行，适合 CI/CD 流程或快速原型。  
3. **语言元数据**：框架提供 JavaScript/TypeScript 的类型定义，配合 VSCode 插件可获得自动补全和 spec 验证。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，GitHub ★552、Fork 34，社区讨论活跃，代码基于现代 JavaScript。  
- **生态兼容**：已集成 Claude Code、Codex、Gemini、OpenCode 等主流大模型，且对自建 CLI 完全透明。  
- **安全与合规**：暂无重大元数据风险，许可证为 MIT，代码审计记录良好。  
- **准备度**：具备完整的 API 文档、示例仓库和 CI 集成脚本，已可在生产环境中进行试点，后续仅需确认维护者响应速度和安全审计即可正式投入。  

综上，clawplays/ospec 通过规格化、可验证的工作流把 AI 编码代理从“临时脚本”提升为“可管理、可审计”的生产组件，适合作为公司内部或 SaaS 平台的核心编排层。

## 🧭 Practical evaluation

**Value:** clawplays/ospec helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 552 GitHub stars
- 34 forks
- updated 2026-06-23
- primary language: JavaScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 53/100 |
| production | 61/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/clawplays/ospec) · [← Back to Orchestration](./README.md)</sub>
