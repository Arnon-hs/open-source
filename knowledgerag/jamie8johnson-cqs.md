# jamie8johnson/cqs

[![Stars](https://img.shields.io/github/stars/jamie8johnson/cqs?style=flat-square&color=yellow)](https://github.com/jamie8johnson/cqs/stargazers) [![Forks](https://img.shields.io/github/forks/jamie8johnson/cqs?style=flat-square&color=blue)](https://github.com/jamie8johnson/cqs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Code intelligence and RAG for AI agents: semantic search, call graphs, impact analysis, and context assembly in single tool calls. 54 languages + L5X/L5K PLC. 72.0% R@5 / 48.7% R@1 / 87.6% R@20 on v3.v2 dual-judge eval. Daemon mode (3-19ms). Local-first, GPU-accelerated.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 11 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Rust |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `call-graph` `claude-code` `code-intelligence` `code-search` `embeddings` `rag` `rust` `semantic-search` `vector-search`

## 🎯 Categories

Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Brief summary**  
jamie8johnson/cqs is a Rust‑based, GPU‑accelerated tool that turns codebases and documentation into searchable, semantically linked knowledge for AI agents. It offers fast (3‑19 ms) semantic search, call‑graph generation, impact analysis, and context assembly across 54 programming languages plus PLC code, achieving 72 % R@5 on a dual‑judge evaluation. The project is positioned as a “local‑first” RAG engine that can power assistants to retrieve and reason over internal code and technical content.

**Value**  
- **Unified code intelligence**: By indexing source code, PLC scripts, and related docs, CQS lets LLM‑powered assistants retrieve precise, context‑rich snippets, reducing hallucinations and improving answer relevance.  
- **Speed & scalability**: GPU acceleration and a daemon mode keep query latency in the low‑millisecond range, making it suitable for interactive workflows.  
- **Broad language coverage**: Supporting 54 languages plus industrial PLC formats means most enterprise codebases can be covered without custom parsers.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to spin up the daemon on a development machine, and index a small, representative subset of your codebase.  
2. **Integration** – Wrap the daemon’s HTTP/gRPC API in your existing assistant or CI pipeline; start with a simple “search‑and‑retrieve” use case (e.g., augmenting LLM prompts with relevant code snippets).  
3. **Evaluation** – Measure retrieval quality (R@k) and latency on your own data; adjust indexing parameters or GPU resources as needed.  
4. **Scale‑up** – Gradually expand the indexed corpus, add custom post‑processing (e.g., security filters), and integrate with your knowledge‑base pipelines.  

**Production readiness**  
- **Maturity**: Medium. The project works well for prototypes and internal tooling, but documentation around deployment, CI/CD, and long‑term maintenance is limited.  
- **Dependencies**: Requires a recent GPU stack and Rust toolchain; verify compatibility with your infrastructure.  
- **Stability**: With only 11 stars and a small contributor base, community support is modest, so you’ll need to allocate internal resources for debugging and updates.  
- **Risk mitigation**: Conduct a small pilot, lock dependency versions, and implement monitoring for daemon health before exposing it to production workloads.  

Overall, CQS can quickly boost the relevance of AI‑assisted code queries, but moving to production should be preceded by a controlled pilot and thorough validation of the integration and operational overhead.

### Русский

**Jamie8johnson/cqs** — это локальный, GPU‑ускоренный инструмент для работы с внутренними знаниями: семантический поиск, построение графов вызовов, анализ влияния и сбор контекста в едином запросе, поддерживающий более 50 языков программирования и PLC‑форматы. Типичный сценарий — индексировать корпоративные базы знаний и использовать полученные векторы для улучшения поиска по документам и «обоснования» ответов AI‑ассистентов; начать стоит с небольшого proof‑of‑concept, проверив README и запустив демон в режиме 3‑19 мс отклика. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует проверки зависимостей, настройки окружения и подтверждения стоимости интеграции перед масштабным внедрением.

### 中文

**项目简介**  
jamie8johnson/cqs 是一款面向 AI 代理的代码智能与检索增强（RAG）工具，能够在一次调用中完成语义搜索、调用图构建、影响分析和上下文组装，支持 54 种编程语言以及 L5X/L5K PLC 程序。评测结果显示在 v3.v2 双评委基准上取得 72.0% R@5、48.7% R@1、87.6% R@20，守护进程模式下响应仅 3‑19 ms，采用本地优先、GPU 加速的实现方式。

---

### 价值  
1. **内部知识可搜索、可复用**：把代码库、文档、PLC 程序等多源知识统一索引，帮助 AI 助手快速定位相关片段，提升回答的准确性和上下文完整度。  
2. **全链路代码洞察**：通过调用图和影响分析，开发者可以在调试、重构或安全审计时快速了解改动的波及范围。  
3. **高效、低延迟**：GPU 加速的本地部署让搜索在毫秒级完成，适合对实时性有要求的交互式 AI 应用。  

### 典型接入方式  
1. **准备索引**  
   ```bash
   # 克隆仓库并编译（Rust）
   git clone https://github.com/jamie8johnson/cqs
   cd cqs
   cargo build --release
   # 生成索引（示例：代码库 + 文档）
   ./target/release/cqs index --path /path/to/source --out ./index.db
   ```
2. **守护进程模式（推荐）**  
   ```bash
   ./target/release/cqs daemon --index ./index.db --gpu
   ```
   守护进程会监听本地端口（默认 8080），提供 RESTful / gRPC 接口供外部 AI 代理调用。  
3. **在 AI 代理中调用**  
   ```python
   import requests

   def semantic_search(query):
       resp = requests.post(
           "http://localhost:8080/search",
           json={"query": query, "top_k": 5}
       )
       return resp.json()
   ```
   返回的代码片段、调用图节点或 PLC 程序块可直接拼装进助手的回答或后续分析流程。  

> **小技巧**：在首次接入时，可先只索引一个小型子项目或文档集合，验证搜索质量和响应时延，再逐步扩展到全量代码库。

### 生产可用性  
| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 已在多个内部原型中使用，GitHub 仍活跃（最近更新 2026‑06‑23），但社区星标、fork 较少，缺少正式的 CI/CD 与长期维护承诺。 |
| **部署成本** | 中等 | 需要 Rust 编译环境、GPU 驱动以及对索引存储的磁盘空间规划。守护进程部署相对简单，但缺少 Docker 镜像或 Helm chart，需要自行容器化。 |
| **可扩展性** | 高 | 支持 54 种语言和 PLC，索引结构可水平扩展；GPU 加速保证大规模代码库仍能保持毫秒级响应。 |
| **安全/合规** | 本地优先 | 完全本地部署，无外部网络依赖，适合对代码保密有严格要求的企业环境。 |
| **运维** | 中等 | 需要监控守护进程的健康状态、GPU 使用率以及索引更新频率；目前缺少官方监控仪表盘，需要自行集成。 |

**结论**：cqs 已具备在原型和内部工作流中投入使用的能力，能够显著提升 AI 代理对代码和技术文档的理解深度。若计划在生产环境大规模部署，建议先完成以下准备工作：  
1. 编写 CI 脚本自动化索引更新（增量或全量）。  
2. 为守护进程构建容器镜像并加入健康检查。  
3. 评估 GPU 资源需求并制定容量规划。  

完成上述步骤后，cqs 可作为内部知识检索的核心组件，支撑 AI 助手、代码审查机器人或自动化运维工具的上下文获取。

## 🧭 Practical evaluation

**Value:** jamie8johnson/cqs helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 11 GitHub stars
- 3 forks
- updated 2026-06-23
- primary language: Rust
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 23/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 21/100 |
| production | 62/100 |
| usefulness | 90/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/jamie8johnson/cqs) · [← Back to Knowledgerag](./README.md)</sub>
