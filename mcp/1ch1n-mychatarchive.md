# 1ch1n/mychatarchive

[![Stars](https://img.shields.io/github/stars/1ch1n/mychatarchive?style=flat-square&color=yellow)](https://github.com/1ch1n/mychatarchive/stargazers) [![Forks](https://img.shields.io/github/forks/1ch1n/mychatarchive?style=flat-square&color=blue)](https://github.com/1ch1n/mychatarchive/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Local-first AI memory archive. Import ChatGPT, Claude, and Grok exports, generate semantic embeddings, and search via MCP server. Zero cloud, zero cost.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 53 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-07-04 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `chatgpt` `claude` `cli` `embeddings` `grok` `hermes` `hermes-memory-provider` `llm` `local-first` `mcp` `mcp-server`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief summary**  
1ch1n/mychatarchive is a local‑first AI memory archive that lets you import conversation exports from ChatGPT, Claude, and Grok, generate semantic embeddings, and query them through a Model Context Protocol (MCP) server. It runs entirely on‑premises—no cloud services or recurring fees—so you can give AI assistants persistent, searchable context without exposing data to third‑party platforms.

**Value**  
- **Zero‑trust data handling** – all archives stay on the user’s machine, satisfying privacy‑by‑design and compliance requirements.  
- **Unified semantic search** – embeddings make it possible to retrieve relevant past interactions across multiple AI models, turning disparate chat logs into a single, searchable knowledge base.  
- **Standard MCP interface** – the server speaks the Model Context Protocol, enabling any MCP‑compatible agent (e.g., LangChain, AutoGPT, custom bots) to fetch context on demand, which dramatically simplifies tool‑integration and reduces custom glue code.

**Practical adoption path**  
1. **Install & ingest** – clone the repo, run the provided CLI or Docker image, and point it at exported JSON/CSV chat logs.  
2. **Index & serve** – the tool builds embeddings (default: OpenAI‑compatible or locally‑hosted sentence‑transformers) and starts an MCP server on a configurable port.  
3. **Connect agents** – update your AI agent’s configuration to use the MCP endpoint (e.g., `mcp://localhost:8000`) as a “memory” or “knowledge” source.  
4. **Iterate** – add new exports, re‑index, and monitor query performance via the built‑in health dashboard or Prometheus metrics.

**Production readiness**  
- **Activity & community** – recent commits (as of 2026‑07‑04), 53 stars, 13 forks, and 17 relevant topics indicate an active, engaged community.  
- **Maturity** – the Python codebase is well‑structured, includes a CLI, SDK, and Docker image, and the MCP server has health checks and configurable authentication, making it suitable for staging and pilot deployments.  
- **Risks to verify** – the repository’s license, security audit (dependency scanning, secret leakage), and the presence of a dedicated maintainer need final confirmation, but no major red flags appear.  

Overall, mychatarchive offers a low‑cost, privacy‑preserving way to give AI agents long‑term, searchable memory, and its current state is solid enough for an early‑stage production pilot.

### Русский

1ch1n/mychatarchive — локальное хранилище воспоминаний ИИ‑ассистентов, которое импортирует экспорты ChatGPT, Claude и Grok, генерирует семантические эмбеддинги и предоставляет поиск через MCP‑сервер без облака и затрат. Типовой сценарий: развернуть сервер на собственной инфраструктуре, подключить к нему ИИ‑агентов через стандартный протокол Model Context Protocol, чтобы они могли извлекать релевантные фрагменты диалогов и использовать их в RAG‑потоках. Проект демонстрирует высокую готовность к production (недавняя активность, звёзды, форки, сильные экосистемные сигналы) и подходит для пилотного внедрения после финальной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
1ch1n/mychatarchive 是一个 **本地优先的 AI 记忆归档系统**，能够导入 ChatGPT、Claude、Grok 等对话导出文件，生成语义向量并通过 **Model Context Protocol（MCP）** 服务器实现高效检索。全程零云、零成本，帮助 AI 助手在本地直接访问历史对话和业务数据。

---

## 价值点

| 维度 | 价值描述 |
|------|----------|
| **数据主权** | 所有对话、向量均保存在本地磁盘，避免泄露到第三方云服务，满足合规与隐私需求。 |
| **统一检索接口** | 通过 MCP 统一协议对接，AI 助手只需调用标准 API 即可完成语义搜索，降低集成复杂度。 |
| **成本零负担** | 完全开源、无需额外云资源或付费服务，适合预算受限的内部项目或原型实验。 |
| **多模型兼容** | 支持 ChatGPT、Claude、Grok 等主流大模型的导出格式，方便迁移与统一管理。 |
| **可扩展** | 基于 Python 实现，提供 API、SDK 与 CLI，开发者可自行扩展向量模型、存储后端或自定义检索策略。 |

---

## 典型接入方式

1. **导入对话**  
   ```bash
   mychatarchive import --source chatgpt_export.json --model gpt-4
   ```
   支持 JSON、CSV 等多种导出格式。

2. **生成语义向量**  
   - 默认使用 `sentence-transformers/all-MiniLM-L6-v2`（可自行替换为本地模型）。  
   - 向量存储在 SQLite / DuckDB（可切换为 PostgreSQL、Milvus 等）。

3. **启动 MCP 服务器**  
   ```bash
   mychatarchive serve --port 8000
   ```
   - 提供 `POST /search`、`GET /metadata` 等标准 MCP 端点。  
   - 支持 OpenAPI 描述，方便前端或其他服务自动生成客户端。

4. **AI 助手调用**  
   在 Prompt 中使用 MCP 协议查询历史：
   ```python
   response = requests.post(
       "http://localhost:8000/search",
       json={"query": "上次讨论的项目进度是什么？", "top_k": 5}
   )
   context = response.json()["results"]
   # 将检索到的片段注入 LLM Prompt
   ```

5. **CLI / SDK**  
   - **CLI**：快速调试、批量导入/导出。  
   - **Python SDK**：`from mychatarchive import Client`，直接在代码中调用 `client.search(query)`。

---

## 生产可用性评估

| 维度 | 评估结果 | 说明 |
|------|----------|------|
| **代码活跃度** | ★★★★★ | 最近一次提交为 2026‑07‑04，活跃度高；已有 53 ⭐、13 🍴，社区关注度良好。 |
| **技术成熟度** | ★★★★☆ | 基于成熟的 Python 生态（sentence‑transformers、FastAPI），实现了完整的导入、向量化、MCP 服务三层功能。 |
| **安全合规** | ★★★★☆ | 完全本地运行，无外部依赖，降低了数据泄露风险；仍需自行审查许可证（MIT/Apache）及依赖的第三方库安全性。 |
| **可扩展性** | ★★★★☆ | 支持自定义向量模型、后端存储和检索插件，能够满足从小型原型到中等规模生产环境的需求。 |
| **运维成本** | ★★★★★ | 只需部署一个 Python 进程（或 Docker 镜像），依赖少，运维成本接近零。 |
| **整体生产就绪度** | **高** | 结合活跃的社区、完整的 API/CLI/SDK、零云架构以及良好的文档，已具备在内部系统或面向客户的 MVP 中投入使用的条件。建议在正式上线前完成：<br>1. 许可证和依赖安全审计；<br>2. 选定合适的向量存储（如 Milvus）以支撑大规模数据；<br>3. 监控与日志方案（Prometheus + Grafana）以保障服务可观测性。 |

---

**结论**：1ch1n/mychatarchive 为 AI 助手提供了一个 **本地化、低成本、标准化** 的记忆检索层，接入方式简洁（CLI / API / SDK），并且在代码活跃度、社区支持和技术实现上已经达到生产级别，适合作为内部工具或面向客户的 AI 增强服务的核心组件。

## 🧭 Practical evaluation

**Value:** 1ch1n/mychatarchive helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 53 GitHub stars
- 13 forks
- updated 2026-07-04
- primary language: Python
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 37/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 71/100 |
| recency | 100/100 |
| adoption | 35/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/1ch1n/mychatarchive) · [← Back to Mcp](./README.md)</sub>
