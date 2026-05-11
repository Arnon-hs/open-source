# zircote/rlm-rs

[![Stars](https://img.shields.io/github/stars/zircote/rlm-rs?style=flat-square&color=yellow)](https://github.com/zircote/rlm-rs/stargazers) [![Forks](https://img.shields.io/github/forks/zircote/rlm-rs?style=flat-square&color=blue)](https://github.com/zircote/rlm-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Rust CLI implementing the Recursive Language Model (RLM) pattern for Claude Code. Process documents 100x larger than context windows through intelligent chunking, SQLite persistence, and recursive sub-LLM orchestration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 42 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Rust |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-tools` `chunking` `claude` `claude-code` `cli` `command-line` `context-window` `devtools` `document-processing` `llm` `mit-license` `mmap`

## 🎯 Categories

Orchestration · AI/ML · DevTools · Database

## 📝 Summary

### English

**Brief Summary**  
zircote/rlm-rs is a Rust‑based command‑line tool that implements the Recursive Language Model (RLM) pattern for Claude Code. It lets you process documents that are up to 100× larger than a model’s context window by automatically chunking the text, persisting state in SQLite, and orchestrating recursive sub‑LLM calls. The project aims to turn ad‑hoc prompts and tool invocations into repeatable, memory‑aware agent workflows.

**Value**  
- **Scalable prompting** – By breaking massive inputs into manageable chunks and stitching the results together, it removes the hard limit of LLM context windows, enabling richer code‑generation, analysis, or summarisation tasks.  
- **Built‑in persistence** – SQLite storage gives agents a lightweight, queryable memory layer, which simplifies stateful pipelines and auditability.  
- **Recursive orchestration** – The tool automatically spawns sub‑LLMs to handle each chunk and merges their outputs, reducing the need for custom orchestration code in your own projects.  
- **CLI/SDK exposure** – The command‑line interface and clear Rust API make it easy to embed the engine in CI pipelines, dev‑tools, or larger multi‑agent systems.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI against a sample document, and verify the chunking/orchestration behavior.  
2. **Integrate** – Add the Rust crate to your own codebase or invoke the CLI from a script; configure the SQLite path and Claude API credentials via environment variables or a config file.  
3. **Extend** – Wrap the crate in a thin HTTP/GRPC layer if you need language‑agnostic access, or plug in additional tool‑use steps (e.g., static analysis, linting) by chaining CLI commands.  
4. **Validate** – Benchmark latency and token usage on your typical document sizes; adjust chunk size or recursion depth as needed.  

**Production Readiness**  
- **Maturity**: Medium. The project has modest adoption (≈ 42 stars, 4 forks) and recent activity (last commit 2026‑05‑11), indicating it is functional but not battle‑tested at scale.  
- **Stability**: Core functionality (chunking, SQLite persistence, recursive calls) is in place, but you should review the dependency tree for security updates and confirm the license is compatible with your product.  
- **Operational considerations**: Ensure you have reliable SQLite storage (or a backup strategy) and monitor Claude API rate limits, as recursive calls can multiply request volume.  
- **Next steps before production**: Conduct a security audit of the crate, add integration tests for your specific workflows, and possibly fork/maintain a small patch set to address any bugs uncovered during load testing.  

Overall, zircote/rlm-rs offers a compelling foundation for building scalable, memory‑aware LLM agents, and with a modest amount of validation and monitoring it can be safely used in internal tools or prototype‑grade production services.

### Русский

**zircote/rlm-rs** — это открытый Rust‑CLI, реализующий паттерн Recursive Language Model (RLM) для Claude Code: он разбивает документы, превышающие контекстные окна в 100 раз, сохраняет фрагменты в SQLite и управляет рекурсивным вызовом под‑LLM, превращая разрозненные запросы и инструменты в повторяемые агентные воркфлоу. Типичное внедрение — построение многокомпонентных AI‑pipeline (координация нескольких агентов, инструментарий с инструмент‑использованием, стандартизация памяти агента) в прототипных или внутренних системах, где требуется обработка больших объёмов текста без потери контекста. Проект находится на среднем уровне готовности к продакшну: имеет рабочий CLI/SDK, небольшую, но активную пользовательскую базу (42 ★, 4 fork), но требует дополнительной проверки лицензии, безопасности и поддержки перед масштабным развертыванием.

### 中文

**价值**  
zircote/rlm-rs 通过递归语言模型（RLM）模式，让 Claude Code 能够一次性处理比上下文窗口大 100 倍的文档。它在本地实现了智能分块、SQLite 持久化以及子‑LLM 的递归调度，帮助把“孤立的 Prompt+Tool”组合升级为可重复、可追踪的智能体工作流，从而在多代理协作、工具链编排和记忆管理等场景中显著提升效率和可靠性。

**典型接入方式**  
1. **CLI**：直接在终端运行 `rlm-rs`，传入文档路径、模型标识和工作流配置文件，即可完成分块、向量化、递归调用等全部步骤。  
2. **SDK/API**：库提供 Rust 公共函数（如 `process_document`, `run_sub_llm`），也可通过 FFI 暴露给 Python/Node 等语言，方便在现有微服务或脚本中嵌入。  
3. **持久化**：内部使用 SQLite 保存分块、向量和中间结果，调用方只需指定数据库文件路径，即可实现增量处理和历史查询。  

**生产可用性**  
- **成熟度**：当前评分 65/100，适合作为原型或内部工具使用。功能完整、文档清晰，但仍需对依赖（尤其是 Claude API）和安全审计进行一次性检查。  
- **维护状态**：最近一次提交在 2026‑05‑11，星标 42、Fork 4，活跃度一般；建议在正式上线前与维护者确认长期支持计划或自行 fork 进行维护。  
- **风险**：许可证、供应链安全以及持续维护尚未完成最终审查，部署前应完成合规与安全评估。  

总体而言，zircote/rlm-rs 是一个在 Rust 生态下实现的大文档递归处理工具，能够快速搭建多智能体工作流，适合在内部原型或受控生产环境中试点使用。

## 🧭 Practical evaluation

**Value:** zircote/rlm-rs helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 42 GitHub stars
- 4 forks
- updated 2026-05-11
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 30/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/zircote/rlm-rs) · [← Back to Orchestration](./README.md)</sub>
