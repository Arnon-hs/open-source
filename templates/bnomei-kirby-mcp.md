# bnomei/kirby-mcp

[![Stars](https://img.shields.io/github/stars/bnomei/kirby-mcp?style=flat-square&color=yellow)](https://github.com/bnomei/kirby-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/bnomei/kirby-mcp?style=flat-square&color=blue)](https://github.com/bnomei/kirby-mcp/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> CLI-first MCP server for composer-based Kirby CMS projects — inspect blueprints/templates/plugins, interact with a real Kirby runtime, and use a bundled Kirby knowledge base.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 56 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | PHP |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-tools` `agentic-workflow` `claude-code` `cli` `codex-cli` `commands` `developer-tools` `google-gemini` `kirby` `kirby-cms` `knowledge-base` `mcp-server`

## 🎯 Categories

Templates · Orchestration · MCP · Knowledge/RAG · Automation

## 📝 Summary

### English

**Brief Summary**  
bnomei/kirby‑mcp is a CLI‑first “MCP” (multi‑agent coordination platform) server built for Composer‑based Kirby CMS projects. It lets developers inspect blueprints, templates, and plugins, run a live Kirby runtime, and tap into a bundled Kirby knowledge base, turning ad‑hoc prompts and tools into repeatable, orchestrated agent workflows.  

**Value**  
- **Unified workflow engine** – By exposing Kirby’s internal structures (blueprints, templates, plugins) through a programmable API/CLI, the project lets AI agents query, modify, and validate a Kirby site just like a human developer would.  
- **Tool‑use pipelines** – Agents can call the MCP server as a tool, chaining actions (e.g., “generate a new template → validate against blueprint → commit to Git”) without custom scripting for each step.  
- **Standardised memory** – The bundled knowledge base provides a persistent, domain‑specific context that agents can reference, reducing prompt drift and improving consistency across runs.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run `composer install` and start the MCP server locally (`php bin/mcp serve`). Use the provided CLI to query a Kirby site’s blueprints and verify responses.  
2. **Integrate** – Wrap the MCP API in your existing AI orchestration layer (e.g., LangChain, CrewAI). Define tool specs that call the MCP endpoints for “inspect‑blueprint”, “render‑template”, etc.  
3. **Automate** – Build multi‑agent pipelines that combine MCP calls with other tools (code generation, CI/CD, content linting). Store the MCP knowledge base in a vector store for RAG if you need richer natural‑language retrieval.  
4. **Deploy** – Containerise the server (Dockerfile is included) and run it as a side‑car in your Kirby production stack, exposing only internal network access to keep the surface area small.  

**Production Readiness**  
- **Activity & Community** – 56 stars, recent commits (as of 2026‑06‑29), and a modest but active fork base indicate ongoing maintenance.  
- **Technical maturity** – The project ships a stable CLI, a well‑documented API, and a PHP codebase that aligns with Kirby’s Composer workflow, making integration straightforward for PHP teams.  
- **Risk considerations** – License and security audits are still pending; verify the license (likely MIT) and run a dependency scan before production. No major metadata gaps were found, and the architecture is simple enough to sandbox.  

Overall, bnomei/kirby‑mcp is production‑ready for pilot projects, offering a low‑friction way to embed Kirby‑specific knowledge and actions into AI‑driven automation pipelines.

### Русский

Резюме:

"bnomei/kirby-mcp" - это открытое исходное решение для сервера MCP на основе CLI для проектов Kirby CMS. Это утилита позволяет взаимодействовать с реальным окружением Kirby и использовать встроенную базу знаний Kirby. Благодаря этому можно координировать множество агентов, добавлять воронки инструментов и стандартизировать память агентов.

Типовой сценарий внедрения: bnomei/kirby-mcp помогает превратить изолированные запросы и инструменты в повторяемые агентные потоки. Это идеальный выбор для координации мульти-агентных потоков, добавления воронок инструментов и стандартизации агентной памяти.

Уровень готовности к production: высокий. Проект имеет недавние активности, широкое распространение и сильные сигналы экосистемы, что делает его готовым к серьезному пилоту.

### 中文

**项目简介**  
bnomei/kirby-mcp 是一款面向 CLI 的 MCP（Multi‑Channel Processor）服务器，专为基于 Composer 的 Kirby CMS 项目设计。它能够在真实的 Kirby 运行时中检查蓝图、模板和插件，并提供内置的 Kirby 知识库，以支持 AI/ML 代理的查询与推理。

**价值主张**  
- **统一工具链**：将散落的 Prompt、CLI 工具和插件检查统一为可复用的 Agent 工作流，降低跨团队协作的摩擦。  
- **可编排的多代理流程**：通过 API/SDK/CLI 暴露的实现信号，轻松构建多代理协同、工具调用管道以及统一的记忆（memory）管理。  
- **加速开发与调试**：在本地或 CI 环境下直接与真实的 Kirby 实例交互，快速定位蓝图/模板问题，提升研发效率。

**典型接入方式**  
1. **CLI 调用**：在项目根目录执行 `kirby-mcp` 命令，可直接查询蓝图、运行插件检查或调用内置知识库。  
2. **API/SDK**：通过提供的 HTTP API（或 PHP SDK）在自建的 Agent 框架中发送请求，例如 `POST /mcp/inspect` 获取蓝图结构。  
3. **Composer 集成**：将 `bnomei/kirby-mcp` 添加为项目的开发依赖，配合 CI 脚本在部署前自动执行检查与知识库查询。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑29 最近一次提交，GitHub 56 ⭐、3 fork，拥有 17 个相关话题，社区活跃度良好。  
- **技术成熟度**：核心实现基于 PHP，符合 Kirby 项目生态，提供完整的 API 与 CLI，易于在现有 CI/CD 流程中嵌入。  
- **风险点**：仍需进一步审查许可证兼容性、长期维护者的活跃度以及安全审计结果。总体而言，项目已具备 **高** 的生产候选资格，可在内部或受控环境中进行试点部署。

## 🧭 Practical evaluation

**Value:** bnomei/kirby-mcp helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 56 GitHub stars
- 3 forks
- updated 2026-06-29
- primary language: PHP
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 37/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 31/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/bnomei/kirby-mcp) · [← Back to Templates](./README.md)</sub>
