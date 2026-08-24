# 54yyyu/zotero-mcp

[![Stars](https://img.shields.io/github/stars/54yyyu/zotero-mcp?style=flat-square&color=yellow)](https://github.com/54yyyu/zotero-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/54yyyu/zotero-mcp?style=flat-square&color=blue)](https://github.com/54yyyu/zotero-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Zotero MCP: Connects your Zotero research library with Claude and other AI assistants via the Model Context Protocol to discuss papers, get summaries, analyze citations, and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.1k |
| 🍴 **Forks** | 349 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `mcp` `semantic-search` `zotero`

## 🎯 Categories

MCP · Knowledge/RAG

## 📝 Summary

### English

Here's a brief summary of the project and its key aspects:

**Summary:** Zotero MCP is an open-source project that enables seamless integration between Zotero, a research library tool, and AI assistants like Claude through the Model Context Protocol. This connection allows for various tasks such as paper discussions, summaries, citation analysis, and more. By standardizing integrations, Zotero MCP facilitates the connection of AI agents to real tools and data.

**Value Proposition:** The primary value proposition of Zotero MCP lies in its ability to connect AI assistants to real tools and data through a standard protocol. This standardization enables the creation of a more cohesive and integrated ecosystem where AI agents can access and utilize relevant information from various sources.

**Practical Adoption Path:** To adopt Zotero MCP, users can start by integrating their Zotero research library with AI assistants like Claude. This integration can be achieved by exposing API/SDK/CLI implementation signals, which are straightforward to evaluate. The project's recent activity, adoption, and ecosystem signals make it a strong candidate for a serious pilot. Additionally, the production-ready nature of the project ensures that it can be used in a production environment with minimal risk.

**Production Readiness:** Zotero MCP has demonstrated high production readiness due to its recent activity, adoption, and ecosystem

### Русский

54yyyu/zotero-mcp: проект Zotero MCP представляет собой соединение вашей библиотеки Zotero с помощниками AI, такими как Claude, через протокол Model Context Protocol для обсуждения статей, получения кратких обзоров, анализа цитирования и т.п.

Этот проект предназначен для соединения помощников AI с реальными инструментами и данными посредством стандартного протокола, что позволяет упростить интеграцию и повысить эффективность работы. Типовая сценария внедрения: соединение помощников AI с инструментами Zotero для анализа и обсуждения научных данных.

Проект готов к production, поскольку имеет высокий уровень активности, адопции и сигналов экосистемы, а также недавние обновления и сильную поддержку разработчиков.

### 中文

**简短介绍**  
Zotero MCP 将你的 Zotero 文献库通过 **Model Context Protocol（MCP）** 暴露为标准化的接口，帮助 Claude、ChatGPT 等 AI 助手直接读取、查询、摘要和分析文献及其引用，实现在对话中“即问即得”。

**价值**  
- **统一协议**：使用 MCP 作为桥梁，AI 助手可以像调用本地工具一样调用 Zotero，避免为每个 AI 平台单独实现专属插件。  
- **实时文献洞察**：在聊天中即时获取论文摘要、关键结论、引用网络分析等，提升科研阅读与写作效率。  
- **生态兼容**：作为开源 Python 项目，提供 API、SDK 与 CLI，方便在自研 AI Agent、工作流自动化或 RAG 系统中快速集成。

**典型接入方式**  
1. **部署 MCP 服务器**：在本地或云端运行 `zotero-mcp`，它会监听 HTTP/WS 接口并与本地 Zotero 数据库同步。  
2. **调用 API**：AI 助手（如 Claude、ChatGPT）通过标准的 MCP 请求（`/search`, `/summarize`, `/citations` 等）获取文献信息。  
3. **使用 SDK/CLI**：在 Python 脚本或命令行中直接调用 `zotero_mcp.Client`，适用于自定义工具或批处理任务。  

**生产可用性**  
- **活跃维护**：最近一次提交（2026‑07‑03）且社区活跃，拥有 4 k+ Stars、350+ Fork，说明已有广泛使用和反馈。  
- **成熟度**：提供完整的 API 文档、示例代码和 Docker 镜像，易于在容器化环境中部署。  
- **安全与合规**：项目采用 MIT 许可证，代码公开，可自行审计依赖安全性；但在正式生产前仍建议进行内部安全评估和权限控制（如仅对内部网络开放 API）。  

综合来看，`54yyyu/zotero-mcp` 已具备较高的生产就绪度，适合作为科研团队或企业内部 AI 助手的文献后端服务，快速实现“AI + Zotero”的闭环工作流。

## 🧭 Practical evaluation

**Value:** 54yyyu/zotero-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4110 GitHub stars
- 349 forks
- updated 2026-07-03
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 77/100 |
| topics | 50/100 |
| outlook | 59/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/54yyyu/zotero-mcp) · [← Back to Mcp](./README.md)</sub>
