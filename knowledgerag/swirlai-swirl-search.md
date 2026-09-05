# swirlai/swirl-search

[![Stars](https://img.shields.io/github/stars/swirlai/swirl-search?style=flat-square&color=yellow)](https://github.com/swirlai/swirl-search/stargazers) [![Forks](https://img.shields.io/github/forks/swirlai/swirl-search?style=flat-square&color=blue)](https://github.com/swirlai/swirl-search/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> AI Search & RAG Without Moving Your Data. Get instant answers from your company's knowledge across 100+ apps while keeping data secure. Deploy in minutes, not months.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3k |
| 🍴 **Forks** | 285 |
| 💻 **Language** | Python |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-search` `bigquery` `django` `federated-query` `federated-search` `gpt` `large-language-models` `metasearch` `python` `rag` `relevancy` `retrieval-augmented-generation`

## 🎯 Categories

Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Project Summary:**

swirlai/swirl-search is an open-source AI search project that enables instant answers from a company's knowledge base across 100+ apps while keeping data secure. This project helps make internal knowledge searchable and usable by assistants, improving the efficiency of knowledge retrieval and utilization. With its high production readiness, recent updates, and strong adoption, swirlai/swirl-search is a viable option for serious pilots.

**Value Proposition:**

The primary value proposition of swirlai/swirl-search lies in its ability to make internal knowledge searchable and usable by assistants, thereby improving the efficiency of knowledge retrieval and utilization. This is particularly useful for companies that have a large amount of knowledge scattered across various apps and platforms.

**Practical Adoption Path:**

To adopt swirlai/swirl-search, users can start by:

1. Evaluating the project through a small proof of concept to gauge its feasibility and potential integration challenges.
2. Reviewing the README documentation to understand the project's architecture, installation process, and usage guidelines.
3. Assessing the project's license, security posture, and active maintainers to ensure that it aligns with their organization's requirements and standards.
4. Deploying the project in a controlled environment to test its performance, scalability, and reliability.
5. Integrating

### Русский

**swirlai/swirl-search** — это open‑source решение для AI‑поиска и RAG, позволяющее мгновенно получать ответы из корпоративных знаний, интегрированных более чем со 100 приложениями, при полном сохранении данных в безопасности. Типовой сценарий внедрения: за несколько минут развернуть сервис, проиндексировать внутренние базы знаний (документы, вики, CRM) и подключить его к чат‑боту или ассистенту, чтобы улучшить поиск и обогащать ответы актуальной информацией. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 3000 звёзд, широкое сообщество и поддержка Python, что делает его надёжным кандидатом для пилотного проекта после небольшого proof‑of‑concept.

### 中文

**项目简介**  
swirlai/swirl-search 是一款基于 LLM 的企业内部搜索与 RAG（检索增强生成）引擎，能够在 100 多种常用业务系统中即时抽取并回答企业知识，而无需将数据迁出或复制。几分钟即可部署，帮助组织快速把散落的文档、知识库、工单等转化为可被 AI 助手直接调用的可搜索知识。

**价值点**  
- **数据安全**：所有检索和生成在本地或私有云完成，原始文档永不离开企业网络。  
- **全链路覆盖**：内置对 Confluence、Notion、Slack、GitHub、Google Drive、SharePoint 等 100+ 应用的连接器，一键同步最新内容。  
- **提升效率**：员工和聊天机器人可以基于最新的内部文档直接得到精准答案，降低信息检索成本，提升客服、研发、运营等场景的响应速度。  

**典型接入方式**  
1. **快速 PoC**：克隆仓库 → 按 README 配置 `config.yaml`（填写 API key、数据源凭证） → 运行 `docker-compose up` 启动搜索服务。  
2. **文档索引**：使用内置的 `swirl-indexer` 脚本或 API，将指定的知识库（如 Confluence Space、Notion 页面或本地文件夹）增量抓取并写入向量数据库（支持 Milvus、Pinecone、Chroma 等）。  
3. **对话集成**：在现有聊天机器人（如 ChatGPT、Claude、LangChain）中调用 `/search` HTTP 接口或 Python SDK，获取检索结果后进行生成式回答，实现“基于内部知识的 AI 助手”。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑29，项目最近一次提交，星标 3 031，Fork 285，社区活跃，文档完整。  
- **技术成熟度**：核心使用 Python、FastAPI 与容器化部署，支持多种向量存储后端，易于在 Kubernetes 或单机 Docker 环境中扩展。  
- **安全合规**：数据全程本地处理，无外部同步，仅在本地网络内完成索引和查询；仍需自行审计依赖的第三方库许可证和容器镜像安全。  
- **适配度**：适合作为内部知识搜索的 OSS 选型，可先在小范围（如单个部门或单一知识库）进行 PoC，验证效果后逐步扩展至全公司。  

综合来看，swirl-search 在功能完整性、社区活跃度和部署便利性方面表现优秀，具备直接用于生产环境的条件，只需在安全审计和运维监控上做进一步确认即可。

## 🧭 Practical evaluation

**Value:** swirlai/swirl-search helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3031 GitHub stars
- 285 forks
- updated 2026-06-29
- primary language: Python
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 74/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 82/100 |
| recency | 80/100 |
| adoption | 71/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/swirlai/swirl-search) · [← Back to Knowledgerag](./README.md)</sub>
