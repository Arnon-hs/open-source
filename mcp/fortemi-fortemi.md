# Fortemi/fortemi

[![Stars](https://img.shields.io/github/stars/Fortemi/fortemi?style=flat-square&color=yellow)](https://github.com/Fortemi/fortemi/stargazers) [![Forks](https://img.shields.io/github/forks/Fortemi/fortemi?style=flat-square&color=blue)](https://github.com/Fortemi/fortemi/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Self-hosted AI knowledge base with hybrid semantic search (pgvector + FTS + RRF), MCP server, multi-provider LLM inference (Ollama, OpenAI, OpenRouter, llama.cpp), multimodal ingestion (vision, audio transcription, speaker diarization), and knowledge graph. Rust + PostgreSQL.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Rust |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-07-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `embeddings` `hybrid-search` `knowledge-base` `knowledge-graph` `llm` `mcp-server` `model-context-protocol` `multimodal` `note-taking` `ollama` `pgvector`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Fortemi is a self‑hosted AI knowledge‑base platform built in Rust and PostgreSQL that combines hybrid semantic search (pgvector, full‑text search, and reciprocal rank fusion) with a multi‑client protocol (MCP) server for LLM inference from many providers (Ollama, OpenAI, OpenRouter, llama.cpp). It supports multimodal ingestion—vision, audio transcription, speaker diarization—and constructs a knowledge graph, enabling AI assistants to retrieve and act on real‑world data through a standard API/SDK/CLI interface.

**Value**  
- **Unified Retrieval Layer**: By fusing vector similarity, traditional FTS, and RRF, Fortemi delivers more accurate and context‑rich results than single‑method approaches, which is critical for Retrieval‑Augmented Generation (RAG) pipelines.  
- **Multi‑Provider LLM Backend**: The MCP server abstracts away the specifics of different LLM providers, letting developers switch or combine models (local Ollama, cloud OpenAI, etc.) without code changes.  
- **Multimodal Knowledge Ingestion**: Automatic processing of images, audio, and speaker diarization expands the knowledge base beyond text, making it suitable for enterprises with diverse data assets.  
- **Standardized Integration**: The exposed API/SDK/CLI follows a clear protocol, simplifying the connection of AI agents, tool‑calling frameworks, or custom Model Context Protocol (MCP) servers.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided Docker compose (or compile locally) and point the PostgreSQL instance to a test dataset. Verify ingestion pipelines (e.g., `fortemi ingest --type image path/…`) and query performance using the REST/CLI endpoints.  
2. **Pilot Integration** – Replace an existing RAG component in a prototype with Fortemi’s `/search` endpoint, configuring the MCP server to use the preferred LLM provider. Use the SDK to embed calls in your agent code.  
3. **Scaling & Customization** – Tune pgvector dimensions, adjust FTS weights, or add custom ranking functions. Deploy the MCP server behind a load balancer, enable TLS, and configure role‑based access in PostgreSQL.  
4. **Production Hardening** – Add monitoring (Prometheus metrics exposed by the server), set up regular backups of the PostgreSQL DB, and run security scans on the container images.  

**Production Readiness**  
Fortemi is at a **medium** readiness level. It is functional for prototypes and internal workflows, with a clean Rust codebase and recent updates (last commit 2026‑07‑13). However, before production use you should:  

- Conduct a thorough security audit (dependency vulnerability check, container hardening).  
- Verify the licensing terms and ensure they align with your organization’s policies.  
- Establish a maintenance plan (e.g., pinning Rust/PG versions, monitoring upstream changes to Ollama/OpenAI APIs).  

With these steps, Fortemi can become a reliable backbone for AI‑augmented applications that need robust, multimodal knowledge retrieval and flexible LLM integration.

### Русский

Fortemi — это self‑hosted платформа на Rust и PostgreSQL, предоставляющая гибридный семантический поиск (pgvector + FTS + RRF), MCP‑сервер и возможность инференса LLM от разных провайдеров (Ollama, OpenAI, OpenRouter, llama.cpp), а также мультимодальную загрузку данных (изображения, аудио, диаризация) и граф знаний. Она позволяет быстро подключать AI‑ассистентов к реальным инструментам и данным через единый протокол, что удобно для прототипов и внутренних workflow, а также для развертывания Model Context Protocol серверов. Готовность к production средняя: проект достаточно стабилен для пилотных внедрений, но требует проверки лицензии, безопасности и поддержки перед масштабным использованием.

### 中文

**项目简介**  
Fortemi（仓库 Fortemi/fortemi）是一款基于 Rust 与 PostgreSQL 的自托管 AI 知识库。它通过 pgvector、全文检索（FTS）以及 Reciprocal Rank Fusion（RRF）实现混合语义搜索，内置 MCP（Model Context Protocol）服务器，支持 Ollama、OpenAI、OpenRouter、llama.cpp 等多供应商 LLM 推理，并提供视觉、音频转写、说话人分离等多模态数据接入以及知识图谱功能。

---

### 价值点
1. **统一的 AI 与工具桥梁**：通过标准化的 MCP 接口，AI 助手可以直接调用企业内部工具、数据库或外部 API，实现“AI‑to‑Tool”的闭环。  
2. **高效检索 + 多模态**：结合向量搜索、全文检索和 RRF，既能处理自然语言查询，又能快速定位结构化或多媒体信息。  
3 **灵活的模型后端**：不锁定单一 LLM，开发者可根据成本、隐私或性能需求自由切换 Ollama、OpenAI、OpenRouter、llama.cpp 等后端。  
4. **可扩展的知识图谱**：内置图谱层，适合构建业务概念、实体关系等复杂语义网络，提升 RAG（Retrieval‑Augmented Generation）质量。  

---

### 典型接入方式
| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **AI Agent 调用企业工具** | **MCP Server (HTTP/JSON)** | 1. 在 Fortemi 中配置业务工具的 API（如 CRM、ERP）<br>2. 启动 MCP 服务<br>3. 在 LLM Prompt 中使用 `model_context` 调用（示例：`{{mcp:tool_name:action}}`） |
| **构建自定义 RAG 流程** | **REST API / SDK / CLI** | 1. 使用 SDK 将文档、图片、音频等上传至 Fortemi（自动进行向量化、FTS 与知识图谱抽取）<br>2. 调用 `/search` 接口获取混合检索结果<br>3. 将结果喂给 LLM 进行生成 |
| **部署模型推理服务** | **Model Provider Adapter** | 1. 在 `config.toml` 中声明使用的模型提供商及凭证<br>2. Fortemi 会在需要时自动路由请求到对应后端（如 Ollama 本地模型或 OpenAI 云模型） |
| **内部原型或工作流自动化** | **CLI + Docker Compose** | 1. `docker compose up -d` 启动 Rust 服务 + PostgreSQL<br>2. 通过 CLI (`fortemi ingest`, `fortemi query`) 快速验证功能 |

---

### 生产可用性评估
| 维度 | 现状 | 备注 |
|------|------|------|
| **成熟度** | 中等（MVP + 功能完整） | 已支持核心功能，适合原型、内部工具或受控生产环境。 |
| **维护活跃度** | 最近一次提交 2026‑07‑13，22 Stars、3 Forks | 项目活跃度一般，建议自行审计代码并关注后续更新。 |
| **依赖风险** | Rust + PostgreSQL + pgvector，依赖库成熟 | 需要自行管理 PostgreSQL 备份、容器安全与模型许可证。 |
| **安全/合规** | 未发现重大元数据泄露风险，仍需检查许可证（MIT/Apache 等）以及模型提供商的使用条款。 |
| **部署复杂度** | 中等 | 推荐使用官方 Docker Compose，或在 Kubernetes 中通过 Helm Chart 部署。 |
| **适用场景** | - 企业内部知识库 / 文档检索<br>- 多模态客服机器人<br>- AI‑to‑Tool 自动化平台 | 对外部高并发或严格 SLA 场景，需要额外的水平扩展与监控方案。 |

**结论**：Fortemi 为希望在自有基础设施上快速搭建 AI‑增强知识检索与工具调用能力的团队提供了“一站式”解决方案。对原型开发和受控生产环境已具备可用性，但在大规模生产部署前，建议完成安全审计、容灾设计以及对模型供应商的合规检查。

## 🧭 Practical evaluation

**Value:** Fortemi/fortemi helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 3 forks
- updated 2026-07-13
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 66/100 |
| recency | 100/100 |
| adoption | 25/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/Fortemi/fortemi) · [← Back to Mcp](./README.md)</sub>
