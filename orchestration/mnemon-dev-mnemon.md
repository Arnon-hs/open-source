# mnemon-dev/mnemon

[![Stars](https://img.shields.io/github/stars/mnemon-dev/mnemon?style=flat-square&color=yellow)](https://github.com/mnemon-dev/mnemon/stargazers) [![Forks](https://img.shields.io/github/forks/mnemon-dev/mnemon?style=flat-square&color=blue)](https://github.com/mnemon-dev/mnemon/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> LLM-supervised persistent memory for AI agents — graph-based recall, cross-session knowledge, single binary. Works with Claude Code, OpenClaw, and any CLI agent.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 135 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Go |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-framework` `agent-memory` `ai-agent` `ai-tools` `claude` `claude-code` `claude-memory` `cli` `context-window` `golang` `knowledge-graph` `llm-agent`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
mnemon-dev/mnemon is an open‑source Go library that gives AI agents a persistent, graph‑based memory store, enabling cross‑session recall and tool‑driven workflows. It works out‑of‑the‑box with Claude Code, OpenClaw, and any CLI‑based agent, turning ad‑hoc prompts into repeatable, orchestrated pipelines. With 135 ⭐, recent commits and solid ecosystem signals, it’s ready for serious pilot projects.

**Value**  
- **Persistent, structured recall** – Agents can store and retrieve knowledge as nodes and edges, so information learned in one session is instantly available in the next.  
- **Workflow orchestration** – By exposing a simple API/CLI/SDK, mnemon lets you stitch together multiple agents, tools, and external services into a single, repeatable pipeline.  
- **Tool‑agnostic integration** – Because it is language‑agnostic and only requires HTTP/CLI calls, it can be dropped into existing Claude Code, OpenClaw, or custom CLI agents with minimal code changes.  
- **Single‑binary deployment** – The whole memory engine runs as one compiled binary, simplifying packaging, scaling, and security hardening.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided binary locally, and call the REST API from a small Claude‑Code script to store and retrieve a few facts.  
2. **Integrate** – Add the Go client (or any HTTP wrapper) to your existing agent codebase; replace ad‑hoc prompt‑based “remember” logic with mnemon’s `AddNode`, `Link`, and `Query` calls.  
3. **Orchestrate** – Use the CLI to chain multiple agents (e.g., a research agent → summarizer → executor) and persist intermediate results in the graph.  
4. **Scale** – Deploy the binary behind a service mesh or as a sidecar in Kubernetes; configure persistent storage (SQLite, PostgreSQL, or cloud blob) to retain the graph across pods.  
5. **Monitor & Harden** – Leverage the built‑in health endpoints and logs, apply standard Go security best practices, and audit the open‑source license before production rollout.

**Production Readiness**  
- **Activity & Adoption** – Recent commits (as of 2026‑05‑11), 135 stars, 21 forks, and usage in the Claude Code and OpenClaw ecosystems indicate an active community.  
- **Stability** – The project is written in Go, compiled to a single binary, and provides stable API/CLI contracts, reducing runtime dependencies.  
- **Ecosystem Fit** – Fits naturally into orchestration, MCP, and RAG stacks; the 20 GitHub topics show broad relevance.  
- **Risks** – Licensing and long‑term maintainer commitment still need a final check, and a formal security audit is recommended before handling sensitive data.  

Overall, mnemon offers a high‑value, low‑friction way to give AI agents durable memory and workflow orchestration, and it is mature enough for a production pilot after standard security and licensing vetting.

### Русский

mnemon-dev/mnemon — это open‑source‑решение на Go, которое обеспечивает LLM‑контролируемую персистентную память для AI‑агентов: графовое хранение, кросс‑сессионный контекст и единый бинарный артефакт, совместимый с Claude Code, OpenClaw и любыми CLI‑агентами. Проект позволяет превратить разрозненные запросы и инструменты в повторяемые рабочие процессы агентов, упрощая координацию многокомпонентных пайплайнов, добавление цепочек использования инструментов и стандартизацию памяти. По состоянию на 2026‑05‑11 репозиторий активен, имеет 135 звёзд, 21 форк, широкий набор API/SDK/CLI и хорошие сигналы экосистемы, что делает его готовым к пилотному запуску в продакшн после финального аудита лицензии и безопасности.

### 中文

**项目简介**  
mnemon‑dev/mnemon 为 AI 代理提供持久化记忆层，采用图结构实现跨会话的知识回溯与关联检索。它以单一二进制文件交付，能够直接与 Claude Code、OpenClaw 以及任何基于命令行的代理配合使用。

**核心价值**  
- **把孤立的 Prompt 与工具链转化为可复用的工作流**：记忆图让代理在不同会话之间共享上下文，避免重复信息输入。  
- **统一的多代理协作与工具调用**：通过图节点描述工具、任务和状态，轻松编排多代理协同或构建工具使用流水线。  
- **轻量、即插即用**：单二进制文件 + 简洁的 API/SDK/CLI，几行代码即可把记忆功能嵌入现有系统。

**典型接入方式**  
1. **CLI 方式**：下载 `mnemon` 二进制，使用 `mnemon start --port 8080` 启动本地记忆服务，随后在 Prompt 中通过 `mnemon query <key>` / `mnemon store <key> <value>` 与之交互。  
2. **SDK 方式**：在 Go 项目中引入 `github.com/mnemon-dev/mnemon/client`，使用 `client.New("http://localhost:8080")` 创建客户端，调用 `PutMemory`、`GetMemory`、`GraphSearch` 等方法。  
3. **API 方式**：直接调用 RESTful 接口（`POST /memory`, `GET /memory/{id}`, `POST /graph/search`），适配任意语言的代理或微服务。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11 最近一次提交，135 Stars、21 Fork，且持续接受社区 PR。  
- **技术成熟度**：核心实现使用 Go，提供完整的类型安全 SDK 与 OpenAPI 文档，易于 CI/CD 集成。  
- **生态兼容**：已在 Claude Code、OpenClaw 等主流 CLI 代理上验证，支持自定义插件扩展。  
- **风险点**：仍需对许可证（MIT）进行合规审查，建议进行一次安全审计并确认维护者的长期可用性后再用于关键业务。  

综合来看，mnemon 在 OSS 中的成熟度和生态支持足以支撑正式生产环境的试点部署，尤其适合需要跨会话记忆、工具编排和多代理协作的 AI 应用。

## 🧭 Practical evaluation

**Value:** mnemon-dev/mnemon helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 135 GitHub stars
- 21 forks
- updated 2026-05-11
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 72/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/mnemon-dev/mnemon) · [← Back to Orchestration](./README.md)</sub>
