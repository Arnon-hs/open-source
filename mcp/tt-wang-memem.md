# TT-Wang/memem

[![Stars](https://img.shields.io/github/stars/TT-Wang/memem?style=flat-square&color=yellow)](https://github.com/TT-Wang/memem/stargazers) [![Forks](https://img.shields.io/github/forks/TT-Wang/memem?style=flat-square&color=blue)](https://github.com/TT-Wang/memem/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> A Claude Code plugin that gives Claude persistent memory across sessions — stores lessons and decisions as markdown in your Obsidian vault, searches them with SQLite FTS5, and mines past transcripts automatically.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 33 |
| 🍴 **Forks** | — |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude-code` `claude-code-plugin` `local-first` `mcp` `mcp-server` `memory` `obsidian` `persistent-memory` `python`

## 🎯 Categories

MCP · AI/ML · Documents · Backend · Database

## 📝 Summary

### English

**Project Summary:** TT-Wang/memem is an open-source Claude Code plugin that enables persistent memory across sessions by storing lessons and decisions in an Obsidian vault, allowing for efficient searching and automatic mining of past transcripts.

**Value Proposition:** This project offers a standard protocol for connecting AI assistants to real tools and data, facilitating seamless integrations and empowering users to build more effective workflows.

**Practical Adoption Path:** To adopt this project, users can start by installing the Claude Code plugin and configuring their Obsidian vault. They can then use the plugin's features to store and search lessons and decisions, and benefit from the automatic mining of past transcripts. As the project is open-source, users can also contribute to its development and customize it to suit their specific needs.

**Production Readiness:** With recent activity, adoption, and strong ecosystem signals, TT-Wang/memem exhibits high production readiness, making it a suitable candidate for serious pilots. However, a final review of the license, security posture, and active maintainers is still necessary to ensure its stability and reliability.

### Русский

TT‑Wang/memem — это плагин для Claude Code, который обеспечивает постоянную память ИИ‑ассистентов, сохраняет уроки и принятые решения в виде markdown‑файлов в вашем хранилище Obsidian, а затем быстро ищет их с помощью SQLite FTS5 и автоматически извлекает релевантные фрагменты из прошлых диалогов. Типичный сценарий: подключить AI‑агента к реальному набору инструментов и данных через стандартный Model Context Protocol, развернув сервер‑интегратор и используя предоставляемый API/CLI для обмена контекстом. Проект имеет высокий уровень готовности к production: активные коммиты, 33 звёзд на GitHub, поддержка Python, обширные метаданные и подтверждённое использование в пилотных проектах, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
TT‑Wang/memem 是一个 Claude Code 插件，能够为 Claude 提供跨会话的持久记忆。它把学习到的教训和决策以 Markdown 文件保存到你的 Obsidian Vault，并通过 SQLite FTS5 实现全文检索，同时自动挖掘历史对话记录。  

**价值主张**  
- **统一协议**：通过标准的 Model Context Protocol（MCP），把 AI 助手与本地工具、数据和知识库无缝连接。  
- **持久化记忆**：AI 能够记住过去的决策和上下文，提升连续对话的质量和效率。  
- **可搜索 & 可追溯**：使用 SQLite FTS5 对 Markdown 记忆库进行高速全文检索，支持快速定位历史教训。  

**典型接入方式**  
1. **API/SDK 接入**：在你的后端服务中调用 `memem` 提供的 HTTP API（或 Python SDK），向 Claude 发送 `store`、`retrieve`、`search` 等指令。  
2. **CLI 工具**：使用自带的命令行界面将 Obsidian Vault 路径、SQLite 数据库位置等配置写入 `memem config`，随后通过 `memem run` 启动 MCP 服务器。  
3. **插件化集成**：在自定义的 Claude Code 插件或其他 LLM 框架中直接引用 `memem` 包，实现“一键”记忆持久化与检索。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑02，项目仍在维护；GitHub ★33，拥有 10+ 相关主题标签。  
- **技术成熟度**：核心使用 Python 实现，依赖成熟的 SQLite FTS5，适配 Obsidian 的 Markdown 结构，易于在容器或虚拟环境中部署。  
- **风险点**：需进一步审查许可证（MIT/Apache 等）以及安全审计情况；确保维护者对安全漏洞的响应及时。  
- **总体评估**：在 OSS 候选中属于 **高生产就绪度**，适合作为内部 pilot 或对外服务的记忆层，尤其在需要 AI 与本地知识库深度集成的场景下。

## 🧭 Practical evaluation

**Value:** TT-Wang/memem helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 33 GitHub stars
- updated 2026-07-02
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 23/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/TT-Wang/memem) · [← Back to Mcp](./README.md)</sub>
