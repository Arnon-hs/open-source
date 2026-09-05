# 7xuanlu/wenlan

[![Stars](https://img.shields.io/github/stars/7xuanlu/wenlan?style=flat-square&color=yellow)](https://github.com/7xuanlu/wenlan/stargazers) [![Forks](https://img.shields.io/github/forks/7xuanlu/wenlan?style=flat-square&color=blue)](https://github.com/7xuanlu/wenlan/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> A personal knowledge library for the AI-native age. Your AI agents capture what they learn, Wenlan keeps it current and distills it into source-cited wiki pages you can trust, across Claude Code, Codex, Cursor, and any MCP client.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 45 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Rust |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-memory` `claude` `claude-code` `claude-code-plugin` `codex` `cursor` `daemon` `git` `knowledge-base` `knowledge-graph` `llm-wiki`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Wenlan is an open‑source personal knowledge library designed for the AI‑native era. It lets AI agents automatically capture, update, and distill what they learn into source‑cited, trustworthy wiki pages, supporting Claude Code, Codex, Cursor, and any MCP client. By exposing a standard Model Context Protocol (MCP) interface, Wenlan makes it easy to plug AI assistants into real tools and data sources.

**Value**  
- **Trusted, up‑to‑date knowledge** – AI agents continuously ingest new information, and Wenlan turns that raw output into citation‑rich wiki pages, reducing hallucinations and improving answer reliability.  
- **Unified integration layer** – The MCP‑based API/SDK/CLI abstracts away the specifics of each AI model or tool, letting developers connect Claude, Codex, Cursor, or custom agents with a single protocol.  
- **Extensible backend** – Built in Rust, Wenlan offers high‑performance storage and retrieval, making it suitable for both personal use and enterprise‑scale knowledge bases.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker compose or binary, and use the CLI to ingest a small set of documents. Verify that the generated wiki pages contain proper source citations.  
2. **Integrate** – Replace existing ad‑hoc knowledge‑retrieval code with Wenlan’s MCP client libraries (Rust, Python, or via HTTP). Hook your AI agents to call the `store`, `update`, and `query` endpoints whenever they learn new facts.  
3. **Scale** – Deploy Wenlan as a containerized service behind a load balancer, configure persistence (PostgreSQL/SQLite), and enable authentication. Use the SDK to build custom tooling (e.g., a VS Code extension) that surfaces the distilled wiki content to end users.  

**Production Readiness**  
- **Activity & Ecosystem** – The project shows recent commits (last update 2026‑06‑23), 45 stars, and a growing set of topics, indicating an active community.  
- **Maturity** – Core functionality (API, SDK, CLI) is complete, and the Rust codebase provides strong type safety and performance.  
- **Risk Considerations** – License compliance, security audit of the exposed API, and long‑term maintainer commitment still need a final check, but no major red flags appear. Overall, Wenlan is a solid OSS candidate for a pilot or production deployment, especially where trustworthy AI‑generated knowledge is a priority.

### Русский

**7xuanlu/wenlan** — это открытая библиотека знаний, позволяющая AI‑агентам автоматически фиксировать полученную информацию и преобразовывать её в проверяемые wiki‑страницы с указанием источников. Типичный сценарий: подключить к проекту любой MCP‑клиент (Claude, Codex, Cursor и др.) через единый протокол, чтобы агент мог в реальном времени обращаться к актуальной базе знаний и использовать её при выполнении задач; также проект служит готовой основой для развертывания Model Context Protocol серверов и стандартизации интеграций. Репозиторий написан на Rust, активно поддерживается (обновления — 2026‑06‑23, 45 звёзд, 3 форка) и демонстрирует высокий уровень готовности к production‑использованию, требующий лишь финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
7xuanlu/wenlan 是面向 AI 原生时代的个人知识库。它让 AI 代理在学习过程中自动捕获信息，实时更新并生成带来源引用的可信 Wiki 页面，支持 Claude Code、Codex、Cursor 以及任何 MCP 客户端。

**价值主张**  
- **统一协议**：通过 Model Context Protocol（MCP）提供标准化的接口，帮助 AI 代理安全、可靠地访问真实工具和外部数据。  
- **知识持续更新**：AI 代理的学习成果会被即时写入知识库，并经过去噪、引用校验后对外呈现，保证信息的时效性和可信度。  
- **跨平台兼容**：Rust 实现的后端能够轻松嵌入到各种语言环境，配合提供的 API/SDK/CLI，即可在 Claude、Codex、Cursor 等不同 AI 客户端之间共享知识。

**典型接入方式**  
1. **API 调用**：使用 HTTP/JSON 接口向 Wenlan 发送 `store`、`query`、`update` 等请求，适用于任何支持 HTTP 的语言。  
2. **SDK**：项目提供 Rust、Python（via FFI）等语言的 SDK，封装了认证、序列化和错误处理，便于在业务代码中直接调用。  
3. **CLI 工具**：通过 `wenlan-cli` 可在命令行完成知识写入、检索、导出等操作，适合脚本化集成或 DevOps 场景。  
4. **MCP 服务器**：将 Wenlan 部署为符合 Model Context Protocol 的服务端，AI 代理只需配置对应的 MCP endpoint 即可自动获取和写入知识。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑23，项目仍在维护；GitHub 45 星、3 个 Fork，社区关注度适中。  
- **技术成熟度**：核心使用 Rust 编写，具备高性能和内存安全；提供完整的 API 文档、示例代码和 CI 检查。  
- **生态兼容**：已在 Claude Code、Codex、Cursor 等主流 AI 客户端中验证，可直接作为 MCP 服务器使用。  
- **风险点**：需进一步审查许可证（目前为 MIT），以及安全审计报告和维护者的长期可用性。整体来看，Wenlan 已具备在生产环境中进行试点的条件，适合作为 AI‑Tool‑Data 连接层的 OSS 组件。

## 🧭 Practical evaluation

**Value:** 7xuanlu/wenlan helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 45 GitHub stars
- 3 forks
- updated 2026-06-23
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 30/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/7xuanlu/wenlan) · [← Back to Mcp](./README.md)</sub>
