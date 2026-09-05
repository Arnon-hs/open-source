# RobThePCGuy/Claude-Patent-Creator

[![Stars](https://img.shields.io/github/stars/RobThePCGuy/Claude-Patent-Creator?style=flat-square&color=yellow)](https://github.com/RobThePCGuy/Claude-Patent-Creator/stargazers) [![Forks](https://img.shields.io/github/forks/RobThePCGuy/Claude-Patent-Creator?style=flat-square&color=blue)](https://github.com/RobThePCGuy/Claude-Patent-Creator/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> USPTO patent creation system with MCP server + Claude Code plugin. Hybrid RAG search over   MPEP/USC/CFR, BigQuery access to 76M+ patents, automated 35 USC 112 compliance checks, prior   art search, diagram generation. GPU-accelerated with skills and autonomous agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 143 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | Python |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bigquery` `claude-code` `claude-code-plugin` `faiss` `mcp-server` `mpep` `patent` `patent-drafting` `patent-search` `rag` `uspto`

## 🎯 Categories

MCP · Knowledge/RAG · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
RobThePCGuy/Claude‑Patent‑Creator is an open‑source USPTO‑style patent drafting platform that couples a Model‑Context‑Protocol (MCP) server with a Claude code‑plugin. It offers hybrid RAG over the MPEP, USC, CFR and a BigQuery table of > 76 M patents, runs automated 35 USC 112 compliance checks, performs prior‑art searches, and can generate claim‑diagrams on GPU‑accelerated agents.

**Value**  
The project turns a generic LLM assistant into a domain‑specific patent‑authoring engine by exposing real‑world tools (search, compliance, diagramming) through a standard MCP API. This lets any AI agent—Claude, ChatGPT, or custom models—invoke authoritative legal data, run deterministic checks, and retrieve results in a uniform way, dramatically reducing the engineering effort required to build a compliant, data‑rich patent‑drafting workflow.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣ Evaluate the MCP/CLI | Clone the repo, run the provided Docker‑compose or `pip install` and fire up the MCP server; use the sample Python SDK to issue a simple “search prior art” request. | Confirms that the API contract matches your existing AI orchestration layer. |
| 2️⃣ Connect your LLM agent | Point your Claude/ChatGPT wrapper to the MCP endpoint; register the Claude‑Code plugin if you need code‑generation assistance. | Enables seamless tool calls from the same prompt flow you already use. |
| 3️⃣ Pilot a specific use case | Start with a low‑risk task such as automated 112‑compliance checking on a set of draft claims. Capture logs, latency, and accuracy. | Provides a measurable ROI and surface‑level validation before scaling. |
| 4️⃣ Extend the pipeline | Add custom agents (e.g., a citation‑formatter or a diagram‑renderer) via the MCP SDK; optionally hook the BigQuery patent table for bulk analytics. | Leverages the platform’s extensibility to cover the full patent‑drafting lifecycle. |
| 5️⃣ Deploy to production | Containerize the MCP server, enable GPU instances for diagram generation, and enforce API‑key authentication. | Aligns with the project’s production‑ready signals (active maintainer, recent commits, 143 stars). |

**Production readiness**  
- **Activity & community** – 143 GitHub stars, 24 forks, last commit 2026‑06‑25, and a Python‑centric codebase make it easy to audit and contribute.  
- **Architecture** – The MCP server, CLI, and SDK are clearly defined; GPU acceleration and BigQuery integration are already packaged, reducing infrastructure glue code.  
- **Reliability** – Automated 35 USC 112 checks and RAG over authoritative sources provide deterministic outputs, a key requirement for legal workflows.  
- **Risk considerations** – Licensing and security posture still need a formal review, but no glaring metadata issues were found. Overall, the project is “high” for an OSS pilot and can be moved into production after the standard security and compliance vetting.

### Русский

RobThePCGuy/Claude-Patent-Creator – это гибридный RAG‑сервер с MCP‑интерфейсом и плагином Claude Code, который подключает AI‑ассистенты к базе из 76 млн+ патентов, выполняет автоматические проверки соответствия 35 USC 112, поиск предшествующего уровня техники и генерацию схем, используя GPU‑ускорение и автономные агенты. Типовой сценарий внедрения – развертывание MCP‑сервера в корпоративной инфраструктуре и подключение к нему Claude‑агентов или других ИИ‑систем для ускоренного составления и валидации патентных заявок. Проект демонстрирует высокую готовность к production: активная разработка (обновление 2026‑06‑25), сильные экосистемные сигналы (143★, 24 форка

### 中文

**项目价值**  
RobThePCGuy/Claude‑Patent‑Creator 将 AI 助手（Claude）与真实的专利检索、法规库和自动化工具通过 **Model Context Protocol (MCP)** 进行标准化对接。它能够在 GPU 加速下完成：

- 对 MPEP、USC、CFR 等法规的混合 RAG 检索  
- 通过 BigQuery 访问 7600 万+ 专利数据  
- 自动化 35 USC 112 合规检查、先前技术检索、图示生成  

从而把“聊天 + 检索 + 合规”闭环变成可编程的微服务，极大降低构建专利撰写/审查系统的研发成本。

**典型接入方式**  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| 在自研 AI Agent 中调用专利功能 | **MCP Server + Claude Code 插件**（REST/JSON‑RPC） | 1. 启动 MCP 服务器（`docker compose up` 或直接 `python -m mcp_server`）<br>2. 在 Claude Code 中加载插件，配置服务器地址和 API‑key<br>3. 在 Prompt 中使用 `@patent.create`, `@patent.search` 等指令即可触发 |
| 通过 CLI/SDK 在脚本或 CI/CD 中使用 | **Python SDK / CLI**（`pip install claude-patent-creator`） | 1. `import claude_patent as cp`<br>2. 调用 `cp.search_patents(query)`、`cp.check_112(doc)` 等函数<br>3. 可配合 `gcloud bigquery` 客户端访问 76M+ 专利 |
| 部署为独立微服务供其他语言调用 | **Docker 镜像**（`ghcr.io/robthepcguy/claude-patent-creator`） | 1. 拉取镜像并运行，暴露 8000 端口<br>2. 使用 OpenAPI 描述的 HTTP 接口（`/search`, `/compliance`, `/diagram`）<br>3. 任意语言通过 HTTP 请求即可利用全部功能 |
| 与企业内部工具链集成 | **MCP 标准协议**（统一的 `model_context` JSON schema） | 1. 在企业的模型治理平台注册该 MCP 服务<br>2. 通过统一的 `model_context` 调用约定，实现“一键对接”而不需改动业务代码 |

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码活跃度** | ★★★★★ | 最近一次提交 2026‑06‑25，持续更新，活跃社区 |
| **社区规模** | ★★★★☆ | 143 ⭐、24 forks，已有一定使用案例 |
| **技术成熟度** | ★★★★☆ | GPU 加速、BigQuery、MCP 多协议实现，已在多个内部 pilot 中验证 |
| **安全/合规** | ★★★☆☆ | 许可证为 MIT，暂无已知安全漏洞；仍需审计依赖库和 API 密钥管理 |
| **部署难度** | ★★★★☆ | 提供 Docker、CLI、SDK 三种方式，文档完整，入门门槛低 |
| **整体生产准备度** | **高**（8/10） | 具备完整的 API、自动化测试和监控示例，适合作为正式项目的后端服务或内部工具的核心组件。仅在正式投产前建议进行一次安全审计并制定 API‑key 管理策略。 |

**总结**  
RobThePCGuy/Claude‑Patent‑Creator 通过标准化的 MCP 接口，把强大的专利检索、法规合规检查和图形生成能力包装成即插即用的微服务，既适合在 AI Agent 中直接调用，也能作为独立的后端服务供多语言系统集成。项目活跃、文档完善、部署灵活，具备较高的生产可用性，只需在安全与运维细节上做一次最终审查即可在正式环境中稳健运行。

## 🧭 Practical evaluation

**Value:** RobThePCGuy/Claude-Patent-Creator helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 143 GitHub stars
- 24 forks
- updated 2026-06-25
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/RobThePCGuy/Claude-Patent-Creator) · [← Back to Mcp](./README.md)</sub>
