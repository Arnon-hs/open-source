# iv-org/invidious

[![Stars](https://img.shields.io/github/stars/iv-org/invidious?style=flat-square&color=yellow)](https://github.com/iv-org/invidious/stargazers) [![Forks](https://img.shields.io/github/forks/iv-org/invidious?style=flat-square&color=blue)](https://github.com/iv-org/invidious/network) [![Language](https://img.shields.io/badge/lang-Crystal-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Invidious is an alternative front-end to YouTube

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20k |
| 🍴 **Forks** | 2.2k |
| 💻 **Language** | Crystal |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agplv3` `hacktoberfest` `invidious` `libre` `video` `watch` `youtube` `youtube-video`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Invidious (iv‑org/invidious) is an open‑source, self‑hosted front‑end for YouTube that lets users watch videos without Google’s tracking, ads, or JavaScript‑heavy UI. With over 19 k stars, frequent commits, and a large user community, it is a mature alternative that can be deployed as a private proxy or integrated into existing workflows that need YouTube content without the official site’s constraints.  

**Value**  
- Provides privacy‑preserving, ad‑free YouTube access, which is valuable for internal tools, educational platforms, or any product that wants to embed video without exposing users to Google’s tracking ecosystem.  
- Because it is language‑agnostic (served via HTTP), it can be used as a drop‑in replacement for YouTube embeds, RSS feeds, or as a backend for custom video‑search services.  

**Practical adoption path**  
1. **Proof of concept** – Clone the repo, follow the README to spin up a Docker container or a simple binary on a test VM, and verify that video playback works for a handful of URLs.  
2. **Configuration** – Adjust the instance’s rate‑limit, caching, and privacy settings to match your organization’s policies; enable HTTPS and optional authentication if the instance will be public.  
3. **Integration** – Replace existing YouTube embed URLs with the Invidious instance URL (e.g., `https://invidious.mycompany.com/watch?v=…`) in your web app or documentation pipeline.  
4. **Monitoring & scaling** – Add health checks, log aggregation, and a basic autoscaling rule (e.g., Docker‑Swarm/K8s) based on observed traffic.  

**Production readiness**  
The project scores high on production readiness: it has recent activity (last commit 2026‑05‑12), a large star/fork count, and active community support. Its core is written in Crystal, which compiles to a single binary, simplifying deployment and reducing runtime dependencies. While the integration steps are not fully described in the metadata, the comprehensive README and abundant community examples make the setup cost manageable. A small pilot can validate performance and compliance before scaling to a full production deployment.

### Русский

Invidious — открытый фронтенд к YouTube, позволяющий просматривать и получать видео без официального клиентского кода, без рекламы и с минимальными запросами к Google. Для типового внедрения рекомендуется начать с небольшого proof‑of‑concept: проверить README, развернуть контейнер или собрать из исходников и протестировать базовый сценарий получения ролика/плейлиста; при положительном результате проект готов к пилотному запуску в продакшн благодаря активному развитию, большому количеству звёзд (≈20 к) и широкому использованию.

### 中文

**价值**  
Invidious 为 YouTube 提供了一个轻量、去中心化的前端，能够在不依赖 Google 官方页面的情况下观看、搜索和订阅视频。它天然屏蔽广告、避免追踪，并且可以通过自建实例或公共实例实现匿名访问，特别适合对隐私、低资源占用或需要在受限网络环境（如学校、企业防火墙）中使用 YouTube 的团队和个人。

**典型接入方式**  

1. **快速验证（PoC）**  
   - 直接使用已有的公共实例（例如 `https://invidious.snopyta.org`）进行功能验证：打开实例 URL，搜索视频、获取 RSS/JSON API，确认返回的数据结构符合业务需求。  
   - 阅读仓库根目录的 `README.md`，确认实例部署文档、API 使用示例以及所需的运行时（Crystal）版本。

2. **自建实例**  
   - **准备环境**：在一台 Linux 服务器或容器（Docker）上安装 Crystal（≥1.11）和 PostgreSQL（可选，用于持久化缓存）。  
   - **克隆仓库**：`git clone https://github.com/iv-org/invidious.git && cd invidious`  
   - **编译并运行**：  
     ```bash
     shards install          # 安装依赖
     crystal build src/invidious.cr -o invidious
     ./invidious
     ```  
   - **配置**：编辑 `config/config.yml`，设置 `host`, `port`, `domain`, `https` 以及可选的 `proxy`、`api_key` 等。  
   - **容器化**（推荐）：官方提供 Dockerfile，直接 `docker build -t invidious . && docker run -p 3000:3000 invidious`，或使用官方的 `docker-compose.yml` 快速启动。

3. **业务集成**  
   - **API 调用**：Invidious 暴露了与 YouTube 类似的 JSON/JSON‑API（如 `/api/v1/videos/:id`、`/api/v1/search?q=...`），可以直接在后端服务或前端页面中调用，替代 Google 的官方 API，省去 API‑Key 申请和配额管理。  
   - **嵌入播放器**：使用返回的 `embed_url` 或直接将 `<iframe src="https://your-instance/watch?v=VIDEO_ID">` 嵌入内部系统，实现统一的播放体验。  
   - **缓存/代理**：在企业网关层面将 Invidious 设为 YouTube 的缓存代理，减少外部流量并提升访问速度。

**生产可用性**  

- **活跃度**：截至 2026‑05‑12，项目仍在积极维护，最近一次提交就在当天；拥有近 20 k 星、2 k Fork，社区活跃度高。  
- **成熟度**：已在多个公开实例（如 `invidious.snopyta.org`、`invidious.kavin.rocks`）长期运行，证明在高并发、跨地域环境下能够稳定提供服务。  
- **安全性**：代码基于 Crystal，默认启用 HTTPS，支持自定义 TLS 证书；可通过防火墙、Rate‑Limit、OAuth2（可选）进一步硬化。  
- **可扩展性**：支持水平扩展（多实例 behind a load balancer），并可配合 Redis/PostgreSQL 做持久化缓存，满足企业级流量需求。  
- **风险**：集成路径主要是通过公开的 REST API 或自建实例，元数据中未提供完整的部署脚本，需要自行验证部署脚本、监控和备份方案。但这些工作在 PoC 阶段即可完成评估。

**结论**：Invidious 具备高生产可用性，适合作为内部或面向用户的 YouTube 替代前端。建议先通过公共实例验证业务需求，再根据流量规模自行部署并在 CI/CD 流程中加入健康检查与自动更新，以确保长期可靠运行。

## 🧭 Practical evaluation

**Value:** iv-org/invidious may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 19954 GitHub stars
- 2204 forks
- updated 2026-05-12
- primary language: Crystal
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 84/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 75/100 |
| recency | 20/100 |
| adoption | 89/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/iv-org/invidious) · [← Back to Misc](./README.md)</sub>
