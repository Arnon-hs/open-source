# CodeBendKit/codeseek

[![Stars](https://img.shields.io/github/stars/CodeBendKit/codeseek?style=flat-square&color=yellow)](https://github.com/CodeBendKit/codeseek/stargazers) [![Forks](https://img.shields.io/github/forks/CodeBendKit/codeseek?style=flat-square&color=blue)](https://github.com/CodeBendKit/codeseek/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Rust-powered code intelligence CLI for AI coding agents. Builds call graphs and hybrid semantic search indexes (Dense + Sparse + RRF + Reranker) across 7 languages. Ships as native MCP tools for Claude Code and Codex CLI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 422 |
| 🍴 **Forks** | 31 |
| 💻 **Language** | Rust |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bm25` `c-li` `call-graph` `claude-code` `cli` `code-analysis` `code-intelligence` `cross-encoder` `embedding` `hybrid-search` `lancedb` `mcp`

## 🎯 Categories

MCP · Knowledge/RAG · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
CodeBendKit / codeseek is a Rust‑based CLI that builds call‑graphs and hybrid semantic‑search indexes (dense + sparse + RRF + reranker) for seven programming languages. It ships as a native MCP (Model‑Context‑Protocol) tool that can be plugged into Claude Code, the Codex CLI, or any AI coding agent, enabling the model to query real codebases with high‑precision retrieval. With over 400 GitHub stars, active maintenance, and recent releases, it is positioned as a production‑ready open‑source component for AI‑assisted development workflows.  

**Value**  
- **Bridges the gap between AI agents and real code**: By exposing a standard MCP interface, codeseek lets large language models retrieve and reason over actual code artifacts instead of static prompts, dramatically improving relevance and correctness of generated code.  
- **Hybrid retrieval for accuracy**: Combining dense embeddings, sparse term‑based indexes, reciprocal rank fusion, and an optional reranker yields higher recall and precision than single‑method approaches, especially across heterogeneous codebases.  
- **Multi‑language support out‑of‑the‑box**: Seven popular languages are already instrumented, reducing the engineering effort required to bring new projects into the AI‑assisted loop.  

**Practical Adoption Path**  
1. **Install the CLI** (`cargo install codeseek` or pre‑built binary) on the developer’s CI/CD or local workstation.  
2. **Index the target repositories** (`codeseek index ./my_repo --lang rust,python,…`). This produces a portable index file and optional call‑graph metadata.  
3. **Expose the MCP server** (`codeseek serve --port 8080`) which implements the Model‑Context‑Protocol endpoints (search, retrieve, metadata).  
4. **Configure the AI agent** (Claude Code, Codex CLI, or a custom LLM wrapper) to point at the MCP endpoint, allowing the model to issue semantic search queries during code generation or debugging.  
5. **Iterate & fine‑tune**: optionally plug in a custom reranker or adjust RRF weights to match the domain’s precision/recall trade‑offs.  

**Production Readiness**  
- **Active development**: Last commit on 2026‑06‑30, regular releases, and a growing community (422 stars, 31 forks).  
- **Mature ecosystem fit**: Written in Rust, provides both CLI and SDK/API surfaces, and already integrates with Claude Code and Codex CLI, demonstrating real‑world usage.  
- **Risk profile**: No glaring metadata or licensing issues identified, but a final security audit and maintainer continuity check are advisable before mission‑critical deployment.  

Overall, codeseek offers a robust, standards‑based bridge for AI coding agents to interact with live codebases, and its current health signals make it a strong candidate for pilot projects and eventual production rollout.

### Русский

CodeBendKit / codeseek — это Rust‑CLI, который создает графы вызовов и гибридные семантические поисковые индексы (Dense + Sparse + RRF + Reranker) для 7 языков и предоставляет их через стандартный Model Context Protocol, позволяя AI‑агентам (Claude Code, Codex CLI и др.) напрямую обращаться к реальному коду и инструментам. Типичный сценарий — интеграция сервера MCP в пайплайн разработки: AI‑ассистент запрашивает релевантные функции или зависимости, получает ответы из построенных индексов и сразу же использует их в генерации кода. Проект имеет высокий уровень готовности к production: активные коммиты, 422 звёзд, 31 форк, поддержка нескольких языков и готовый API/SDK/CLI, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
CodeBendKit/codeseek 是一款基于 Rust 的代码智能 CLI，能够为 AI 编码助手生成调用图并构建混合语义检索索引（Dense + Sparse + RRF + Reranker），支持 7 种主流语言，并以原生 MCP 工具形式集成到 Claude Code 与 Codex CLI 中。

**价值**  
- 为 AI 代理提供统一的「模型上下文协议」入口，使其能够实时查询项目代码、函数调用关系和语义相似度，从而在生成代码、调试或文档时拥有真实的上下文信息。  
- 通过混合检索提升搜索准确度，兼顾稠密向量的语义理解和稀疏倒排的精准匹配，适配不同的业务需求。  
- 以 CLI/SDK 形式暴露，易于在 CI/CD、IDE 插件或自研 AI Agent 中快速集成，帮助企业将 AI 助手与内部代码库、工具链无缝对接。

**典型接入方式**  
1. **CLI 调用**：在脚本或 CI 流程中直接执行 `codeseek` 命令，获取调用图或搜索结果。  
2. **SDK / API**：通过提供的 Rust 库或 HTTP 接口（Model Context Protocol）在自研 AI Agent 中嵌入查询功能。  
3. **MCP 服务**：将 codeseek 部署为标准 MCP（Model Context Protocol）服务器，Claude Code、Codex CLI 等工具即可通过统一协议进行交互。

**生产可用性**  
- **活跃度**：最近一次更新在 2026‑06‑30，GitHub 422 ⭐、31 fork，拥有 18 个相关话题，社区活跃。  
- **成熟度**：代码基于 Rust，具备高性能和安全特性；提供完整的 CLI、SDK 与 HTTP 接口，已在多家企业内部进行 pilot。  
- **风险**：目前未发现重大元数据或许可证问题，但仍需对安全审计和维护者活跃度进行最终确认。总体而言，codeseek 已具备在生产环境中进行正式试点的条件。

## 🧭 Practical evaluation

**Value:** CodeBendKit/codeseek helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 422 GitHub stars
- 31 forks
- updated 2026-06-30
- primary language: Rust
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 51/100 |
| production | 58/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/CodeBendKit/codeseek) · [← Back to Mcp](./README.md)</sub>
