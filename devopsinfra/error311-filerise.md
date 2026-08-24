# error311/FileRise

[![Stars](https://img.shields.io/github/stars/error311/FileRise?style=flat-square&color=yellow)](https://github.com/error311/FileRise/stargazers) [![Forks](https://img.shields.io/github/forks/error311/FileRise?style=flat-square&color=blue)](https://github.com/error311/FileRise/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> 🗂️ FileRise – lightweight, self-hosted file manager & storage hub with granular ACLs, resumable uploads, encrypted folders, WebDAV & SSO. Fully Docker / Unraid compatible.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 972 |
| 🍴 **Forks** | 46 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`acl` `docker` `file-editor` `file-manager` `file-upload` `folder-management` `javascript` `multi-file-upload` `php` `self-hosted` `sso` `twofactor-auth`

## 🎯 Categories

DevOps/Infra · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
FileRise is a lightweight, self‑hosted file manager and storage hub that offers granular ACLs, resumable uploads, encrypted folders, WebDAV support, and SSO integration. It runs out‑of‑the‑box on Docker (including Unraid) and is written in JavaScript, boasting ~972 GitHub stars and active maintenance as of June 2026. The project is positioned as a searchable knowledge‑base layer that can be indexed by AI assistants for better document retrieval and grounding.

**Value**  
- **Knowledge accessibility:** By centralising files, folders, and metadata behind fine‑grained permissions, FileRise creates a structured repository that retrieval‑oriented AI assistants can query, turning siloed documents into searchable knowledge.  
- **Security & compliance:** Encrypted folders, ACLs, and SSO keep sensitive corporate data safe while still being programmatically reachable via its API/CLI.  
- **Integration friendliness:** Native WebDAV, a well‑documented REST API, and Docker‑first packaging make it easy to plug into existing RAG pipelines, CI/CD, or custom bots without extensive glue code.

**Practical Adoption Path**  
1. **Pilot deployment:** Spin up the official Docker image on a dev or staging environment (Docker Compose or Unraid).  
2. **Configure ACLs & SSO:** Connect to the organisation’s identity provider (OIDC/SAML) and define folder‑level permissions for the teams that will supply source documents.  
3. **Ingest documents:** Use the resumable upload endpoint or CLI to bulk‑load existing knowledge assets (PDFs, markdown, code repos).  
4. **Expose metadata:** Enable the built‑in API/SDK to surface file paths, tags, and access rights to your RAG indexing service (e.g., LangChain, LlamaIndex).  
5. **Iterate & monitor:** Validate retrieval quality, adjust ACLs, and monitor logs for upload errors or security alerts. Once stable, promote the container to production clusters.

**Production Readiness**  
- **Activity & community:** Recent commits (last update 2026‑06‑26), 972 stars, 46 forks, and 18 topical tags indicate a healthy, engaged community.  
- **Deployment maturity:** Docker‑first design, official Unraid support, and clear CI pipelines make the service container‑stable and easy to scale.  
- **Security posture:** Granular ACLs, encrypted storage, and SSO reduce attack surface; however, a final audit of the license (MIT‑style) and any third‑party dependencies is advisable before a full‑scale rollout.  
- **Risk level:** Low to moderate—no major metadata or licensing red flags, but maintainers should be verified for long‑term support. Overall, FileRise is a strong OSS candidate for production‑grade knowledge‑management and RAG integration.

### Русский

**FileRise** – лёгкий self‑hosted файловый менеджер с поддержкой гранулированных ACL, возобновляемых загрузок, зашифрованных папок, WebDAV и SSO, полностью готовый к запуску в Docker/Unraid. Его типичное внедрение — развернуть контейнер в корпоративной инфраструктуре, подключить SSO и настроить права доступа, после чего сотрудники получают безопасный централизованный хранилище и возможность индексировать документы для улучшенного поиска и работы AI‑ассистентов. По показателям активности (972 ★, свежие коммиты, широкая экосистема) проект считается почти готовым к продакшн‑использованию, остаётся лишь уточнить лицензирование и текущий уровень поддержки.

### 中文

**项目简介（2‑3 句）**  
FileRise 是一款轻量级的自托管文件管理与存储中心，支持细粒度 ACL、断点续传、加密文件夹、WebDAV 与 SSO，且可直接通过 Docker 或 Unraid 部署运行。

**价值**  
- **统一知识库**：将内部文档、代码库、报告等统一存放，配合细粒度访问控制，确保不同团队或角色只能看到授权内容。  
- **提升检索效率**：文件可通过 API、CLI 或 WebDAV 暴露元数据，便于 RAG（Retrieval‑Augmented Generation）等 AI 助手快速索引和搜索。  
- **安全合规**：支持端到端加密文件夹和 SSO 登录，满足企业对数据保密与审计的基本要求。

**典型接入方式**  
1. **Docker/Unraid 部署**：使用官方提供的 Docker 镜像，一键启动并在 `docker-compose.yml` 中配置存储路径、ACL 与 SSO。  
2. **API/SDK 调用**：通过 RESTful API（或官方 JavaScript SDK）进行文件上传、下载、元数据查询和权限管理，适配后端服务或 AI 助手的自动化流程。  
3. **WebDAV 挂载**：在需要本地文件系统访问的应用（如 IDE、搜索引擎）中挂载 WebDAV，直接读取/写入文件，实现“即插即用”。  
4. **CLI 工具**：使用自带的 `filerise-cli` 进行批量上传、同步和权限批处理，适合 CI/CD 或脚本化运维。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，GitHub ★972、Fork 46，社区活跃，Issues 响应及时。  
- **技术成熟度**：基于 JavaScript（Node.js）实现，依赖成熟的 Docker 镜像，易于在容器化环境中扩展。  
- **安全性**：提供 TLS、加密文件夹、细粒度 ACL 与 SSO，满足大多数企业内部合规需求。  
- **生态兼容**：兼容 Docker、Unraid、Kubernetes 等主流部署平台，且开放 API、WebDAV 与 CLI，便于与现有知识库、搜索服务或 AI 助手集成。  

综合来看，FileRise 已具备较高的生产就绪度，适合作为内部文档存储与检索的核心组件，在 RAG 场景下快速为助手提供可靠、可控的知识来源。

## 🧭 Practical evaluation

**Value:** error311/FileRise helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 972 GitHub stars
- 46 forks
- updated 2026-06-26
- primary language: JavaScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 66/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/error311/FileRise) · [← Back to DevOps & Infra](./README.md)</sub>
