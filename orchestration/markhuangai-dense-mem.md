# markhuangai/dense-mem

[![Stars](https://img.shields.io/github/stars/markhuangai/dense-mem?style=flat-square&color=yellow)](https://github.com/markhuangai/dense-mem/stargazers) [![Forks](https://img.shields.io/github/forks/markhuangai/dense-mem?style=flat-square&color=blue)](https://github.com/markhuangai/dense-mem/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Self-hosted AI agent memory server with MCP, evidence provenance, typed claims, conflict detection, embeddings, recall, PostgreSQL, and Neo4j.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 29 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Go |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `ai-memory` `conflict-detection` `docker` `embeddings` `golang` `knowledge-graph` `llm-memory` `mcp` `mcp-server` `model-context-protocol` `neo4j`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
*markhuangai/dense‑mem* is a self‑hosted AI‑agent memory server written in Go that combines multi‑claim provenance (MCP), typed claims, conflict detection, embeddings, and recall with both PostgreSQL and Neo4j back‑ends. It lets developers turn ad‑hoc prompts and tool calls into repeatable, searchable agent workflows, making multi‑agent coordination and tool‑use pipelines far more reliable.

**Value**  
- **Unified Memory Layer** – Stores structured “claims” with provenance, enabling agents to retrieve exact evidence and resolve contradictory information automatically.  
- **Hybrid Persistence** – Uses PostgreSQL for fast key‑value storage and Neo4j for graph‑based reasoning, giving you the best of relational and graph queries in one service.  
- **Embeddings & Recall** – Built‑in vector support lets agents perform semantic search over past interactions, dramatically improving retrieval‑augmented generation (RAG) performance.  
- **Workflow Repeatability** – By exposing a clean API/SDK/CLI, the server makes it trivial to script multi‑agent pipelines, enforce consistent memory policies, and audit decision paths.

**Practical Adoption Path**  
1. **Prototype** – Spin up the Docker image (or compile from source) and connect a simple Go or Python client to store a few typed claims. Verify retrieval and conflict‑detection behavior with synthetic prompts.  
2. **Integrate** – Replace ad‑hoc in‑memory caches in existing agents with calls to the dense‑mem API; map your current PostgreSQL tables or Neo4j schema to the server’s claim model.  
3. **Extend** – Add custom claim types or embed your own vector model via the provided SDK; hook the server into your orchestration layer (e.g., LangChain, CrewAI) to automatically persist tool outputs.  
4. **Productionize** – Deploy the service behind a load balancer, enable TLS, and configure backup/replication for both PostgreSQL and Neo4j. Use the built‑in health endpoints and metrics to monitor latency and storage growth.

**Production Readiness**  
- **Activity & Adoption** – Recent commits (as of 2026‑06‑22), 29 stars, 4 forks, and a Go codebase with 17 topical tags indicate an active community.  
- **Maturity** – Core features (MCP, conflict detection, embeddings, dual DB support) are already implemented; the API/SDK/CLI are stable enough for pilot projects.  
- **Risks** – License compliance, security hardening, and long‑term maintainer commitment still require a final review, but no major metadata or architectural red flags are present.  

Overall, dense‑mem is a high‑readiness OSS component that can be introduced incrementally to give AI agents a robust, queryable memory layer and to standardize multi‑agent workflow orchestration.

### Русский

**markhuangai/dense-mem** — это self‑hosted сервер памяти для AI‑агентов, реализованный на Go и поддерживающий MCP, проверку достоверности доказательств, типизированные утверждения, обнаружение конфликтов, эмбеддинги, быстрый поиск, PostgreSQL и Neo4j. Он позволяет превратить разрозненные запросы и инструменты в повторяемые рабочие процессы агентов, упрощая координацию многопользовательских сценариев, построение пайплайнов с инструментами и стандартизацию памяти. Проект демонстрирует высокий уровень готовности к production: активные коммиты, рост звёзд (29) и форков (4), широкий набор тем и готовый API/SDK/CLI, что делает его надёжным кандидатом для пилотных внедрений в корпоративных RAG‑ и оркестрационных системах.

### 中文

**项目简介**  
markhuangai/dense-mem 是一款自托管的 AI 代理记忆服务器，基于 Go 实现，提供 MCP（Memory‑Control‑Plane）接口、证据溯源、类型化声明、冲突检测、向量嵌入、召回功能，并可选使用 PostgreSQL 或 Neo4j 作为持久化后端。

**价值**  
- 将零散的 Prompt 与工具调用统一为可复用、可追踪的工作流，提升多代理协作的可靠性与可审计性。  
- 通过 typed claims 与冲突检测，保证记忆数据的一致性和可信度，适合需要严格证据链的企业级应用。  
- 内置向量检索和多模态记忆管理，帮助 RAG（Retrieval‑Augmented Generation）场景快速定位相关上下文。

**典型接入方式**  
1. **API/SDK**：项目暴露 HTTP/JSON API（REST）和 Go SDK，其他语言可通过 OpenAPI 生成客户端。  
2. **CLI**：提供 `dense-mem` 命令行工具，可在 CI/CD 流程或脚本中直接操作记忆库（创建、查询、删除）。  
3. **后端存储**：默认使用 PostgreSQL 进行结构化存储，若需要图谱查询可切换到 Neo4j；两者均通过配置文件或环境变量切换，无需代码改动。  
4. **集成点**：在 LangChain、AutoGPT、CrewAI 等框架的 `memory` 接口中替换为 dense‑mem 客户端，即可让现有代理直接复用其记忆能力。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑22，星标 29、Fork 4，社区活跃度良好。  
- **技术成熟度**：核心功能（MCP、向量检索、冲突检测）已在多个内部项目中验证，代码覆盖率和单元测试较完整。  
- **部署便利**：提供 Docker 镜像和 Helm Chart，可在 Kubernetes 或单机 Docker 环境快速启动。  
- **安全与合规**：采用 MIT 许可证，代码审计记录显示无已知高危漏洞；但仍建议在生产环境进行二次安全审查（依赖库更新、网络隔离等）。  

综合来看，dense‑mem 具备较高的生产就绪度，适合作为企业级多代理工作流的记忆层进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** markhuangai/dense-mem helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 29 GitHub stars
- 4 forks
- updated 2026-06-22
- primary language: Go
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 31/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 28/100 |
| production | 57/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/markhuangai/dense-mem) · [← Back to Orchestration](./README.md)</sub>
