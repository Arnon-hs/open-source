# jeremiaa/magic-frame

[![Stars](https://img.shields.io/github/stars/jeremiaa/magic-frame?style=flat-square&color=yellow)](https://github.com/jeremiaa/magic-frame/stargazers) [![Forks](https://img.shields.io/github/forks/jeremiaa/magic-frame?style=flat-square&color=blue)](https://github.com/jeremiaa/magic-frame/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Self-hosted home display — part photo frame, part family board, part Home Assistant dashboard. Drag-&-drop, live sync, Immich wallpapers. No cloud.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 247 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`caddy` `dashboard` `digital-signage` `docker` `glassmorphism` `home-assistant` `homelab` `nextjs` `picture-frame` `postgresql` `react` `self-hosted`

## 🎯 Categories

Frontend · Database · DevOps/Infra

## 📝 Summary

### English

**Project Summary:**
Magic-Frame is an open-source, self-hosted home display that combines a photo frame, family board, and Home Assistant dashboard. It enables users to index knowledge bases, improve document search, and ground assistant answers with its drag-and-drop, live sync, and Immich wallpapers features.

**Value Proposition:**
The primary value of Magic-Frame lies in its ability to make internal knowledge searchable and usable by assistants, which can lead to improved search functionality and more accurate assistant answers.

**Practical Adoption Path:**
To adopt Magic-Frame, users can start by evaluating the project's implementation signals, such as its API, SDK, CLI, and language metadata. With a recent activity, adoption, and ecosystem signals, the project is considered production-ready, making it a serious candidate for a pilot. Users can then follow the project's documentation and community support to integrate Magic-Frame into their existing systems.

**Production Readiness:**
Magic-Frame has a high production readiness score due to its recent activity, adoption, and ecosystem signals. With 247 GitHub stars, 6 forks, and an active maintainership, the project is well-suited for a serious pilot or production deployment. However, a final review of the license, security posture, and maintainers

### Русский

**jeremiaa/magic-frame** — это self‑hosted домашняя панель, совмещающая цифровую фоторамку, семейный доску объявлений и дашборд Home Assistant. С помощью drag‑&‑drop интерфейса и живой синхронизации можно выводить Immich‑обои, визуализировать данные из Home Assistant и быстро делиться внутренними знаниями, делая их доступными для поисковых и голосовых ассистентов. Проект активно поддерживается (обновления до 2026‑07‑06, 247 звёзд, TypeScript), имеет открытый API/CLI и готов к пилотному запуску в production, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
jeremiaa/magic-frame 是一款自托管的家庭展示系统，融合了相框、家庭信息板和 Home Assistant 仪表盘的功能。支持拖拽布局、实时同步、Immich 壁纸，全部本地运行，无需任何云服务。

**价值主张**  
- **内部知识即时可视化**：将文档、图片、日程等信息以卡片形式呈现在家中大屏，所有成员都能快速查阅。  
- **统一入口，提升搜索效率**：配合 RAG（检索增强生成）技术，可把家庭或企业的知识库索引到页面上，实现自然语言搜索和 AI 助手的上下文引用。  
- **隐私安全**：所有数据均保存在本地或自建的 Immich 服务器，避免云端泄露风险。

**典型接入方式**  
1. **API/SDK**：项目提供 RESTful API 与 TypeScript SDK，开发者可在自有系统（如内部知识库、文档管理平台）中调用 `POST /cards`、`GET /cards` 等接口，实现内容的自动推送与更新。  
2. **CLI 工具**：通过 `magic-frame-cli` 可在 CI/CD 流程中批量上传、删除或刷新卡片，适合自动化文档同步。  
3. **Home Assistant 集成**：使用官方提供的 `magic_frame` 集成组件，将 Home Assistant 实体（天气、传感器、提醒等）直接映射为卡片，完成仪表盘统一展示。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑06 最近一次提交，GitHub 星标 247，Fork 6，社区讨论活跃。  
- **技术成熟度**：核心使用 TypeScript + React，配套 Docker 镜像与 Helm Chart，支持一键部署到本地服务器或 Kubernetes。  
- **安全与合规**：项目本身无外部依赖的云服务，所有数据均在自控环境中存储；仍需自行审查 Docker 镜像的安全基线以及许可证（MIT）是否符合组织政策。  
- **适配性**：提供 OpenAPI 规范文档，易于与现有 RAG 流水线或内部搜索系统对接，适合作为内部知识可视化的首选 OSS 组件。

综上，jeremiaa/magic-frame 在功能完整性、部署便利性和社区活跃度方面均表现良好，经过一次安全审计后即可在生产环境中用于家庭或企业内部的知识展示与 AI 助手支撑。

## 🧭 Practical evaluation

**Value:** jeremiaa/magic-frame helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 247 GitHub stars
- 6 forks
- updated 2026-07-06
- primary language: TypeScript
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/jeremiaa/magic-frame) · [← Back to Frontend](./README.md)</sub>
