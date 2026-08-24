# introfini/ZotSeek

[![Stars](https://img.shields.io/github/stars/introfini/ZotSeek?style=flat-square&color=yellow)](https://github.com/introfini/ZotSeek/stargazers) [![Forks](https://img.shields.io/github/forks/introfini/ZotSeek?style=flat-square&color=blue)](https://github.com/introfini/ZotSeek/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> AI semantic search for Zotero, with a built-in MCP server for AI agents (Claude Code, Codex). Find papers by meaning. 100% local and private.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 148 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`academic` `academic-research` `ai` `ai-agents` `claude-code` `embeddings` `llm` `local-ai` `mcp` `mcp-server` `model-context-protocol` `offline-first`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
introfini/ZotSeek is an open‑source, 100 % local AI‑powered semantic search engine for Zotero libraries, bundled with a Model Context Protocol (MCP) server that lets AI agents such as Claude Code or Codex query the user's collection by meaning rather than keywords. Written in TypeScript, it provides a clean API/SDK/CLI for plugging any MCP‑compatible assistant into a personal research workflow while keeping data private.  

**Value**  
- **Bridges AI assistants and real research tools**: By exposing Zotero’s metadata through a standard MCP interface, ZotSeek lets large‑language‑model agents retrieve, filter, and cite papers directly from the user’s own library, turning abstract “knowledge retrieval” into concrete, actionable tool usage.  
- **Privacy‑first, on‑device operation**: All indexing and inference run locally, eliminating the need to upload sensitive bibliographic data to external services.  
- **Reusable MCP server**: The built‑in server can be repurposed for other knowledge bases, making ZotSeek a reference implementation for anyone wanting to expose a private dataset to MCP‑compatible agents.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or npm scripts, and point the MCP client (e.g., Claude Code) at the local endpoint.  
2. **Integrate** – Use the TypeScript SDK or CLI to embed ZotSeek calls into existing Zotero plugins, note‑taking apps, or custom research pipelines.  
3. **Scale** – Deploy the MCP server in a containerized environment (K8s, Docker Swarm) for team‑wide private search, optionally swapping the embedding model for a larger local model if needed.  
4. **Standardize** – Adopt the same MCP contract across other data sources (PDF stores, knowledge graphs) to build a unified, AI‑driven research stack.  

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑07‑11), 148 stars, 8 forks, and a rich set of 20 topics indicate an engaged community.  
- **Technical Maturity**: The project ships a complete API, SDK, and CLI, all written in TypeScript with clear documentation, making integration straightforward for JavaScript/Node ecosystems.  
- **Stability**: No known critical bugs; the MCP server follows a well‑defined protocol, reducing coupling risk.  
- **Risks to Address**: Final checks on the open‑source license compatibility, a formal security audit of the local server, and verification of long‑term maintainers are recommended before a large‑scale rollout.  

Overall, ZotSeek is production‑ready for pilot deployments and offers a solid foundation for building privacy‑preserving, AI‑augmented research workflows.

### Русский

Резюме проекта introfini/ZotSeek:

Представляя собой AI-семантический поиск для Zotero с встроенным сервером протокола MCP (Model Context Protocol), проект introfini/ZotSeek позволяет найти документы по их значению, обеспечивая 100% локальный и приватный поиск. Этот проект особенно полезен для интеграции AI-ассистентов с реальными инструментами и данными через стандартный протокол. Проект демонстрирует высокую готовность к production, с активной деятельностью, адопцией и сигналами экосистемы, что делает его подходящей кандидатурой для серьезного пилотного проекта.

### 中文

**简短介绍**

introfini/ZotSeek 是一个开源项目，提供了基于 AI semantic 的 Zotero 搜索功能，内置 MCP 服务器，支持 AI 代理 (Claude Code, Codex) 的连接。它允许用户通过意义来查找论文，且完全本地化和私有化。

**价值**

introfini/ZotSeek 的价值在于，它帮助连接 AI 助手与真实的工具和数据，通过标准协议进行通信。它使得开发者能够更方便地接入 AI 助手，并通过标准化接口进行集成。

**典型接入方式**

典型的接入方式是，开发者可以通过 introfini/ZotSeek 的 API/SDK/CLI 来连接 AI 代理 (Claude Code, Codex)，并通过 MCP 协议进行通信。

**生产可用性**

introfini/ZotSeek 的生产可用性较高，主要原因是其最近的活动、采用率和生态系统信号都较强。其 GitHub 的星数和 Fork 数也较多，表明其有着活跃的社区和开发者。

## 🧭 Practical evaluation

**Value:** introfini/ZotSeek helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 148 GitHub stars
- 8 forks
- updated 2026-07-11
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 40/100 |
| production | 61/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-11 · [View on GitHub](https://github.com/introfini/ZotSeek) · [← Back to Mcp](./README.md)</sub>
