# neo4j-labs/agent-memory

[![Stars](https://img.shields.io/github/stars/neo4j-labs/agent-memory?style=flat-square&color=yellow)](https://github.com/neo4j-labs/agent-memory/stargazers) [![Forks](https://img.shields.io/github/forks/neo4j-labs/agent-memory?style=flat-square&color=blue)](https://github.com/neo4j-labs/agent-memory/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> A graph-native memory system for AI agents and context graphs. Store conversations, build knowledge graphs, and let your agents learn from their own reasoning — all backed by Neo4j.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 362 |
| 🍴 **Forks** | 83 |
| 💻 **Language** | Python |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `context-graph` `context-graphs` `graph-based-reasoning` `knowledge-graph` `neo4j`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary**  
neo4j‑labs/agent‑memory is a Python library that turns Neo4j into a graph‑native “memory” for AI agents. It lets you persist conversation turns, build and query knowledge graphs, and feed an agent’s own reasoning back into the graph so that future interactions can reuse and extend that context.

**Value**  
- **Unified context store** – Instead of scattering prompts, logs, and embeddings across files or vector stores, all information lives in a single Neo4j graph, making it easy to traverse relationships, reason over provenance, and retrieve the most relevant facts.  
- **Repeatable workflows** – By persisting tool‑use results and intermediate reasoning steps, agents can pick up where they left off, enabling multi‑step, multi‑agent pipelines that are deterministic and auditable.  
- **Knowledge‑graph enrichment** – Each conversation can automatically extend a domain‑specific knowledge graph, turning raw dialogue into structured entities and relations that downstream agents or analytics can consume.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided notebooks or example scripts against a local Neo4j sandbox. Verify that you can store a simple turn‑taking dialogue and retrieve it with Cypher queries.  
2. **Integrate with an existing agent** – Wrap the library’s `store_message` / `retrieve_context` helpers around your LLM call chain (e.g., LangChain, LlamaIndex). Start with a single‑agent use case such as “customer‑support chat history.”  
3. **Scale to multi‑agent pipelines** – Extend the graph schema to include tool‑use nodes (API calls, function executions). Use Neo4j’s built‑in graph algorithms or APOC procedures to route tasks between agents based on graph topology.  
4. **Production hardening** –  
   * Pin the Neo4j version (e.g., 5.x) and lock the library’s dependency versions.  
   * Add authentication/role‑based access controls to the Neo4j instance.  
   * Implement monitoring (query latency, graph size) and backup policies.  
   * Write integration tests that exercise the full store‑retrieve‑reason loop.

**Production Readiness**  
- **Maturity**: Medium. The project has a solid base (362 ★, recent commits, Python‑first) and is suitable for prototypes or internal services.  
- **Dependencies**: Relies on Neo4j (self‑hosted or Aura) and standard Python ML stacks; these are well‑understood but require version management.  
- **Risks**: License and long‑term maintainer activity need confirmation; security posture depends on how the Neo4j deployment is configured.  
- **Next steps for production**: Conduct a security review of the Neo4j instance, establish CI/CD pipelines that include dependency scanning, and run load tests to confirm the graph can handle the expected volume of agent interactions.

In short, neo4j‑labs/agent‑memory offers a compelling way to give AI agents a persistent, queryable memory backed by a graph database, with a clear incremental path from sandbox experimentation to a hardened production service.

### Русский

**neo4j-labs/agent-memory** – это графо‑ориентированная система памяти для AI‑агентов, позволяющая сохранять диалоги, автоматически формировать графы знаний и использовать их для последующего вывода, полностью опираясь на Neo4j. Типичный сценарий внедрения — создание небольшого proof‑of‑concept, в котором агенты обмениваются результатами через единый контекстный граф (координация нескольких агентов, добавление пайплайнов инструментов и стандартизация их памяти); после подтверждения работоспособности можно расширять решение до внутренних или клиентских сервисов. Готовность к production — средняя: проект стабилен для прототипов и внутренних workflow, но требует проверки лицензии, безопасности и наличия активных мейнтейнеров перед запуском в продакшн.

### 中文

**项目简介**  
neo4j‑labs/agent‑memory 是一个面向图数据库的 AI 记忆系统，能够把对话、推理过程以及工具使用记录持久化为 Neo4j 图谱，让智能体在后续交互中直接检索和复用已有的上下文与知识。  

**价值**  
- **统一记忆层**：把分散的 Prompt、工具调用和推理结果统一存入图谱，消除“孤岛”式的 Prompt，形成可查询、可演化的知识网络。  
- **可视化与可解释**：基于 Neo4j 的图形化界面，开发者和业务方可以直观看到智能体的思考路径和知识结构，提升调试和审计效率。  
- **复用与学习**：通过图查询（Cypher）快速检索历史对话或推理片段，实现跨会话、跨智能体的记忆共享和自我学习。  

**典型接入方式**  
1. **依赖安装**：`pip install neo4j-agent-memory`（或直接克隆仓库并安装 `requirements.txt`）。  
2. **连接 Neo4j**：在代码中创建 `Neo4jMemoryStore(uri, auth)` 实例，配置 Bolt URL 与凭证。  
3. **包装智能体**：将现有的 LLM 调用或工具链包装为 `Agent(memory_store=store)`，在每一次 `run()` 前后自动写入/读取记忆节点。  
4. **查询与扩展**：利用 Cypher 编写自定义查询或图算法（如路径搜索、社区检测），为后续 Prompt 提供上下文或进行知识图谱的自动扩展。  

**生产可用性评估**  
- **成熟度**：目前在 GitHub 上有 362 ⭐、83 🍴，活跃度高（最近一次提交 2026‑07‑12），代码主要使用 Python，适合作为原型或内部工具快速落地。  
- **依赖与运维**：核心依赖仅为官方 Neo4j Python 驱动，部署上只需要一套 Neo4j（可选 Aura Cloud 或自建集群），无需额外的消息队列或状态服务。  
- **风险点**：  
  - 许可证（Apache‑2.0）需确认与企业合规性匹配。  
  - 维护者活跃度虽在近期有提交，但长期维护计划尚未公开，建议在生产环境前锁定特定版本并自行制定升级策略。  
  - 安全方面主要是 Neo4j 访问控制和网络隔离，需要在企业防火墙或 VPC 中部署，并使用强密码或 TLS。  
- **适用场景**：原型验证、内部业务流程自动化、教学实验、以及需要可追溯记忆的多智能体协作。对外部高并发、严格 SLA 的业务，可在完成以下步骤后投入生产：  
  1. **小规模 PoC**：在沙盒 Neo4j 实例上跑通完整的记忆写入/查询链路。  
  2. **性能基准**：通过并发写入/查询压测确认图库规模（节点/关系）对响应时间的影响。  
  3. **监控与备份**：开启 Neo4j 的监控插件（Metrics、Auditing），并配置定期快照。  
  4. **CI/CD 与版本锁定**：将 `neo4j-agent-memory` 以固定版本写入 `requirements.txt`，并在 CI 中加入安全扫描。  

综上，neo4j‑labs/agent‑memory 在 **原型和内部工作流** 中具备即插即用的价值，接入成本低；在 **生产环境** 使用时，只要做好版本管理、权限控制和性能验证，就可以达到中等可靠性的要求。

## 🧭 Practical evaluation

**Value:** neo4j-labs/agent-memory helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 362 GitHub stars
- 83 forks
- updated 2026-07-12
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 54/100 |
| topics | 75/100 |
| outlook | 70/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/neo4j-labs/agent-memory) · [← Back to Orchestration](./README.md)</sub>
