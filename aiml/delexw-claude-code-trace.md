# delexw/claude-code-trace

[![Stars](https://img.shields.io/github/stars/delexw/claude-code-trace?style=flat-square&color=yellow)](https://github.com/delexw/claude-code-trace/stargazers) [![Forks](https://img.shields.io/github/forks/delexw/claude-code-trace?style=flat-square&color=blue)](https://github.com/delexw/claude-code-trace/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Claude Code session log viewer for JSONL files in ~/.claude/projects. Browse conversations, tool calls, tokens, and live tail sessions on desktop, web, and TUI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 271 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | Rust |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-tools` `anthropic` `claude` `claude-code` `desktop-app` `developer-tools` `jsonl` `llm-tools` `log-viewer` `react` `rust` `session-viewer`

## 🎯 Categories

AI/ML · Frontend · DevTools

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
delexw/claude-code-trace is a Rust‑based viewer for Claude Code session logs stored as JSONL files in ~/.claude/projects. It lets developers browse full conversations, tool‑call payloads, token usage, and even live‑tail active sessions through a desktop GUI, a web interface, or a terminal UI. The project is aimed at quickly adding AI‑assisted features, RAG pipelines, or agent workflows without building a model stack from scratch.

**Value**  
- **Rapid prototyping:** By visualizing Claude Code interactions out‑of‑the‑box, teams can iterate on prompts, tool integrations, and retrieval‑augmented generation without writing custom logging or UI code.  
- **Multi‑modal access:** The same viewer works on the desktop, in a browser, or as a TUI, fitting into diverse developer workflows and CI pipelines.  
- **Open‑source transparency:** With 271 stars and an active Rust codebase, the tool provides a community‑vetted way to inspect token economics and debugging data, which is often missing in closed‑source AI platforms.

**Practical adoption path**  
1. **Proof‑of‑concept:** Clone the repo, run the provided README steps, and point the viewer at a local `~/.claude/projects` directory containing a few JSONL logs. Verify that conversations, tool calls, and token stats appear correctly.  
2. **Integration testing:** Wrap the viewer in a small internal script that dumps Claude Code logs from your CI or dev environment into the expected directory, then use the TUI mode for quick developer checks.  
3. **Embedding:** If the UI is useful, embed the web version in an internal dashboard or expose the desktop binary as part of a larger AI‑ops toolbox.  
4. **Production gate:** Conduct a dependency audit (Rust toolchain, any native libraries), add version pinning, and write a minimal wrapper that starts the viewer as a service only when needed.

**Production readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑05‑11) and has a modest but healthy community signal (stars, forks).  
- **Stability:** Core functionality (log parsing, UI rendering) appears solid, but the integration surface (how logs are generated and where they are stored) is not standardized, so some custom glue code will be required.  
- **Risks:** Lack of detailed integration documentation may increase setup time; Rust runtime and native dependencies need verification for your target environment. A small pilot is advisable before scaling to critical workflows.  

Overall, delexw/claude-code-trace is a practical, low‑cost option for teams that need visibility into Claude Code sessions and want to prototype AI‑enhanced features quickly, provided they allocate time for a brief proof‑of‑concept and dependency validation.

### Русский

**delexw/claude-code-trace** — это open‑source‑утилита на Rust, позволяющая просматривать и «тянуть в реальном времени» логи сессий Claude Code (JSONL в ~/.claude/projects). Она удобна для прототипирования AI‑фич, построения RAG‑агентов и оценки инструментов модели: достаточно добавить небольшую библиотеку в проект, запустить CLI/TUI или открыть веб‑интерфейс и сразу получать доступ к диалогам, вызовам инструментов и токенам. Готовность к production — средняя: проект уже имеет 271 звезду, активные обновления и поддерживает несколько UI, но требует проверки зависимостей и небольшого proof‑of‑concept перед масштабным внедрением.

### 中文

**项目简介**  
delexw/claude-code‑trace 是一款用于查看 `~/.claude/projects` 目录下 JSONL 会话日志的工具，支持在桌面、浏览器以及 TUI 中浏览 Claude Code 对话、工具调用、 token 消耗，并可实时 tail 会话。

**价值**  
- **快速赋能 AI 功能**：无需自行搭建模型堆栈，直接读取 Claude Code 的会话日志即可进行原型验证、RAG/Agent 工作流调试或工具链评估。  
- **多端统一视图**：桌面、Web 与终端三种 UI 同时可用，方便不同角色（开发者、产品、运维）统一查看和分析。  
- **实时监控**：支持 live‑tail，帮助在调试阶段即时捕获模型输出和工具调用细节，提升迭代效率。

**典型接入方式**  
1. **依赖安装**：项目基于 Rust，使用 `cargo install claude-code-trace` 或下载预编译二进制。  
2. **配置路径**：确保 Claude Code 将日志写入 `~/.claude/projects/*.jsonl`（默认行为），或在启动时通过 `--log-dir` 指定自定义目录。  
3. **启动方式**  
   - **桌面/Web**：`claude-code-trace --mode gui`（会启动本地 Electron/wasm 前端）。  
   - **TUI**：`claude-code-trace --mode tui`（在终端直接交互）。  
   - **实时 tail**：`claude-code-trace --tail`，配合 CI/CD 或本地调试脚本使用。  
4. **集成到 CI**：在测试脚本结束后调用 `claude-code-trace export --format html` 生成可视化报告，供团队审阅。

**生产可用性**  
- **成熟度**：GitHub ★271，最近一次更新 2026‑05‑11，代码以 Rust 编写，社区活跃度一般。  
- **适用场景**：内部原型、研发调试、日志审计等 **中等** 可靠性需求。  
- **风险与准备**  
  - 依赖链相对简单，但需自行管理 Rust 环境和二进制分发。  
  - 文档主要在 README，缺少完整的 CI/CD 集成示例，建议先做 **POC**（如在开发分支集成一次日志可视化），确认部署成本与安全合规后再推广。  
  - 生产环境使用前，建议：  
    1. 对日志目录进行访问控制。  
    2. 评估二进制的安全签名与更新策略。  
    3. 在非关键业务上做容错测试（如日志滚动、异常退出恢复）。  

综上，delexw/claude-code-trace 能显著降低 AI 功能原型的搭建门槛，适合作为内部研发或实验平台的日志可视化组件；在经过小规模验证并做好依赖与安全审查后，可逐步推广到生产环境。

## 🧭 Practical evaluation

**Value:** delexw/claude-code-trace helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 271 GitHub stars
- 6 forks
- updated 2026-05-11
- primary language: Rust
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 52/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 43/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/delexw/claude-code-trace) · [← Back to AI/ML](./README.md)</sub>
