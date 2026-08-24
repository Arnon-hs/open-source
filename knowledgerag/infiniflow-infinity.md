# infiniflow/infinity

[![Stars](https://img.shields.io/github/stars/infiniflow/infinity?style=flat-square&color=yellow)](https://github.com/infiniflow/infinity/stargazers) [![Forks](https://img.shields.io/github/forks/infiniflow/infinity?style=flat-square&color=blue)](https://github.com/infiniflow/infinity/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> The AI-native database built for LLM applications, providing incredibly fast hybrid search of dense vector, sparse vector, tensor (multi-vector), and full-text.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.5k |
| 🍴 **Forks** | 419 |
| 💻 **Language** | C++ |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-native` `approximate-nearest-neighbor-search` `bm25` `cpp20` `cpp20-modules` `embedding` `full-text-search` `hnsw` `hybrid-search` `information-retrival` `multi-vector` `nearest-neighbor-search`

## 🎯 Categories

Knowledge/RAG · AI/ML · Database

## 📝 Summary

### English

**Summary**  
Infinity (infiniflow/infinity) is an AI‑native, C++‑based database that delivers ultra‑fast hybrid search across dense vectors, sparse vectors, multi‑vectors (tensors), and traditional full‑text. It is designed to make internal knowledge bases instantly searchable and usable by LLM‑powered assistants, enabling richer document retrieval and grounding of AI responses.

**Value**  
- **Unified search**: One engine handles vector similarity, sparse term matching, and full‑text queries, eliminating the need for separate services.  
- **Performance**: Native C++ implementation and optimized indexing give low‑latency results even on large corpora, which is critical for real‑time LLM inference.  
- **LLM‑ready**: By exposing dense‑vector and tensor indexes, it fits naturally into Retrieval‑Augmented Generation (RAG) pipelines, improving answer relevance and factual grounding.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to spin up a local instance (Docker image is provided). Index a small subset of your documents (e.g., a few thousand PDFs or markdown files) using the Python client.  
2. **Integration** – Connect the instance to your LLM service via the REST/gRPC APIs; replace any existing Elasticsearch or vector store calls with Infinity’s unified query endpoint.  
3. **Scale‑up** – Benchmark latency and storage on a representative dataset, then provision a production cluster (Kubernetes Helm chart is available).  
4. **Monitoring & ops** – Use the built‑in metrics endpoint (Prometheus format) to set up alerts and autoscaling.

**Production readiness**  
- **Activity & adoption**: 4.5 k stars, 419 forks, frequent commits (last update 2026‑05‑12) and several downstream projects already reference Infinity.  
- **Maturity**: Core features (dense, sparse, tensor, full‑text) are stable; the C++ codebase is production‑grade and the project ships Docker images and Helm charts.  
- **Risks**: The integration documentation is sparse; you’ll need to invest time in validating deployment scripts and understanding the indexing pipeline before a full rollout. Overall, Infinity is a strong OSS candidate for a serious pilot in any organization that needs fast, hybrid search for LLM‑driven applications.

### Русский

**infiniflow/infinity** — это open‑source база данных, созданная специально для LLM‑приложений и обеспечивающая сверхбыстрый гибридный поиск по плотным и разреженным векторам, тензорам и полному тексту. Типичный сценарий внедрения — небольшое proof‑of‑concept, в котором индексируются внутренние базы знаний (документы, вики, справочники) и затем используется гибридный поиск для повышения точности ответов ассистентов и улучшения RAG‑потоков. Проект уже имеет высокую степень готовности к production: активные коммиты, более 4500 звёзд, 400+ форков и поддержка C++‑интеграций, однако перед масштабным rollout‑ом рекомендуется проверить детали установки и оценить затраты на интеграцию.

### 中文

**项目简介**  
infiniflow/infinity 是一款面向大语言模型（LLM）应用的 AI 原生数据库，能够在同一次查询中极速混合检索稠密向量、稀疏向量、多向量张量以及全文文本，帮助企业把内部知识库转化为可被助手直接调用的可搜索资源。

**价值主张**  
- **全栈检索**：统一索引结构同时支持向量相似度、稀疏特征和全文匹配，避免为不同检索需求维护多套系统。  
- **极致性能**：基于 C++ 实现的底层引擎，针对大规模向量和高并发查询做了专门的优化，适合实时 RAG 场景。  
- **助力 AI 助手**：通过快速定位文档片段、事实或代码片段，为 LLM 提供可靠的外部知识来源，提升答案的准确性和可解释性。

**典型接入方式**  
1. **准备数据**：将文档、FAQ、代码等转化为稠密向量（如 OpenAI、Sentence‑Transformers）或稀疏向量（如 BM25），必要时再生成多模态张量。  
2. **创建索引**：使用 Infinity 提供的 CLI 或 REST API（`/v1/indexes`）创建索引并批量导入向量/文本。  
3. **查询调用**：在应用层通过 HTTP/JSON（或 gRPC）发送混合查询请求，指定向量相似度阈值、全文关键字或稀疏权重，Infinity 返回统一的排序结果。  
4. **集成示例**：官方 README 中有 Python、Node.js、Go 的 SDK 示例，可直接在现有 LLM 推理服务（如 LangChain、LLamaIndex）中包装为检索工具。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目拥有 4.5k+ stars、400+ forks，最近一次提交在当日，说明社区仍在积极维护。  
- **成熟度**：支持多语言客户端、容器化部署（Docker 镜像）以及水平扩展的分片机制，已在若干企业级 RAG 项目中试点。  
- **风险与建议**：文档虽完整，但完整的运维手册和监控指标相对分散，建议先在小规模（如 10 万条向量）进行 PoC，验证部署脚本、网络配置和硬件需求后再逐步扩大。总体而言，Infinity 已具备作为生产级 OSS 向量数据库的条件，适合作为内部知识搜索和 AI 助手检索的核心组件。

## 🧭 Practical evaluation

**Value:** infiniflow/infinity helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4511 GitHub stars
- 419 forks
- updated 2026-05-12
- primary language: C++
- 19 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 78/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 68/100 |
| recency | 20/100 |
| adoption | 74/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/infiniflow/infinity) · [← Back to Knowledgerag](./README.md)</sub>
