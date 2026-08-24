# deroverda/recommended-radio-streams

[![Stars](https://img.shields.io/github/stars/deroverda/recommended-radio-streams?style=flat-square&color=yellow)](https://github.com/deroverda/recommended-radio-streams/stargazers) [![Forks](https://img.shields.io/github/forks/deroverda/recommended-radio-streams?style=flat-square&color=blue)](https://github.com/deroverda/recommended-radio-streams/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> Internet radio stations I actually listen to - underground electronic, freeform, jazz, ambient, and weird stuff. Direct stream URLs and the apps to play them.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 301 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`awesome-list` `icecast` `internet-radio` `music-discovery` `radio` `radio-stations` `radio-streams` `shoutcast` `streaming-audio` `webradio`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
`deroverda/recommended-radio-streams` is a curated collection of direct URLs for underground electronic, free‑form, jazz, ambient and other “weird” internet radio stations, together with the client apps that can play them. Although the repo is essentially a lightweight database of stream links, it can serve as a ready‑made data source for prototypes or internal tools that need to query, filter, or display radio‑stream metadata.  

**Value**  
The project removes the tedious “search‑and‑copy‑URL” step for developers building music‑oriented apps, giving teams a pre‑populated, searchable list of high‑quality streams that can be persisted in a database or used directly in UI components. Because the data is already structured (station name, genre, stream URL, player recommendations), it speeds up the data‑access layer of any radio‑oriented service and reduces custom plumbing.  

**Practical adoption path**  
1. **Clone the repo** and inspect the `streams.json` (or equivalent) file to understand the schema.  
2. **Import the data** into your preferred datastore (SQL, NoSQL, or even a simple CSV import) using a one‑off script; the format is straightforward, so mapping to your own tables is trivial.  
3. **Wrap a query layer** (e.g., a tiny REST API or GraphQL resolver) that filters by genre, language, or popularity, then plug it into your front‑end player component.  
4. **Validate** the stream URLs in your environment (some stations may geo‑block or change URLs) before shipping.  

**Production readiness**  
The repository is moderately production‑ready: it has recent activity (last updated 2026‑06‑30), 301 GitHub stars, and a modest fork count, indicating community interest. However, the integration signals are sparse—there is no formal schema, SDK, or CI pipeline—so teams should treat it as a prototype‑grade data source. Before moving to production, perform a small integration proof‑of‑concept, verify the reliability of each stream, and add monitoring/health‑checks for URL availability. With those safeguards, the project is suitable for internal tools or MVPs, but it may require additional maintenance (e.g., periodic URL validation) for long‑term, customer‑facing deployments.

### Русский

Резюме проекта deroverda/recommended-radio-streams:

Проект deroverda/recommended-radio-streams представляет собой коллекцию интернет-радиостанций, которые я действительно слушаю, включая электронную музыку, джаз, ампанент и экзотические жанры. Это помогает командам сохранять, запросить и перемещать данные с минимальным количеством настраиваемого кода.

Проект предназначен для управления persistence, ускорения доступа к данным и прототипирования приложений с базой данных. Он подойдет для прототипирования или внутренних рабочих процессов, но требует проверки настроек и поддержки перед выпуском в производство.

Проект имеет средний уровень готовности к производству (Medium) из-за необходимости ручной проверки перед внедрением.

### 中文

**项目简介**  
deroverda/recommended-radio-streams 收录了作者平时收听的地下电子、自由即兴、爵士、氛围以及各种怪试风格的网络电台，提供了直接的流媒体 URL 以及常用播放器的配置信息，方便快速接入和收听。

**价值**  
- **统一目录**：把分散的电台资源集中在一个仓库，省去手动搜索、验证 URL 的时间。  
- **即插即用**：提供标准的流媒体链接，可直接在 VLC、mpv、MPRIS、Web 播放器等工具中使用。  
- **开源可定制**：企业或个人可基于列表自行扩展、过滤或与内部系统（如音乐推荐、背景音效服务）集成。

**典型接入方式**  
1. **直接引用**：在代码或配置文件中读取 `streams.json`（或类似的列表文件），取出 `url` 字段并交给播放器 SDK（如 HTML5 `<audio>`、ExoPlayer、GStreamer）。  
2. **自动化同步**：使用 CI/CD 脚本定期 `git pull` 最新仓库内容，将列表同步到内部数据库或缓存（Redis、MongoDB），供后端查询。  
3. **包装 API**：在微服务层面封装一个轻量的查询接口（REST/GraphQL），返回符合标签（genre、country）的电台 URL，供前端或移动端调用。

**生产可用性**  
- **成熟度**：仓库已有 301 星、11 Fork，最近一次提交在 2026‑06‑30，活跃度尚可。  
- **适用场景**：适合原型开发、内部工具或娱乐类产品的快速集成；对外正式服务仍需自行完成以下检查：  
  - **版权/合法性**：确认所列电台在目标地区的播放许可。  
  - **可用性监控**：流媒体 URL 可能随时失效，需要实现健康检查或 fallback。  
  - **依赖管理**：项目本身仅是数据集合，无运行时依赖，但接入方的播放器或数据库层需做好版本兼容。  
- **生产等级**：评估为 **Medium**——在经过上述验证与监控后，可用于内部业务或低风险的面向用户的功能；若要支撑大规模、关键业务，建议自行构建冗余缓存、自动更新与错误恢复机制后再投入生产。

## 🧭 Practical evaluation

**Value:** deroverda/recommended-radio-streams helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 301 GitHub stars
- 11 forks
- updated 2026-06-30
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 54/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/deroverda/recommended-radio-streams) · [← Back to Misc](./README.md)</sub>
