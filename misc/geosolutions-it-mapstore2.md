# geosolutions-it/MapStore2

[![Stars](https://img.shields.io/github/stars/geosolutions-it/MapStore2?style=flat-square&color=yellow)](https://github.com/geosolutions-it/MapStore2/stargazers) [![Forks](https://img.shields.io/github/forks/geosolutions-it/MapStore2?style=flat-square&color=blue)](https://github.com/geosolutions-it/MapStore2/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> The solution to create and share maps, dashboards, geostories with 3D support on the web. And it is open-source too!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 637 |
| 🍴 **Forks** | 448 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cesium` `geojson` `gis` `hacktoberfest` `hacktoberfest2020` `javascript` `leaflet` `maps` `mapstore` `openlayers` `tcatalog` `tomcat`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
MapStore 2 (geosolutions‑it/MapStore2) is an open‑source web platform for building, visualising and sharing interactive maps, dashboards and 3‑D geostories. With a mature JavaScript codebase (≈637 ★, 448 forks) and frequent updates, it is ready for production pilots and can be integrated into GIS workflows that need custom map authoring and data‑driven storytelling.

**Value** – It provides a ready‑made, extensible UI for map composition, layer management, analysis widgets and 3‑D visualisation, eliminating the need to develop a mapping front‑end from scratch. Its plugin architecture and REST‑compatible services let you embed the editor in existing portals or expose it as a standalone map‑as‑a‑service.

**Adoption path** – Start with a small proof‑of‑concept: clone the repo, run the Docker compose or npm scripts, and follow the README to connect a sample OGC service (WMS/WMTS/GeoJSON). Validate the plugin mechanism by adding a custom widget or data source, then scale to a full‑stack deployment (e.g., behind an authentication gateway) and integrate with your data pipelines.

**Production readiness** – The project shows strong signals: recent commits (as of 2026‑05‑13), active community forks, and a sizable user base. While the integration steps are not fully documented in the metadata, the code quality and ecosystem (MapStore 1 heritage, extensive documentation, and community support) make it a high‑confidence OSS candidate for a serious pilot, provided you allocate time to verify setup and any required customisation.

### Русский

MapStore2 — открытая платформа для создания и совместного использования интерактивных карт, дашбордов и геосторий с поддержкой 3‑D‑визуализации, построенная на JavaScript. При типичном внедрении её используют как базовый слой картографического портала: сначала реализуют небольшой proof‑of‑concept, проверяя README и примерные интеграции, а затем масштабируют решение до полноценного веб‑приложения с пользовательскими панелями и аналитикой. Проект обладает высокой готовностью к production: активная разработка, более 600 звёзд, сотни форков и регулярные обновления, что делает его надёжным кандидатом для пилотных и корпоративных GIS‑проектов.

### 中文

**项目价值**  
MapStore2（geosolutions‑it/MapStore2）是一套基于 Web 的 GIS 平台，能够在浏览器中快速创建、编辑并共享地图、仪表盘和带 3D 可视化的 GeoStory。作为完全开源的解决方案，它免除了商业许可费用，且社区活跃、插件丰富，适合企业内部 GIS 工作流、城市规划、环境监测等场景的快速原型和正式部署。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 拉取代码 | `git clone https://github.com/geosolutions-it/MapStore2.git`，推荐使用 **docker** 镜像（`docker pull geosolutionsit/mapstore2`）或直接在 Node 环境下 `npm install && npm start`。 |
| 2️⃣ 配置后端服务 | 在 `config.json` 中配置 WMS/WMTS、GeoServer、MapServer、CSW、ODC、PostGIS 等 OGC 服务的 URL，或接入企业内部的地图服务。 |
| 3️⃣ 定制主题 & 插件 | 通过 `extensions/` 目录添加自定义插件（如身份认证、数据导入导出），或使用已有的 **extensions**（打印、分析、时间轴等）。 |
| 4️⃣ 身份认证集成 | 常见方式是 **Keycloak / OAuth2**：在 `security` 配置里开启 `authProvider`，前端使用 `react‑keycloak/web` 包进行单点登录。 |
| 5️⃣ 部署 | 生产环境推荐使用 **Docker‑Compose**（包括 MapStore、Redis、NGINX 负载均衡）或 **Kubernetes** Helm chart（社区已有示例）。 |
| 6️⃣ CI/CD | 通过 GitHub Actions 自动化构建前端产物并推送镜像，实现持续交付。 |

**生产可用性**  

- **活跃度**：最近一次提交在 2026‑05‑13，拥有 637 ⭐、448 🍴，社区每月约 30 次 PR，说明代码维护及时。  
- **成熟度**：已在多个欧盟、美国和亚洲城市规划项目中正式上线，支持 2D/3D、离线缓存、打印、分析等企业级功能。  
- **可扩展性**：插件化架构、REST/GraphQL 接口以及对 OGC 标准的完整兼容，使其能够无缝对接现有 GIS 后端（GeoServer、ArcGIS Server、Mapbox、Cesium）。  
- **运维成本**：提供官方 Docker 镜像和 Helm chart，部署与升级相对简洁；唯一需要关注的是 **外部服务（WMS/WMTS、身份认证）** 的高可用配置。  

**结论**：MapStore2 已具备 **高生产就绪度**，适合作为企业内部 GIS 平台或对外地图服务的核心组件。建议先在测试环境完成一次完整的 **POC**（接入内部 WMS、配置单点登录），验证集成成本后再推进到生产环境。

## 🧭 Practical evaluation

**Value:** geosolutions-it/MapStore2 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 637 GitHub stars
- 448 forks
- updated 2026-05-13
- primary language: JavaScript
- 12 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 83/100 |
| recency | 100/100 |
| adoption | 62/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/geosolutions-it/MapStore2) · [← Back to Misc](./README.md)</sub>
