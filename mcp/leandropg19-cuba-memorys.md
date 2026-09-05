# LeandroPG19/cuba-memorys

[![Stars](https://img.shields.io/github/stars/LeandroPG19/cuba-memorys?style=flat-square&color=yellow)](https://github.com/LeandroPG19/cuba-memorys/stargazers) [![Forks](https://img.shields.io/github/forks/LeandroPG19/cuba-memorys?style=flat-square&color=blue)](https://github.com/LeandroPG19/cuba-memorys/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Persistent memory MCP server for AI agents — Rust, 19 tools, knowledge graph, Hebbian learning, episodic memory, contradiction detection, prospective triggers, Bayesian calibration, zero-config Docker setup.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 26 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Rust |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-memory` `ai-tools` `anti-hallucination` `episodic-memory` `exponential-decay` `graph-database` `graphrag` `hebbian-learning` `knowledge-graph` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief summary**  
LeandroPG19 / cuba‑memorys is a Rust‑based persistent‑memory MCP (Model Context Protocol) server that equips AI agents with a rich episodic knowledge graph, Hebbian learning, contradiction detection, prospective triggers, and Bayesian calibration. It ships as a zero‑config Docker image and bundles 19 ready‑to‑use tools for connecting agents to external data and services.

**Value proposition**  
The project gives developers a drop‑in back‑end that turns raw tool outputs into a structured, self‑updating memory store, enabling agents to reason over past interactions, detect inconsistencies, and generate context‑aware prompts. By exposing a standard MCP API (plus an SDK and CLI), it removes the need to hand‑craft bespoke memory layers, accelerating the creation of “tool‑aware” assistants and simplifying the rollout of Model Context Protocol servers.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣ Clone / pull the Docker image | `docker run leandropg19/cuba-memorys` | Immediate, zero‑config sandbox for evaluation. |
| 2️⃣ Connect a prototype agent | Point the agent’s MCP client to `http://localhost:…` and use the provided SDK (Rust/Python bindings) to store/retrieve memories. | Validates API compatibility and data flow. |
| 3️⃣ Extend with custom tools | Register additional tool‑handlers via the MCP `register_tool` endpoint or the CLI. | Demonstrates the “19 tools” extensibility and integrates domain‑specific services. |
| 4️⃣ Tune learning & calibration | Adjust Hebbian learning rates, Bayesian priors, and trigger thresholds via the REST config endpoint. | Aligns the memory behavior with the target use case (e.g., customer support vs. research). |
| 5️⃣ Harden for production | Add TLS termination, persistent volume mounts, and monitoring (Prometheus exporter is built‑in). | Meets security, observability, and durability requirements. |

**Production readiness**  
- **Maturity:** Medium – the codebase is functional and actively updated (last commit 2026‑07‑13) with a clean Docker deployment, making it suitable for prototypes and internal tools.  
- **Stability signals:** 26 stars, 3 forks, and a modest but focused Rust community; the API surface is stable, but the project lacks a formal CI/CD pipeline and extensive integration tests.  
- **Operational considerations:** Verify the open‑source license, perform a security audit of the Docker image, and pin dependency versions (Rust crates) before using it in a production environment. With those checks, the server can be promoted to production for workloads where occasional memory drift is acceptable (e.g., research assistants, internal chatbots).  

In short, cuba‑memorys offers a ready‑made, extensible memory layer for AI agents, with a straightforward Docker‑first onboarding path; after a brief security and dependency review, it can move from prototype to production for many internal‑facing AI services.

### Русский

Резюме:

Проект LeandroPG19/cuba-memorys представляет собой сервер MCP для агентов AI, который обеспечивает постоянную память и позволяет соединять AI-ассистентов с реальными инструментами и данными через стандартный протокол. Он идеален для типового сценария внедрения, когда необходимо подключить AI-агента к инструментам или интегрировать Model Context Protocol серверы. Проект готов к использованию в прототипах или внутренних рабочих процессах, но требует проверки зависимостей и поддержки перед выпуском в производство.

### 中文

**项目简介（2‑3 句）**  
LeandroPG19/cuba‑memorys 是一款基于 Rust 实现的持久化记忆 MCP（Model Context Protocol）服务器，内置 19 种工具、知识图谱、Hebbian 学习、情景记忆、矛盾检测、前瞻触发与贝叶斯校准等功能，并提供零配置 Docker 镜像，帮助 AI 代理快速接入真实工具和数据。

**价值**  
- **统一协议**：通过标准化的 MCP 接口，让不同的 AI 助手能够以统一方式调用外部工具、查询知识图谱或写入记忆，实现“工具即服务”。  
- **强化记忆与推理**：内置 Hebbian 学习、情景记忆和矛盾检测，使代理能够在交互过程中持续积累、校正并利用经验，提高响应的一致性和可靠性。  
- **易部署**：提供即开即用的 Docker 镜像，免除复杂环境配置，适合快速原型验证和内部实验。

**典型接入方式**  
1. **Docker 部署**：`docker run -p 8080:8080 ghcr.io/leandropg19/cuba-memorys:latest`，即可启动 MCP 服务器。  
2. **API/SDK 调用**：服务器暴露 HTTP/JSON（或 gRPC）接口，AI 代理只需在对话流中发送符合 MCP 规范的请求即可调用工具、写入/读取记忆。  
3. **CLI/插件**：项目自带 CLI，可在本地或 CI 环境中直接执行记忆查询或工具触发，亦可作为自定义插件嵌入现有后端服务。  

**生产可用性**  
- **成熟度**：当前评分 74/100，适合作为原型或内部工作流的核心组件。  
- **依赖与维护**：Rust 生态相对稳定，项目已有 26 星、3 分叉，最近一次提交为 2026‑07‑13，活跃度尚可。上线前建议审查依赖的安全报告并制定更新策略。  
- **可扩展性**：通过插件机制可自行添加新工具或扩展知识图谱，支持水平扩容的 Docker 部署。  
- **风险**：需进一步确认许可证兼容性、长期维护者计划以及安全加固（如 API 鉴权、容器安全基线）后方可在面向外部用户的生产环境中使用。  

综上，cuba‑memorys 为 AI 代理提供了“一站式”记忆与工具接入层，适合快速验证概念或在受控的生产环境中实现标准化的模型上下文交互。

## 🧭 Practical evaluation

**Value:** LeandroPG19/cuba-memorys helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 26 GitHub stars
- 3 forks
- updated 2026-07-13
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 67/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/LeandroPG19/cuba-memorys) · [← Back to Mcp](./README.md)</sub>
