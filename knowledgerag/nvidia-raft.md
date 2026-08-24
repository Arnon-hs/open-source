# NVIDIA/raft

[![Stars](https://img.shields.io/github/stars/NVIDIA/raft?style=flat-square&color=yellow)](https://github.com/NVIDIA/raft/stargazers) [![Forks](https://img.shields.io/github/forks/NVIDIA/raft?style=flat-square&color=blue)](https://github.com/NVIDIA/raft/network) [![Language](https://img.shields.io/badge/lang-Cuda-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> RAFT contains fundamental widely-used algorithms and primitives for machine learning and information retrieval. The algorithms are CUDA-accelerated and form building blocks for more easily writing high performance applications.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 237 |
| 💻 **Language** | Cuda |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anns` `building-blocks` `clustering` `cuda` `distance` `gpu` `information-retrieval` `linear-algebra` `llm` `machine-learning` `nearest-neighbors` `neighborhood-methods`

## 🎯 Categories

Knowledge/RAG · AI/ML

## 📝 Summary

### English

NVIDIA/raft provides CUDA‑accelerated, reusable algorithms and primitives that serve as building blocks for high‑performance machine‑learning and information‑retrieval pipelines, enabling faster knowledge‑base indexing and more responsive assistant search. Adoption can begin with a small proof‑of‑concept — checking the README and evaluating the core components — before scaling to full integration. The project shows strong recent activity, solid adoption, and ecosystem signals, indicating high production readiness for a serious pilot despite the need for a final license, security, and maintainer review.

### Русский

NVIDIA/raft — это набор CUDA‑ускоренных алгоритмов и примитивов для машинного обучения и поиска информации, позволяющий быстро индексировать и искать большие объёмы знаний, что делает внутренние базы данных доступными для ассистентов. Типовой сценарий внедрения — построение небольшого proof‑of‑concept для индексации корпоративных документов и ускорения поиска по ним, после чего масштабирование до production‑уровня. Благодаря активной разработке, высокой звёздности и сильным экосистемным сигналам проект готов к серьёзному пилоту в продакшене.

### 中文

**项目简介**  
RAFT（NVIDIA/raft）是一个面向机器学习和信息检索的基础算法库，提供了大量经 CUDA 加速的核心原语和常用算法。它把底层高性能实现封装成易于调用的模块，使得开发者能够快速构建出性能卓越的 ML 与检索应用。

**价值**  
- **高效搜索与检索**：通过 GPU 加速的索引、聚类、最近邻搜索等算法，显著提升大规模知识库、文档库的检索速度和准确性。  
- **加速助理系统**：在对话助理或生成式 AI 中，RAFT 可用于快速检索上下文、实现向量相似度搜索，从而让答案更贴合用户需求。  
- **降低研发成本**：提供即插即用的原语，避免团队自行实现并优化底层 CUDA 代码，缩短产品迭代周期。

**典型接入方式**  
1. **依赖引入**：在 CMake 项目或 Python 环境中通过 `find_package(raft)`（C++）或 `pip install nvidia-raft`（Python）引入库。  
2. **构建索引**：使用 `raft::neighbors::ivf_flat`、`raft::neighbors::cagra` 等 API 构建向量索引或聚类模型。  
3. **查询调用**：在业务代码中调用 `search` 接口完成最近邻查询，将返回的向量 ID 与内部知识库映射，完成文档或答案的检索。  
4. **小规模 PoC**：先在已有的向量数据集（如 10 万条）上跑通索引‑查询流程，验证性能提升，再逐步扩展到生产规模。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目仍在持续更新，拥有 1 019 个 GitHub 星、237 个 Fork，社区活跃度高。  
- **成熟度**：核心算法已在 NVIDIA 自家产品和多家行业客户中使用，具备生产级别的可靠性。  
- **生态兼容**：与 RAPIDS、FAISS、cuML 等生态良好集成，支持多语言绑定（C++、Python）。  
- **风险**：需进一步确认许可证（BSD‑3/Apache‑2.0）与安全审计情况，确保符合企业合规要求。  

综上，RAFT 是一个高性能、成熟的 GPU 加速检索库，适合作为内部知识库搜索或助理系统的向量检索后端，具备直接投入生产的条件，只需在正式上线前完成许可证与安全评估以及小规模概念验证。

## 🧭 Practical evaluation

**Value:** NVIDIA/raft helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1019 GitHub stars
- 237 forks
- updated 2026-06-30
- primary language: Cuda
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/NVIDIA/raft) · [← Back to Knowledgerag](./README.md)</sub>
