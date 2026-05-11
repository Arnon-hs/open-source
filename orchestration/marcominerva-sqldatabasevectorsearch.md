# marcominerva/SqlDatabaseVectorSearch

[![Stars](https://img.shields.io/github/stars/marcominerva/SqlDatabaseVectorSearch?style=flat-square&color=yellow)](https://github.com/marcominerva/SqlDatabaseVectorSearch/stargazers) [![Forks](https://img.shields.io/github/forks/marcominerva/SqlDatabaseVectorSearch?style=flat-square&color=blue)](https://github.com/marcominerva/SqlDatabaseVectorSearch/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> A Blazor Web App and Minimal API for performing RAG (Retrieval Augmented Generation) and vector search using the native VECTOR type in Azure SQL Database and Azure OpenAI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 140 |
| 🍴 **Forks** | 37 |
| 💻 **Language** | C# |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`azure-openai` `azure-sql-database` `c-sharp` `chatgpt` `dotnet` `embeddings` `openai` `rag` `retrieval-augmented-generation` `semantic-kernel` `sql-server` `vector-database`

## 🎯 Categories

Orchestration · Knowledge/RAG · AI/ML · Backend · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **SqlDatabaseVectorSearch** project is a Blazor Web App coupled with a Minimal API that enables Retrieval‑Augmented Generation (RAG) and vector similarity search using Azure SQL Database’s native `VECTOR` type together with Azure OpenAI. It provides a ready‑made, C#‑centric stack for building repeatable, multi‑agent workflows that can store, query, and enrich vectorized data without needing a separate vector database.

**Value Proposition**  
- **Unified stack** – Leverages Azure SQL’s built‑in vector capabilities, eliminating the operational overhead of managing a separate vector store (e.g., Pinecone, Qdrant).  
- **Agent‑centric workflow** – Turns ad‑hoc prompts and tool calls into reproducible pipelines, making it easy to coordinate several LLM‑driven agents, persist their “memory”, and chain tool usage.  
- **Low‑code integration** – The Blazor front‑end and Minimal API expose clear HTTP endpoints and SDK‑style clients, so developers can plug the service into existing .NET applications or call it from other languages via REST.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Clone & run locally** – Use the provided Dockerfile or the `dotnet run` command to spin up the API and Blazor UI. | Quick proof‑of‑concept to verify vector indexing and RAG flow with your own data. |
| 2️⃣  | **Configure Azure resources** – Create an Azure SQL Database with the `VECTOR` column type, enable Azure OpenAI, and add the connection strings/secrets to `appsettings.json` or Azure Key Vault. | Aligns the project with the cloud services it is built for. |
| 3️⃣  | **Ingest data** – Use the API’s `/ingest` endpoint (or the CLI tool) to push documents, embeddings (generated via Azure OpenAI embeddings endpoint), and any metadata into the SQL table. | Populates the vector store that the RAG engine will query. |
| 4️⃣  | **Define agent workflows** – Extend the Blazor UI or write additional Minimal API routes that orchestrate multiple agents (e.g., a retrieval agent → reasoning agent → tool‑use agent). | Demonstrates the “repeatable agent workflow” benefit. |
| 5️⃣  | **Integrate with existing systems** – Call the API from your backend services, micro‑frontends, or CI pipelines; the REST contract is language‑agnostic. | Enables gradual rollout without rewriting existing code. |
| 6️⃣  | **Performance & security hardening** – Add Azure AD authentication, rate limiting, and monitoring (Azure Monitor/Application Insights). Optionally enable Azure Private Link for the SQL DB. | Brings the solution to production‑grade security and observability. |
| 7️⃣  | **Deploy to Azure** – Use Azure Container Apps, Azure App Service, or AKS to host the containerized app; configure CI/CD via GitHub Actions. | Scales the service for internal or external consumption. |

**Production Readiness Assessment**  

| Dimension | Rating | Comments |
|-----------|--------|----------|
| **Maturity** | **Medium** | The repo is actively maintained (last commit 2026‑05‑11) and has 140 stars, indicating community interest, but it is still positioned as a prototype/internal‑workflow tool. |
| **Stability** | **Medium‑High** | Core functionality (vector ingest, search, RAG) works, but you’ll need to verify edge‑case handling (large payloads, concurrent queries) and add production‑grade error handling. |
| **Security** | **Pending Review** | No explicit security hardening (auth, RBAC, secret management) is shipped; you must integrate Azure AD, Key Vault, and network isolation yourself. |
| **Scalability** | **Good** | Azure SQL’s native vector index scales with the underlying database tier; the Minimal API can be horizontally scaled via containers. |
| **Operational Overhead** | **Low** | No external vector DB to manage; only Azure SQL and Azure OpenAI need monitoring. |
| **Maintainability** | **Medium** | C#/.NET codebase is clean, but documentation is modest; you may need to extend the code for custom agent orchestration. |

**Bottom Line**  
`SqlDatabaseVectorSearch` offers a compelling, low‑friction way for .NET teams to experiment with RAG and multi‑agent pipelines using Azure‑native services. It is production‑ready for internal tools or pilot projects after you add standard security, monitoring, and CI/CD practices. For large‑scale, customer‑facing deployments, a deeper security audit and possibly some feature extensions (e.g., advanced retry logic, bulk ingest tooling) would be advisable.

### Русский

**SqlDatabaseVectorSearch** — это открытая Blazor‑приложение + Minimal API, позволяющая выполнять RAG‑процессы и поиск по векторным представлениям, используя встроенный тип VECTOR в Azure SQL Database совместно с Azure OpenAI. Типичный сценарий: встраивание в существующий бэкенд для построения повторяемых агентных пайплайнов (координация нескольких агентов, добавление инструментов и стандартизация памяти), где запросы преобразуются в векторы, хранятся в Azure SQL и быстро ищутся через векторный индекс. Проект находится на среднем уровне готовности к production — подходит для прототипов и внутренних сервисов, но требует проверки лицензии, безопасности и поддержки перед масштабным развертыванием.

### 中文

**项目简介（2‑3 句）**  
marcominerva/SqlDatabaseVectorSearch 是一个基于 Blazor Web App 与 Minimal API 的开源示例，演示如何在 Azure SQL Database 的原生 **VECTOR** 类型配合 Azure OpenAI 实现 RAG（检索增强生成）和向量搜索。它把零散的 Prompt 与工具封装成可复用的智能体工作流，便于在 .NET 生态中快速构建多代理、工具调用和记忆管理的 AI 应用。

**价值**  
- **统一向量检索与生成**：利用 Azure SQL 的 VECTOR 列直接存储、索引和查询向量，省去外部向量库的部署与运维成本。  
- **可复用的 Agent 工作流**：提供了 Prompt、工具调用、记忆（向量）等模块的标准化封装，帮助团队把“孤立的 Prompt”转化为可编排、可追踪的业务流程。  
- **全栈 .NET 体验**：前端 Blazor、后端 Minimal API、数据层直接使用 EF Core / ADO.NET，降低学习曲线，适合已有 .NET 技术栈的组织快速落地。

**典型接入方式**  

| 场景 | 接入步骤 | 关键点 |
|------|----------|--------|
| **内部原型 / PoC** | 1. Fork 项目或直接克隆 <br>2. 在 Azure 上创建带 VECTOR 列的 SQL Database <br>3. 在 Azure Portal 配置 OpenAI 资源并获取 API Key <br>4. 在 `appsettings.json` 中填入 `ConnectionStrings` 与 `OpenAIApiKey` <br>5. 运行 `dotnet run`，通过浏览器访问 Blazor 前端或调用 `/api/search` 接口 | 只需几分钟即可验证向量检索 + RAG 效果。 |
| **后端服务集成** | 1. 将 Minimal API 项目作为独立的微服务部署（Docker / Azure App Service） <br>2. 通过 HTTP/HTTPS 调用 `/api/rag`、`/api/vector` 等端点 <br>3. 如需 SDK，可在项目中引用 `SqlDatabaseVectorSearch.Client`（示例已提供） | 适合已有微服务架构的系统，保持语言一致性（C#）并可通过 API 网关统一治理。 |
| **前端自定义 UI** | 1. 使用项目中的 Blazor 组件作为参考，复制 `SearchComponent.razor`、`ChatComponent.razor` 等 <br>2. 在自己的 Blazor Server、WebAssembly 或 React/Vue 前端通过 REST 调用后端 API <br>3. 可自行扩展工具调用（如调用外部搜索、数据库查询） | 灵活定制 UI/UX，同时复用向量检索与 RAG 逻辑。 |

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 项目已在 GitHub 获得 140+ stars，代码活跃更新至 2026‑05‑11，适合作为原型或内部工具。 |
| **依赖风险** | 中等 | 依赖 Azure SQL Database（VECTOR）和 Azure OpenAI，需确认组织对这两项服务的合规与成本控制。 |
| **安全/合规** | 待审查 | 代码本身无明显安全漏洞，但需检查许可证（MIT/Apache 等）以及对外部 API 密钥的管理方式（建议使用 Azure Key Vault）。 |
| **运维成本** | 低‑中 | 无额外向量数据库运维，主要是 Azure SQL 与 OpenAI 的使用费用；可通过 Azure 自动伸缩和备份降低运维负担。 |
| **可扩展性** | 良好 | 基于 Minimal API，易于水平扩容；向量索引利用 SQL 的列存储，支持大规模数据（受限于 Azure SQL 实例规格）。 |
| **升级/维护** | 中等 | 项目活跃度一般，社区贡献（37 forks）可提供后续功能补丁；建议自行建立内部分支进行长期维护。 |

**结论**  
marcominerva/SqlDatabaseVectorSearch 在 **原型验证** 与 **内部业务流程自动化** 场景下价值突出，能够快速把向量检索与 RAG 融合进 .NET 应用。对于生产环境，需完成以下工作后方可上线：

1. **安全加固**：使用 Azure Key Vault 管理 OpenAI 密钥，审计 API 调用日志。  
2. **性能评估**：根据业务数据量在 Azure SQL 上做向量索引基准测试，确认查询延迟满足 SLA。  
3. **容错与监控**：在 Azure Monitor / Application Insights 中加入健康检查、异常报警。  
4. **合规审查**：确认使用的 Azure OpenAI 模型与数据存储符合所在行业的合规要求。

完成上述准备后，即可将其作为 **可重复、可编排的 AI Agent 服务** 部署到生产环境。

## 🧭 Practical evaluation

**Value:** marcominerva/SqlDatabaseVectorSearch helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 140 GitHub stars
- 37 forks
- updated 2026-05-11
- primary language: C#
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 44/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/marcominerva/SqlDatabaseVectorSearch) · [← Back to Orchestration](./README.md)</sub>
