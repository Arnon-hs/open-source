# Purfview/IMDb-Scout-Mod

[![Stars](https://img.shields.io/github/stars/Purfview/IMDb-Scout-Mod?style=flat-square&color=yellow)](https://github.com/Purfview/IMDb-Scout-Mod/stargazers) [![Forks](https://img.shields.io/github/forks/Purfview/IMDb-Scout-Mod?style=flat-square&color=blue)](https://github.com/Purfview/IMDb-Scout-Mod/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Auto search for movie/series on torrent, usenet, ddl, subtitles, streaming, predb and other sites. Adds links to IMDb pages from hundreds various sites. Adds movies/series to Radarr/Sonarr. Adds external ratings from Metacritic, Rotten Tomatoes, Letterboxd, Douban, Allocine. Media Server indicators for Plex, Jellyfin, Emby. Dark theme/style for Reference View. Adds/Removes to/from Trakt's watchlist. Removes ads

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 559 |
| 🍴 **Forks** | 75 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`1337x` `bittorrent` `download` `imdb` `jellyfin` `p2p` `plex` `radarr` `rarbg` `search` `sonarr` `streaming`

## 🎯 Categories

Video Editing · Marketing

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Purfview/IMDb‑Scout‑Mod is a JavaScript‑based tool that enriches IMDb pages with links to torrents, Usenet, DDL services, subtitles, streaming sites, pre‑db listings and external ratings (Metacritic, Rotten Tomatoes, Letterboxd, Douban, Allocine). It can push titles to Radarr/Sonarr, sync watch‑list status with Trakt, provide Plex/Jellyfin/Emby media‑server indicators, and includes a dark‑theme Reference View while stripping ads.

**Value**  
The project consolidates a wide range of media‑discovery and management APIs into a single, reusable backend component. By plugging it in, teams avoid re‑implementing the tedious logic for fetching torrent/streaming links, aggregating ratings, and integrating with popular automation tools (Radarr, Sonarr, Trakt), thereby accelerating the delivery of media‑catalogue services and ensuring a consistent user experience across platforms.

**Practical adoption path**  

1. **Proof‑of‑concept** – Clone the repo, run the supplied README steps, and test the core “add links to IMDb” and “push to Radarr/Sonarr” functions against a sandbox environment.  
2. **Integration wrapper** – Wrap the exposed functions in your service’s API layer (e.g., an Express route) and configure credentials for the external services you need.  
3. **Feature gating** – Enable only the required modules (e.g., rating aggregation or Trakt sync) to keep the dependency surface small.  
4. **CI/CD validation** – Add unit tests for your wrapper and run the project’s existing test suite to catch breaking changes.  
5. **Gradual rollout** – Deploy the wrapper to a staging environment, monitor logs for failed look‑ups, then gradually expose the new endpoints to a subset of users.

**Production readiness**  
- **Maturity**: Medium. The repo is actively maintained (last commit 2026‑06‑27), has 559 ★ and 75 forks, and covers many integration points, but the integration documentation is sparse and the exact setup steps can be opaque.  
- **Suitability**: Good for prototypes, internal tools, or services where rapid media‑metadata enrichment is needed. Before production use, perform a dependency audit (torrent/Usenet APIs, rate‑limit handling) and verify licensing/compliance for the linked content sources.  
- **Risk mitigation**: Conduct a small‑scale pilot, lock down external API keys, and implement fallback logic for services that may become unavailable. With those checks in place, the module can be hardened for production deployments.

### Русский

Purfview/IMDb‑Scout‑Mod — это открытый модуль, который автоматически ищет фильмы и сериалы на торрент‑треках, usenet, DDL‑ресурсах, субтитрах, стриминговых сервисах и пред‑базах, добавляя найденные ссылки к страницам IMDb и интегрируя контент в Radarr/Sonarr, Trakt, Plex/Jellyfin/Emby, а также обогащая их внешними рейтингами (Metacritic, Rotten Tomatoes, Letterboxd, Douban, Allocine) и темной темой для Reference View. Типичный сценарий внедрения — подключить модуль к существующей медиаплатформе в виде небольшого proof‑of‑concept, проверить README и настроить API‑ключи, после чего использовать готовый набор функций для ускорения разработки и стандартизации бэкенда. Готовность к production — средняя: проект уже имеет 559 звёзд, активные обновления и широкую функциональность, но требует проверки зависимостей и возможных затрат на интеграцию перед выводом в продакшн.

### 中文

**项目简介**  
Purfview/IMDb-Scout-Mod 是一款基于 JavaScript 的媒体信息聚合插件，能够自动在 torrent、Usenet、DDL、字幕站、流媒体平台、PreDB 等数百个资源网站上搜索电影/剧集，并将对应链接直接注入 IMDb 页面。插件还会同步外部评分（Metacritic、Rotten Tomatoes、Letterboxd、豆瓣、Allocine），为 Plex、Jellyfin、Emby 等媒体服务器提供指示器，支持一键添加至 Radarr/Sonarr、管理 Trakt 观看列表，并去除页面广告，同时提供暗色主题的 Reference View。

---

### 价值
- **复用基础设施**：无需自行实现资源搜索、评分聚合、媒体服务器对接等公共功能，直接复用成熟的搜索与数据整合逻辑。  
- **加速后端交付**：在内部项目中嵌入插件即可快速提供完整的媒体检索与管理 API，缩短开发周期。  
- **统一体验**：为用户统一的 IMDb 页面提供丰富的扩展信息和操作入口，提升产品的可用性和用户满意度。  

### 典型接入方式
1. **代码层面**  
   - 将仓库克隆或通过 npm 包引入（`npm i imdb-scout-mod`），在后端服务的启动脚本中初始化插件。  
   - 配置 `config.json`（或环境变量）指定需要对接的服务（Radarr、Sonarr、Trakt、Plex 等）以及要启用的评分源。  
2. **API 网关**  
   - 在现有的 API 网关（如 Kong、Traefik）上添加一个路由，将 IMDb 页面请求转发至插件的 HTTP 接口，插件返回已注入的 HTML。  
3. **小范围 PoC**  
   - 先在测试环境部署一个独立的 Node.js 实例，调用插件的搜索/添加接口，验证与内部媒体库（Radarr/Sonarr）和 Trakt 的交互是否符合预期。  
4. **CI/CD 集成**  
   - 将插件的依赖和配置写入 Dockerfile，配合现有的容器化流水线，实现“一键部署”。  

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★★☆☆ (中等) | 代码活跃，最近一次更新为 2026‑06‑27，拥有 559 ⭐ 和 75 🍴，社区活跃度尚可。 |
| **功能完整性** | ★★★★☆ | 已覆盖搜索、评分、媒体服务器指示、Trakt 管理、广告过滤等核心需求。 |
| **依赖风险** | ★★☆☆☆ | 依赖多个外部站点的 API/页面结构，若目标站点改版可能导致失效，需要定期监控。 |
| **部署复杂度** | ★★☆☆☆ | 插件本身是 Node.js 应用，部署相对简单，但与现有媒体服务器、Trakt 等的鉴权集成需要额外配置。 |
| **适用场景** | ★★★★★ | 原型、内部工具、媒体管理平台的功能扩展；生产环境建议在监控和回退机制完善后使用。 |
| **总体生产可用性** | 中等 | 适合作为 **原型/内部业务** 的加速组件，正式投产前需完成：<br>1. 小范围 PoC 验证搜索/添加流程；<br>2. 编写健康检查和错误报警；<br>3. 评估外部站点的稳定性与合规性。 |

**结论**：Purfview/IMDb-Scout-Mod 能显著降低媒体检索与管理功能的研发成本，适合作为内部服务的快速集成层。建议先在测试环境完成 PoC，确认与现有媒体库、Trakt 的对接细节后，再评估是否进入生产环境。

## 🧭 Practical evaluation

**Value:** Purfview/IMDb-Scout-Mod helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 559 GitHub stars
- 75 forks
- updated 2026-06-27
- primary language: JavaScript
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 55/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Purfview/IMDb-Scout-Mod) · [← Back to Video-editing](./README.md)</sub>
