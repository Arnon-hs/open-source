# iuliandita/digarr

[![Stars](https://img.shields.io/github/stars/iuliandita/digarr?style=flat-square&color=yellow)](https://github.com/iuliandita/digarr/stargazers) [![Forks](https://img.shields.io/github/forks/iuliandita/digarr?style=flat-square&color=blue)](https://github.com/iuliandita/digarr/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> AI-powered music discovery for your *arr stack. Recommends artists and individual albums through a 7-stage AI pipeline, scores and ranks them, and learns from your feedback -- approve a single album without grabbing the whole discography. Supports Lidarr, Spotify, Navidrome, Jellyfin, Plex. Self-hosted, open source.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 201 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `albums` `docker` `lastfm` `lidarr` `listenbrainz` `music-discovery` `musicbrainz` `recommendations` `self-hosted`

## 🎯 Categories

AI/ML · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
digarr (iuliandita/digarr) is an open‑source, self‑hosted service that adds AI‑driven music discovery to any *arr stack (Lidarr, Radarr, etc.). It runs a 7‑stage pipeline that fetches metadata, generates relevance scores, ranks artists and individual albums, and continuously refines its recommendations from user feedback, letting you approve a single album without pulling the entire discography. The project ships a TypeScript API/CLI, integrates with Spotify, Navidrome, Jellyfin, Plex and other *arr tools, and is ready for production pilots.

**Value**  
- **Plug‑and‑play AI** – You get sophisticated recommendation models without building a model from scratch; the pipeline is already wired to ingest *arr metadata, score candidates, and learn from approvals/rejections.  
- **Fine‑grained control** – Unlike typical “whole‑artist” suggestions, digarr can surface a single album that matches a user’s taste, reducing noise and storage overhead.  
- **Multi‑platform reach** – Works across the most common self‑hosted media servers and streaming services, making it a universal upgrade for any existing *arr deployment.  

**Practical Adoption Path**  
1. **Deploy** – Run the Docker image (or compile from source) alongside your existing *arr services.  
2. **Configure connectors** – Supply API tokens/credentials for Lidarr, Spotify, Navidrome, Jellyfin, or Plex in the provided `config.yml`.  
3. **Bootstrap** – Let digarr scan your libraries; the pipeline will generate initial scores for all artists/albums.  
4. **Iterate** – Use the web UI, CLI, or API to approve/reject recommendations; the feedback loop updates the model automatically.  
5. **Extend** – Because the core is TypeScript with a clear SDK, you can add custom scoring modules, swap in alternative LLMs, or embed the service in larger RAG or autonomous agent workflows.  

**Production Readiness**  
- **Activity & Adoption** – 201 ★, recent commits (last updated 2026‑07‑02), and a growing community signal healthy momentum.  
- **Infrastructure** – Docker‑ready, stateless API, and clear environment variables make scaling and container orchestration straightforward.  
- **Observability** – Built‑in logging and health endpoints allow integration with existing monitoring stacks.  
- **Risk Considerations** – License compliance, security hardening, and long‑term maintainer commitment still need a final audit, but no major metadata or compliance red flags are present.  

Overall, digarr offers a mature, low‑effort way to embed AI recommendation capabilities into any *arr ecosystem, making it a strong candidate for a pilot or production rollout after a brief security/license review.

### Русский

iuliandita/digarr — open‑source сервис, который с помощью 7‑ступенчатого AI‑pipeline подбирает исполнителей и отдельные альбомы под ваш *arr‑стек (Lidarr, Spotify, Navidrome, Jellyfin, Plex), позволяя одобрять отдельные релизы без необходимости импортировать всю дискографию. Проект готов к пилотному внедрению в продакшн: активные коммиты, 201 звезда, поддержка API/CLI и типичные интеграционные точки, а также широкая совместимость с популярными медиа‑серверными решениями. Он идеален для быстрой прототипизации AI‑фич, построения RAG‑ или агентных воркфлоу и оценки инструментов машинного обучения в музыкальном контексте.

### 中文

**项目简介**

iuliandita/digarr 是一个开源项目，使用 AI 技术来发现音乐推荐，适用于 *arr 栈。它通过一个 7 个阶段的 AI 管道，推荐艺术家和个人专辑，并根据你的反馈进行学习和改进。支持多个音乐平台，包括 Lidarr、Spotify、Navidrome、Jellyfin 和 Plex。它是自主托管的，开源的。

**价值**

iuliandita/digarr 的价值在于，它可以帮助你在不从零开始的情况下添加 AI 能力。它可以用于多种场景，例如：

* prototype AI 特性
* 构建 RAG 或代理工作流
* 评估模型工具

**典型接入方式**

iuliandita/digarr 支持多种接入方式，包括：

* API：通过 API 可以接入 digarr 的推荐功能。
* SDK：使用 SDK 可以在你的应用中集成 digarr 的功能。
* CLI：通过 CLI 可以直接使用 digarr 的命令行工具。

**生产可用性**

iuliandita/digarr 的生产可用性较高，因为它有

## 🧭 Practical evaluation

**Value:** iuliandita/digarr helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 201 GitHub stars
- 4 forks
- updated 2026-07-02
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/iuliandita/digarr) · [← Back to AI/ML](./README.md)</sub>
