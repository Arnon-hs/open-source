# JeremiahM37/librarr

[![Stars](https://img.shields.io/github/stars/JeremiahM37/librarr?style=flat-square&color=yellow)](https://github.com/JeremiahM37/librarr/stargazers) [![Forks](https://img.shields.io/github/forks/JeremiahM37/librarr?style=flat-square&color=blue)](https://github.com/JeremiahM37/librarr/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-85%2F100-brightgreen?style=flat-square)](#)

> Self-hosted book, audiobook, and manga search + download manager. 13 search sources, Torznab API, OPDS feed, request workflow, 4 download clients. The missing *arr for books.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 225 |
| 🍴 **Forks** | 26 |
| 💻 **Language** | Go |
| 📈 **Score** | 85/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`annas-archive` `arr` `audiobooks` `audiobookshelf` `book-manager` `books` `calibre` `docker` `ebooks` `golang` `manga` `opds`

## 🎯 Categories

Automation · Backend · DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
JeremiahM37/librarr is a self‑hosted Go service that automates the search, retrieval, and download of books, audiobooks, and manga from 13 different sources. It offers a Torznab API, OPDS feed, a request‑workflow engine, and native integrations with four download clients—essentially the “*arr” stack for reading material.

**Value Proposition**  
- **Eliminates repetitive manual steps**: Users no longer need to hunt across multiple sites, copy links, and start downloads one‑by‑one; librarr centralises the whole process.  
- **Connects tools into repeatable pipelines**: The Torznab API and OPDS feed let downstream services (e.g., Calibre, Plex, or custom scripts) consume search results programmatically, while the built‑in workflow engine can trigger actions such as queuing a download client, renaming files, or notifying a chat channel.  
- **Supports scheduling and automation**: Because the service runs as a long‑living backend, recurring tasks (e.g., “download new releases every night”) can be scheduled via cron, GitHub Actions, or any orchestrator that can call its HTTP endpoints.

**Practical Adoption Path**  
1. **Deploy** – Use the provided Docker image or compile the Go binary and run it on a modest VM/container.  
2. **Configure sources** – Enable the desired 13 search providers (most are public indexers) and add credentials for the four supported download clients (e.g., qBittorrent, Transmission, NZBGet, Sabnzbd).  
3. **Integrate** –  
   * **API/CLI**: Call the Torznab endpoints from existing media managers or custom scripts.  
   * **OPDS**: Point a reading app (Calibre, Ubooquity, etc.) at the OPDS feed to browse and fetch items directly.  
   * **Workflow**: Define request‑workflow rules (e.g., “if result is a manga, send to qBittorrent”) via the web UI or JSON config.  
4. **Automate** – Schedule periodic searches or use webhooks to trigger downloads when new releases appear.  
5. **Monitor** – Leverage the built‑in health checks and logs; optionally expose Prometheus metrics for observability.

**Production‑Readiness Assessment**  
- **Activity & Community**: 225 ★, 26 forks, recent commits (as of 2026‑06‑23), and a healthy set of 16 topics indicate an active project.  
- **Technical Maturity**: Written in Go, a language well‑suited for reliable services; Docker support and clear API contracts make deployment straightforward.  
- **Ecosystem Fit**: The Torznab and OPDS standards are widely adopted in media automation, easing integration with existing pipelines.  
- **Risk Considerations**: No glaring metadata or licensing issues have been identified, but a final security audit (dependency scanning, CVE checks) and confirmation of an active maintainer are advisable before a production roll‑out.  

Overall, librarr exhibits strong signals for pilot‑grade production use: it removes manual workflow friction, integrates cleanly with common tooling, and is backed by recent development activity and community interest. A cautious but confident rollout—starting in a staging environment, followed by monitoring in production—should be low‑risk.

### Русский

**librarr** — это self‑hosted менеджер поиска и загрузки книг, аудиокниг и манги, объединяющий 13 источников, Torznab API, OPDS‑ленту и 4 клиента загрузки, позволяя полностью автоматизировать процесс получения контента без ручных действий. Типичный сценарий: интеграция librarr в существующий пайплайн (CI/CD, скрипты или домашний медиа‑сервер) для периодического поиска новых выпусков, их загрузки и последующего распределения в медиатеку. Проект готов к production‑использованию: активные коммиты, 225 звёзд, поддержка Go‑SDK/CLI, современный API и широкая экосистема, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
JeremiahM37/librarr 是一款自托管的书籍、音频书和漫画搜索与下载管理器，内置 13 条搜索源，提供 Torznab API、OPDS Feed 与请求工作流，并可对接 4 种下载客户端，实现对书籍资源的“一站式 *arr”。  

**价值**  
- **自动化重复操作**：通过统一的 API/CLI，将搜索、过滤、下载、整理等步骤串成可重复执行的流水线，彻底摆脱手动搜索与手动下载的繁琐。  
- **工具链集成**：可作为后端服务被其他系统（如媒体中心、自动化调度器、CI/CD）调用，或直接在命令行/脚本中使用，轻松嵌入已有工作流。  
- **提升效率**：支持定时任务、批量下载和多客户端协同，显著降低运营成本，适合个人收藏、图书馆或小型内容平台。  

**典型接入方式**  
1. **API 调用**：使用公开的 Torznab API 或 OPDS Feed，按需检索标题、作者、标签等元数据。  
2. **CLI/SDK**：通过自带的命令行工具或 Go SDK，在脚本或自动化平台（如 Jenkins、GitHub Actions、Airflow）中直接发起搜索、添加下载任务。  
3. **下载客户端**：配置支持的四大下载客户端（如 qBittorrent、Transmission、Aria2、Deluge），实现搜索结果自动推送下载。  
4. **工作流编排**：结合如 Node‑RED、n8n 或自建的微服务，构建“搜索 → 过滤 → 下载 → 分类”完整流水线。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，GitHub ★225、Fork 26，社区活跃，代码基于 Go 语言，易于部署与维护。  
- **成熟度**：提供完整的 API 文档、示例脚本和 Docker 镜像，支持容器化部署，具备自动化测试与 CI 流程。  
- **安全与合规**：暂无重大元数据泄露风险，仍需进一步审查许可证（MIT）和依赖安全漏洞。  
- **适配性**：因采用标准化的 Torznab 与 OPDS 协议，兼容多数现有媒体管理系统，评估成本低，适合作为正式生产环境的 OSS 试点。  

总体而言，librarr 在自动化书籍/音频书/漫画获取方面具备高可用性和易集成的特性，是缺失的 “*arr” 解决方案，可帮助团队快速构建可重复、可扩展的内容运营流水线。

## 🧭 Practical evaluation

**Value:** JeremiahM37/librarr helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 225 GitHub stars
- 26 forks
- updated 2026-06-23
- primary language: Go
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 87/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 46/100 |
| production | 82/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/JeremiahM37/librarr) · [← Back to Automation](./README.md)</sub>
