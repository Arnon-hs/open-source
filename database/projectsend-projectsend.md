# projectsend/projectsend

[![Stars](https://img.shields.io/github/stars/projectsend/projectsend?style=flat-square&color=yellow)](https://github.com/projectsend/projectsend/stargazers) [![Forks](https://img.shields.io/github/forks/projectsend/projectsend?style=flat-square&color=blue)](https://github.com/projectsend/projectsend/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> ProjectSend is a free, open source software that lets you share files with your clients, focused on ease of use and privacy. It supports clients groups, system users roles, statistics, multiple languages, detailed logs... and much more!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 347 |
| 💻 **Language** | PHP |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`business-tools` `client-portal` `clients-oriented` `document-sharing` `file-management` `file-sharing` `file-upload` `free-software` `mysql` `open-source` `php` `projectsend`

## 🎯 Categories

Database · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ProjectSend is a free, open‑source file‑sharing platform designed for secure, client‑focused transfers. It offers granular user roles, client groups, usage statistics, multilingual support, detailed logging, and a host of other features, all packaged in a lightweight PHP application.

**Value**  
ProjectSend turns a scattered collection of client files into a searchable, permission‑controlled repository that can be indexed by AI assistants or knowledge‑base tools. By exposing a clear API/CLI and rich metadata (file tags, user roles, timestamps, logs), it enables downstream applications to retrieve, filter, and reason over documents, boosting the relevance and accuracy of AI‑driven answers.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Deploy** a Docker container or install the PHP package on a web server (LAMP stack). | Quick, reproducible setup; official Docker image is available. |
| 2️⃣  | **Configure** groups, roles, and storage locations to match your internal client hierarchy. | Aligns the permission model with existing business processes. |
| 3️⃣  | **Enable API/CLI** (ProjectSend’s built‑in REST endpoints or the `ps-cli` tool). | Provides programmatic access for indexing pipelines. |
| 4️⃣  | **Integrate** with a knowledge‑base indexer (e.g., Elastic, Typesense, or a vector store). Pull file metadata and content via the API, enrich with embeddings, and store alongside logs. | Turns the file store into a searchable knowledge graph for assistants. |
| 5️⃣  | **Secure** the installation (TLS, firewall, regular updates) and set up monitoring (logs, usage stats). | Guarantees privacy and compliance for client data. |
| 6️⃣  | **Pilot** the integrated system with a limited set of clients, evaluate search relevance and latency, then roll out organization‑wide. | Validates value before full production rollout. |

**Production Readiness**  
- **Activity & Adoption:** 1,919 ★, 347 forks, recent commits (as of 2026‑06‑23) and an active issue‑tracker indicate a healthy community.  
- **Maturity:** Core features (roles, groups, logging, multilingual UI) are stable; the PHP codebase is well‑documented and widely deployed.  
- **Observability:** Built‑in statistics and detailed logs make monitoring straightforward, and the API surface is sufficient for automated indexing.  
- **Risk Profile:** No immediate licensing or security red flags, though a final review of the GPL‑2.0 license compatibility and a security audit are recommended before enterprise use.  

Overall, ProjectSend is a production‑ready OSS candidate for organizations that need a secure, searchable client file hub that can be seamlessly integrated into AI‑augmented knowledge workflows.

### Русский

ProjectSend — бесплатное open‑source решение для безопасного обмена файлами с клиентами: позволяет создавать группы клиентов, управлять ролями пользователей, вести статистику и детальные логи, поддерживает множество языков и расширяется через API/CLI. Типичное внедрение — установка на собственный сервер, интеграция с существующей CRM/ERP для автоматической загрузки и предоставления клиентам нужных документов, а также индексация файлов для быстрого поиска. Проект имеет высокий уровень готовности к production: активные коммиты, более 1900 звёзд на GitHub, широкое сообщество и стабильный стек (PHP), что делает его надёжным кандидатом для пилотного и масштабного использования.

### 中文

**项目简介（2‑3 句话）**  
ProjectSend 是一款免费开源的文件共享系统，专为向客户安全、便捷地交付资料而设计。它提供客户端分组、用户角色、访问统计、多语言支持、详细日志等功能，兼顾易用性与隐私保护。

**价值**  
- **内部知识可检索**：把企业内部文档、合同、技术手册等统一上传到 ProjectSend，配合搜索或向量化索引后，AI 助手即可在对话中直接引用最新的原始文件，提升答复的准确性与可信度。  
- **安全合规**：细粒度的权限控制和完整的访问日志帮助企业满足合规审计需求，防止敏感文件泄露。  
- **多语言与统计**：内置多语言界面和使用统计，适合跨地区团队协作，同时可监控文件下载量、活跃用户等关键指标。

**典型接入方式**  
1. **API / Webhook**：ProjectSend 提供 REST‑ful API（或通过官方插件实现），可以在业务系统中实现文件上传、下载、权限管理等自动化操作。  
2. **CLI / SDK**：使用官方或社区提供的 PHP/Node.js/Python SDK（或直接调用 curl），在 CI/CD 流水线或脚本中批量同步文档。  
3. **数据库直连**：项目使用 MySQL/MariaDB 存储元数据，若需要深度集成（如自定义搜索索引），可以直接读取 `files`, `groups`, `users` 表进行二次加工。  
4. **前端嵌入**：通过 iframe 或自定义主题将 ProjectSend 界面嵌入内部门户，实现“一站式”文件中心。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目拥有 1919 ⭐、347 🍴，最近一次提交在 2026‑06‑23，表明仍在积极维护。  
- **技术成熟度**：核心使用 PHP + MySQL，技术栈成熟、部署成本低，且官方提供 Docker 镜像，便于在容器化环境中快速上线。  
- **安全性**：提供细粒度权限、完整审计日志，且社区对安全漏洞响应及时（可在 GitHub Security tab 查看历史 CVE）。  
- **可扩展性**：插件机制支持自定义身份验证（LDAP、OAuth）和文件存储后端（S3、Azure Blob），满足企业级扩展需求。  

综合来看，ProjectSend 已具备高可用、易集成、功能完整的特征，适合作为内部文档管理与 AI 助手知识库的可靠 OSS 基础设施。

## 🧭 Practical evaluation

**Value:** projectsend/projectsend helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1919 GitHub stars
- 347 forks
- updated 2026-06-23
- primary language: PHP
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 70/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 68/100 |
| production | 59/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/projectsend/projectsend) · [← Back to Database](./README.md)</sub>
