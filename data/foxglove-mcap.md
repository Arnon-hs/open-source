# foxglove/mcap

[![Stars](https://img.shields.io/github/stars/foxglove/mcap?style=flat-square&color=yellow)](https://github.com/foxglove/mcap/stargazers) [![Forks](https://img.shields.io/github/forks/foxglove/mcap?style=flat-square&color=blue)](https://github.com/foxglove/mcap/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> MCAP is a modular, performant, and serialization-agnostic container file format, useful for pub/sub and robotics applications.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 983 |
| 🍴 **Forks** | 214 |
| 💻 **Language** | Rust |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cpp` `data` `deserialization` `golang` `python` `robotics` `serialization` `swift` `typescript`

## 🎯 Categories

Data

## 📝 Summary

### English

**Brief Summary**  
MCAP (foxglove/mcap) is a high‑performance, modular container format that is agnostic to the underlying serialization method, making it ideal for pub/sub and robotics data pipelines. Its Rust implementation and growing community (≈1 k stars, 200+ forks) give it the robustness needed for production‑grade agent workflows.

**Value**  
- Provides a single, efficient file format for streaming sensor data, logs, and inter‑agent messages, eliminating the need for custom serialization layers.  
- Enables repeatable, auditable agent workflows by standardizing how prompts, tool outputs, and state snapshots are stored and retrieved.  
- Facilitates coordination of multi‑agent pipelines and persistent “memory” across sessions, which is essential for complex AI/ML orchestration.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the example scripts, and verify that your agents can write/read MCAP files using the provided Rust (or language bindings) APIs.  
2. **Integration Layer** – Wrap the MCAP read/write calls in a thin adapter that translates your existing prompt/tool payloads into MCAP records.  
3. **Pilot** – Deploy the adapter in a sandboxed workflow (e.g., a single multi‑agent task) and validate latency, size, and recoverability against your SLAs.  
4. **Scale** – Extend the adapter to all relevant pipelines, add schema validation if needed, and incorporate MCAP archives into your data lake or artifact store.

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑06‑24), active issue discussion, and a healthy fork/star ratio indicate ongoing maintenance.  
- **Performance**: Benchmarks from the repository show low overhead for both write and read paths, suitable for high‑throughput robotics and real‑time AI pipelines.  
- **Ecosystem Fit**: Rust core with language bindings (Python, C++, etc.) eases integration into most AI stacks.  
- **Risk**: No major metadata or licensing concerns identified, but a final security audit and confirmation of active maintainers are recommended before a full production rollout.  

Overall, MCAP is a mature OSS candidate that can be safely piloted now and, after the small PoC and security review, promoted to a production‑grade component for orchestrating multi‑agent AI workflows.

### Русский

**foxglove/mcap** — это высокопроизводительный, модульный формат контейнерных файлов, независимый от сериализации, который упрощает хранение и обмен потоковыми данными в системах pub/sub и робототехнике. Его типичное внедрение — построение повторяемых агентных конвейеров: от координации многопользовательских рабочих процессов до стандартизации памяти агентов и интеграции инструментов в единую пайплайн. Проект готов к production‑использованию: активная разработка, 983 звёзд на GitHub, регулярные обновления и широкое принятие в экосистеме, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介**  
MCAP（foxglove/mcap）是一种模块化、高性能且与序列化方式无关的容器文件格式，专为 Pub/Sub 与机器人系统设计，能够高效地存储和回放大规模时序数据。

**价值**  
- **统一数据存储**：提供统一的二进制封装，消除不同工具之间的格式壁垒，使多代理（agent）间的交互和记忆能够以同一标准进行持久化。  
- **提升工作流可复用性**：将孤立的 Prompt、工具调用等转化为可重复、可组合的工作流，便于构建复杂的多代理协同任务。  
- **高性能**：基于 Rust 实现的底层 I/O 与压缩，支持毫秒级写入/读取，适合实时机器人与大规模日志场景。

**典型接入方式**  
1. **依赖引入**：在 Rust 项目中直接 `cargo add mcap`，或在 Python/JS 等语言通过官方或社区提供的绑定库（如 `mcap-python`、`mcap-js`）进行调用。  
2. **写入数据**：创建 `Writer`，按时间戳顺序写入任意序列化的消息（protobuf、JSON、flatbuffers 等），文件自动分片、压缩。  
3. **读取与回放**：使用 `Reader` 进行流式遍历，配合过滤器仅读取感兴趣的主题，实现多代理的记忆检索或回放仿真。  
4. **与现有平台对接**：可在 ROS、DDS、Kafka 等 Pub/Sub 中间件前后层使用 MCAP 进行持久化或离线分析，仅需实现少量适配层。

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目拥有 983 ★、214 Fork，最近一次提交在同日，说明维护活跃。  
- **生态兼容**：提供多语言绑定和丰富的示例文档，易于在现有机器人或多代理平台中快速验证。  
- **可靠性**：Rust 实现保证内存安全与高并发，已在多个机器人项目和数据平台中实际使用，具备生产级稳定性。  
- **风险**：需进一步审查许可证（BSD‑3/Apache‑2.0 等）和安全审计报告，确认无隐蔽漏洞后即可在关键业务中推广。  

**结论**：MCAP 具备高性能、跨语言、易集成的特性，是构建可复用、多代理工作流和统一记忆存储的可靠底层组件，适合作为生产环境的核心数据容器。

## 🧭 Practical evaluation

**Value:** foxglove/mcap helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 983 GitHub stars
- 214 forks
- updated 2026-06-24
- primary language: Rust
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/foxglove/mcap) · [← Back to Data](./README.md)</sub>
