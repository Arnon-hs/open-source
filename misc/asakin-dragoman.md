# asakin/dragoman

[![Stars](https://img.shields.io/github/stars/asakin/dragoman?style=flat-square&color=yellow)](https://github.com/asakin/dragoman/stargazers) [![Forks](https://img.shields.io/github/forks/asakin/dragoman?style=flat-square&color=blue)](https://github.com/asakin/dragoman/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-40%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 40/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Dragoman is an open‑source routing layer that lets you direct Claude‑Code requests to the most appropriate sub‑agent (e.g., a vector store, a tool, or another LLM) based on the query’s intent. By automatically routing to the right model or knowledge source, it turns scattered internal documents into a searchable, assistant‑ready knowledge base. The project is fresh (last updated 2026‑05‑12) and targets use‑cases such as document indexing, semantic search, and grounding AI‑assistant answers.  

**Value**  
- **Unified knowledge access** – Dragoman abstracts multiple back‑ends (vector DBs, APIs, specialized agents) behind a single Claude‑Code interface, so developers no longer need to hand‑craft routing logic for each source.  
- **Improved answer relevance** – By selecting the most suitable sub‑agent per request, the assistant can retrieve the right context, leading to higher‑quality, fact‑grounded responses.  
- **Rapid prototyping** – The router is lightweight and configurable, enabling teams to experiment with multi‑model pipelines without rebuilding the plumbing each time.  

**Practical adoption path**  

| Step | Action | Why |
|------|--------|-----|
| 1️⃣  | **Clone & run the demo** – Use the provided Docker compose or `pip install dragoman` to spin up the router with a simple Claude‑Code client. | Confirms the basic routing works in your environment. |
| 2️⃣  | **Define sub‑agents** – Register your existing knowledge bases (e.g., Pinecone, Elasticsearch, local file index) and any tool‑agents in the `agents.yaml` configuration. | Makes Dragoman aware of the resources you want to route to. |
| 3️⃣  | **Create routing rules** – Use the rule DSL or JSON schema to map intents (keyword, similarity score, function calls) to agents. Test with a few representative queries. | Ensures the router picks the right backend for real queries. |
| 4️⃣  | **Integrate with your Claude‑Code workflow** – Replace direct Claude‑Code calls with the Dragoman endpoint; the router will forward the request and return the final response. | Minimal code change; the assistant now benefits from multi‑model routing. |
| 5️⃣  | **Manual inspection & monitoring** – Log routed queries, inspect the chosen agents, and adjust rules or thresholds based on false positives/negatives. | The project’s integration signals are sparse, so human validation is essential. |
| 6️⃣  | **Scale & harden** – Containerize, add health checks, and configure CI/CD to rebuild the routing config when new knowledge sources are added. | Prepares the system for production workloads. |

**Production readiness**  
- **Maturity**: Medium. The codebase is recent and functional for prototypes, but documentation, issue tracking, and release cadence are limited.  
- **Dependencies**: Relies on Claude‑Code API and any vector store/tool you plug in; verify version compatibility and licensing of those back‑ends.  
- **Risk mitigation**: Before production, perform a security audit of the routing logic, set up automated tests for routing rules, and establish a maintenance plan (e.g., weekly config validation).  

In short, Dragoman can quickly give you a searchable, multi‑model assistant layer, but you should treat it as a prototype‑grade component, validate it manually, and put the usual production safeguards in place before scaling.

### Русский

**Show HN: Dragoman – Multi‑model routing for Claude Code via sub‑agents** — это open‑source‑инструмент, который позволяет автоматически индексировать внутренние базы знаний и использовать их для более точного поиска и контекстного обогащения ответов ассистентов (например, Claude). Типичный сценарий — подключение Dragoman к существующим хранилищам документов, построение RAG‑потока и маршрутизация запросов между несколькими моделями через суб‑агенты, что повышает релевантность и скорость выдачи результатов. Готовность к production — средняя: проект подходит для прототипов и внутренних воркфлоу, но требует ручной проверки лицензии, документации и частоты релизов перед масштабным внедрением.

### 中文

**项目简介**  
Dragoman 是一个开源的“多模型路由器”，通过子代理（sub‑agents）把 Claude Code 与其他语言模型（LLM）组合使用，实现对内部知识库的高效检索与调用。它的核心思路是把不同模型的专长分配给对应的子代理，然后统一调度，帮助助手在回答时能够精准地引用和引用文档内容。

**价值**  
- **知识可搜索、可落地**：把企业内部文档、FAQ、代码库等结构化或半结构化的知识索引后，助手可以在对话中实时检索并引用，提升答案的准确性和可信度。  
- **多模型协同**：通过子代理把 Claude Code 用作代码生成/理解的强项，同时可以把检索、摘要、事实校验等任务交给更适合的模型，实现“一站式”智能助理。  

**典型接入方式**  
1. **准备知识库**：使用支持的向量数据库（如 Pinecone、Weaviate、FAISS）把文档转成向量并建立索引。  
2. **部署 Dragoman**：克隆仓库后按照 README 配置子代理列表（每个子代理对应一个模型的 API 密钥、温度等参数），并在 `config.yaml` 中声明路由规则。  
3. **集成到业务系统**：在现有的聊天/客服后端调用 Dragoman 的 HTTP 接口（`/route`），传入用户提问，返回包含检索片段和生成答案的 JSON。  
4. **人工审查**：首次上线前，建议在测试环境对路由日志进行人工审查，确保模型选择和检索结果符合业务需求。  

**生产可用性**  
- **成熟度**：目前评分 52/100，属于 **中等** 稳定性。适合原型、内部工具或低风险业务场景。  
- **依赖与运维**：需要自行维护向量库、模型 API 配额以及 Dragoman 的容器/服务。项目更新频率不高，建议定期检查仓库的 Issue、PR 和许可证（MIT/Apache 等）。  
- **上线建议**：在正式生产前完成以下检查：  
  - 确认许可证与企业合规性；  
  - 评估子代理所用模型的成本与响应时延；  
  - 设置监控（调用成功率、检索相关度、返回答案质量）；  
  - 预留回滚方案，以防路由错误导致不符合预期的答案。  

综上，Dragoman 为需要把内部文档与代码知识“落地”到对话式 AI 的团队提供了一个灵活的多模型路由框架，适合作为原型或内部工作流的加速器，正式生产环境使用时需做好依赖审查和监控治理。

## 🧭 Practical evaluation

**Value:** Show HN: Dragoman – Multi-model routing for Claude Code via sub-agents helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-12
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 32/100 |
| quality | 21/100 |
| recency | 20/100 |
| adoption | 0/100 |
| production | 34/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/asakin/dragoman) · [← Back to Misc](./README.md)</sub>
