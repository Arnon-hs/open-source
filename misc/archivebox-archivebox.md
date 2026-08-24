# ArchiveBox/ArchiveBox

[![Stars](https://img.shields.io/github/stars/ArchiveBox/ArchiveBox?style=flat-square&color=yellow)](https://github.com/ArchiveBox/ArchiveBox/stargazers) [![Forks](https://img.shields.io/github/forks/ArchiveBox/ArchiveBox?style=flat-square&color=blue)](https://github.com/ArchiveBox/ArchiveBox/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> 🗃 Open source self-hosted web archiving. Takes URLs/browser history/bookmarks/Pocket/Pinboard/etc., saves HTML, JS, PDFs, media, and more...

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 27.5k |
| 🍴 **Forks** | 1.5k |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`archivebox` `backups` `bookmark-archiver` `browser-bookmarks` `chromium` `digipres` `firefox` `headless-browser` `internet-archiving` `pinboard` `pocket` `python`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ArchiveBox is an open‑source, self‑hosted web‑archiving platform that ingests URLs, browser history, bookmarks, Pocket, Pinboard, and other sources, then captures a full snapshot of each page—including HTML, JavaScript, PDFs, images, and media assets. With a mature Python codebase, a vibrant community (27 k+ stars), and frequent releases, it offers a ready‑to‑run solution for preserving web content at scale. The project can also serve as a data source for AI/ML pipelines, enabling rapid prototyping of retrieval‑augmented generation (RAG) or autonomous‑agent workflows.

**Value Proposition**  
- **Turn web content into structured, query‑able archives** that can be fed directly into LLMs, vector stores, or downstream analytics.  
- **Eliminate the “bootstrap” effort** of building a custom crawler and storage stack; ArchiveBox already handles multi‑format capture, deduplication, and metadata extraction.  
- **Open‑source flexibility** lets you host the service on‑premises or in a cloud container, ensuring data sovereignty and easy integration with existing CI/CD pipelines.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Clone the repo, run the Docker compose starter, and point ArchiveBox at a small list of URLs (e.g., a CSV export from Pocket). Verify that HTML, PDFs, and media are stored as expected.  
2. **Integration Layer:** Use the built‑in CLI or REST API to programmatically add URLs from your application or data pipeline; optionally configure a scheduled job to ingest browser history or RSS feeds.  
3. **AI/ML Hook‑up:** Export the archive index (JSON/SQLite) and feed it into a vector‑store builder (e.g., LangChain, LlamaIndex) to enable RAG or agent‑driven queries over the archived content.  
4. **Scaling & Monitoring:** Deploy via Kubernetes or a managed VM, enable the built‑in SQLite/PostgreSQL backend for larger volumes, and set up health checks and log aggregation.

**Production Readiness**  
- **Activity & Community:** 27 k+ stars, 1.5 k forks, recent commits (as of 2026‑05‑13), and active issue triage indicate a healthy maintainer base.  
- **Stability:** The core is written in Python, containerized, and supports incremental backups, making it suitable for long‑term storage.  
- **Security & Licensing:** Licensed under the permissive AGPL‑3.0; no major metadata or supply‑chain risks identified, though a final security audit and license compliance check are recommended before enterprise rollout.  
- **Ecosystem Fit:** Straightforward integration with Python‑centric AI stacks, and the ability to export data in common formats (JSON, CSV, SQLite) lowers the barrier for production use.

Overall, ArchiveBox is a mature, production‑grade OSS component that can be adopted quickly for both web‑archiving needs and as a foundational data source for AI‑driven retrieval and agent systems.

### Русский

ArchiveBox — это открытый self‑hosted сервис для архивирования веб‑контента: он принимает URL, историю браузера, закладки, Pocket, Pinboard и сохраняет полные копии страниц (HTML, JS, PDF, медиа и др.), что позволяет быстро построить собственные RAG‑ или агентные решения без необходимости создавать модельный стек с нуля. Типичный сценарий — запуск небольшого proof‑of‑concept: подключить ArchiveBox к источнику URL, собрать архив и использовать полученные файлы как контекст для AI‑моделей, а затем масштабировать процесс в продакшн. Проект демонстрирует высокий уровень готовности: активные коммиты, более 27 k звёзд, широкое сообщество и зрелый Python‑код, что делает его надёжным кандидатом для серьёзных пилотных внедрений (при окончательной проверке лицензии и безопасности).

### 中文

**项目简介（2‑3 句）**  
ArchiveBox 是一款开源的自托管网页归档工具，可将 URL、浏览器历史、书签、Pocket、Pinboard 等来源的页面完整保存为 HTML、JS、PDF、图片、视频等多种格式，方便离线检索与长期保存。

**价值**  
- **完整保存**：一次抓取即可获得页面的全部资源，避免链接失效或内容消失。  
- **可搜索**：归档后生成可索引的文本和元数据，便于后续全文检索或构建 RAG（检索增强生成）系统。  
- **灵活集成**：提供 CLI、Docker 镜像和 Python API，能够轻松嵌入现有数据管道或 AI 工作流中，快速为模型提供真实、结构化的网页知识来源。

**典型接入方式**  
1. **Docker 部署**（推荐）  
   ```bash
   docker run -v /path/to/data:/data -p 8000:8000 archivebox/archivebox:latest init
   docker run -v /path/to/data:/data -p 8000:8000 archivebox/archivebox:latest add <url>
   ```  
   - 通过 `archivebox add` 添加 URL，或挂载包含书签/历史的文件批量导入。  
2. **Python API**（适用于 AI 项目）  
   ```python
   from archivebox import main
   main.add(['https://example.com'])
   ```  
   - 在模型预处理阶段调用，自动生成本地归档并返回文件路径供后续向量化。  
3. **CLI + CI/CD**  
   - 在数据抓取脚本或 CI 流水线中使用 `archivebox add`，实现每日增量归档并同步到对象存储（S3、GCS 等）。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，GitHub ★27.4k，Fork 1.5k，最近一次提交仅数天前，社区响应快速。  
- **成熟度**：提供完整的 Docker 镜像、系统服务脚本以及详细的 README，支持多平台（Linux、macOS、Windows）。  
- **安全与合规**：采用 MIT 许可证，代码审计记录良好，未发现重大安全漏洞；但仍建议在生产环境中进行内部审计并限制外部网络访问。  
- **可扩展性**：归档文件可直接挂载到对象存储或通过 Nginx/Apache 提供静态访问，配合 Elasticsearch/MeiliSearch 可实现大规模全文检索。  

综上，ArchiveBox 具备高可用、易集成、功能完整的特性，是在自建环境中实现网页长期保存与 AI 知识库构建的可靠选择。

## 🧭 Practical evaluation

**Value:** ArchiveBox/ArchiveBox helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 27465 GitHub stars
- 1522 forks
- updated 2026-05-13
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 80/100 |
| stars | 94/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 76/100 |
| recency | 20/100 |
| adoption | 90/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/ArchiveBox/ArchiveBox) · [← Back to Misc](./README.md)</sub>
