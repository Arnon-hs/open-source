# datawhalechina/all-in-rag

[![Stars](https://img.shields.io/github/stars/datawhalechina/all-in-rag?style=flat-square&color=yellow)](https://github.com/datawhalechina/all-in-rag/stargazers) [![Forks](https://img.shields.io/github/forks/datawhalechina/all-in-rag?style=flat-square&color=blue)](https://github.com/datawhalechina/all-in-rag/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> 🔍大模型应用开发实战一：RAG 技术全栈指南，在线阅读地址：https://datawhalechina.github.io/all-in-rag/

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.2k |
| 🍴 **Forks** | 3.6k |
| 💻 **Language** | Python |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `deepseek` `embedding` `kimi-k2` `langchain` `llama-index` `llm` `milvus` `multimodal` `neo4j` `python` `rag`

## 🎯 Categories

Orchestration · Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *datawhalechina/all‑in‑RAG* repository is a full‑stack guide and codebase for building Retrieval‑Augmented Generation (RAG) pipelines with large language models. It demonstrates how to stitch together prompts, tools, memory, and multi‑agent orchestration into repeatable, production‑ready workflows, and is documented in an online tutorial (https://datawhalechina.github.io/all‑in‑rag/). With over 7 k stars, active maintenance, and a Python‑centric ecosystem, it is a mature open‑source option for teams looking to operationalize RAG‑based AI applications.

**Value**  
- **Turn ad‑hoc prompts into reusable agents** – the project supplies patterns, wrappers, and utilities that convert isolated LLM calls into orchestrated agents with built‑in tool use, memory, and state management.  
- **Accelerate multi‑agent workflows** – pre‑configured pipelines let you coordinate several agents (e.g., retriever, generator, validator) without writing boilerplate orchestration code.  
- **Standardized memory and tool integration** – reusable components for vector stores, external APIs, and persistent memory simplify the otherwise error‑prone “glue” code that most RAG projects need.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided notebooks or scripts on a small dataset to verify the end‑to‑end RAG flow.  
2. **Readme & Docs Review** – Ensure the documentation covers the specific vector store, LLM provider, and tool APIs you plan to use; adapt the configuration files accordingly.  
3. **Pilot Integration** – Replace the demo data with your domain documents, plug in your preferred LLM (e.g., OpenAI, Anthropic, or an on‑prem model), and expose the agent via a lightweight API (FastAPI/Flask).  
4. **Scale & Harden** – Add monitoring, logging, and security layers; containerize the service (Docker) and deploy to your orchestration platform (Kubernetes, Airflow, etc.).  

**Production Readiness**  
- **Activity & Community** – The repo shows recent commits (as of 2026‑05‑11), a large star/fork base, and active issue discussions, indicating strong community support.  
- **Technical Maturity** – Implemented in Python, leverages widely‑adopted libraries (LangChain, FAISS/Chroma, etc.), and follows modular design patterns suitable for CI/CD pipelines.  
- **Risk Assessment** – No major metadata or licensing concerns have been identified, though a final security audit and verification of maintainers’ responsiveness are recommended before full production rollout.  

Overall, *datawhalechina/all‑in‑RAG* is a high‑readiness OSS candidate for teams that need a battle‑tested, extensible foundation to move from experimental prompts to robust, orchestrated RAG services.

### Русский

**datawhalechina/all‑in‑rag** — это открытый Python‑проект, который превращает разрозненные запросы к большим моделям и наборы инструментов в воспроизводимые RAG‑агентские пайплайны: он упрощает оркестрацию многопользовательских воркфлоу, добавление инструментов и стандартизацию памяти агентов. Типичный сценарий — небольшая POC‑интеграция в существующее приложение (например, чат‑бот или система поиска), где требуется объединить внешние источники данных, инструменты (поиск, базы знаний) и LLM‑модели в единый «агент‑workflow». По готовности к продакшн проект считается высоким: активные коммиты, более 7 000 звёзд, многочисленные форки, свежая поддержка (обновление – 2026‑05‑11) и широкая экосистема, однако перед масштабным запуском следует проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
`datawhalechina/all-in-rag` 是一套面向大模型开发者的 RAG（Retrieval‑Augmented Generation）全栈实战指南，提供从数据检索、上下文构建到生成的完整工作流示例，并配有在线文档（https://datawhalechina.github.io/all-in-rag/）。  

**价值**  
- **统一 Prompt 与工具**：将零散的 Prompt、检索库、工具调用封装为可复用的 Agent 工作流，降低研发门槛。  
- **多 Agent 编排**：示例代码展示了如何在同一流水线中调度多个 Agent，实现复杂的查询、记忆、工具使用等场景。  
- **标准化记忆与工具管道**：提供了 Agent Memory、Tool‑Use、结果缓存等最佳实践，帮助团队快速落地可维护的 RAG 系统。  

**典型接入方式**  
1. **阅读官方文档**，选取对应的示例（如 `rag_pipeline_demo.py`）。  
2. **克隆仓库**并在本地或容器中安装依赖（`pip install -r requirements.txt`），确保 Python 3.9+ 环境。  
3. **替换关键配置**：  
   - 将向量数据库（FAISS、Milvus、ElasticSearch 等）凭证或本地路径改为自己的数据源。  
   - 将 LLM 接口（OpenAI、Claude、ChatGLM 等）改为企业内部模型或 API Key。  
   - 如需自定义工具（搜索、计算、数据库查询），在 `tools/` 目录实现 `BaseTool` 子类并在 `workflow.yaml` 中注册。  
4. **运行小规模 PoC**：使用示例数据集跑一次完整的检索‑生成链路，验证检索质量、响应时延和成本。  
5. **逐步扩展**：在 PoC 基础上加入多 Agent 编排、记忆持久化或业务专属工具，最终形成生产级 RAG 服务。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目仍在持续更新，拥有 7,244+ ★、3,562+ Fork，社区活跃，Issue 反馈快速。  
- **技术成熟度**：基于 Python 实现，使用主流向量库和 LLM 接口，代码结构清晰，配套 CI/CD。  
- **适配性**：支持多种向量数据库、LLM 提供商，易于在私有云或企业内部环境中部署。  
- **风险**：需自行审查许可证（MIT）与安全依赖（第三方库），并在生产前完成安全扫描和性能压测。  

综合来看，`datawhalechina/all-in-rag` 已具备高可用的 OSS 基础，适合作为 RAG 项目的快速原型平台，随后通过上述小规模 PoC‑>全链路集成的路径平滑迁移到生产环境。

## 🧭 Practical evaluation

**Value:** datawhalechina/all-in-rag helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7244 GitHub stars
- 3562 forks
- updated 2026-05-11
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 89/100 |
| stars | 82/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 73/100 |
| recency | 20/100 |
| adoption | 84/100 |
| production | 55/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/datawhalechina/all-in-rag) · [← Back to Orchestration](./README.md)</sub>
