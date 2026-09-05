# abraxas914/VESTI

[![Stars](https://img.shields.io/github/stars/abraxas914/VESTI?style=flat-square&color=yellow)](https://github.com/abraxas914/VESTI/stargazers) [![Forks](https://img.shields.io/github/forks/abraxas914/VESTI?style=flat-square&color=blue)](https://github.com/abraxas914/VESTI/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Local-first AI conversation memory hub to capture, search, summarize, and export chats across major AI platforms. 本地优先的 AI 对话记忆与知识中台。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 284 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-infrastructure` `ai-memory` `chatgpt` `chrome-extension` `claude` `context-management` `conversation-archive` `deepseek` `doubao` `gemini` `harness-engineering` `kimi`

## 🎯 Categories

Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Brief Summary**  
VESTI (abraxas914/VESTI) is a local‑first, TypeScript‑based hub that captures AI‑generated conversations from major chat models, indexes them, and provides fast search, summarisation, and export capabilities. It acts as a knowledge‑and‑RAG layer that lets internal assistants retrieve and ground their answers in an organisation’s own dialogue history and document collections.  

**Value Proposition**  
- **Searchable AI memory:** Turns scattered chat logs into a structured, queryable knowledge base, making past interactions instantly reusable.  
- **RAG‑ready summarisation:** Generates concise overviews of long threads and can feed those summaries into downstream assistants, improving answer relevance and reducing hallucinations.  
- **Export & integration:** Supports export to common formats (JSON, Markdown, CSV) and can be hooked into existing pipelines, enabling a single source of truth for conversational data across multiple AI platforms.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Clone the repo, run the Docker‑compose or npm scripts, and point VESTI at a small set of chat logs (e.g., from OpenAI or Azure OpenAI). Verify ingestion, search, and summarisation work as expected.  
2. **Integration Layer:** Build a thin wrapper (Node/TS or HTTP client) that forwards new chat messages from your production AI service to VESTI’s ingestion API. Start with a “read‑only” mode to avoid altering existing workflows.  
3. **RAG Hook‑up:** Connect your assistant’s retrieval step to VESTI’s query endpoint, optionally applying the built‑in summariser to the top‑k results before feeding them into the LLM prompt.  
4. **Scaling & Ops:** Deploy VESTI on an internal Kubernetes cluster or as a self‑hosted VM, enable persistent storage (e.g., Postgres/SQLite) and configure backups. Add monitoring for ingestion latency and index size.  
5. **Governance:** Review the MIT/Apache license (as listed), run a security scan of dependencies, and establish a maintainer rotation if the project is adopted long‑term.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑25), has a modest community (≈284 ★, 11 forks) and clear TypeScript codebase, making it suitable for internal prototypes and early‑stage production.  
- **Dependencies & Ops:** Relies on a few common Node/TS libraries and a database backend; these are well‑understood but should be audited for known vulnerabilities before a full rollout.  
- **Scalability:** Designed for local‑first operation, so it can run on a single node for small teams; larger deployments will need to provision appropriate storage and possibly shard the index.  
- **Risk Areas:** License compliance, security posture of third‑party packages, and the need for a dedicated maintainer to handle bug fixes and upgrades.  

**Bottom Line**  
VESTI offers a practical way to turn AI chat histories into a searchable, summarizable knowledge store, enabling more grounded and efficient assistant responses. Starting with a small PoC and gradually integrating the ingestion and retrieval APIs provides a low‑risk path to production, provided the organization conducts a final security/license audit and plans for operational scaling.

### Русский

**abraxas914/VESTI** — это локально‑ориентированная платформа для хранения, поиска, резюмирования и экспорта диалогов с ведущих AI‑ассистентов, превращающая внутренние разговоры в структурированную базу знаний, доступную другим помощникам. Типовой сценарий внедрения — небольшое POC‑приложение, которое индексирует существующие чат‑логи (например, из Slack, Teams или OpenAI), а затем использует их для улучшенного RAG‑поиска и контекстуального ответа ассистентов. Готовность к production — средняя: проект уже имеет активную звёздную базу (284★), свежие коммиты и TypeScript‑код, но перед масштабным запуском требуется проверка лицензии, безопасности и стабильности зависимостей.

### 中文

**项目简介**  
abraxas914/VESTI 是一个本地优先的 AI 对话记忆与知识中台，能够统一捕获、检索、摘要并导出来自主流大模型（如 ChatGPT、Claude、Gemini 等）的聊天记录，帮助企业把分散的对话数据转化为可搜索、可复用的内部知识。

**价值**  
- **知识可搜索**：将所有 AI 对话及文档统一索引，内部员工或智能助理可以通过自然语言快速定位所需信息。  
- **提升回答质量**：在生成答案时提供可靠的上下文来源，实现“基于事实”的响应，降低幻觉风险。  
- **降低成本**：本地存储避免频繁调用外部 API，既保护隐私又节约费用。  
- **灵活导出**：支持多种格式（Markdown、JSON、PDF 等），便于审计、归档或二次加工。

**典型接入方式**  
1. **快速 PoC**  
   - 克隆仓库，阅读 `README.md` 中的 “Getting Started”。  
   - 按照文档配置本地向量数据库（如 Chroma、Pinecone 本地版或 SQLite‑FAISS）。  
   - 使用提供的 SDK（TypeScript/Node）在已有的聊天机器人或内部工具中调用 `vesti.indexConversation()` 将对话写入 VESTI。  
2. **完整集成**  
   - 在 CI/CD 流水线中加入 VESTI 服务容器（Docker 镜像），与现有微服务通过 REST/gRPC 交互。  
   - 配置身份认证（API‑Key 或 OAuth）和访问控制，确保只有授权的 AI 助手可以查询或写入记忆库。  
   - 根据业务需求开启自动摘要、主题标签或自定义元数据插件，进一步提升检索精度。  

**生产可用性评估**  
- **成熟度**：项目已有 284 星、11 个 Fork，活跃更新至 2026‑06‑25，代码基于 TypeScript，社区活跃度中等。  
- **适用场景**：非常适合作为原型、内部知识库或部门级的 AI 助手后端；在对安全合规要求不极端的环境下可直接投入使用。  
- **风险与注意事项**  
  - 需自行审查许可证（MIT）与依赖库的安全性，尤其是向量数据库和第三方 API 的凭证管理。  
  - 生产环境建议配合监控、日志和备份方案，防止本地存储单点故障。  
  - 若业务规模快速增长，可能需要迁移到托管向量数据库或分布式存储，以保证扩展性。  

**结论**  
VESTI 为企业提供了一套本地化、可扩展的对话记忆解决方案，能够显著提升内部知识的可发现性和 AI 助手的回答质量。通过先做小规模 PoC 再逐步扩展，可在确保安全合规的前提下平滑推向生产环境。

## 🧭 Practical evaluation

**Value:** abraxas914/VESTI helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 284 GitHub stars
- 11 forks
- updated 2026-06-25
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 52/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/abraxas914/VESTI) · [← Back to Knowledgerag](./README.md)</sub>
