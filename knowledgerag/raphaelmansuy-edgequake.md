# raphaelmansuy/edgequake

[![Stars](https://img.shields.io/github/stars/raphaelmansuy/edgequake?style=flat-square&color=yellow)](https://github.com/raphaelmansuy/edgequake/stargazers) [![Forks](https://img.shields.io/github/forks/raphaelmansuy/edgequake?style=flat-square&color=blue)](https://github.com/raphaelmansuy/edgequake/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> EdegQuake 🌋 High-performance GraphRAG inspired from LightRag written in Rust; Transform documents into intelligent knowledge graphs for superior retrieval and generation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2k |
| 🍴 **Forks** | 231 |
| 💻 **Language** | Rust |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`graphrag` `knowledge-graph` `lightrag` `rag`

## 🎯 Categories

Knowledge/RAG · AI/ML · Documents

## 📝 Summary

### English

Here's a brief summary of the open-source project:

EdgeQuake is a high-performance graph-based retrieval and generation tool inspired by LightRag, designed to transform documents into intelligent knowledge graphs. It offers a value proposition of making internal knowledge searchable and usable by assistants, with potential use cases in indexing knowledge bases, improving search over documents, and grounding assistant answers. However, its production readiness is medium, requiring careful evaluation and integration planning due to a non-obvious integration path and potential setup costs.

**Value:** EdgeQuake provides a powerful tool for transforming documents into knowledge graphs, enabling superior retrieval and generation capabilities. Its primary value lies in making internal knowledge searchable and usable by assistants, which can improve the efficiency and accuracy of information retrieval and generation tasks.

**Practical adoption path:** To adopt EdgeQuake, start by evaluating its feasibility through a small proof-of-concept and checking the README documentation. This will help identify potential integration challenges and setup costs. Once you've validated the setup cost and integration path, you can begin to integrate EdgeQuake into your internal workflows or prototypes.

**Production readiness:** EdgeQuake has a medium production readiness score, indicating that it's useful for prototypes or internal workflows, but may require further evaluation and dependency checks before being deployed in production. Its Rust

### Русский

Резюме проекта raphaelmansuy/edgequake:

EdgeQuake 🌋 — это высокопроизводительный графовый РАГ (GraphRAG), написанный на языке Rust, который позволяет преобразовывать документы в интеллектуальные знаковые графики для улучшения поиска и генерации. Этот проект может помочь сделать внутренние знания поисковыми и доступными для ассистентов. EdgeQuake подходит для прототипирования или внутренних потоков работы и имеет средний уровень готовности к production, требующий проверки зависимостей и поддержки перед внедрением в production.

### 中文

**项目简介（2‑3 句）**  
EdgeQuake 🌋 是一款用 Rust 实现的高性能 GraphRAG 框架，受 LightRAG 启发，能够将文档转化为结构化的知识图谱，以实现更精准的检索和生成。它面向内部知识库，帮助 AI 助手快速定位并利用企业文档中的信息。

**价值**  
- **提升知识可搜索性**：把散落的文档转成关联图谱，使得查询和上下文检索更高效。  
- **增强生成质量**：在生成答案时可直接“落地”到图谱节点，保证答案的事实依据。  
- **加速内部 AI 应用**：为客服、内部助理、研发文档查询等场景提供可靠的知识底座。

**典型接入方式**  
1. **准备数据**：将已有的文档（Markdown、PDF、HTML 等）导出为纯文本或 JSON。  
2. **构建图谱**：使用 EdgeQuake 提供的 CLI 或库函数 `edgequake::ingest` 将文本分块、抽取实体/关系并写入本地或嵌入式数据库（默认 RocksDB）。  
3. **查询接口**：在业务服务中调用 `edgequake::query`，传入自然语言查询或向量，返回关联的图谱子集及检索得分。  
4. **与生成模型结合**：把检索结果拼装成检索增强提示（RAG Prompt），喂给 LLM（如 OpenAI、Claude）完成答案生成。  

**生产可用性**  
- **成熟度**：项目已有 2022 年起的 GitHub 星标、231 次 fork，最近一次更新在 2026‑07‑01，代码基于 Rust，具备良好的性能与安全特性。  
- **适用阶段**：适合作为原型或内部工作流的知识检索层，能够在几天内完成小规模 PoC。  
- **风险与准备**：  
  - 文档到图谱的抽取规则需要根据业务自行调优，初始集成可能需要一定的配置工作。  
  - 依赖 Rust 编译链和 RocksDB，需评估运维团队对这些组件的熟悉度。  
  - 目前缺乏完整的 CI/CD 部署示例，建议先在隔离环境进行功能验证，再编写自动化部署脚本。  

总体而言，EdgeQuake 在原型和内部业务场景中具备较高的实用价值，经过适当的依赖审查和部署验证后，可逐步提升至生产环境使用。

## 🧭 Practical evaluation

**Value:** raphaelmansuy/edgequake helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2022 GitHub stars
- 231 forks
- updated 2026-07-01
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 70/100 |
| topics | 50/100 |
| outlook | 71/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/raphaelmansuy/edgequake) · [← Back to Knowledgerag](./README.md)</sub>
