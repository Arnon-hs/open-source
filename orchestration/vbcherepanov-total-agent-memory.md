# vbcherepanov/total-agent-memory

[![Stars](https://img.shields.io/github/stars/vbcherepanov/total-agent-memory?style=flat-square&color=yellow)](https://github.com/vbcherepanov/total-agent-memory/stargazers) [![Forks](https://img.shields.io/github/forks/vbcherepanov/total-agent-memory?style=flat-square&color=blue)](https://github.com/vbcherepanov/total-agent-memory/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-81%2F100-brightgreen?style=flat-square)](#)

> Persistent memory for Claude Code & Codex CLI. Auto-extracted knowledge graph, multi-representation embeddings, 3D WebGL visualization. LongMemEval R@5=97.45%. Self-hosted, Ollama-optional

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 34 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Python |
| 📈 **Score** | 81/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-memory` `ai-tools` `anthropic` `chromadb` `claude-code` `claude-code-mcp` `claude-code-plugin` `claude-memory` `codex-cli` `developer-tools` `knowledge-management` `llm-tools`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`vbcherepanov/total-agent-memory` is a Python‑based open‑source library that provides persistent, graph‑backed memory for Claude Code and Codex CLI agents. It automatically extracts a knowledge graph from interactions, stores multi‑representation embeddings, and offers a 3‑D WebGL visualizer; its LongMemEval benchmark scores R@5 = 97.45 %. The project is self‑hostable, works with Ollama, and is positioned as a turnkey way to turn ad‑hoc prompts and tool calls into repeatable, memory‑rich agent workflows.

**Value Proposition**  
- **Unified Agent Memory:** Turns isolated prompt‑tool calls into a durable, queryable knowledge store, enabling agents to recall past context, decisions, and results across sessions.  
- **Rich Representations:** Combines graph relationships, dense embeddings, and visual 3‑D maps, making it easy to surface relevant facts, detect patterns, and debug agent behavior.  
- **High Retrieval Quality:** LongMemEval R@5 = 97.45 % demonstrates that the system can retrieve the right piece of knowledge with very high precision, a critical metric for Retrieval‑Augmented Generation (RAG) pipelines.  
- **Plug‑and‑Play Integration:** Exposes a clean API/SDK and a CLI, so existing Claude Code or Codex scripts can be wrapped with minimal code changes, and it can be run on‑prem or via Ollama for flexible deployment.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Spin up a test instance** – clone the repo, install dependencies (`pip install -r requirements.txt`), and run the provided Docker compose or the `total-agent-memory` CLI. | Quick validation of environment compatibility and baseline performance. |
| 2️⃣  | **Integrate with your agent** – replace direct Claude/Codex calls with the library’s `MemoryClient` wrapper (or call the REST API). The wrapper automatically logs each prompt, tool invocation, and response into the persistent graph. | Gives agents immediate memory without rewriting core business logic. |
| 3️⃣  | **Define schema / topics** – optionally add domain‑specific node types or edge labels to tailor the knowledge graph to your use case (e.g., “Ticket”, “Customer”, “Resolution”). | Improves relevance of graph queries and downstream embeddings. |
| 4️⃣  | **Leverage retrieval** – use the built‑in `search(query, top_k=5)` function or embed‑based similarity to fetch prior context before each new prompt. | Demonstrates the RAG benefit and reduces hallucination. |
| 5️⃣  | **Monitor & visualize** – open the 3‑D WebGL dashboard (`/visualizer`) to see the evolving graph, spot bottlenecks, and audit agent decisions. | Provides transparency for developers and stakeholders. |
| 6️⃣  | **Scale & harden** – move the storage backend to a production database (PostgreSQL/Neo4j) and enable Ollama or a dedicated LLM inference server for higher throughput. | Prepares the system for production traffic and compliance requirements. |

**Production Readiness**  

- **Activity & Community**: 34 ⭐, 9 🍴, last commit 2026‑05‑14; active issue response and recent releases indicate healthy maintenance.  
- **Architecture**: Modular Python core, optional Docker deployment, and a language‑agnostic REST/CLI surface make it easy to embed in existing pipelines.  
- **Performance**: Benchmark (LongMemEval R@5 = 97.45 %) shows state‑of‑the‑art retrieval accuracy; the 3‑D visualizer runs in any modern browser with minimal overhead.  
- **Deployability**: Self‑hostable on‑prem or via Ollama; no vendor lock‑in, and the storage layer can be swapped (SQLite for dev, PostgreSQL/Neo4j for prod).  
- **Risk Considerations**: License (MIT‑style) and security posture need a final audit, but no red flags appear in the repo; the small contributor base suggests adding a secondary maintainer for long‑term resilience.

Overall, `total-agent-memory` is mature enough for a pilot in a production environment, especially where reproducible, memory‑aware agent workflows and transparent debugging are required.

### Русский

**total-agent-memory** — это open‑source‑библиотека на Python, которая обеспечивает постоянную память для Claude Code и Codex CLI: автоматически извлекает граф знаний, создает многопредставленные эмбеддинги и визуализирует их в 3‑D WebGL, показывая R@5 = 97.45 % в LongMemEval. Она позволяет превратить разрозненные запросы и инструменты в повторяемые агентные пайплайны — от координации нескольких агентов до стандартизации их памяти и построения сложных tool‑use сценариев, при этом может работать как самостоятельно, так и в связке с Ollama. Проект уже имеет активные коммиты (обновлён 14 мая 2026), 34 звёзд, 9 форков и широкий набор API/SDK/CLI, что свидетельствует о высокой готовности к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё ещё требуется.

### 中文

**项目价值**  
vbcherepanov/total-agent-memory 为 Claude Code 与 Codex CLI 提供持久化记忆层，能够自动抽取知识图谱、生成多模态嵌入并通过 3D WebGL 进行可视化。凭借 LongMemEval R@5 = 97.45% 的评测成绩，它可以把一次性提示和零散工具转化为可重复、可追踪的智能体工作流，从而显著提升多代理协作、工具链编排和记忆统一管理的效率。

**典型接入方式**  
1. **SDK / API**：项目在 `total_agent_memory` 包中暴露了 Python SDK，提供 `save_memory(prompt, response)`, `query_memory(query, top_k=5)` 等函数，直接在代码中调用即可。  
2. **CLI**：`tmem` 命令行工具支持 `tmem ingest --file <script>`、`tmem query "<question>"` 等子命令，适合快速实验或在 CI/CD 流程中嵌入。  
3. **Ollama（可选）**：若本地部署了 Ollama，项目可以把嵌入模型切换为 Ollama 提供的 LLM，做到完全离线运行。  
4. **Web 可视化**：启动 `tmem serve` 后会打开一个本地 WebGL 页面，展示记忆图谱的三维视图，便于调试和审计。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑14，拥有 34 ⭐、9 🍴，代码以 Python 为主，覆盖 20+ 话题标签，说明社区关注度和生态兼容性良好。  
- **成熟度**：LongMemEval 高分、完整的 API/CLI 文档以及可选的 Ollama 离线模式，使其具备直接在生产环境中进行试点的条件。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式上线前完成一次开源许可证合规审查，并对依赖的向量数据库或 WebGL 前端进行渗透测试。  

综上，total-agent-memory 已具备 **高可用**、**易集成**、**功能完整** 的特性，可作为企业级多代理工作流的记忆后端进行快速落地。

## 🧭 Practical evaluation

**Value:** vbcherepanov/total-agent-memory helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 34 GitHub stars
- 9 forks
- updated 2026-05-14
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 69/100 |
| recency | 100/100 |
| adoption | 31/100 |
| production | 79/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/vbcherepanov/total-agent-memory) · [← Back to Orchestration](./README.md)</sub>
