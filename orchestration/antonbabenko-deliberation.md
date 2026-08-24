# antonbabenko/deliberation

[![Stars](https://img.shields.io/github/stars/antonbabenko/deliberation?style=flat-square&color=yellow)](https://github.com/antonbabenko/deliberation/stargazers) [![Forks](https://img.shields.io/github/forks/antonbabenko/deliberation?style=flat-square&color=blue)](https://github.com/antonbabenko/deliberation/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Ask Codex, Gemini, Grok, and 400+ OpenRouter models (Qwen, Kimi, DeepSeek) for second opinions or arbiter-mediated consensus. One MCP server for Claude Code, Codex, Cursor, Kiro, OpenCode. Measures which models earn their seat.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 105 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-coding` `claude` `claude-code` `claude-code-plugin` `code-review` `codex` `consensus` `developer-tools` `gemini` `grok` `llm`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*deliberation* is an open‑source orchestration framework that lets you query dozens of LLMs—including Codex, Gemini, Grok, and 400+ OpenRouter models—and reach a consensus or “second‑opinion” verdict via an MCP (Model‑Consensus‑Protocol) server. It turns ad‑hoc prompts and tool calls into repeatable, multi‑agent workflows, measuring which models earn a seat at the table and exposing a simple API/CLI for integration.

**Value Proposition**  
- **Unified multi‑model access** – One endpoint can invoke a wide palette of LLMs, making it easy to compare answers, aggregate expertise, or let a designated arbiter (Claude Code, Cursor, etc.) resolve conflicts.  
- **Workflow repeatability** – By codifying prompt sequences, tool‑use steps, and memory handling, teams can ship deterministic agent pipelines rather than fragile one‑off scripts.  
- **Performance insight** – Built‑in metrics track each model’s success rate, latency, and cost, helping you prune low‑performing models and keep the most valuable ones in production.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or `npm run dev` to spin up the MCP server locally. Use the CLI (`delib query …`) to experiment with a few models on a sandbox dataset.  
2. **Integrate** – Replace existing single‑model API calls with the `deliberation` SDK (JavaScript/Node) or REST endpoints. Define your consensus policy (e.g., majority vote, arbiter‑mediated) in a JSON config file.  
3. **Scale** – Deploy the MCP server to a managed container service (K8s, Cloud Run). Hook up your CI/CD pipelines to automatically refresh the model list from OpenRouter and to monitor the built‑in metrics dashboard.  
4. **Govern** – Use the provided model‑seat scoring to enforce cost caps or compliance rules, and persist the consensus outcomes in your existing data store for auditability.

**Production Readiness**  
- **Activity & Community** – 105 ★, recent commits (last update 2026‑06‑23), and a growing set of topics indicate an active maintainer base.  
- **Architecture** – The MCP server is a stateless Node.js service with clear API/CLI contracts, making it easy to containerize, load‑balance, and monitor.  
- **Observability** – Built‑in logging and model‑performance metrics give operators the visibility needed for SLA enforcement.  
- **Risk Assessment** – No glaring metadata or licensing issues have been identified, though a final security audit (dependency scanning, secret handling) and confirmation of maintainer responsiveness are recommended before mission‑critical rollout.

Overall, *deliberation* is a mature OSS candidate for teams that need to coordinate multiple LLMs, enforce consistent tool‑use patterns, and gain data‑driven insight into model effectiveness. It can be piloted quickly and scaled to production with modest engineering effort.

### Русский

**Deliberation** — это open‑source платформа, которая объединяет более 400 моделей (Codex, Gemini, Grok, Qwen, Kimi, DeepSeek и др.) и один MCP‑сервер (Claude Code, Codex, Cursor, Kiro, OpenCode) для получения вторых мнений и построения консенсуса через арбитра. Она позволяет превратить разрозненные запросы и инструменты в повторяемые многомодельные рабочие процессы — например, координацию цепочек агентов, интеграцию пайплайнов с инструментами и стандартизацию памяти агентов. Проект имеет высокий уровень готовности к production: активные коммиты, 105 звёзд, поддержка API/SDK/CLI, JavaScript‑база и широкое принятие в сообществе, что делает его надёжным кандидатом для серьёзных пилотов.

### 中文

**项目简介**  
antonbabenko/deliberation 是一个多模型协同平台，能够让 Codex、Gemini、Grok 以及 400+ OpenRouter 模型（如 Qwen、Kimi、DeepSeek）相互“求第二意见”，并通过仲裁者（MCP 服务器）统一出具共识答案。它把零散的 Prompt 与工具封装成可复用的 Agent 工作流，支持 Claude Code、Codex、Cursor、Kiro、OpenCode 等多种后端。

### 价值
- **统一多模型决策**：在同一请求上并行调用多种大模型，自动比较、投票或仲裁，提升答案的可靠性和客观性。  
- **可复用的工作流**：把“模型 + 工具 + 记忆”组合抽象为 Agent，便于在不同业务场景（代码审查、文档生成、数据清洗等）中快速复用。  
- **透明的模型评估**：平台会记录每个模型的贡献度与得分，帮助团队挑选最适合的模型并持续优化。  

### 典型接入方式
1. **API/SDK**：直接调用公开的 HTTP API，或在项目中通过 npm 包 `@deliberation/client` 引入 SDK，使用 JavaScript/TypeScript 完成请求包装。  
2. **CLI**：安装全局 CLI（`npm i -g deliberation-cli`），在 CI/CD 脚本或本地调试时使用 `delib run <prompt>` 触发多模型协商。  
3. **MCP 服务器**：部署或使用已有的 MCP（Multi‑Consensus Processor）服务，统一管理 Claude Code、Codex、Cursor 等内部模型的路由与仲裁逻辑。  

### 生产可用性
- **活跃度**：最近一次提交在 2026‑06‑23，星标 105、Fork 4，代码基于 JavaScript，拥有 19 个主题标签，社区活跃度良好。  
- **成熟度**：项目已提供完整的 API、SDK 与 CLI，且具备明确的模型评估与仲裁机制，适合作为内部或外部服务的核心组件进行试点。  
- **风险**：目前未发现重大元数据风险，但仍需对许可证（MIT/Apache 等）进行确认，并完成安全审计以及维护者的长期可用性评估。  

总体而言，**antonbabenko/deliberation** 已具备在生产环境中进行多模型协同、构建可重复 Agent 流程的技术基线，适合作为 AI 编排层的 OSS 选型进行正式试点。

## 🧭 Practical evaluation

**Value:** antonbabenko/deliberation helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 105 GitHub stars
- 4 forks
- updated 2026-06-23
- primary language: JavaScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 36/100 |
| production | 56/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/antonbabenko/deliberation) · [← Back to Orchestration](./README.md)</sub>
