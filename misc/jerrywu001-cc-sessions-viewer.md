# jerrywu001/cc-sessions-viewer

[![Stars](https://img.shields.io/github/stars/jerrywu001/cc-sessions-viewer?style=flat-square&color=yellow)](https://github.com/jerrywu001/cc-sessions-viewer/stargazers) [![Forks](https://img.shields.io/github/forks/jerrywu001/cc-sessions-viewer?style=flat-square&color=blue)](https://github.com/jerrywu001/cc-sessions-viewer/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> support cc/codex/gemini sessions viewer, token usage statistics, global search, resume, and export to html

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 159 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Rust |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`jerrywu001/cc‑sessions‑viewer` is a Rust‑based tool that visualises Chat‑GPT/Claude/Codex/Gemini conversation sessions, showing token‑usage statistics, offering global search, resumable playback, and HTML export. It targets developers who need quick insight into LLM interaction logs for prototyping, RAG pipelines, or agent‑workflow debugging.

**Value Proposition**  
- **Immediate observability:** Turns raw session dumps into an interactive UI with usage metrics, letting teams spot prompt‑engineering issues, cost overruns, or model drift without building custom parsers.  
- **Export & shareability:** One‑click HTML export creates portable reports for stakeholders or compliance audits.  
- **Language‑agnostic session support:** Works with the major commercial LLM APIs (OpenAI, Anthropic, Google Gemini), so you can reuse it across heterogeneous projects.

**Practical Adoption Path**  
1. **Clone & build** the repository (Rust toolchain ≥ 1.70).  
2. **Configure** API‑specific session importers (JSON/NDJSON) according to the README; no runtime API keys are needed unless you want to fetch live sessions.  
3. **Run** the viewer locally (`cargo run --release`) and point it at your session log directory.  
4. **Iterate**: use the UI to identify problematic prompts, then feed the cleaned prompts back into your prototype or RAG pipeline.  
5. **Optional integration**: wrap the binary in a Docker container or expose it as a micro‑service for internal CI/CD dashboards.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑06‑26) and has modest community traction (≈160 ★, 9 forks).  
- **Stability:** Core viewer functions are stable, but the integration hooks (session import formats, authentication) are not fully documented, requiring manual validation.  
- **Operational considerations:**  
  * Verify compatibility with your log format; you may need a small adapter script.  
  * Assess dependency maintenance (Rust crates) and containerise the binary to isolate version drift.  
  * For production use, add health‑checks, logging, and restrict file‑system access to avoid accidental data leakage.  

In short, `cc‑sessions‑viewer` is a ready‑to‑use observability layer for LLM session data—ideal for prototypes and internal tooling—but it should be vetted and containerised before being promoted to a production‑grade service.

### Русский

**jerrywu001/cc-sessions-viewer** — это open‑source‑утилита на Rust, позволяющая просматривать и анализировать сессии моделей Claude, Codex и Gemini: отображает статистику токенов, поддерживает глобальный поиск, возобновление и экспорт в HTML. Проект идеально подходит для быстрого прототипирования RAG‑ или агентных решений и оценки инструментов моделей, однако требует ручной проверки и уточнения интеграционных точек из‑за скудной метаданных. Готовность к production — средняя: пригоден для внутренних и экспериментальных сценариев, но перед выпуском в продакшн следует оценить зависимости и затраты на настройку.

### 中文

**项目简介（2‑3 句话）**  
jerrywu001/cc‑sessions‑viewer 是一款基于 Rust 的会话浏览工具，支持 CodeChat、Codex、Gemini 等模型的会话查看、令牌使用统计、全局搜索、会话恢复以及导出为 HTML。它帮助开发者快速洞察对话内容和资源消耗，为原型开发和内部调试提供可视化支撑。

**价值**  
- **快速评估模型行为**：通过可视化的令牌统计和全文搜索，帮助团队快速定位模型输出异常或成本热点。  
- **加速原型迭代**：无需自行实现会话持久化和统计功能，即可在 RAG、Agent 或其他 AI 工作流中直接使用，显著降低开发门槛。  
- **结果可共享**：导出为 HTML 的报告可直接嵌入文档或内部 Wiki，方便团队审阅和复盘。

**典型接入方式**  
1. **依赖引入**：在 Cargo.toml 中添加 `cc-sessions-viewer`（或克隆仓库）并编译。  
2. **会话持久化**：在业务代码中调用库提供的 API，将每次对话的请求/响应保存为 JSON/SQLite（库自带的存储后端）。  
3. **启动 Viewer**：运行 `cargo run --bin viewer`（或使用提供的二进制），指定会话存储路径，即可在本地浏览器中打开 UI。  
4. **可选集成**：通过环境变量或配置文件开启全局搜索、令牌统计或 HTML 导出功能，随后在 CI/CD 流程中自动生成报告。

**生产可用性**  
- **成熟度**：已有 159 ⭐、9 fork，最近一次更新为 2026‑06‑26，代码活跃度较高。  
- **适用场景**：适合原型、内部调试或研发团队的实验环境；在正式生产环境使用前，需要评估以下几点：  
  - **集成成本**：项目未提供完整的 SDK 文档，集成时需自行阅读源码并确认存储格式与现有日志体系兼容。  
  - **依赖维护**：Rust 生态相对稳定，但应锁定版本并定期检查上游安全公告。  
  - **性能与可扩展性**：在大规模会话（数十万条）下的搜索和统计性能尚未公开基准，建议先在测试环境进行压测。  

综合来看，cc‑sessions‑viewer 在原型和内部工作流中价值突出，具备中等生产就绪度；在正式上线前建议完成集成验证、性能评估以及依赖审计。

## 🧭 Practical evaluation

**Value:** jerrywu001/cc-sessions-viewer helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 159 GitHub stars
- 9 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 47/100 |
| topics | 0/100 |
| outlook | 57/100 |
| quality | 53/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/jerrywu001/cc-sessions-viewer) · [← Back to Misc](./README.md)</sub>
