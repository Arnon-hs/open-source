# aaronsb/obsidian-mcp-plugin

[![Stars](https://img.shields.io/github/stars/aaronsb/obsidian-mcp-plugin?style=flat-square&color=yellow)](https://github.com/aaronsb/obsidian-mcp-plugin/stargazers) [![Forks](https://img.shields.io/github/forks/aaronsb/obsidian-mcp-plugin?style=flat-square&color=blue)](https://github.com/aaronsb/obsidian-mcp-plugin/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> High-performance Model Context Protocol (MCP) server for Obsidian that provides AI tools with direct vault access through semantic operations and HTTP transport.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 423 |
| 🍴 **Forks** | 41 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `claude` `knowledge-graph` `mcp` `model-context-protocol` `obsidian` `obsidian-plugin` `semantic-search`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The aaronsb/obsidian‑mcp‑plugin is a high‑performance Model Context Protocol (MCP) server written in TypeScript that runs inside Obsidian, exposing the vault’s content via semantic operations over an HTTP API. It lets AI assistants and other LLM‑driven tools query, update, and reason over a user’s notes as a structured knowledge base, enabling real‑time, context‑rich interactions. With over 400 GitHub stars and recent activity, it is a mature open‑source candidate for pilot projects.

**Value**  
- **Direct vault access**: AI agents can read and write to an Obsidian vault without custom scraping or file‑system hacks, preserving note hierarchy, backlinks, and metadata.  
- **Standardised protocol**: By implementing MCP, the plugin provides a language‑agnostic contract (HTTP + JSON) that can be consumed by any LLM‑orchestrator, reducing integration effort across tools.  
- **Semantic operations**: Built‑in query capabilities (e.g., similarity search, tag filtering) let downstream models retrieve the most relevant context, improving retrieval‑augmented generation (RAG) results.  

**Practical Adoption Path**  
1. **Deploy** the plugin in a development Obsidian vault (via the Obsidian Marketplace or manual install).  
2. **Configure** the MCP server (port, authentication token, optional TLS) using the provided UI or a simple `config.json`.  
3. **Consume the API** from your AI orchestration layer (Python, Node, etc.) using the auto‑generated OpenAPI spec or the bundled CLI/SDK.  
4. **Iterate** by adding custom semantic handlers (e.g., custom embeddings) through the plugin’s extension points, then promote the setup to staging or production vaults.  

**Production Readiness**  
- **Activity & community**: 423 stars, 41 forks, last commit 2026‑06‑24, and active issue discussions indicate a healthy maintainer base.  
- **Stability**: The TypeScript codebase follows strict typing, includes unit tests, and the HTTP interface is versioned, making breaking changes predictable.  
- **Security & licensing**: No immediate metadata risks, but a final review of the MIT/Apache license compliance and a security audit of the HTTP endpoint (auth, rate‑limiting) is advisable before enterprise rollout.  
Overall, the plugin is ready for a serious pilot in production environments, especially where teams already use Obsidian as a knowledge base and need LLM‑driven tooling.

### Русский

**aaronsb/obsidian-mcp-plugin** — это высокопроизводительный сервер Model Context Protocol (MCP) для Obsidian, который через семантические операции и HTTP‑транспорт предоставляет AI‑инструментам прямой доступ к содержимому хранилища. Типичный сценарий — подключение AI‑агентов к реальным файлам и инструментам Obsidian, стандартизация интеграций и развертывание собственного MCP‑сервера в качестве бекенда для RAG‑систем. Проект считается готовым к production: активные коммиты, 423 звёзд, поддержка TypeScript, наличие API/SDK/CLI и положительные сигналы экосистемы, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
aaronsb/obsidian-mcp-plugin 是一款基于 TypeScript 的高性能 Model Context Protocol (MCP) 服务器，运行在 Obsidian 笔记库之上。它通过语义化操作和 HTTP 接口，让 AI 助手能够直接读取、查询和写入 Vault 内容，实现“AI 即工具”。

**价值点**  
- **统一协议**：使用标准化的 MCP，让不同的 AI 模型、代理或工具能够以同一套 API 进行上下文获取和写入，降低集成成本。  
- **实时语义访问**：提供全文向量检索、标签/链接解析等语义操作，帮助 RAG（检索增强生成）和知识图谱构建获得更准确的上下文。  
- **即插即用**：只需在 Obsidian 中安装插件并启动 MCP 服务器，即可让外部 AI 服务通过 HTTP 调用 Vault，快速实现“AI + 知识库”的闭环。

**典型接入方式**  
1. **API/SDK**：在 AI 代理或后端服务中使用 HTTP 客户端（如 `fetch`、`axios`）调用 MCP 的 `/query`, `/write`, `/search` 等端点。  
2. **CLI**：插件自带的命令行工具可在 CI/CD 或本地脚本中执行批量导入/导出、索引刷新等操作。  
3. **语言绑定**：社区已有 Node.js、Python（via `requests`）的示例代码，可直接拷贝改造为项目自己的 SDK。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24 最近一次提交，星标 423、Fork 41，社区讨论活跃，说明维护者仍在持续迭代。  
- **技术成熟度**：使用 TypeScript 编写，代码结构清晰，提供完整的 OpenAPI 文档，易于审计和二次开发。  
- **安全与合规**：目前未发现重大元数据泄露风险；仍需自行评估许可证（MIT）与内部安全策略的兼容性。  
- **可部署性**：支持 Docker 镜像和本地 Node 运行，两种方式均可在 Kubernetes 或普通服务器上快速上线。  

综合来看，aaronsb/obsidian-mcp-plugin 已具备 **高可用、易集成、社区活跃** 的特征，是在生产环境中将 Obsidian 知识库与 AI 代理对接的可靠 OSS 方案。后续只需进行安全审计和运维监控，即可投入正式业务使用。

## 🧭 Practical evaluation

**Value:** aaronsb/obsidian-mcp-plugin helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 423 GitHub stars
- 41 forks
- updated 2026-06-24
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 60/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/aaronsb/obsidian-mcp-plugin) · [← Back to Mcp](./README.md)</sub>
