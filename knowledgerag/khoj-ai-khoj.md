# khoj-ai/khoj

[![Stars](https://img.shields.io/github/stars/khoj-ai/khoj?style=flat-square&color=yellow)](https://github.com/khoj-ai/khoj/stargazers) [![Forks](https://img.shields.io/github/forks/khoj-ai/khoj?style=flat-square&color=blue)](https://github.com/khoj-ai/khoj/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-83%2F100-brightgreen?style=flat-square)](#)

> Your AI second brain. Self-hostable. Get answers from the web or your docs. Build custom agents, schedule automations, do deep research. Turn any online or local LLM into your personal, autonomous AI (gpt, claude, gemini, llama, qwen, mistral). Get started - free.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35.3k |
| 🍴 **Forks** | 2.3k |
| 💻 **Language** | Python |
| 📈 **Score** | 83/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai` `assistant` `chat` `chatgpt` `emacs` `image-generation` `llama3` `llamacpp` `llm` `obsidian` `obsidian-md`

## 🎯 Categories

Knowledge/RAG · Automation · AI/ML · Communication · Productivity

## 📝 Summary

### English

**Brief summary**  
Khoj (khoj‑ai/khoj) is an open‑source “AI second brain” that lets you self‑host a searchable knowledge base powered by any LLM (GPT, Claude, Gemini, LLaMA, Qwen, Mistral, etc.). It indexes web content and private documents, exposes a RAG‑enabled chat/agent interface, and supports automation and scheduling for deep research or workflow tasks.  

**Value**  
- Turns fragmented internal docs, code repos, and web resources into a single, LLM‑augmented knowledge store that assistants can query accurately.  
- Enables custom agents and scheduled automations, so teams can automate repetitive research, report generation, or ticket triage without leaving their own infrastructure.  
- Supports any LLM backend, giving flexibility to use open‑source models for cost or privacy reasons while still getting the same conversational experience.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the Docker compose setup, and point Khoj at a small pilot knowledge source (e.g., a Confluence space or a local markdown folder). Verify that queries return relevant, source‑cited answers.  
2. **Integration** – Extend the indexing pipeline to ingest your production data stores (SharePoint, Git, S3, etc.) using the provided Python SDK or webhooks. Hook the chat UI or API into existing internal tools (Slack, Teams, ticketing systems).  
3. **Automation** – Define scheduled agents (e.g., nightly research digests) via the built‑in scheduler or external cron jobs, and test end‑to‑end flows.  
4. **Scaling** – Deploy the chosen LLM backend (self‑hosted Llama‑3, Mistral, or a hosted API) behind a load‑balanced service, enable caching, and configure RBAC for multi‑tenant access.  

**Production readiness**  
- **Activity & community**: 35 k+ stars, 2 k+ forks, frequent commits (latest update 2026‑06‑24) and active issue discussions indicate a healthy, maintained project.  
- **Architecture**: Python core, containerized deployment, and clear REST/GraphQL APIs make it easy to embed in existing CI/CD pipelines.  
- **Scalability**: Supports both cloud‑hosted and on‑prem LLMs; can be horizontally scaled via Docker/K8s.  
- **Risks**: License and security posture still need a final legal review, and you’ll want to audit any custom connectors for data leakage. Overall, the project is mature enough for a serious pilot in production environments.

### Русский

**khoj-ai/khoj** — это открытая платформа «второго мозга» на базе LLM, позволяющая быстро индексировать и делать доступными внутренние документы, веб‑источники и любые другие данные, а затем отвечать на запросы через чат‑бота, кастомные агенты или автоматические сценарии. Типичный пилотный сценарий — подключить khoj к корпоративному хранилищу знаний (Confluence, SharePoint, локальные файлы), построить RAG‑индекс и протестировать поиск‑по‑контексту в небольшом проекте, после чего масштабировать на всю организацию. Проект считается почти готовым к продакшн: активные коммиты, более 35 тыс. звёзд, регулярные релизы и поддержка популярных LLM (GPT, Claude, Gemini, LLaMA и др.), однако перед полномасштабным внедрением рекомендуется проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**价值**  
khoj‑ai/khoj 将内部文档、网页、代码库等知识资产统一索引，并通过可自托管的 LLM（GPT、Claude、Gemini、Llama、Qwen、Mistral 等）提供自然语言检索和自动化响应。它可以把散落的知识转化为可直接对话的“第二大脑”，帮助团队快速定位信息、提升客服/助理的准确性、实现基于文档的自动化工作流。

**典型接入方式**  
1. **快速 POC**：克隆仓库 → 按 README 配置 Docker‑Compose（或直接使用 `docker compose up`），提供 `config.yaml` 指定要索引的本地目录或公开 URL。  
2. **文档索引**：运行 `khoj index`，支持 Markdown、PDF、HTML、Word 等常见格式，生成向量索引并存入内置的 SQLite/PG 向量库。  
3. **LLM 接入**：在 `config.yaml` 中配置所需的模型 API（OpenAI、Anthropic、Google、Open‑Source）或本地部署的模型服务（vLLM、Ollama），即可让 Khoj 调用对应模型进行检索增强生成（RAG）。  
4. **自定义 Agent / 自动化**：通过 `khoj agents` 定义触发条件（cron、Webhook、文件变更），让系统在特定时间或事件发生时自动执行搜索、摘要、报告生成等任务。  
5. **前端集成**：项目自带 React 前端，可直接嵌入到内部门户；也可以通过 REST API (`/api/query`) 与已有聊天机器人或内部工具对接。

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，仓库拥有 35 281 星、2 265 Fork，最近提交在数天前，说明社区和维护者仍在积极迭代。  
- **技术成熟度**：核心使用 Python + FastAPI，向量存储支持 SQLite、PostgreSQL + pgvector，兼容主流向量数据库（FAISS、Milvus），易于横向扩展。  
- **部署可靠性**：提供官方 Docker‑Compose 与 Helm Chart，支持 Kubernetes 原生部署，具备健康检查、日志、监控（Prometheus）等生产特性。  
- **安全与合规**：代码开源，可自行审计；支持在私有网络内完全离线运行，满足内部敏感数据隔离要求。  
- **风险**：仍需对所选模型的许可证与费用、容器镜像的安全扫描以及长期维护者的可用性进行二次确认。

综上，khoj‑ai/khoj 在 **知识检索 + 自动化 RAG** 场景下具备高可用、易集成、可自托管的特性，适合作为内部知识库搜索和 AI 助手的生产级底层平台。建议先在单机 Docker 环境完成一次完整的索引‑查询‑自动化流程验证（Proof‑of‑Concept），确认业务匹配后再迁移到 Kubernetes 并开启高可用部署。

## 🧭 Practical evaluation

**Value:** khoj-ai/khoj helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 35281 GitHub stars
- 2265 forks
- updated 2026-06-24
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 84/100 |
| stars | 97/100 |
| topics | 100/100 |
| outlook | 91/100 |
| quality | 92/100 |
| recency | 80/100 |
| adoption | 93/100 |
| production | 76/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/khoj-ai/khoj) · [← Back to Knowledgerag](./README.md)</sub>
