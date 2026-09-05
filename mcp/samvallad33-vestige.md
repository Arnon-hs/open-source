# samvallad33/vestige

[![Stars](https://img.shields.io/github/stars/samvallad33/vestige?style=flat-square&color=yellow)](https://github.com/samvallad33/vestige/stargazers) [![Forks](https://img.shields.io/github/forks/samvallad33/vestige?style=flat-square&color=blue)](https://github.com/samvallad33/vestige/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Cognitive memory for AI agents: FSRS-6 spaced repetition, Brain modules, 3D dashboard, single small Rust binary. MCP server for Claude, Cursor, VS Code, Xcode, JetBrains.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 565 |
| 🍴 **Forks** | 57 |
| 💻 **Language** | Rust |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-memory` `claude` `cognitive-science` `cursor` `embeddings` `fsrs` `local-first` `long-term-memory` `mcp` `mcp-server` `neuroscience` `onnx`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief summary**  
Vestige (samvallad33/vestige) is a Rust‑based, single‑binary platform that implements the Model Context Protocol (MCP) to give AI agents real‑world memory and tool access. It combines a spaced‑repetition engine (FSRS‑6), modular “brain” components, and a 3D dashboard, and ships ready‑to‑run MCP servers for popular assistants such as Claude, Cursor, VS Code, Xcode, and JetBrains IDEs.

**Value proposition**  
- **Unified memory layer** – The built‑in FSRS‑6 spaced‑repetition system lets agents retain and recall information over time, turning stateless LLM calls into a cognitively persistent assistant.  
- **Standardized integration** – By exposing the Model Context Protocol, Vestige provides a common API/SDK/CLI that any MCP‑compatible agent can plug into, eliminating bespoke glue code for each tool.  
- **Tool‑centric execution** – Pre‑packaged MCP servers for major development environments let agents invoke IDE commands, run code, or query local data without custom extensions, accelerating “agent‑as‑a‑service” use cases.  
- **Low operational overhead** – A single small Rust binary means minimal dependencies, fast startup, and easy containerisation, which is attractive for both dev‑ops and edge deployments.

**Practical adoption path**  
1. **Prototype** – Clone the repo, build the binary, and run the supplied MCP server for the target tool (e.g., `vestige --serve claude`).  
2. **Connect an agent** – Configure your LLM‑based assistant (Claude, Cursor, etc.) to use the MCP endpoint (`http://localhost:xxxx`). Use the provided SDK or simple HTTP calls to store/retrieve memories and invoke tool actions.  
3. **Extend** – Add custom brain modules or replace the default FSRS‑6 scheduler if your domain needs a different forgetting curve. The modular Rust codebase makes this straightforward.  
4. **Scale** – Deploy the binary in a container orchestration platform (Docker/K8s) behind a load balancer; the stateless API can be horizontally scaled while the underlying SQLite/embedded store can be swapped for a distributed DB if needed.  
5. **Monitor & iterate** – Leverage the 3D dashboard for real‑time visibility into memory usage, request latency, and tool invocations, then fine‑tune the spaced‑repetition parameters.

**Production readiness**  
- **Activity & community** – 565 ★, 57 forks, recent commits (as of 2026‑06‑26), and a growing ecosystem of MCP‑compatible agents indicate healthy momentum.  
- **Stability** – The project is a single compiled Rust binary with no external runtime dependencies, reducing surface‑area for runtime failures.  
- **Security & licensing** – No major metadata risks have been flagged, but a final audit of the open‑source license and any third‑party crates is advisable before a wide‑scale rollout.  
- **Operational maturity** – Built‑in dashboard, clear API spec, and ready‑made server adapters for major IDEs make it “pilot‑ready”; teams can start with a sandbox deployment and graduate to production once integration tests validate the memory and tool‑calling semantics.  

Overall, Vestige offers a pragmatic, low‑friction way to give AI assistants persistent, tool‑aware capabilities, and its current state is solid enough for serious pilot projects and early production use.

### Русский

**samvallad33/vestige** — это компактный Rust‑бинарный сервер протокола MCP, который обеспечивает AI‑агентам «когнитивную память» (FSRS‑6 spaced repetition, мозговые модули) и 3‑D‑дашборд, позволяя им безопасно подключаться к реальным инструментам (Claude, Cursor, VS Code, Xcode, JetBrains). Типичный сценарий: развернуть MCP‑сервер, интегрировать его через API/SDK/CLI в существующие CI/CD или IDE, и дать моделям контекстный доступ к коду, данным и инструментам без кастомных надстроек. Проект считается почти готовым к production: активные коммиты, 565 звёзд, широкая экосистема Rust и подтверждённая совместимость с популярными инструментами, требующая лишь финального аудита лицензий и безопасности.

### 中文

**项目简介**  
samvallad33/vestige 是一个为 AI 代理提供认知记忆的开源框架，内置 FSRS‑6 间隔重复算法、可视化 3D 仪表盘和多种 Brain 模块，全部打包成一个体积小巧的 Rust 可执行文件。它实现了 Model Context Protocol (MCP) 服务器，可让 Claude、Cursor、VS Code、Xcode、JetBrains 等工具以统一协议接入 AI 助手。

**价值**  
- **统一协议**：通过 MCP 将 AI 代理与真实工具、代码库和业务数据进行标准化连接，降低集成成本。  
- **认知记忆**：FSRS‑6 间隔重复帮助 AI 持久记忆关键信息，提升对话连续性和任务执行效率。  
- **可视化与可扩展**：3D 仪表盘直观展示记忆状态，Brain 模块支持自定义知识库和推理逻辑。  
- **轻量部署**：单个 Rust 二进制文件，跨平台、启动快、资源占用低，适合边缘或云端部署。

**典型接入方式**  
1. **部署 MCP 服务器**：下载或自行编译 `vestige` 二进制，配置 `config.toml`（指定后端存储、记忆策略等），运行后在本地或容器中提供 HTTP/gRPC 接口。  
2. **使用 SDK/CLI**：项目提供 Rust、Python、Node.js 的客户端库以及命令行工具，开发者可直接调用 `create_memory`, `query_memory`, `update_brain` 等 API。  
3. **集成到 IDE/工具**：在 VS Code、JetBrains 插件或 Xcode 扩展中配置 MCP 端点，IDE 即可向 Vestige 发送上下文请求，实现代码补全、调试建议等功能。  
4. **与其他模型服务配合**：将 Claude、OpenAI、Claude‑2 等模型的上下文获取逻辑指向 Vestige，实现“记忆增强”的模型调用链。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，GitHub ★565、Fork 57，社区活跃，已有多个企业内部 pilot。  
- **技术成熟度**：核心使用 Rust 编写，单文件二进制保证了安全性与性能；提供完整的单元/集成测试。  
- **生态兼容**：实现标准 MCP，已有插件适配 VS Code、JetBrains、Cursor，易于扩展到其他工具。  
- **风险**：需进一步审查许可证（MIT/Apache 双许可）和安全审计报告；保持维护者活跃是后续关注点。  

综合来看，Vestige 已具备在生产环境中作为 AI 记忆层和工具桥接层的条件，适合作为企业级 AI 助手的核心组件进行试点并逐步推广。

## 🧭 Practical evaluation

**Value:** samvallad33/vestige helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 565 GitHub stars
- 57 forks
- updated 2026-06-26
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/samvallad33/vestige) · [← Back to Mcp](./README.md)</sub>
