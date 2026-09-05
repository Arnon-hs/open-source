# legioncodeinc/honeycomb

[![Stars](https://img.shields.io/github/stars/legioncodeinc/honeycomb?style=flat-square&color=yellow)](https://github.com/legioncodeinc/honeycomb/stargazers) [![Forks](https://img.shields.io/github/forks/legioncodeinc/honeycomb?style=flat-square&color=blue)](https://github.com/legioncodeinc/honeycomb/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> AI coding agents forget. They forget across sessions, and they forget across tools. A decision you reached in Claude Code at midnight is invisible to Cursor the next morning. Honeycomb fixes that. Learn something once; recall it everywhere,

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `aimemory` `anthropic` `anthropic-claude` `claude` `claude-code` `codex` `codex-cli` `codex-skill` `cursor` `cursor-ai`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Project Summary:**
Honeycomb is an open-source project that enables AI coding agents to retain learned knowledge across sessions and tools, allowing them to recall decisions and information consistently. This project helps developers add AI capability without starting from scratch, making it an ideal solution for prototyping AI features and building agent workflows. By leveraging Honeycomb, developers can create more efficient and effective AI-powered applications.

**Value Proposition:**
The primary value proposition of Honeycomb lies in its ability to provide a foundation for AI capabilities without requiring developers to start from a blank model stack. This means that developers can focus on building and integrating AI-powered features into their applications without having to invest significant time and resources in building a custom AI stack from scratch.

**Practical Adoption Path:**
The practical adoption path for Honeycomb involves the following steps:

1. **Evaluate and Explore:** Developers can start by evaluating Honeycomb's API, SDK, and CLI to understand its implementation signals and language metadata.
2. **Prototype and Test:** Developers can use Honeycomb to prototype AI features and build agent workflows, allowing them to test and refine their AI-powered applications.
3. **Integrate and Refine:** Once the prototype is complete, developers can integrate Honeycomb into their production environment, refining and optimizing its performance as needed.

### Русский

Honeycomb — это open‑source‑платформа, позволяющая AI‑агентам сохранять знания между сессиями и инструментами: один раз обученный навык (например, решение, найденное в Claude Code) автоматически доступен в Cursor, Cursor и других средах. Типичный сценарий — быстрый прототипинг AI‑функций, построение RAG‑ или агентных пайплайнов и оценка новых моделей без необходимости разворачивать собственный стек; интеграция происходит через простой API/SDK/CLI и поддерживает TypeScript‑проекты. Готовность к production — средняя: проект подходит для прототипов и внутренних воркфлоу, но перед выпуском в продакшн требуется проверка лицензии, безопасности и поддержки зависимостей.

### 中文

**项目简介**  
Honeycomb（legioncodeinc/honeycomb）是一款帮助 AI 编码代理跨会话、跨工具保持记忆的框架。它让开发者只需学习一次决策或上下文，就能在 Claude Code、Cursor、VS Code 等不同环境中随时调取，解决了 AI 代理“忘记”问题。

**价值**  
- **统一记忆层**：一次学习、全局可召回，提升 AI 助手的连续性和可靠性。  
- **快速原型**：提供即插即用的 API/SDK/CLI，帮助团队在几行代码内为产品或内部工具添加 AI 能力，无需从零搭建检索或代理流水线。  
- **灵活的 RAG 与工作流**：支持构建检索增强生成（RAG）以及多代理协作的复杂工作流，适用于原型验证和内部评估。

**典型接入方式**  
1. **API/SDK**：在 TypeScript/JavaScript 项目中通过 `npm install @legioncode/honeycomb` 引入 SDK，调用 `HoneycombClient` 完成记忆写入与查询。  
2. **CLI**：使用提供的命令行工具在 CI/CD 或本地脚本中快速保存/检索上下文，例如 `honeycomb put --key session-123 --value "...`。  
3. **语言/主题元数据**：通过项目的 `honeycomb.config.json` 声明支持的语言、主题或工具，框架会自动在对应 IDE 插件或 AI 平台中注入记忆层。

**生产可用性**  
- **成熟度**：当前评分 72/100，GitHub 35 星、8 fork，活跃更新至 2026‑06‑28，代码基于 TypeScript，具备基本的文档和示例。  
- **适用场景**：非常适合原型开发、内部研发工作流以及需要快速评估 AI 功能的团队。  
- **生产准备度**：属于 **中等**（Medium）级别。用于生产环境前建议进行：  
  - 依赖审计（确保第三方库安全）  
  - 运行时监控与日志接入  
  - 评估许可证兼容性与维护者响应速度  
  - 如有高可用需求，可自行部署或在受控环境中做容灾设计。  

总体而言，Honeycomb 能显著降低 AI 代理记忆管理的工程成本，是原型到内部工具快速落地的可靠助手，经过适当的安全与运维审查后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** legioncodeinc/honeycomb helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 35 GitHub stars
- 8 forks
- updated 2026-06-28
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 31/100 |
| production | 68/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/legioncodeinc/honeycomb) · [← Back to AI/ML](./README.md)</sub>
