# DEEP-PolyU/LinearRAG

[![Stars](https://img.shields.io/github/stars/DEEP-PolyU/LinearRAG?style=flat-square&color=yellow)](https://github.com/DEEP-PolyU/LinearRAG/stargazers) [![Forks](https://img.shields.io/github/forks/DEEP-PolyU/LinearRAG?style=flat-square&color=blue)](https://github.com/DEEP-PolyU/LinearRAG/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> [ICLR 2026] LinearRAG: Linear Graph Retrieval Augmented Generation on Large-scale Corpora

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 523 |
| 🍴 **Forks** | 61 |
| 💻 **Language** | Python |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`graphrag` `llms` `rag`

## 🎯 Categories

Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Brief Summary**  
LinearRAG (DEEP‑PolyU/LinearRAG) is an open‑source framework that augments large‑language‑model generation with fast, linear‑time graph‑based retrieval over massive corpora. By indexing internal knowledge bases as a retrieval graph, it lets assistants ground their answers in up‑to‑date documents while keeping latency low.

**Value**  
- **Searchable internal knowledge:** Transforms siloed documents, FAQs, or product manuals into a graph that can be queried instantly, making the information readily available to chat‑based assistants.  
- **Improved answer grounding:** Retrieval‑augmented generation (RAG) reduces hallucinations and boosts factual accuracy because the model can cite specific nodes from the graph.  
- **Scalable performance:** Linear‑time retrieval scales to millions of passages without the heavy indexing overhead of traditional dense‑vector methods, keeping costs predictable.

**Practical Adoption Path**  
1. **Data preparation:** Export the target knowledge base (e.g., PDFs, markdown, Confluence pages) into plain‑text chunks.  
2. **Graph construction:** Run LinearRAG’s indexing script to build the retrieval graph; optionally tune edge weights or add domain‑specific metadata.  
3. **Pilot integration:** Connect the generated graph to an LLM via the provided Python API or REST wrapper; test with a small set of queries and manually inspect retrieved passages for relevance.  
4. **Feedback loop:** Use the inspection results to refine chunking, edge creation, or prompt templates, then expand the index to the full corpus.  
5. **Deployment:** Containerize the service (Docker/Helm), expose the retrieval endpoint, and integrate it with your assistant platform (e.g., LangChain, Botpress).  

**Production Readiness**  
- **Maturity:** Medium. The codebase is actively maintained (last commit 2026‑07‑05) and has modest community traction (523 ★, 61 forks). It is suitable for prototypes, internal tools, or staged roll‑outs.  
- **Dependencies & Maintenance:** Pure‑Python with a few standard ML libraries; verify compatibility with your existing stack and pin versions to avoid breaking changes.  
- **Operational considerations:** Because integration signals are sparse, a manual validation step is recommended before full rollout. Conduct security and licensing reviews (the repository’s license is not yet confirmed) and set up monitoring for retrieval latency and graph health.  

Overall, LinearRAG offers a compelling, scalable way to make internal knowledge searchable and usable by AI assistants, provided you allocate time for initial data curation, validation, and the standard production hardening steps.

### Русский

**DEEP-PolyU/LinearRAG** — это open‑source библиотека, позволяющая быстро индексировать внутренние базы знаний и использовать их в RAG‑системах: она строит линейные графовые индексы, что ускоряет поиск по большим корпусам и повышает точность ответов ассистентов. Типичный сценарий — интеграция в пайплайн поиска/генерации (например, в чат‑боте компании) с последующей ручной проверкой результатов, поскольку метаданные интеграции пока редки. Готовность к production — средний уровень: проект подходит для прототипов и внутренних процессов, но требует проверки зависимостей, лицензии и безопасности перед развертыванием в продакшн.

### 中文

**项目简介（2‑3 句）**  
LinearRAG（DEEP-PolyU/LinearRAG）是 ICLR 2026 论文实现，提供基于线性图检索的增强生成（RAG）框架，能够在大规模语料库上快速定位相关文档并将检索结果无缝注入生成式模型。项目使用纯 Python 编写，已获 523 星、61 Fork，近期仍在活跃维护。

**价值**  
- 将企业内部知识库转化为可检索的向量图结构，使得聊天机器人或助手能够在回答时直接引用最新文档，实现“检索‑生成”闭环。  
- 提升文档搜索的召回率与响应速度，尤其适用于海量、结构化或半结构化的企业文档、FAQ、技术手册等场景。  

**典型接入方式**  
1. **数据准备**：将知识库（PDF、Markdown、HTML 等）批量转为文本并使用项目提供的预处理脚本生成向量节点。  
2. **索引构建**：利用 LinearRAG 的线性图构建工具（基于 FAISS/ScaNN）创建可增量更新的检索索引。  
3. **服务集成**：在已有的对话系统或 LLM 接口中调用 `retrieve_and_generate` API，先检索 Top‑k 文档节点，再将检索结果拼接到提示词中交给生成模型。  
4. **人工审查**：由于元数据中检索信号稀疏，建议在正式上线前对检索结果进行抽样审查，确保相关性与安全性。  

**生产可用性**  
- **成熟度**：Medium。代码结构清晰、依赖主要为常用的 PyTorch、FAISS 等库，适合原型开发和内部工作流。  
- **上线前检查**：需确认许可证兼容性、对依赖库的安全审计以及维护者响应速度；若在高并发环境使用，建议进行负载测试并考虑水平扩展检索服务。  
- **运维要求**：定期更新索引（增量或全量），监控检索延迟与生成质量，必要时对模型和向量编码器进行再训练。  

总体而言，LinearRAG 是一个在内部知识检索与生成之间搭建高效桥梁的实用工具，适合在内部原型或受控生产环境中快速落地。

## 🧭 Practical evaluation

**Value:** DEEP-PolyU/LinearRAG helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 523 GitHub stars
- 61 forks
- updated 2026-07-05
- primary language: Python
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 58/100 |
| topics | 38/100 |
| outlook | 67/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/DEEP-PolyU/LinearRAG) · [← Back to Knowledgerag](./README.md)</sub>
