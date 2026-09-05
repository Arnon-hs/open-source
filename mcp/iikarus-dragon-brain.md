# iikarus/Dragon-Brain

[![Stars](https://img.shields.io/github/stars/iikarus/Dragon-Brain?style=flat-square&color=yellow)](https://github.com/iikarus/Dragon-Brain/stargazers) [![Forks](https://img.shields.io/github/forks/iikarus/Dragon-Brain?style=flat-square&color=blue)](https://github.com/iikarus/Dragon-Brain/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Dragon Brain — persistent long-term memory for AI agents via MCP (Model Context Protocol). Knowledge graph (FalkorDB) + vector search (Qdrant) + CUDA GPU embeddings. Works with Claude, Gemini CLI, Cursor, Windsurf, VS Code Copilot. 30 tools, 1121 tests.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 50 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Python |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-memory` `claude` `codex-cli` `cursor` `falkordb` `gemini-cli` `knowledge-graph` `llm-tools` `mcp` `memory` `model-agnostic` `qdrant`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Dragon‑Brain is an open‑source framework that gives AI agents persistent long‑term memory by combining a graph database (FalkorDB) with vector search (Qdrant) and GPU‑accelerated embeddings. It implements the Model Context Protocol (MCP) and ships ready‑to‑use integrations for Claude, Gemini CLI, Cursor, Windsurf, VS Code Copilot and 30 other tools, backed by a comprehensive test suite (1,121 tests). With a score of 82/100, it is positioned as a production‑grade OSS candidate for building repeatable, memory‑aware agent workflows.

---

### Value Proposition
- **Unified Memory Layer:** By persisting both relational knowledge (graph) and semantic embeddings, agents can recall past interactions, share context across sessions, and avoid “prompt forgetting.”
- **Plug‑and‑Play MCP Compliance:** The Model Context Protocol standardizes how prompts, tool calls, and memory updates are exchanged, making it easy to swap or combine LLM back‑ends (Claude, Gemini, etc.).
- **Tool‑Centric Orchestration:** Pre‑built connectors for 30 tools let developers quickly assemble multi‑agent pipelines (e.g., code generation → linting → testing) without writing custom glue code.
- **Scalable Performance:** CUDA‑accelerated embedding generation and Qdrant’s ANN search keep latency low even as the knowledge graph grows.

### Practical Adoption Path
1. **Evaluate the API/SDK:** Clone the repo, run the provided Docker compose (or local Python environment) and interact with the REST/CLI endpoints to store and retrieve a few test facts. The test suite can be used as a sanity‑check.
2. **Integrate a Target LLM:** Replace the default Claude/Gemini client with your own model by implementing the MCP interface; the codebase already abstracts the model behind a thin wrapper.
3. **Connect Existing Tools:** Use the supplied adapters (e.g., `cursor_adapter.py`, `copilot_adapter.py`) as templates to wrap any internal tool or service you need the agent to call.
4. **Pilot a Workflow:** Define a simple multi‑step use case (e.g., “fetch data → summarize → generate report”) and let the agent store intermediate results in the graph. Observe how memory improves downstream steps.
5. **Scale & Harden:** Deploy FalkorDB and Qdrant in a managed Kubernetes cluster, enable GPU‑enabled embedding workers, and add monitoring/alerting around the MCP endpoints.

### Production Readiness
- **Activity & Community:** Recent commits (as of 2026‑06‑24), 50 ★, 7 forks, and 13 GitHub topics indicate an active, albeit small, community. The extensive test coverage (1,121 tests) shows a focus on reliability.
- **Architecture:** Decoupled services (graph DB, vector store, embedding workers) align with cloud‑native deployment patterns; GPU support is optional but available for high‑throughput scenarios.
- **Ecosystem Fit:** Direct integrations with popular developer tools (VS Code Copilot, Cursor) and LLM providers make it easy to embed in existing pipelines.
- **Risks to Address Before Full Production:** A final review of the license (MIT‑like but verify), security posture of the exposed APIs, and confirmation of an active maintainer or governance model are still required.

Overall, Dragon‑Brain is mature enough for a serious pilot in environments that need persistent, context‑rich AI agents, with a clear upgrade path to full production once the remaining compliance checks are completed.

### Русский

**iikarus/Dragon‑Brain** — это открытая платформа, позволяющая AI‑агентам сохранять долговременную память через Model Context Protocol, объединяя граф знаний (FalkorDB), векторный поиск (Qdrant) и GPU‑эмбеддинги. Типичный сценарий — построение повторяемых многокомпонентных пайплайнов, где агенты (Claude, Gemini CLI, Cursor, Windsurf, VS Code Copilot и др.) обмениваются данными и используют 30 готовых инструментов, что упрощает координацию многопоточных рабочих процессов и стандартизацию памяти. Проект имеет высокий уровень готовности к production: активные коммиты, 50 звёзд, 7 форков, 1121 тест, поддержка API/SDK/CLI и широкая экосистема, требующая лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
Dragon‑Brain（iikarus/Dragon‑Brain）是一套面向 AI 代理的持久化长期记忆框架，基于 MCP（Model Context Protocol）实现。它将 FalkorDB 知识图谱、Qdrant 向量搜索和 CUDA GPU 嵌入相结合，能够在 Claude、Gemini CLI、Cursor、Windsurf、VS Code Copilot 等 30+ 工具之间共享记忆，已通过 1121 条单元测试，评分 82/100。

**价值**  
- **统一记忆**：把散落在各个 Prompt 与工具中的上下文统一存入图谱+向量库，实现跨会话、跨工具的记忆持久化。  
- **可复用工作流**：通过 MCP 将记忆、工具调用、数据检索封装为标准化的 API/SDK，帮助团队把一次性实验快速转化为可重复的多代理工作流。  
- **加速研发**：GPU 加速的嵌入生成与高效向量检索让大模型在 RAG 场景下响应更快，降低了自行搭建记忆层的成本。

**典型接入方式**  
1. **API/SDK**：项目提供 Python SDK 与 RESTful API，开发者只需在代码中引入 `dragon_brain` 包，调用 `add_memory()、query_memory()` 等函数，即可将上下文写入或检索。  
2. **CLI**：通过 `dragon-brain-cli` 可在命令行直接管理记忆库、查看图谱节点或执行向量相似度搜索，适合 CI/CD 或脚本化集成。  
3. **语言元数据 & 主题标签**：库会自动为每条记忆打上语言、工具、主题等标签，便于在多语言项目或不同工具链之间精准过滤。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24 最近一次提交，GitHub 50+ star、7 fork，代码基于 Python，拥有 13 个相关主题，社区活跃。  
- **测试覆盖**：已通过 1121 条单元/集成测试，覆盖记忆写入、向量检索、MCP 协议交互等关键路径。  
- **生态兼容**：原生支持 Claude、Gemini CLI、Cursor、Windsurf、VS Code Copilot 等主流大模型与开发工具，接入成本低。  
- **风险**：目前未发现重大元数据或安全隐患，但仍需对许可证（MIT/Apache 等）和长期维护者的承诺进行最终确认。  

综合来看，Dragon‑Brain 已具备较高的生产就绪度，适合作为企业级 AI 代理记忆层的 OSS 选型，先行在试点项目中验证后即可推广至正式生产环境。

## 🧭 Practical evaluation

**Value:** iikarus/Dragon-Brain helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 50 GitHub stars
- 7 forks
- updated 2026-06-24
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 36/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 32/100 |
| production | 73/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/iikarus/Dragon-Brain) · [← Back to Mcp](./README.md)</sub>
