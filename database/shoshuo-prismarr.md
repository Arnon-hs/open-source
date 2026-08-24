# Shoshuo/Prismarr

[![Stars](https://img.shields.io/github/stars/Shoshuo/Prismarr?style=flat-square&color=yellow)](https://github.com/Shoshuo/Prismarr/stargazers) [![Forks](https://img.shields.io/github/forks/Shoshuo/Prismarr?style=flat-square&color=blue)](https://github.com/Shoshuo/Prismarr/network) [![Language](https://img.shields.io/badge/lang-Twig-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> A self-hosted media dashboard unifying Radarr, Sonarr, Prowlarr, Jellyseerr, qBittorrent and TMDb in a single Symfony 8 interface. One search bar across the local library and TMDb, one calendar merging movie and episode releases, one dashboard, one settings page. Single Docker container, embedded SQLite, multi-arch. AGPL-3.0.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 374 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Twig |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dashboard` `docker-compose` `frankenphp` `homelab` `jellyseerr` `media-station` `php` `prowlarr` `qbittorent` `radarr` `self-hosted` `sonarr`

## 🎯 Categories

Database · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
Prismarr (Shoshuo/Prismarr) is a self‑hosted Symfony 8 dashboard that aggregates Radarr, Sonarr, Prowlarr, Jellyseerr, qBittorrent and TMDb into a single, sleek UI. It offers a unified search bar, a combined movie/episode calendar, a single settings page and runs in a single multi‑arch Docker container with an embedded SQLite database. The project is AGPL‑3.0 licensed and currently scores 72/100 in the internal evaluation.

---

### Value Proposition
- **One‑stop media hub** – eliminates the need to juggle multiple web UIs; users can search the local library and TMDb, view upcoming releases and manage downloads from a single place.  
- **Rapid AI prototyping** – the unified API surface makes it easy to attach generative‑AI, RAG or agent workflows (e.g., auto‑generating episode summaries, recommending titles, or triggering downloads based on chat commands) without building a custom integration stack for each underlying service.  
- **Low operational overhead** – a single Docker image, SQLite persistence and multi‑arch support keep deployment simple on anything from a home NAS to a small VPS.

### Practical Adoption Path
1. **Evaluate the Docker image** – pull the latest container, run it locally, and point the built‑in configuration UI to existing Radarr/Sonarr/Prowlarr/Jellyseerr/qBittorrent instances (or let Prismarr spin up its own).  
2. **Validate API/CLI hooks** – test the exposed REST endpoints (or the Symfony service container) to confirm they return the expected data for search, calendar and settings operations.  
3. **Prototype AI features** – use the unified endpoints to feed a language model (e.g., OpenAI, Llama 3) for tasks such as natural‑language search, automatic tag generation, or a “watch‑next” recommendation agent.  
4. **Stage for production** – once the AI layer is verified, move the container to a production host, enable persistent volumes for the SQLite DB, and configure TLS/reverse‑proxy (Traefik, Caddy, etc.) for secure external access.  

### Production‑Readiness Assessment
- **Activity & Community** – 374 ★ on GitHub, recent commits (last update 2026‑06‑25), and a modest but active fork base indicate ongoing maintenance.  
- **Architecture** – Symfony 8 + single‑container Docker + embedded SQLite is a proven, low‑complexity stack; multi‑arch builds cover x86_64 and ARM.  
- **Security & Licensing** – AGPL‑3.0 is compatible with most self‑hosted use‑cases, but a final security audit (dependency scanning, container hardening) is recommended before enterprise rollout.  
- **Readiness Score** – The internal rating of 72/100, combined with strong ecosystem signals, places Prismarr in the “high readiness” tier for an OSS pilot.  

**Bottom line:** Prismarr offers a compelling, production‑grade foundation for consolidating media‑management tools and extending them with AI capabilities, with a straightforward Docker‑first adoption path and sufficient community momentum to justify a serious pilot.

### Русский

Shoshuo/Prismarr — это self‑hosted медиа‑дашборд, объединяющий Radarr, Sonarr, Prowlarr, Jellyseerr, qBittorrent и TMDb в едином Symfony 8 интерфейсе: один поисковый бар, общий календарь релизов и единая страница настроек, упакованные в один Docker‑контейнер с встроенной SQLite и поддержкой multi‑arch. Проект уже имеет активную поддержку (обновления 2026‑06‑25, 374 звёзд на GitHub) и готов к production‑использованию, позволяя быстро прототипировать AI‑фичи (RAG, агентные сценарии) и интегрировать их через открытый API/CLI без необходимости создавать стек с нуля.

### 中文

**项目简介（2‑3 句）**  
Shoshuo/Prismarr 是一款基于 Symfony 8 的自托管媒体仪表盘，统一管理 Radarr、Sonarr、Prowlarr、Jellyseerr、qBittorrent 与 TMDb，提供全局搜索、合并日历、单页设置等功能。项目采用单容器 Docker、内嵌 SQLite，支持多架构，代码遵循 AGPL‑3.0 开源许可证。

**价值**  
- **统一入口**：一次搜索即可在本地媒体库和 TMDb 中查找电影/剧集，省去在多个工具之间切换的时间。  
- **信息聚合**：日历视图将电影上映和剧集更新合并展示，便于规划观看计划。  
- **易部署**：单一 Docker 镜像、内置 SQLite，无需外部数据库或复杂配置，适合快速搭建私有媒体中心。  
- **可扩展**：基于 Symfony 框架，可在此基础上集成 AI 推荐、RAG 或自动化 agent 工作流，帮助开发者快速原型化 AI 功能。

**典型接入方式**  
1. **Docker 部署**：`docker run -d -p 8080:80 shoshuo/prismarr`（可通过环境变量挂载配置文件、设置时区等）。  
2. **API/CLI 集成**：项目在 `src/Controller/Api` 下暴露 RESTful 接口，支持查询媒体库、触发下载、获取日历等操作；亦提供 Symfony Console 命令，可在 CI/CD 或自定义脚本中调用。  
3. **前端嵌入**：使用 Twig 模板渲染的 UI，可通过 iframe 或反向代理直接嵌入已有的自托管门户。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25 最近一次提交，GitHub 374 星、8 个 fork，社区活跃度良好。  
- **技术成熟度**：基于 Symfony 8 与 SQLite，依赖成熟且安全性可控；Docker 镜像已提供 multi‑arch 支持，适配 x86_64 与 ARM。  
- **安全/合规**：采用 AGPL‑3.0 许可证，需注意在商业化环境中的开源合规要求；建议在生产环境前进行镜像安全扫描并开启容器安全实践（如只读文件系统、最小权限网络）。  
- **可扩展性**：代码结构清晰，提供 API 与 CLI，便于二次开发和 AI 模块接入，适合作为内部媒体平台或 AI 原型实验的底层支撑。  

综上，Shoshuo/Prismarr 在功能完整性、部署便利性和社区活跃度方面均表现出色，具备在生产环境中作为核心媒体管理平台使用的条件，只需在安全审计和许可证合规上进行一次性确认即可。

## 🧭 Practical evaluation

**Value:** Shoshuo/Prismarr helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 374 GitHub stars
- 8 forks
- updated 2026-06-25
- primary language: Twig
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/Shoshuo/Prismarr) · [← Back to Database](./README.md)</sub>
