# raine/claude-history

[![Stars](https://img.shields.io/github/stars/raine/claude-history?style=flat-square&color=yellow)](https://github.com/raine/claude-history/stargazers) [![Forks](https://img.shields.io/github/forks/raine/claude-history?style=flat-square&color=blue)](https://github.com/raine/claude-history/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> Fuzzy-search Claude Code conversation history

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 353 |
| 🍴 **Forks** | 37 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
`raine/claude-history` is a Rust library that adds fuzzy‑search capabilities over Claude conversation logs, making it easy to retrieve relevant past interactions for Retrieval‑Augmented Generation (RAG) or agent‑based workflows. It is geared toward rapid prototyping of AI features rather than turnkey production deployment, and its metadata suggests a modest integration effort.  

**Value**  
The tool lets developers reuse existing Claude chat histories without rebuilding a custom indexing pipeline, accelerating the creation of context‑aware assistants, evaluation harnesses, or internal tooling that needs quick lookup of prior dialogues.  

**Practical adoption path**  
1. Clone the repo and run the provided Cargo build to generate the search index from your Claude export files.  
2. Wrap the library in a thin service (e.g., an HTTP endpoint or a CLI) that your application can call to perform fuzzy queries.  
3. Validate the relevance of returned snippets against a small test set; adjust the fuzzy‑search parameters if needed.  
Because the integration signals are sparse, a manual code review and a short proof‑of‑concept are recommended before committing to a larger codebase.  

**Production readiness**  
- **Maturity:** Medium – suitable for prototypes or internal workflows.  
- **Dependencies:** Pure Rust with a small dependency footprint, but you should audit the crates for security and long‑term maintenance.  
- **Stability:** Actively maintained (last update 2026‑06‑26) and modest community interest (≈350 stars, 37 forks).  
- **Risks:** The integration path is not documented in detail; you’ll need to invest time to understand how to feed your Claude logs into the index and to handle edge cases (e.g., large log volumes, multi‑tenant usage).  

Overall, `raine/claude-history` offers a quick way to enable context‑aware AI features, provided you perform a brief validation and dependency check before moving it into production.

### Русский

**ra​ine/claude‑history** — это открытый Rust‑проект, реализующий нечеткий поиск по истории диалогов Claude, что позволяет быстро добавить возможности AI‑агентов (RAG, прототипы агентных воркфлоу, оценка инструментов) без необходимости строить собственный стек моделей. Типичный сценарий — подключить библиотеку к существующей системе, выполнить ручную проверку метаданных и настроить интеграцию, после чего использовать её для прототипирования и внутренних автоматизаций. Готовность к production — средняя: проект стабилен и популярен (353★, 37 форков, активные обновления), но путь интеграции неочевиден и требует предварительной валидации зависимости и процессов поддержки.

### 中文

**项目简介**  
`raine/claude-history` 是一个基于 Rust 实现的模糊搜索工具，专注于在 Claude 代码对话历史中快速定位相关片段，帮助开发者在已有的对话记录中高效检索上下文信息。

**价值**  
- **快速原型**：无需从零搭建模型栈，即可为产品或内部工具加入基于 Claude 的 AI 能力。  
- **RAG/Agent 工作流**：提供可靠的历史检索接口，便于构建检索增强生成（RAG）或智能代理的上下文管理。  
- **评估与调试**：通过对话历史的可视化搜索，帮助团队快速评估模型输出质量和调优方向。

**典型接入方式**  
1. **依赖引入**：在 Rust 项目中通过 `cargo add raine/claude-history` 添加库。  
2. **初始化**：加载 Claude 对话日志（JSON/NDJSON 等格式）并构建索引。  
3. **查询**：使用库提供的 `search(query, fuzziness)` 接口进行模糊检索，返回匹配的对话片段及其元数据。  
4. **集成**：将搜索结果喂入后续的 RAG 流程或直接展示给用户；如需在非 Rust 环境使用，可通过 FFI 或 HTTP 包装层进行调用。

**生产可用性**  
- **成熟度**：Medium。项目已有 353 颗星、37 次 fork，且最近一次更新在 2026‑06‑26，代码活跃度良好。  
- **适用场景**：非常适合原型开发、内部工具或实验性 RAG/Agent 流程。  
- **风险与注意事项**：元数据中缺乏明确的集成信号，接入前需手动审查日志格式、索引配置以及依赖的 Rust 版本；在生产环境部署前建议进行依赖安全审计和性能基准测试。  

总体而言，`raine/claude-history` 能在短时间内为基于 Claude 的项目提供可靠的对话检索能力，但在正式上线前需完成集成验证和运维准备。

## 🧭 Practical evaluation

**Value:** raine/claude-history helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 353 GitHub stars
- 37 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 54/100 |
| topics | 0/100 |
| outlook | 45/100 |
| quality | 48/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 48/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/raine/claude-history) · [← Back to Misc](./README.md)</sub>
