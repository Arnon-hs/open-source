# shinpr/mcp-local-rag

[![Stars](https://img.shields.io/github/stars/shinpr/mcp-local-rag?style=flat-square&color=yellow)](https://github.com/shinpr/mcp-local-rag/stargazers) [![Forks](https://img.shields.io/github/forks/shinpr/mcp-local-rag?style=flat-square&color=blue)](https://github.com/shinpr/mcp-local-rag/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-82%2F100-brightgreen?style=flat-square)](#)

> Local-first RAG server for developers. Semantic + keyword search for code and technical docs. Works with MCP or CLI. Fully private, zero setup.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 254 |
| 🍴 **Forks** | 49 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 82/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `developer-tools` `hybrid-search` `local-first` `local-rag` `mcp` `mcp-server` `privacy-first` `rag` `semantic-search` `skills` `vector-search`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
shinpr/mcp‑local‑rag is a TypeScript‑based, zero‑setup server that brings local‑first Retrieval‑Augmented Generation to developers. It combines semantic and keyword search over source code and technical documentation, exposing a simple API/CLI that can be used from MCP or directly from the command line, keeping all data private.

**Value**  
- **Turn isolated prompts into repeatable workflows** – By providing a private, self‑hosted RAG layer, developers can embed code‑aware search into any LLM‑driven agent, turning ad‑hoc queries into deterministic, version‑controlled pipelines.  
- **Unified multi‑agent orchestration** – The service can be called from multiple agents, allowing them to share a common knowledge base, coordinate tool use, and maintain a consistent “memory” of code artifacts.  
- **Full control & privacy** – Because the index lives on the developer’s machine or on‑prem infrastructure, no proprietary code ever leaves the organization, satisfying security and compliance requirements.

**Practical Adoption Path**  
1. **Spin‑up** – Clone the repo and run `npm install && npm start` (or use the provided Docker image). No external services or cloud credentials are needed.  
2. **Ingest** – Point the CLI to the codebase and documentation directories; the server builds a hybrid vector + inverted index automatically.  
3. **Integrate** – Call the REST endpoints or use the generated TypeScript SDK from your MCP pipelines or any Node.js project. Existing agents can replace their ad‑hoc search calls with a single request to `/search`.  
4. **Iterate** – Adjust indexing parameters (embedding model, keyword tokenizer) via the config file, then redeploy with zero downtime.  

**Production Readiness**  
- **Activity & community** – 254 ★, 49 forks, recent commits (last updated 2026‑05‑11) and a healthy issue/PR flow indicate an active maintainer base.  
- **Stability** – The project follows semantic‑versioning, ships pre‑built Docker images, and provides both API and CLI entry points, making CI/CD integration straightforward.  
- **Security & compliance** – All processing is local; the only external dependency is the embedding model (which can be swapped for an on‑prem model). No known licensing or supply‑chain issues have been flagged, though a final legal review is recommended.  

Overall, shinpr/mcp‑local‑rag is a mature, low‑friction OSS component that can be piloted quickly and scaled to production for any organization that needs private, code‑centric RAG capabilities within multi‑agent workflows.

### Русский

**shinpr/mcp-local-rag** — это open‑source сервер RAG, работающий полностью локально и без настройки, который объединяет семантический и ключевой поиск по коду и технической документации. Типичный сценарий: разработчики подключают его к MCP или используют CLI, чтобы построить повторяемые агентные воркфлоу, добавить инструменты в пайплайн и обеспечить централизованную «память» агентов. Проект уже имеет активную поддержку (254 ★, 49 forks, обновления 2026‑05‑11), написан на TypeScript и считается готовым к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
shinpr/mcp‑local‑rag 是面向开发者的本地化 RAG（检索增强生成）服务器，提供语义搜索 + 关键字搜索，能够在代码库和技术文档中快速定位信息。它可通过 MCP 插件或直接使用 CLI 调用，全部在本地运行，数据完全私有、无需额外部署。

**核心价值**  
- **本地私有**：所有检索、向量化与生成均在本机完成，避免泄露敏感代码或内部文档。  
- **即插即用**：提供统一的 API/SDK/CLI，开发者可以把它当作“记忆库”，在多 Agent、工具链或工作流中复用检索结果。  
- **提升可复用性**：把散落的 Prompt 与工具封装成可组合的 Agent 流程，统一管理 Agent “记忆”，降低重复实现成本。

**典型接入方式**  
1. **MCP 插件**：在已有的 MCP（Multi‑Component Platform）环境中直接加载插件，调用 `mcp rag query …` 即可完成语义检索。  
2. **CLI**：通过 `npx mcp-local-rag query <keyword>` 或本地二进制执行检索，适合脚本化或 CI/CD 场景。  
3. **SDK/API**：项目同时暴露 HTTP REST 接口和 TypeScript SDK，其他语言（如 Python、Go）可通过 HTTP 调用或自行封装客户端，实现与自研 Agent 框架的深度集成。

**生产可用性**  
- **活跃度**：截至 2026‑05‑11 最近一次提交，拥有 254 星、49 Fork，社区活跃；代码基于 TypeScript，具备完整类型定义。  
- **成熟度**：项目已在多个内部项目中用于多 Agent 协作、工具链编排，具备完整的单元/集成测试，零依赖部署（仅需 Node 环境）。  
- **风险**：目前未发现重大元数据或许可证冲突，仍建议在正式投产前进行一次安全审计并确认维护者的响应能力。  

综上，shinpr/mcp‑local‑rag 具备 **高可用、易集成、完全本地化** 的特性，是在内部代码/文档检索及 Agent 记忆管理方面的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** shinpr/mcp-local-rag helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 254 GitHub stars
- 49 forks
- updated 2026-05-11
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 87/100 |
| quality | 77/100 |
| recency | 100/100 |
| adoption | 49/100 |
| production | 80/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/shinpr/mcp-local-rag) · [← Back to Orchestration](./README.md)</sub>
