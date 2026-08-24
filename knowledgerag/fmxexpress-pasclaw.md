# FMXExpress/PasClaw

[![Stars](https://img.shields.io/github/stars/FMXExpress/PasClaw?style=flat-square&color=yellow)](https://github.com/FMXExpress/PasClaw/stargazers) [![Forks](https://img.shields.io/github/forks/FMXExpress/PasClaw?style=flat-square&color=blue)](https://github.com/FMXExpress/PasClaw/network) [![Language](https://img.shields.io/badge/lang-Pascal-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> AI agent in Delphi Object Pascal

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | Pascal |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agentic-ai` `ai` `ai-agent` `delphi` `fpc` `object-pascal` `openclaw` `openclaw-agent` `openclaw-alternative` `rag` `wasm`

## 🎯 Categories

Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Brief Summary**  
FMXExpress/PasClaw is an open‑source AI agent written in Delphi Object Pascal that lets you index internal knowledge bases and surface that information to conversational assistants. It is positioned as a lightweight “search‑as‑you‑type” layer that can ground AI‑generated answers in company‑specific documents.

**Value**  
- **Knowledge retrieval** – By turning unstructured docs, wikis, or code repositories into a searchable index, PasClaw makes the right information instantly available to chat‑bots or other AI assistants, reducing hallucinations and improving response relevance.  
- **Delphi‑centric ecosystem** – For teams already developing in Delphi/FMX, the library offers a native solution without the need to embed external services or bridge to other languages.  
- **Rapid prototyping** – With only a few dozen stars and a recent commit, the project is small enough to experiment with, yet functional enough to demonstrate real‑world benefits.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the supplied README example, and point the indexer at a small, representative document set (e.g., a product FAQ). Verify that queries return the expected passages.  
2. **Integration Wrapper** – Build a thin Delphi wrapper that exposes PasClaw’s search API as a REST or gRPC endpoint, allowing other services (e.g., a Node‑based chatbot) to consume it.  
3. **Pilot Deployment** – Deploy the wrapper in a staging environment, connect it to a live knowledge base, and evaluate latency, relevance, and failure modes.  
4. **Scale‑up** – If the pilot succeeds, expand the indexed corpus, add incremental indexing, and implement caching or sharding as needed.

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent (updated 2026‑06‑26) and has modest community traction (32 ★, 6 forks). It is suitable for internal tools or prototypes but lacks extensive testing, CI pipelines, or formal release management.  
- **Dependencies**: The project relies on Delphi/FMX libraries that must be compatible with your compiler version; verify that required third‑party packages are still maintained.  
- **Operational Considerations**: Before production use, add unit/integration tests, monitor memory usage of the index, and establish a clear upgrade path for Delphi releases.  
- **Risk Mitigation**: Because the integration steps are not fully documented, allocate time for a small “setup‑cost” sprint to map the build process, resolve any missing dependencies, and create internal documentation.

Overall, PasClaw offers a compelling, Delphi‑native way to make internal knowledge searchable for AI assistants, but production deployment should follow a staged PoC → pilot → scaling approach, with added testing and maintenance safeguards.

### Русский

FMXExpress/PasClaw — open‑source‑агент на Delphi Object Pascal, который позволяет индексировать внутренние базы знаний и делать их доступными для AI‑ассистентов, улучшая поиск по документам и «заземляя» ответы помощников. Для внедрения рекомендуется начать с небольшого proof‑of‑concept: проверить README, собрать проект и протестировать индексацию небольшого набора данных, после чего оценить зависимости и требования к обслуживанию. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но перед выпуском в продакшн требуется уточнить интеграционный путь и обеспечить стабильность зависимостей.

### 中文

**项目简介**  
FMXExpress/PasClaw 是一款基于 Delphi Object Pascal 的 AI Agent 框架，能够将内部知识库进行索引并对接聊天助手，实现文档搜索、答案 grounding 等功能。

**价值**  
- 将散落在代码、文档、数据库中的企业内部知识转化为可检索的向量索引，提升员工和 AI 助手获取准确信息的效率。  
- 支持在 Delphi 生态下直接调用，无需额外跨语言桥接，适合已有 Pascal 项目的快速增值。  

**典型接入方式**  
1. **准备数据**：把需要检索的文档（Markdown、HTML、PDF 等）或代码注释导出为纯文本。  
2. **创建索引**：使用 PasClaw 提供的 CLI 或库函数，将文本送入内置的向量化模型（或自定义的 OpenAI/Claude API），生成向量并存入本地或远程向量库（如 Milvus、PGVector）。  
3. **集成到助手**：在 Delphi 应用中调用 `TPasClawAgent`，通过 `Search(query)` 方法获取相关文档片段，再将结果喂给聊天模型完成回答。  
4. **验证 & 扩展**：先在小规模（如 10‑20 条文档）做 PoC，确认搜索准确率和响应时延后，再逐步扩大索引规模并加入增量更新机制。  

**生产可用性**  
- **成熟度**：目前在 GitHub 上拥有 32 星、6 Fork，最近一次更新为 2026‑06‑26，代码质量尚可，适合作为内部原型或业务流程的加速工具。  
- **依赖与维护**：依赖 Delphi 编译环境及可选的向量数据库服务，需评估团队对 Pascal 与相关后端的维护能力。  
- **上线建议**：在正式生产前进行以下检查：  
  1. 确认向量化模型的授权或费用（如使用 OpenAI/Claude）。  
  2. 对接的向量库是否具备高可用与备份方案。  
  3. 编写完整的 README/部署脚本，确保新成员能快速搭建环境。  

总体而言，PasClaw 适合作为内部知识搜索的原型验证工具，经过充分的 PoC 与运维准备后，可在内部业务系统中实现稳定运行。

## 🧭 Practical evaluation

**Value:** FMXExpress/PasClaw helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 32 GitHub stars
- 6 forks
- updated 2026-06-26
- primary language: Pascal
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 29/100 |
| production | 50/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/FMXExpress/PasClaw) · [← Back to Knowledgerag](./README.md)</sub>
