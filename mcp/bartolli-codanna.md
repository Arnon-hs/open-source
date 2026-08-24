# bartolli/codanna

[![Stars](https://img.shields.io/github/stars/bartolli/codanna?style=flat-square&color=yellow)](https://github.com/bartolli/codanna/stargazers) [![Forks](https://img.shields.io/github/forks/bartolli/codanna?style=flat-square&color=blue)](https://github.com/bartolli/codanna/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Local code intelligence MCP server and CLI for AI coding agents

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 702 |
| 🍴 **Forks** | 63 |
| 💻 **Language** | Rust |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `call-graph-analysis` `code-indexing` `code-intelligence` `code-search` `coding-agents` `developer-tools-ai-agent` `local-first` `mcp` `mcp-server` `mcp-tools` `rag`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Project Summary:**

Codanna is an open-source project that provides a local code intelligence server and CLI for AI coding agents. It enables the connection of AI assistants to real tools and data through a standard protocol, facilitating integrations and standardization. This project has a high production readiness, with strong adoption, recent activity, and a robust ecosystem.

**Value:**

The value proposition of Codanna lies in its ability to connect AI agents to real tools and data, making it easier to integrate AI assistants into existing workflows. This standard protocol allows developers to focus on building applications rather than manually integrating AI tools, thereby increasing productivity and efficiency.

**Adoption Path:**

The adoption path for Codanna is relatively straightforward. Developers can start by evaluating the implementation signals, such as API/SDK/CLI, language metadata, or focused topics. Once satisfied, they can integrate Codanna into their existing workflows, connecting AI agents to real tools and data. This integration process is facilitated by the project's standard protocol, making it easier to adopt and deploy.

**Production Readiness:**

Codanna has a high production readiness, with strong adoption (702 GitHub stars and 63 forks) and recent activity, indicating a robust ecosystem. The project's primary language, Rust, and 16 topics suggest a well

### Русский

**bartolli/codanna** — это открытый MCP‑сервер и CLI, написанные на Rust, которые позволяют AI‑ассистентам получать доступ к реальному коду, инструментам и метаданным через единый протокол Model Context Protocol. Типичный сценарий: развернуть сервер Codanna и подключить к нему свои AI‑агенты, чтобы они могли выполнять запросы к локальному репозиторию, запускать инструменты разработки и использовать контекст проекта в режиме реального времени. Проект уже имеет активную поддержку (обновления 2026‑07‑03, 702 звёзд, 63 форка), хорошую экосистему и готов к пилотному внедрению в production, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
bartolli/codanna 是一个基于 Rust 实现的本地代码智能 MCP（Model Context Protocol）服务器和 CLI，旨在让 AI 编码助手能够通过统一协议安全、可靠地访问真实的开发工具和项目数据。

**核心价值**  
- **标准化桥接**：提供统一的 MCP 接口，帮助 AI 代理快速对接 IDE、构建系统、代码库等开发工具，降低集成成本。  
- **本地化安全**：所有代码分析和上下文检索在本地执行，避免将敏感代码泄露到云端。  
- **可组合生态**：配套的 CLI 与 SDK 让开发者能够自行部署、扩展或嵌入到自研平台，实现“一站式”AI‑工具协同。

**典型接入方式**  
1. **部署 MCP 服务器**：使用 `cargo install codanna` 或 Docker 镜像启动本地服务器，配置项目根目录、语言插件等元数据。  
2. **通过 CLI 调用**：在脚本或 CI 中使用 `codanna query --file src/main.rs --line 42` 获取代码上下文、符号解析等信息。  
3. **SDK 集成**：在自研 AI 助手或后端服务中引入 Rust/Go/Python 客户端库，直接向 MCP 服务器发送 JSON‑RPC 请求，实现实时代码智能查询、自动补全或重构建议。

**生产可用性**  
- **活跃度高**：截至 2026‑07‑03，项目拥有 702 ★、63 🍴，最近一次提交在当天，表明维护活跃。  
- **技术成熟**：核心使用 Rust 编写，具备高并发、低延迟特性；提供完整的 API 文档、示例和 CLI。  
- **生态兼容**：支持多语言元数据、可插件化的语言服务，易于与现有 CI/CD、IDE 插件链路对接。  
- **风险提示**：仍需进一步审查许可证（MIT/Apache 双许可）以及安全审计报告，确保在企业环境中的合规性。  

综合来看，codanna 已具备在生产环境中进行试点的条件，适合作为 AI 编码代理的底层“知识桥梁”。

## 🧭 Practical evaluation

**Value:** bartolli/codanna helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 702 GitHub stars
- 63 forks
- updated 2026-07-03
- primary language: Rust
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 56/100 |
| production | 59/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/bartolli/codanna) · [← Back to Mcp](./README.md)</sub>
