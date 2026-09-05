# yantrikos/yantrikdb-mcp

[![Stars](https://img.shields.io/github/stars/yantrikos/yantrikdb-mcp?style=flat-square&color=yellow)](https://github.com/yantrikos/yantrikdb-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/yantrikos/yantrikdb-mcp?style=flat-square&color=blue)](https://github.com/yantrikos/yantrikdb-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Persistent cognitive memory for AI agents — drop-in MCP server for Claude Code, Cursor, Windsurf. Temporal decay, contradiction detection, knowledge graph, autonomous consolidation. Backed by the YantrikDB Rust engine. Install: pip install yantrikdb-mcp.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Python |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `agent-skills` `ai-agents` `anthropic` `claude-code` `claude-desktop` `cognitive-memory` `cursor` `embeddings` `knowledge-graph` `llm` `mcp`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Yantrikos / yantrikdb‑mcp provides a drop‑in “memory‑consolidation‑protocol” (MCP) server that equips AI agents such as Claude Code, Cursor, and Windsurf with persistent, temporally‑decaying cognitive memory, contradiction detection, and a knowledge‑graph backed by the high‑performance YantrikDB Rust engine. Installable via a single `pip install yantrikdb-mcp`, it lets developers turn ad‑hoc prompts and tool calls into repeatable, autonomous agent workflows.

**Value Proposition**  
- **Unified Agent Memory:** By persisting and automatically consolidating the facts an agent learns, the MCP eliminates the “stateless” problem that forces developers to re‑inject context on every turn.  
- **Temporal Decay & Consistency Checks:** Information fades unless reinforced, and built‑in contradiction detection prevents agents from acting on stale or conflicting data.  
- **Knowledge‑Graph Export:** The stored memory can be queried as a graph, enabling downstream RAG, analytics, or audit trails.  
- **Plug‑and‑Play Integration:** A lightweight Python SDK/CLI and HTTP API make it trivial to attach the service to existing Claude Code, Cursor, or Windsurf pipelines without rewriting core logic.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Prototype** – Spin up the MCP locally (`yantrikdb-mcp serve`) and connect a single agent via the Python SDK. Verify that prompts and tool outputs are persisted and that decay works as expected. | Quick feedback loop; no infrastructure commitment. |
| 2️⃣  | **Integrate into a Multi‑Agent Pipeline** – Extend the prototype to coordinate two or more agents (e.g., Claude Code for code generation + Cursor for execution). Use the MCP’s “consolidation” endpoint to share learned facts across agents. | Demonstrates the core benefit of shared, consistent memory. |
| 3️⃣  | **Add Persistence Layer** – Deploy the MCP as a containerized service (Docker/K8s) behind an internal load balancer. Hook the service to a durable storage backend (e.g., PostgreSQL or S3) using YantrikDB’s configuration options. | Makes the memory durable across restarts and scales with traffic. |
| 4️⃣  | **Security & Governance Review** – Apply authentication (OAuth/JWT), enable audit logging, and run a dependency scan (e.g., `safety`, `trivy`). | Addresses the open‑risk items (license, security posture). |
| 5️⃣  | **Production Roll‑out** – Gradually route a subset of production workloads to the MCP‑backed agents, monitor latency, decay metrics, and contradiction alerts. Adjust decay parameters and consolidation frequency based on real‑world usage. | Controlled exposure mitigates risk while validating performance. |

**Production Readiness Assessment**  

- **Maturity:** Medium. The project is functional and actively updated (last commit 2026‑06‑28) with a modest but growing community (22 ★, 5 forks).  
- **Dependencies:** Pure‑Python client plus a Rust‑based engine packaged as a binary; requires monitoring of the native dependency for OS compatibility and security patches.  
- **Operational Considerations:**  
  - *Scalability* – Deployable as a stateless HTTP service; horizontal scaling is straightforward, but underlying YantrikDB storage must be sized for the expected graph volume.  
  - *Reliability* – No built‑in high‑availability features; you’ll need to run multiple replicas behind a load balancer and configure persistent storage.  
  - *Observability* – Exposes basic health endpoints; you’ll likely need to instrument custom metrics for decay rates and contradiction events.  
- **Risk Areas:** License verification, security audit of the Rust engine, and the need for an active maintainer to respond to bugs.  

**Bottom Line**  
YantrikDB‑MCP is a compelling building block for teams that want to give their AI agents a coherent, self‑maintaining memory layer without rewriting the agents themselves. It is ready for prototype and internal‑tool use today; with a modest amount of ops work (containerization, security hardening, and HA setup) it can be hardened for production‑grade deployments.

### Русский

Резюме для проекта yantrikos/yantrikdb-mcp:

Проект yantrikos/yantrikdb-mcp предлагает Persistent cognitive memory for AI агентов, который может быть легко интегрирован в существующие системы, такие как Claude Code, Cursor и Windsurf. Он позволяет координировать множество агентов, добавлять пайплайны использования инструментов и стандартизировать память агентов, что делает его идеальным решением для создания повторяемых агентских потоков. Проект имеет средний уровень готовности к production и требует дополнительных проверок зависимостей и поддержки перед внедрением в производную среду.

### 中文

**项目简介（2‑3 句话）**  
yantrikos/yantrikdb-mcp 为 AI 代理提供持久化的认知记忆层，作为 Claude Code、Cursor、Windsurf 等模型的即插即用 MCP（Memory Consolidation & Persistence）服务器。它基于高性能的 Rust 实现 YantrikDB，引入时间衰减、矛盾检测、知识图谱和自动归纳等功能，使代理能够在长期对话和多工具协作中保持一致且可追溯的记忆。

**价值**  
- **统一记忆**：把分散在不同提示、工具和子代理中的信息统一存入可查询的记忆库，避免信息丢失和重复计算。  
- **自动化归纳**：通过时间衰减和矛盾检测，系统会自行清理陈旧或冲突的记忆，并将关键事实抽象为知识图谱，提升后续推理和检索效率。  
- **快速原型**：只需 `pip install yantrikdb-mcp` 并在代码中调用提供的 API/SDK，即可为现有 AI 工作流添加持久记忆，显著降低构建多代理协作系统的门槛。

**典型接入方式**  
1. **Python SDK**：`import yantrikdb_mcp as mcp`，使用 `mcp.Client(endpoint)` 创建客户端，调用 `store_memory()、query_memory()、consolidate()` 等方法。  
2. **REST API**：启动 MCP 服务器（`yantrikdb-mcp serve --port 8000`），其他语言或工具通过 HTTP POST/GET 与 `/memory`, `/query`, `/consolidate` 端点交互。  
3. **CLI**：`yantrikdb-mcp add --key … --value …`、`yantrikdb-mcp get --key …`，适合脚本化或调试时使用。  

**生产可用性**  
- **成熟度**：当前评分 71/100，适合原型和内部业务流程。功能完整、文档清晰，依赖仅为 Python 与 Rust 编译产物。  
- **准备度**：中等。项目已有 22 星、5 个 fork，最近一次更新在 2026‑06‑28，代码活跃度尚可。仍需在正式上线前完成以下检查：  
  - 许可证兼容性（确认是否为 Apache‑2.0/MIT 等商业友好协议）  
  - 安全审计：检查依赖的 Rust 库和 Python 包是否存在已知漏洞  
  - 运维准备：监控 MCP 服务的健康状态、持久化存储备份与扩容策略  
- **部署建议**：在容器化环境（Docker/K8s）中运行 MCP 服务，配合持久化卷或云对象存储；在生产环境前进行压力测试，验证时间衰减和查询延迟是否满足业务 SLA。  

综上，yantrikos/yantrikdb-mcp 能帮助团队快速为 AI 代理添加可靠的记忆层，适合作为原型验证和内部自动化流程的核心组件，经过安全与运维评估后即可在生产环境中使用。

## 🧭 Practical evaluation

**Value:** yantrikos/yantrikdb-mcp helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 5 forks
- updated 2026-06-28
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 67/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/yantrikos/yantrikdb-mcp) · [← Back to Orchestration](./README.md)</sub>
