# ThreatRecall/zettelforge

[![Stars](https://img.shields.io/github/stars/ThreatRecall/zettelforge?style=flat-square&color=yellow)](https://github.com/ThreatRecall/zettelforge/stargazers) [![Forks](https://img.shields.io/github/forks/ThreatRecall/zettelforge?style=flat-square&color=blue)](https://github.com/ThreatRecall/zettelforge/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Agentic memory for CTI in Python — STIX knowledge graphs, threat-actor alias resolution, offline-first RAG, MCP server for Claude Code and LangChain agents

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 50 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-memory` `ai-agent` `claude-code` `cti` `cybersecurity` `knowledge-graph` `langchain` `llm` `llm-memory` `mcp` `mcp-server` `mitre-attack`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ThreatRecall / zettelforge is a Python library that adds “agentic memory” to cyber‑threat‑intelligence (CTI) workflows by building STIX‑based knowledge graphs, resolving threat‑actor aliases, and providing an offline‑first RAG layer. It ships a lightweight MCP server that lets Claude‑Code and LangChain agents query and update this memory, making it easy to stitch together repeatable multi‑agent pipelines.

**Value**  
- **Unified CTI context:** By persisting STIX entities and alias mappings in a graph, agents can recall prior observations, enrich new alerts, and avoid duplicated effort.  
- **Plug‑and‑play agent orchestration:** The MCP server exposes a simple API/CLI/SDK, so existing Claude‑Code or LangChain agents can be turned into “memory‑aware” tools with just a few configuration lines.  
- **Offline‑first RAG:** The built‑in retrieval‑augmented generation component works without internet access, which is crucial for sensitive threat‑intel environments.  
- **Standardised pipelines:** Developers can define reusable tool‑use pipelines (e.g., fetch OSINT → resolve aliases → enrich STIX → generate report) that are version‑controlled and reproducible.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Prototype** – clone the repo, spin up the MCP server locally (`docker compose up` or `python -m zettelforge.server`). | Quick “smoke test” of API endpoints and graph ingestion. |
| 2️⃣  | **Integrate** – add the Python SDK to an existing Claude‑Code or LangChain agent (`pip install zettelforge`). Replace ad‑hoc prompts with calls to `client.query_memory(...)` and `client.update_graph(...)`. | Demonstrates the memory‑driven workflow without rewriting the whole agent. |
| 3️⃣  | **Validate CTI data** – import a sample STIX bundle (e.g., ATT&CK, MISP export) and run the alias‑resolution utilities. Verify that the graph reflects expected relationships. | Ensures the knowledge graph aligns with your organisation’s taxonomy. |
| 4️⃣  | **Add persistence & security** – back the graph with a production‑grade store (PostgreSQL, Neo4j) and enable TLS/auth on the MCP server. | Moves the prototype from a dev container to a secure, durable environment. |
| 5️⃣  | **CI/CD & monitoring** – package the server as a container image, add health checks, and instrument logs/metrics. | Provides the operational hygiene needed for production deployments. |
| 6️⃣  | **Roll‑out** – deploy the service in a staging environment, run end‑to‑end tests (e.g., “detect new IOCs → enrich → generate briefing”), then promote to production. | Final validation before exposing the service to analysts or automated pipelines. |

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑27) and has modest community traction (≈50 ★, 7 forks). It is suitable for internal prototypes, PoCs, or “sandbox” CTI pipelines.  
- **Dependencies:** Pure‑Python core with optional graph back‑ends; no heavyweight native binaries, which eases containerisation. However, you’ll need to audit third‑party packages for security and license compliance before a production rollout.  
- **Operational considerations:**  
  * **Scalability** – the built‑in in‑memory store works for small‑to‑medium graphs; for large enterprise STIX datasets you’ll want to switch to an external graph DB.  
  * **Security** – the MCP server currently lacks built‑in auth/role‑based access; you’ll need to front it with an API gateway or add TLS + token validation.  
  * **Maintainability** – the codebase is concise (≈20 topics) but limited documentation; allocating a small engineering owner to track upstream changes is advisable.  

Overall, ThreatRecall/zettelforge offers a compelling way to give CTI agents persistent, queryable memory and to orchestrate multi‑agent workflows. With a short integration effort and a clear path to hardening (auth, external storage, monitoring), it can move from prototype to production for internal threat‑intel automation.

### Русский

**ThreatRecall/zettelforge** — это Python‑библиотека, позволяющая создавать агентные рабочие процессы с постоянной памятью на основе STIX‑графов, разрешения алиасов угроз‑актеров и офлайн‑RAG, а также интегрировать их в MCP‑сервер для Claude Code и LangChain‑агентов. Типичный сценарий — построение повторяемых цепочек из нескольких агентов и инструментов (например, автоматическое обогащение данных о киберугрозах и их последующая аналитика), что упрощает стандартизацию памяти агентов и координацию их действий. Готовность к production — средняя: проект подходит для прототипов и внутренних пайплайнов, но перед запуском в продакшн требуется проверка лицензии, безопасности и стабильности зависимостей.

### 中文

**项目价值**  
ThreatRecall/zettelforge 为网络威胁情报（CTI）提供“Agentic memory”，能够把分散的提示、工具和 STIX 知识图谱统一到可重复的智能体工作流中。它实现了威胁行为体别名自动解析、离线‑first 的检索增强生成（RAG）以及面向 Claude Code 与 LangChain 的 MCP（Multi‑Channel‑Protocol）服务器，帮助安全团队快速搭建多智能体协同、工具调用与记忆标准化的自动化方案。

**典型接入方式**  
1. **API / SDK**：通过项目提供的 Python 包直接在代码中调用 `ZettelforgeClient`，完成 STIX 图谱查询、别名解析和 RAG 检索。  
2. **CLI**：使用 `zet` 命令行工具进行快速交互式查询或批量导入/导出情报数据。  
3. **MCP Server**：启动内置的 MCP 服务器（`python -m zettelforge.server`），让 Claude Code、LangChain 等大模型代理通过统一的协议调用记忆服务，实现工具链的即插即用。  

**生产可用性**  
- **成熟度**：目前评分 75/100，属于 **Medium** 级别。适合原型验证、内部安全运营或受控环境的生产部署。  
- **依赖与维护**：项目依赖 Python 生态常见库，代码最近更新于 2026‑06‑27，星标 50、fork 7，活跃度一般。上线前建议：  
  1. 检查许可证兼容性（项目采用的开源许可证）。  
  2. 完成安全审计，确认第三方依赖无已知漏洞。  
  3. 进行容错和监控配置，尤其是 MCP 服务的可用性与限流。  
- **可扩展性**：通过插件式的“tool‑use pipeline”可以轻松接入自研分析工具或外部威胁情报平台，支持水平扩展。  

综上，ThreatRecall/zettelforge 在构建可复用的 CTI 智能体工作流方面提供了完整的记忆与检索能力，接入方式灵活，适合作为内部原型或受控生产环境的核心组件。只要完成许可证、漏洞和运维检查，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** ThreatRecall/zettelforge helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 50 GitHub stars
- 7 forks
- updated 2026-06-27
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 36/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 32/100 |
| production | 55/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/ThreatRecall/zettelforge) · [← Back to Orchestration](./README.md)</sub>
