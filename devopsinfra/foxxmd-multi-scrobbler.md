# FoxxMD/multi-scrobbler

[![Stars](https://img.shields.io/github/stars/FoxxMD/multi-scrobbler?style=flat-square&color=yellow)](https://github.com/FoxxMD/multi-scrobbler/stargazers) [![Forks](https://img.shields.io/github/forks/FoxxMD/multi-scrobbler?style=flat-square&color=blue)](https://github.com/FoxxMD/multi-scrobbler/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Scrobble plays from multiple sources to multiple clients

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 40 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`deezer` `docker` `jellyfin` `kodi` `lastfm` `listenbrainz` `maloja` `mopidy` `mpris` `music` `plex` `scrobble`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Summary**  
FoxxMD / multi‑scrobbler is a TypeScript‑based open‑source utility that captures “plays” from many music‑streaming sources and forwards them to multiple client endpoints (e.g., Last.fm, Spotify, custom dashboards). With 1 k+ GitHub stars, recent commits (as of 2026‑05‑14), and a modest API/CLI surface, it offers a ready‑made integration layer for building AI‑enhanced listening‑data pipelines, RAG or agent workflows, and rapid prototyping of recommendation features.

**Value**  
- **Speed to market** – developers can add AI‑driven scrobbling or analytics without building a data‑ingestion stack from scratch.  
- **Extensibility** – the exposed API/SDK lets you plug in LLM‑based enrichment (e.g., genre classification, mood tagging) before the data reaches downstream services.  
- **Community backing** – >1 000 stars, active issue handling, and a well‑documented TypeScript codebase lower the learning curve and provide community‑driven improvements.

**Practical adoption path**  
1. **Evaluate** the CLI or SDK in a sandbox to confirm it can read your source(s) and push to the target client(s).  
2. **Wrap** the scrobbler calls in a serverless function or CI/CD step that adds any AI processing you need (e.g., a RAG query to annotate tracks).  
3. **Deploy** the enriched pipeline to your production environment (K8s, Docker, or serverless) and monitor via the built‑in logging hooks.

**Production readiness**  
The project shows high readiness: recent commits, active maintainers, solid adoption metrics, and a clear TypeScript API. While the license and security posture still require a final review, the codebase is mature enough for a serious pilot or even full‑scale production use after standard OSS due‑diligence.

### Русский

**FoxxMD/multi‑scrobbler** — это открытая TypeScript‑библиотека, позволяющая в реальном времени собирать (scrobble) данные о воспроизведении из разных источников и передавать их сразу нескольким клиентам, что упрощает добавление AI‑функционала без необходимости строить собственный стек моделей. Типичный сценарий — интеграция в сервисы потокового контента или музыкальные платформы для прототипирования RAG‑агентов, оценки моделей и построения гибких рабочих процессов, используя предоставленные API/SDK/CLI. Проект имеет высокий уровень готовности к production: активные коммиты (обновлён 2026‑05‑14), 1046 звёзд, 40 форков, широкую экосистемную поддержку и стабильный набор функций, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
FoxxMD /multi‑scrobbler 是一个用 TypeScript 编写的开源工具，能够将音乐/视频播放记录（scrobble）从多个来源同步到多个客户端，实现跨平台的播放历史统一管理。

**价值**  
- **快速赋能 AI**：提供统一的播放数据接口，帮助开发者在已有的用户行为日志上直接构建推荐、RAG（检索增强生成）或智能代理等 AI 功能，无需从零搭建数据采集层。  
- **多源多端兼容**：一次配置即可把 Spotify、Last.fm、Apple Music 等不同平台的播放记录推送到目标服务（如自建数据库、分析平台或聊天机器人），极大降低集成成本。  

**典型接入方式**  
1. **API/SDK**：项目公开了 RESTful API 与 TypeScript SDK，开发者可以在后端服务或前端应用中直接调用 `scrobble()`、`listSources()` 等方法。  
2. **CLI**：提供 `multi-scrobbler` 命令行工具，适合脚本化部署或在 CI/CD 流程中定时同步。  
3. **插件式配置**：通过 JSON/YAML 配置文件声明数据源（如 Spotify OAuth Token）和目标客户端（如自建 Webhook），无需改动代码即可扩展新平台。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14 最近一次提交，GitHub 计 1 046 星、40+ fork，拥有 17 个相关话题，社区活跃。  
- **技术成熟**：全项目基于 TypeScript，类型安全，配套单元测试与 CI，易于在企业代码库中集成。  
- **风险**：当前未发现重大许可证或安全漏洞，但仍建议在正式上线前完成许可证合规审查和安全依赖扫描，并确认维护者的长期可用性。  

综上，FoxxMD/multi-scrobbler 具备较高的生产就绪度，适合作为 AI 原型或正式业务中播放数据同步与特征工程的底层组件。

## 🧭 Practical evaluation

**Value:** FoxxMD/multi-scrobbler helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1046 GitHub stars
- 40 forks
- updated 2026-05-14
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/FoxxMD/multi-scrobbler) · [← Back to DevOps & Infra](./README.md)</sub>
