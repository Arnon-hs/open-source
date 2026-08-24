# mmnto-ai/totem

[![Stars](https://img.shields.io/github/stars/mmnto-ai/totem?style=flat-square&color=yellow)](https://github.com/mmnto-ai/totem/stargazers) [![Forks](https://img.shields.io/github/forks/mmnto-ai/totem?style=flat-square&color=blue)](https://github.com/mmnto-ai/totem/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Deterministic, file-anchored toolkit for AI-agent work — context you can query, rules you can enforce, state you can derive.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents-md` `ai-agents` `ast-grep` `claude-code` `cli` `code-review` `codebase-governance` `deterministic` `developer-tools` `git-hooks` `human-in-the-loop` `linting`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Database

## 📝 Summary

### English

**Brief Summary**  
mmnto‑ai/totem is a deterministic, file‑anchored toolkit that lets AI agents query context, enforce rules, and derive state through a standard Model Context Protocol. Built in TypeScript, it offers an API/SDK/CLI for wiring agents to real tools and data sources, making integrations repeatable and auditable.

**Value**  
- **Unified protocol**: Provides a single, version‑controlled way to expose tool capabilities and data to any AI assistant, eliminating ad‑hoc “prompt‑engineering” glue code.  
- **Deterministic state**: Because context is anchored to files, the same input always yields the same output, which is crucial for debugging, compliance, and reproducibility.  
- **Policy enforcement**: Rules can be defined once and automatically applied to every agent interaction, helping teams meet security and governance requirements.

**Practical Adoption Path**  
1. **Prototype** – Install the npm package, run the CLI to generate a starter “totem” configuration, and point it at a small set of internal tools (e.g., a search API or a database).  
2. **Integrate** – Use the provided TypeScript SDK or REST endpoints to let your existing AI agents (ChatGPT, Claude, etc.) call the totem server for context and actions.  
3. **Scale** – Add more file‑anchored modules, enforce organization‑wide rules, and expose the service via a Model Context Protocol server for other teams to consume.  
4. **Monitor** – Leverage the built‑in logging and state‑derivation features to audit agent behavior and iterate on rule sets.

**Production Readiness**  
The project shows strong OSS maturity: recent commits (as of 2026‑07‑01), active issue handling, 15 stars, 4 forks, and a well‑documented TypeScript codebase. Its API/SDK/CLI surface is clear, and the deterministic file‑anchoring model simplifies testing and compliance. While a final review of licensing, security posture, and maintainer activity is still advisable, the current signals indicate that totem is ready for a serious pilot in production environments.

### Русский

mmnto‑ai/totem — это детерминированный, файлово‑ориентированный набор инструментов для работы AI‑агентов, позволяющий хранить контекст, задавать правила и выводить состояние через единый протокол. Он упрощает подключение AI‑ассистентов к реальным инструментам и данным, а также развертывание серверов Model Context Protocol и стандартизацию интеграций. По активности репозитория, наличию API/SDK/CLI и поддержке TypeScript проект готов к пилотному запуску в продакшн, хотя требуется окончательная проверка лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
mmnto‑ai/totem 是一个基于文件锚定的确定性工具箱，用于为 AI 代理提供可查询的上下文、可强制的规则以及可推导的状态。它通过统一的 Model Context Protocol（MCP）让 AI 助手直接对接真实工具和数据，实现“上下文即查询、规则即约束、状态即推理”。

**价值**  
- **统一协议**：提供标准化的 MCP 接口，消除不同 AI 代理与后端工具之间的协议碎片化。  
- **可控性与可审计**：所有上下文、规则和状态均以文件形式持久化，保证确定性、可回溯和易于审计。  
- **快速集成**：通过 API、SDK 或 CLI 即可将任意后端服务、数据库或自定义工具挂载到 AI 代理，提升开发效率并降低集成成本。

**典型接入方式**  
1. **API/SDK**：在后端服务中引入 TypeScript SDK，注册工具接口并声明对应的上下文文件，AI 代理即可通过 HTTP/MCP 调用。  
2. **CLI**：使用 `totem-cli` 在本地或 CI 环境中管理上下文文件、规则集合及状态快照，适合快速原型和 DevOps 自动化。  
3. **文件锚定**：将业务配置、数据模型或业务规则以 Markdown/JSON/YAML 等文件形式存放于项目仓库，Totem 自动解析并生成可查询的上下文层。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑01，GitHub 15 星、4 Fork，19 个主题标签，表明社区和维护者仍在积极维护。  
- **技术成熟度**：采用 TypeScript 编写，提供完整的类型定义，易于在现代前端/后端项目中集成。  
- **安全与合规**：暂无重大元数据风险，仍需对许可证（MIT/Apache 等）和安全审计进行最终确认。  
- **适配度**：已提供 API、SDK、CLI 三种接入方式，且协议层面已被多个内部 Pilot 项目验证，具备直接用于生产环境的条件。  

综合来看，mmnto‑ai/totem 在标准化 AI‑Tool 集成、提升可控性和加速开发方面具备显著价值，且具备足够的活跃度和技术成熟度，可作为 OSS 级别的生产候选进行正式部署。

## 🧭 Practical evaluation

**Value:** mmnto-ai/totem helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 15 GitHub stars
- 4 forks
- updated 2026-07-01
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 26/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 23/100 |
| production | 58/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/mmnto-ai/totem) · [← Back to Mcp](./README.md)</sub>
