# vitali87/code-graph-rag

[![Stars](https://img.shields.io/github/stars/vitali87/code-graph-rag?style=flat-square&color=yellow)](https://github.com/vitali87/code-graph-rag/stargazers) [![Forks](https://img.shields.io/github/forks/vitali87/code-graph-rag?style=flat-square&color=blue)](https://github.com/vitali87/code-graph-rag/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> The ultimate RAG for your monorepo. Query, understand, and edit multi-language codebases with the power of AI and knowledge graphs

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 379 |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ast` `claude-code` `code-analysis` `code-understanding` `codebase-search` `developer-tools` `graph-database` `knowledge-graph` `llm` `mcp` `mcp-server`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
vitali87/code‑graph‑rag is an open‑source RAG (Retrieval‑Augmented Generation) platform that builds knowledge graphs over multi‑language monorepos, letting AI assistants query, understand, and even edit code across the whole codebase. It ships a standard Model Context Protocol (MCP) server, SDK and CLI, making it easy to connect external AI agents to real development tools and data.  

**Value**  
- **Unified code insight**: By converting a repository into a searchable knowledge graph, developers and AI agents can retrieve precise code fragments, dependencies, and architectural context in a single query.  
- **Tool‑agnostic integration**: The MCP‑compliant server and language‑agnostic SDK let any AI model or automation framework hook into the graph without custom adapters, accelerating the creation of AI‑driven tooling (e.g., code review bots, automated refactors, documentation generators).  
- **Multi‑language support**: Works out‑of‑the‑box for polyglot monorepos, reducing the friction of building separate parsers or embeddings for each language.  

**Practical Adoption Path**  
1. **Pilot** – Deploy the provided Docker image or run the Python server locally; point it at a target monorepo and let it index the code.  
2. **Integrate** – Use the MCP‑compatible SDK/CLI to issue queries from an existing AI assistant (e.g., OpenAI, Claude) or from a custom bot.  
3. **Extend** – Add custom metadata (e.g., CI status, issue links) via the SDK to enrich the graph, then expose the enhanced context to downstream tools.  
4. **Scale** – Move the server to a managed environment (K8s, serverless) and enable caching or sharding for very large repos; adopt the provided Helm chart for production rollout.  

**Production Readiness**  
- **Strong community signals**: 2.2 k GitHub stars, 379 forks, recent commits (as of 2026‑06‑27) and active issue discussion indicate a healthy, maintained project.  
- **Mature artifact set**: API, SDK, and CLI are all released, and the MCP spec is already used by several early adopters, reducing integration risk.  
- **Scalable architecture**: Built in Python with optional containerization; can be horizontally scaled and integrated into CI/CD pipelines.  
- **Remaining checks**: A final review of licensing compliance, security hardening (dependency scanning), and maintainer responsiveness is advised, but the overall risk profile is low, making it suitable for serious pilot deployments and, with the above due‑diligence, for production use.

### Русский

Резюме:

Валютный граф (code-graph-rag) - это мощный инструмент для анализа и редактирования кодовой базы монорепозитория с помощью искусственного интеллекта и знакомых графиков. Этот проект позволяет соединять агентов AI с реальными инструментами и данными посредством стандартного протокола, что делает его идеальным решением для интеграции AI в существующие процессы разработки. Проект полностью готов к производству (production readiness: High) и уже получил широкое признание в сообществе (2274 GitHub stars, 379 forks).

### 中文

**项目简介**  
vitali87/code-graph-rag 是面向单体仓库（monorepo）的全功能 RAG（检索增强生成）工具。它通过知识图谱把多语言代码库转化为结构化语义信息，配合大模型实现代码查询、理解乃至自动编辑。

**价值主张**  
- **统一协议**：提供标准化的 Model Context Protocol（MCP），让 AI 助手能够安全、可靠地调用真实工具和底层数据。  
- **跨语言、跨项目**：一次索引即可在同一仓库内的不同语言（Python、JavaScript、Go 等）之间进行语义搜索和关联。  
- **提升开发效率**：开发者和 AI 代理可以直接通过 API/CLI 查询代码上下文、获取调用示例或自动生成补丁，显著降低调试和维护成本。

**典型接入方式**  
1. **API/SDK**：在现有后端服务中引入 Python SDK，调用 `search`, `edit` 等端点即可完成代码检索和修改。  
2. **CLI**：通过提供的命令行工具在 CI/CD 流水线或本地开发环境中执行快速查询或批量编辑。  
3. **MCP 服务器**：部署 Model Context Protocol 服务器，作为统一的 “AI‑Tool Bridge”，供多种 AI 代理（如 ChatGPT、Claude）统一访问。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑27，项目拥有 2,274 星、379 Fork，最近一次提交仅几天前，社区活跃。  
- **技术成熟**：核心实现基于 Python，提供完整的 API、SDK 与 CLI，文档齐全，已在多个开源项目中试点。  
- **风险可控**：暂无重大元数据或许可证风险，仍建议在正式投产前进行一次安全审计和维护者确认。  

综合来看，code-graph-rag 已具备在生产环境中进行试点的条件，适合作为 AI‑驱动代码工具链的核心组件。

## 🧭 Practical evaluation

**Value:** vitali87/code-graph-rag helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2274 GitHub stars
- 379 forks
- updated 2026-06-27
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 61/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/vitali87/code-graph-rag) · [← Back to Mcp](./README.md)</sub>
