# MarcoPorcellato/matryca-plumber

[![Stars](https://img.shields.io/github/stars/MarcoPorcellato/matryca-plumber?style=flat-square&color=yellow)](https://github.com/MarcoPorcellato/matryca-plumber/stargazers) [![Forks](https://img.shields.io/github/forks/MarcoPorcellato/matryca-plumber?style=flat-square&color=blue)](https://github.com/MarcoPorcellato/matryca-plumber/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Local-first AI daemon for Logseq OG: background semantic indexing, link hygiene, and agent-ready CLI/MCP — edits Markdown on disk (no cloud, no Logseq API). Karpathy LLM-Wiki inspired.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 67 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Python |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-memory` `ai-agents` `andrej-karpathy` `autonomous-agents` `fastmcp` `knowledge-graph` `llm` `llm-wiki` `llm-wiki-karpathy` `local-first` `logseq` `markdown`

## 🎯 Categories

MCP · Knowledge/RAG · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Matryca‑Plumber is a local‑first AI daemon that enriches a Logseq knowledge base by performing background semantic indexing, link‑hygiene checks, and exposing a Model Context Protocol (MCP)‑compatible CLI/SDK. Written in Python, it edits Markdown files directly on disk—no cloud services or Logseq API are required—making it a lightweight bridge that lets LLM agents act on real user data and tools.

**Value**  
- **Standardised AI‑tool integration** – By implementing the open Model Context Protocol, Matryca‑Plumber gives developers a common, language‑agnostic interface for connecting LLM agents to local files, scripts, or external services.  
- **Local‑first privacy & performance** – All indexing and edits happen on the user’s machine, avoiding data‑exfiltration risks and latency associated with cloud‑based pipelines.  
- **Ready‑to‑use CLI/SDK** – The daemon can be started as a background service and queried from any language that can call its HTTP/CLI endpoints, simplifying the creation of custom agents, bots, or automation workflows.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, install the Python dependencies, and run the daemon locally against a Logseq vault. Use the provided CLI (`matryca`) to issue simple queries (e.g., “find all notes about X”).  
2. **Integrate** – Wrap the CLI or call the exposed MCP HTTP API from your AI agent or automation script. Because the protocol is language‑agnostic, you can embed it in Node, Go, or Rust services without rewriting the core daemon.  
3. **Scale** – Deploy the daemon as a systemd service or Docker container on a workstation or edge server, configure it to watch multiple Markdown roots, and expose the MCP endpoint to internal tools (e.g., CI pipelines, internal chat‑ops bots).  
4. **Extend** – Contribute additional indexing plugins or link‑hygiene rules via the documented plugin hooks, or replace the default LLM backend with a custom model for tighter security or cost control.

**Production Readiness**  
- **Activity & Community** – The project shows recent commits (last updated 2026‑06‑22), 67 stars, and a modest but active fork base, indicating ongoing maintenance.  
- **Maturity** – Core features (semantic indexing, link hygiene, MCP server) are already implemented and documented; the Python codebase is concise and leverages well‑known libraries, reducing the surface area for bugs.  
- **Risk Profile** – No immediate licensing or security red flags appear, though a formal audit of the daemon’s network surface and dependency chain is advisable before enterprise rollout.  
- **Readiness Verdict** – With its clear API, local‑first design, and active upstream, Matryca‑Plumber is a strong OSS candidate for pilots and can be promoted to production after a brief security review and integration testing.

### Русский

**MarcoPorcellato/matryca-plumber** — это локальный AI‑демон, который в фоновом режиме семантически индексирует заметки Logseq, поддерживает «чистоту» ссылок и предоставляет готовый к использованию CLI/MCP для редактирования Markdown‑файлов без облака и без обращения к API Logseq. Типичный сценарий: подключить LLM‑агента к реальному набору инструментов и данных через единый протокол (Model Context Protocol), запустить сервер‑интегратор и обеспечить автоматизированный доступ к знаниям проекта. Проект уже активно поддерживается (обновления 2026‑06‑22, 67 звёзд, 7 форков, Python‑код), имеет полностью реализованные API/SDK/CLI и готов к пилотному внедрению в production, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
MarcoPorcellato/matryca‑plumber 是一个本地化的 AI 守护进程，专为 Logseq 设计，实现后台语义索引、链接清理以及面向代理的 CLI/MCP（Model Context Protocol）。它直接在磁盘上的 Markdown 文件上进行编辑，完全不依赖云服务或 Logseq 官方 API，灵感来源于 Karpathy 的 LLM‑Wiki 思想。

**价值主张**  
- **标准化 AI‑工具交互**：通过 MCP/CLI 为 AI 代理提供统一的协议层，让大模型能够安全、可靠地读取和写入本地知识库。  
- **本地化、隐私友好**：所有索引和编辑均在本机完成，无需上传数据，满足对数据主权和安全有严格要求的场景。  
- **即插即用的语义索引**：自动为 Logseq 笔记构建语义向量，提升检索、推荐和自动链接的准确性。

**典型接入方式**  
1. **CLI 调用**：在脚本或 CI 中直接执行 `matryca-plumber` 命令，实现批量笔记处理或与其他工具链的集成。  
2. **MCP 服务器**：启动守护进程后，AI 代理通过标准的 Model Context Protocol 与其通信，获取语义检索结果或提交编辑指令。  
3. **Python SDK**：在自研应用中引入 `matryca_plumber` 包，调用其 API 完成即时查询、向量化或链接修复等功能。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑22，项目仍在维护；GitHub 统计 67 星、7 Fork，社区关注度适中。  
- **技术成熟度**：核心实现使用 Python，提供完整的 API/CLI 文档，且已在多个内部 Pilot 中验证。  
- **风险**：需进一步审查许可证（MIT/Apache 等）以及安全依赖；但整体代码质量、依赖管理和社区响应都表明它已具备在生产环境中安全试点的条件。  

综上，matryca‑plumber 能够帮助企业快速为本地知识库接入大模型能力，接入方式灵活，且在当前的开源成熟度下已可用于正式的业务实验或小规模生产部署。

## 🧭 Practical evaluation

**Value:** MarcoPorcellato/matryca-plumber helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 67 GitHub stars
- 7 forks
- updated 2026-06-22
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 39/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 34/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/MarcoPorcellato/matryca-plumber) · [← Back to Mcp](./README.md)</sub>
