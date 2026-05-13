# mathomhaus/guild

[![Stars](https://img.shields.io/github/stars/mathomhaus/guild?style=flat-square&color=yellow)](https://github.com/mathomhaus/guild/stargazers) [![Forks](https://img.shields.io/github/forks/mathomhaus/guild?style=flat-square&color=blue)](https://github.com/mathomhaus/guild/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Shared context, memory, and task coordination across AI coding agents. Single Go binary, local SQLite, hybrid keyword and semantic search.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 188 |
| 🍴 **Forks** | 26 |
| 💻 **Language** | Go |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-coordination` `agent-memory` `ai-agents` `claude` `claude-code` `codex` `cursor` `golang` `harness-engineering` `local-first` `mcp` `mcp-server`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Frontend

## 📝 Summary

### English

**Brief Summary**  
mathomhaus/guild is an open‑source Go‑based framework that lets multiple AI coding agents share context, memory, and task coordination through a single binary backed by a local SQLite store and hybrid keyword‑plus‑semantic search. It turns ad‑hoc prompts and tool calls into repeatable, orchestrated agent workflows, making multi‑agent pipelines easier to build, debug, and reuse.  

**Value**  
- **Unified memory & context** – agents can read/write a shared SQLite knowledge base, eliminating the “cold‑start” problem and enabling cumulative learning across runs.  
- **Hybrid search** – keyword and embedding‑based retrieval lets agents locate relevant code snippets, documentation, or prior results quickly, improving accuracy and speed.  
- **Workflow repeatability** – by defining pipelines in a declarative DSL or via the CLI/SDK, teams can version‑control entire multi‑agent processes, turning experimental prompts into production‑grade services.  

**Practical Adoption Path**  
1. **Pilot** – Clone the repo, run the provided binary, and point it at an existing SQLite file or let it create a fresh one.  
2. **Integrate** – Use the exposed REST/SDK endpoints (or the CLI) from your existing AI coding agents (e.g., OpenAI, Claude, or self‑hosted LLMs) to store/retrieve context and trigger coordinated steps.  
3. **Define pipelines** – Encode your multi‑agent workflow in the simple YAML/JSON DSL or via Go code, then version‑control the definitions alongside your application code.  
4. **Scale** – Deploy the binary as a side‑car or a lightweight service in Kubernetes; the SQLite store can be mounted as a persistent volume or swapped for a distributed KV store if higher throughput is needed.  

**Production Readiness**  
- **Activity & community** – 188 ★, 26 forks, recent commits (as of 2026‑05‑13) and a healthy set of topics indicate active maintenance.  
- **Stability** – Single‑binary deployment, Go’s static linking, and a local SQLite backend make the runtime predictable and easy to containerize.  
- **Signals** – Clear API/SDK/CLI surface, strong adoption cues, and no immediate licensing or security red flags suggest it is ready for a serious pilot or production rollout, pending a final security/license audit.

### Русский

**mathomhaus/guild** — это открытая платформа на Go, позволяющая объединять контекст, память и координацию задач между несколькими AI‑агентами через единый бинарный файл, локальную SQLite и гибридный поиск (ключевые слова + семантика). Типичный сценарий — построение повторяемых рабочих потоков, где различные кодирующие агенты последовательно используют инструменты и делятся результатами через общую память; такой подход упрощает создание многокомпонентных пайплайнов и стандартизацию агентных взаимодействий. Проект имеет высокий уровень готовности к production: активные коммиты, 188 звёзд, поддержка API/SDK/CLI, широкая тема‑ориентированность и недавнее обновление (13 мая 2026), что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
mathomhaus/guild 是一款基于单一 Go 可执行文件的开源框架，提供共享上下文、记忆与任务协同功能，内部使用本地 SQLite 存储，并结合关键词与语义检索，实现 AI 编码代理之间的高效协作。

**价值主张**  
- 将零散的 Prompt 与工具包装成可复用的 Agent 工作流，降低跨代理的上下文切换成本。  
- 通过统一的记忆层和混合检索，提升多代理协同任务的准确性与效率。  
- 支持自定义工具链和任务管线，帮助团队快速构建复杂的 AI 编码流水线。

**典型接入方式**  
1. **CLI**：直接下载单个二进制文件，使用命令行启动 Guild 服务或执行单次任务。  
2. **SDK/API**：通过 Go 包或 HTTP API 与现有系统对接，调用 `CreateContext`、`AddMemory`、`Search` 等接口实现实时协同。  
3. **插件式工具链**：在 CI/CD、IDE 插件或自研前端中嵌入 Guild，利用其记忆库和检索能力为代码生成、审查或自动化重构提供上下文支撑。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13 最近一次提交，拥有 188 ★、26 Fork，13 个主题标签，社区活跃。  
- **技术成熟度**：单文件二进制 + 本地 SQLite，部署与运维成本低；混合检索实现了关键词与向量搜索的平衡。  
- **生态兼容**：提供标准化的 API/SDK，易于在 Go 项目或通过 HTTP 调用的多语言环境中集成。  
- **风险**：许可证、完整的安全审计以及维护者的长期可用性仍需进一步确认，但目前已具备足够的信号支持在生产环境进行试点。  

综上，mathomhaus/guild 已具备较高的生产就绪度，适合作为 AI 编码代理编排的核心组件，在多代理协作、工具链集成以及记忆标准化等场景中快速落地。

## 🧭 Practical evaluation

**Value:** mathomhaus/guild helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 188 GitHub stars
- 26 forks
- updated 2026-05-13
- primary language: Go
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 45/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/mathomhaus/guild) · [← Back to Orchestration](./README.md)</sub>
