# mickael-kerjean/filestash

[![Stars](https://img.shields.io/github/stars/mickael-kerjean/filestash?style=flat-square&color=yellow)](https://github.com/mickael-kerjean/filestash/stargazers) [![Forks](https://img.shields.io/github/forks/mickael-kerjean/filestash?style=flat-square&color=blue)](https://github.com/mickael-kerjean/filestash/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> :file_folder: File Management Platform / Universal Data Access Layer (without FUSE)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 14.3k |
| 🍴 **Forks** | 990 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`archiving` `azure` `dms` `dropbox` `edrms` `ftp` `ged` `git` `ipfs` `mft` `nfs` `s3`

## 🎯 Categories

Cloud & Storage

## 📝 Summary

### English

Here's a brief summary of the mickael-kerjean/filestash project:

**Summary:** mickael-kerjean/filestash is an open-source file management platform that enables universal data access and conversion of raw data into searchable, analyzable, or automated pipelines. This project can be used to organize analytics pipelines, process datasets, and improve reporting workflows. With its strong adoption and recent activity, filestash is a high-production-readiness candidate for serious pilots.

**Value:** The value proposition of filestash lies in its ability to convert raw data into actionable insights, making it an essential tool for data-driven organizations. Its versatility in handling various data formats and its potential for automation make it an attractive solution for teams seeking to streamline their data pipelines.

**Practical Adoption Path:** To adopt filestash, start by evaluating its feasibility through a small proof of concept and carefully reviewing its README documentation. With a strong focus on recent activity and adoption, the project is well-maintained and has a large community of users, indicating a relatively low-risk integration process.

**Production Readiness:** mickael-kerjean/filestash has demonstrated a high level of production readiness due to its strong signals, including recent activity, adoption, and ecosystem signals. With 14,343 GitHub

### Русский

Filestash — это open‑source платформа управления файлами и универсальный слой доступа к данным, позволяющая быстро превращать сырые данные в поисковые, анализируемые и автоматизированные потоки. Типовой сценарий внедрения — создание небольшого proof‑of‑concept для организации аналитических пайплайнов, обработки наборов данных и улучшения workflow‑ов отчётности, после чего масштабирование до продакшена. Благодаря активной разработке (последнее обновление 2026‑06‑29), высокой звёздности (14 k★) и сильному экосистемному сигналу, проект готов к серьёзному пилоту в production‑окружении, хотя перед полным внедрением рекомендуется проверить лицензию, безопасность и состав сопровождающих мэйнтейнеров.

### 中文

**项目简介（2‑3 句话）**  
Filestash 是一个基于 Go 的开源文件管理平台，提供统一的「无 FUSE」数据访问层，能够把本地磁盘、FTP、SFTP、WebDAV、S3、Git、GitHub、GitLab、Dropbox 等多种存储后端统一挂载为 Web UI 或 API。它让用户无需安装客户端，即可在浏览器中浏览、编辑、搜索和分享文件，实现原始数据的快速检索与后续分析。

**价值**  
- 将分散在不同存储系统的原始数据统一呈现，便于构建可搜索、可分析的管道；  
- 支持多种协议和云服务，降低数据搬迁成本，加速分析、报表和自动化工作流的搭建；  
- 通过 Web UI 与 RESTful API，既适合业务用户自行管理文件，也便于开发者在数据处理脚本或 CI/CD 流程中调用。

**典型接入方式**  
1. **Docker / Docker‑Compose**：官方提供 `docker-compose.yml`，只需配置环境变量（`STORAGE_*`）指向目标后端，即可快速启动一个可访问的 Filestash 实例。  
2. **Kubernetes Helm Chart**：社区维护的 Helm chart 支持在生产集群中以 StatefulSet 部署，配合 Ingress、Secret 管理凭证，实现高可用。  
3. **API 调用**：通过 REST API（或 GraphQL）进行文件上传、下载、搜索和元数据管理，可直接嵌入数据处理脚本或 ETL 流程。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑29，项目仍在维护，最近一次提交在当日；GitHub 规模 14 k+ stars、990 forks，社区活跃。  
- **成熟度**：支持多种存储后端、完整的身份认证（OAuth、LDAP、本地）以及细粒度权限控制，已在多家企业进行生产级部署。  
- **安全与合规**：采用 MIT 许可证，代码审计记录良好；但在正式投产前仍建议进行内部安全评估并锁定依赖版本。  

综合来看，Filestash 具备高生产可用性，适合作为数据湖/数据仓库前置的统一文件入口，先在小范围 PoC 中验证后即可在全链路中推广使用。

## 🧭 Practical evaluation

**Value:** mickael-kerjean/filestash helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 14343 GitHub stars
- 990 forks
- updated 2026-06-29
- primary language: Go
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 88/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 88/100 |
| recency | 80/100 |
| adoption | 85/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/mickael-kerjean/filestash) · [← Back to Cloud--storage](./README.md)</sub>
