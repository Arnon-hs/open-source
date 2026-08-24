# sdsrss/claude-mem-lite

[![Stars](https://img.shields.io/github/stars/sdsrss/claude-mem-lite?style=flat-square&color=yellow)](https://github.com/sdsrss/claude-mem-lite/stargazers) [![Forks](https://img.shields.io/github/forks/sdsrss/claude-mem-lite?style=flat-square&color=blue)](https://github.com/sdsrss/claude-mem-lite/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Persistent long-term memory for Claude Code via MCP — captures coding decisions, bugfixes, and context across sessions. Hybrid FTS5 + TF-IDF search with episode batching. Single SQLite DB, no external services. Alternative to claude-mem with 600x lower cost.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 47 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `ai-coding-assistant` `ai-memory` `anthropic` `claude` `claude-code` `claude-code-plugin` `fts5` `hooks` `hybrid-search` `llm-memory` `long-term-memory`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief summary**  
sdsrss/claude‑mem‑lite provides a lightweight, persistent long‑term memory layer for Claude Code agents, storing coding decisions, bug‑fixes and contextual information in a single SQLite database. It combines full‑text search (FTS5) with TF‑IDF‑based relevance scoring and episode batching, delivering the same capabilities as the original claude‑mem at roughly 1/600 of the cost and without any external services.

**Value**  
The library turns ad‑hoc Claude prompts and tool calls into repeatable, stateful workflows, enabling multi‑agent coordination, tool‑use pipelines, and standardized agent memory across sessions. By keeping all data locally in SQLite, it eliminates network latency, reduces operational overhead, and offers developers full control over privacy and security while still delivering fast, relevance‑aware retrieval.

**Practical adoption path**  

1. **Prototype** – Clone the repo, install the JavaScript package, and run the provided CLI or SDK examples to connect your Claude Code agent to the SQLite store.  
2. **Integration** – Replace the default stateless prompt handling in your agent code with the `memLite` API (e.g., `addEpisode`, `searchEpisodes`). Adjust the episode‑batch size or TF‑IDF weighting to match your domain.  
3. **Testing** – Validate retrieval quality on a representative code‑base, and benchmark cost vs. the full claude‑mem solution.  
4. **Production hardening** – Containerize the SQLite DB, set up regular backups, and audit the license and dependency tree. Add monitoring for DB size and query latency before rolling out to production.

**Production readiness**  
The project is at a *medium* readiness level: it is functional, actively maintained (last commit 2026‑06‑23), and has modest community interest (47 stars, 3 forks). It is suitable for prototypes, internal tools, or low‑to‑moderate traffic services, but production deployments should first address:  

* **Dependency & security review** – verify third‑party packages and confirm no known vulnerabilities.  
* **License compliance** – ensure the repository’s license aligns with your organization’s policies.  
* **Operational concerns** – plan for SQLite scaling limits, backup/restore procedures, and monitoring.  

Once these checks are completed, claude‑mem‑lite can be safely promoted to production for cost‑effective, on‑premise agent memory.

### Русский

**sdsrss/claude-mem-lite** — это лёгкая open‑source‑библиотека, обеспечивающая постоянную долгосрочную память для Claude Code через MCP, фиксируя принятые решения, исправления багов и контекст между сессиями. Она позволяет быстро построить повторяемые агентные воркфлоу: объединять несколько агентов, подключать инструменты и стандартизировать их память, используя гибридный поиск FTS5 + TF‑IDF и единую SQLite‑БД без внешних сервисов (600 × дешевле, чем оригинальный claude‑mem). Готовность к продакшну — средняя: проект уже стабилен для прототипов и внутренних процессов, но требует проверки лицензии, безопасности и поддержки перед масштабным внедрением.

### 中文

**项目简介（2‑3 句话）**  
`sdsrss/claude-mem-lite` 为 Claude Code 提供持久化的长期记忆层，使用 MCP 将编码决策、Bug 修复和上下文以 SQLite 单库形式保存，并通过 FTS5+TF‑IDF 实现高效检索。相较于原版 `claude-mem`，成本降低约 600 倍，且无需外部服务。

**价值**  
- 将零散的 Prompt 与工具调用统一为可复用的 Agent 工作流，提升多 Agent 协同和工具链自动化的可靠性。  
- 通过本地 SQLite 存储实现数据安全、低延迟和成本可控，适合研发团队内部的知识管理与代码审查追踪。  
- 混合全文检索 + 关键词加权（TF‑IDF）让历史决策与上下文快速定位，显著加速 bug 定位和代码生成。

**典型接入方式**  
1. **SDK / API**：项目提供 JavaScript SDK，直接在 Node.js 项目中 `import ClaudeMemLite from 'claude-mem-lite'` 并调用 `storeEpisode()`、`search(query)` 等方法。  
2. **CLI**：通过 `npx claude-mem-lite` 可在本地命令行执行 `add`, `search`, `export` 等操作，适合 CI/CD 流程或脚本化调用。  
3. **语言元数据**：库自动捕获文件路径、函数签名、Git 提交信息等元数据，便于在后续检索时过滤特定语言或模块。  

**生产可用性**  
- **成熟度**：Medium。已有 47 星、3 个 Fork，近期（2026‑06‑23）仍在更新，适合作为原型或内部工具快速落地。  
- **依赖**：唯一外部依赖为 SQLite（内置于 Node），部署简单，无需额外云服务。  
- **风险**：需进一步审查许可证兼容性、代码安全审计以及维护者活跃度后方可在对外服务中使用。  

总体而言，`claude-mem-lite` 是一个低成本、易集成的本地记忆层，适合在研发团队内部或受限环境中快速实现可重复的 Claude Agent 工作流。

## 🧭 Practical evaluation

**Value:** sdsrss/claude-mem-lite helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 47 GitHub stars
- 3 forks
- updated 2026-06-23
- primary language: JavaScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 36/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 30/100 |
| production | 55/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/sdsrss/claude-mem-lite) · [← Back to Orchestration](./README.md)</sub>
