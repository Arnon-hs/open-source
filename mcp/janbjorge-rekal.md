# janbjorge/rekal

[![Stars](https://img.shields.io/github/stars/janbjorge/rekal?style=flat-square&color=yellow)](https://github.com/janbjorge/rekal/stargazers) [![Forks](https://img.shields.io/github/forks/janbjorge/rekal?style=flat-square&color=blue)](https://github.com/janbjorge/rekal/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Long-term memory for LLMs. MCP server backed by hybrid search in a single SQLite file.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 46 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Python |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`llm` `mcp` `mcp-server` `memory` `python` `sqlite` `vector-search`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary**  
Rekal (janbjorge/rekal) provides a lightweight “Model Context Protocol” (MCP) server that gives large language models long‑term memory by storing and retrieving embeddings in a single SQLite file using hybrid (vector + lexical) search. It lets AI assistants hook into real tools and data sources through a simple, language‑agnostic API/CLI, making it easy to prototype knowledge‑augmented agents.

**Value**  
- **Unified memory layer**: By persisting embeddings locally, Rekal enables LLMs to recall past interactions, facts, or tool outputs without external vector stores.  
- **Standardized integration**: The MCP interface abstracts away the specifics of each downstream system, allowing the same agent code to talk to databases, APIs, or custom tools with minimal glue code.  
- **Low operational overhead**: SQLite is file‑based, requires no separate service, and the hybrid search gives decent relevance for both semantic and keyword queries, ideal for small‑to‑medium workloads.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/CLI, and point your LLM client (e.g., LangChain, LlamaIndex) at the MCP endpoint.  
2. **Integrate** – Use the SDK (Python) or HTTP API to push embeddings of tool outputs or domain documents and query them from your agent during inference.  
3. **Scale** – For higher query volume, replace the SQLite backend with a read‑replica or mount the file on a fast SSD; the protocol remains unchanged.  
4. **Productionize** – Wrap the server in a managed container, add authentication (e.g., API keys or mTLS), and monitor the file size and index rebuild schedule.

**Production Readiness**  
- **Maturity**: Medium. The project is functional and actively updated (latest commit 2026‑05‑12), with 46 stars and a small but engaged community.  
- **Dependencies**: Pure‑Python with SQLite; minimal external services, which simplifies deployment but requires careful version pinning.  
- **Risks**: License and security posture need a final review; the single‑file SQLite store may become a bottleneck for very large corpora or high‑concurrency workloads, so load testing and backup strategies are advisable.  
- **Suitability**: Well‑suited for prototypes, internal tools, or low‑to‑moderate traffic applications; production use cases should add monitoring, authentication, and possibly a more scalable vector store if scaling beyond a few hundred thousand embeddings.

### Русский

**rekal** — это сервер MCP, реализующий гибридный поиск и долговременную память для LLM, полностью хранится в одном файле SQLite. Он позволяет быстро подключать AI‑агентов к внешним инструментам и базам знаний через единый протокол (API/SDK/CLI), что упрощает создание прототипов и внутренних workflow‑интеграций. Проект находится на среднем уровне готовности: подходит для прототипов и ограниченных продакшн‑сценариев после проверки зависимостей, лицензии и безопасности.

### 中文

**项目简介**  
janbjorge/rekal 为大模型提供长期记忆能力，基于单文件 SQLite 实现混合检索，并通过 Model Context Protocol (MCP) 对外提供统一的查询服务。  

**价值**  
- **统一协议**：使用标准的 MCP，让 AI 助手可以像调用本地工具一样轻松访问外部数据和工具。  
- **低成本持久化**：所有向量、元数据和全文索引都保存在一个 SQLite 文件中，无需额外的搜索引擎或分布式存储，部署和备份都非常简洁。  
- **混合搜索**：同时支持向量相似度检索和关键字全文检索，提升检索准确性和召回率，适合需要长期上下文记忆的对话或 RAG 场景。  

**典型接入方式**  
1. **API/SDK**：直接调用提供的 HTTP API（或通过 Python SDK）进行 `add`, `query`, `update` 等操作。  
2. **CLI**：使用自带的命令行工具在本地快速创建、导入或查询记忆库，适合原型验证。  
3. **MCP Server**：将 Rekal 以 MCP 服务器方式启动，其他遵循 MCP 的 AI 框架（如 LangChain、AutoGPT 等）即可通过标准协议接入，无需了解底层实现细节。  

**生产可用性**  
- **成熟度**：当前评分 63/100，GitHub 46 ⭐、4 forks，近期（2026‑05‑12）仍有更新，代码以 Python 为主，适合快速集成。  
- **适用场景**：原型开发、内部工作流、实验性产品以及对成本敏感的中小规模部署。  
- **上线注意**：在生产环境使用前建议：  
  - 完成安全审计（尤其是 SQLite 文件的访问控制与 API 鉴权）。  
  - 评估依赖库的维护状态，锁定版本防止意外升级。  
  - 进行备份与恢复演练，确保单文件故障时可快速恢复。  
- **总体评估**：具备“中等”生产准备度，适合作为内部服务或 MVP，上线前进行上述检查即可提升到可在生产环境安全运行的水平。

## 🧭 Practical evaluation

**Value:** janbjorge/rekal helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 46 GitHub stars
- 4 forks
- updated 2026-05-12
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 36/100 |
| topics | 88/100 |
| outlook | 73/100 |
| quality | 67/100 |
| recency | 100/100 |
| adoption | 31/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/janbjorge/rekal) · [← Back to Mcp](./README.md)</sub>
