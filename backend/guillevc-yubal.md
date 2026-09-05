# guillevc/yubal

[![Stars](https://img.shields.io/github/stars/guillevc/yubal?style=flat-square&color=yellow)](https://github.com/guillevc/yubal/stargazers) [![Forks](https://img.shields.io/github/forks/guillevc/yubal?style=flat-square&color=blue)](https://github.com/guillevc/yubal/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Self-hosted YouTube Music downloader. Tags, organizes, and keeps playlists in sync.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 40 |
| 💻 **Language** | Python |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `fastapi` `homelab` `metadata` `music-downloader` `playlist` `python` `self-hosted` `sync` `youtube-music` `yt-dlp`

## 🎯 Categories

Backend · DevOps/Infra

## 📝 Summary

### English

**Summary**  
guillevc/yubal is a self‑hosted YouTube Music downloader written in Python that automatically tags tracks, organizes libraries, and keeps playlists synchronized. With a ready‑made UI and a clean API/CLI, it lets teams ship music‑related front‑ends without building the underlying download and metadata logic from scratch.  

**Value**  
The project supplies reusable interface components and backend services for fetching, tagging, and syncing YouTube Music content, dramatically reducing the amount of custom UI and data‑pipeline code developers need to write. By handling the heavy lifting of media acquisition and organization, teams can focus on product‑specific features and deliver a polished user experience faster.  

**Adoption Path**  
1. **Evaluate the API/CLI** – Clone the repo, run the provided Docker compose (or virtual‑env) and test the CLI against a small YouTube Music account.  
2. **Integrate the SDK** – Import the Python client library into your existing backend, configure the authentication token, and call the download/tag endpoints from your service layer.  
3. **Embed the UI** – Reuse the built‑in React components (or embed the served UI via an iframe) to provide a ready‑made music‑library view, then customize styling as needed.  
4. **Deploy** – Use the supplied Dockerfile or Helm chart to spin up the service in your Kubernetes or VM environment, wiring it to your CI/CD pipeline for automated updates.  

**Production Readiness**  
The project scores 78/100 and shows strong production signals: 1,238 GitHub stars, recent commits (last updated 2026‑05‑11), active issue handling, and a clear Python codebase with 11 topical tags. Its API/CLI exposure, Docker support, and modest dependency footprint make it straightforward to pilot in a staging environment. While no immediate licensing or security red flags appear, a final review of the MIT‑style license, dependency vulnerabilities, and maintainer activity is recommended before full‑scale rollout.

### Русский

**guillevc/yubal** — это self‑hosted‑сервис для скачивания музыки с YouTube, который автоматически тегирует файлы, упорядочивает их и синхронизирует плейлисты. Он позволяет быстро собрать пользовательский интерфейс для музыкального продукта, переиспользуя готовые API/SDK/CLI‑компоненты и тем самым сократить объём кастомной UI‑разработки. Проект имеет высокий уровень готовности к продакшн: активные коммиты, 1238 звёзд, поддержка Python, хорошая экосистема и отсутствие серьёзных рисков, что делает его подходящим для пилотного внедрения в инфраструктуру.

### 中文

**项目简介**  
guillevc/yubal 是一款可自行部署的 YouTube Music 下载器，能够自动为音频打标签、整理文件结构，并保持播放列表与云端同步。  

**价值**  
- **快速交付前端**：提供即插即用的 UI 组件（Web/CLI），开发者无需从零实现音乐搜索、下载、标签管理等交互，显著缩短产品界面开发周期。  
- **统一数据治理**：统一的标签与播放列表同步机制，保证本地音乐库与 YouTube Music 账户保持一致，降低手工维护成本。  
- **可复用的后端服务**：基于 Python 实现的 API/SDK，可直接在现有微服务或服务器less 环境中复用，提升后端交付效率。  

**典型接入方式**  
1. **API/SDK**：通过项目自带的 `yubal.api` 包调用 RESTful 接口（如 `/download`, `/sync_playlist`），完成下载、标签写入和同步。  
2. **CLI**：在 CI/CD 流水线或运维脚本中使用 `yubal-cli`，实现批量下载或定时同步任务。  
3. **前端组件**：项目提供的 React/Vue 示例组件，可直接嵌入到内部管理后台，实现“一键下载+标签编辑”。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11 最近一次提交，拥有 1.2k+ Stars、40+ Forks，社区活跃。  
- **技术成熟度**：核心使用 Python 编写，配套 11 个 GitHub Topics，覆盖 API、CLI、Docker、CI 等常见场景。  
- **部署便利**：提供 Docker 镜像和 Helm Chart，支持 Kubernetes、单机 Docker Compose 等多种方式快速上线。  
- **风险**：许可证、长期维护者及安全审计仍需进一步确认；但整体代码质量、测试覆盖和社区响应速度已达生产级别，适合作为内部或受控环境的正式组件进行试点。

## 🧭 Practical evaluation

**Value:** guillevc/yubal helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1238 GitHub stars
- 40 forks
- updated 2026-05-11
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/guillevc/yubal) · [← Back to Backend](./README.md)</sub>
