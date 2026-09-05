# osmandapp/OsmAnd-iOS

[![Stars](https://img.shields.io/github/stars/osmandapp/OsmAnd-iOS?style=flat-square&color=yellow)](https://github.com/osmandapp/OsmAnd-iOS/stargazers) [![Forks](https://img.shields.io/github/forks/osmandapp/OsmAnd-iOS?style=flat-square&color=blue)](https://github.com/osmandapp/OsmAnd-iOS/network) [![Language](https://img.shields.io/badge/lang-Objective-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> OsmAnd for iOS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 341 |
| 🍴 **Forks** | 115 |
| 💻 **Language** | Objective-C++ |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
OsmAnd‑iOS is the iOS client for the popular offline mapping and navigation platform OsmAnd, written in Objective‑C++ and actively maintained (last update 2026‑06‑25). With 341 ⭐ on GitHub, it provides turn‑by‑turn routing, offline maps, and POI search for iPhone/iPad developers who need a feature‑rich, open‑source mapping solution.  

**Value**  
- **Rich offline capabilities** – full‑screen vector maps, routing, and points‑of‑interest that work without a data connection, ideal for field‑work, travel, or privacy‑focused apps.  
- **Open‑source and extensible** – you can customize UI, add custom map layers, or integrate with your own location services without licensing fees.  
- **Active community** – a moderate star/fork count and recent commits indicate ongoing bug fixes and feature updates.  

**Practical Adoption Path**  
1. **Clone the repository** and open the Xcode project; the README points to required sub‑modules (e.g., map data packs) that must be fetched manually.  
2. **Run the sample app** to verify the build environment (iOS 15+, Xcode 15).  
3. **Integrate** by either:  
   - Adding the OsmAnd‑iOS framework as a sub‑project in your own Xcode workspace, or  
   - Forking the repo and extracting the core mapping engine into a CocoaPod/Swift Package for tighter coupling.  
4. **Configure** map sources, routing profiles, and any required API keys (if you use online services).  
5. **Test** offline map loading and routing on target devices, then iterate on UI/feature customisation.  

**Production Readiness**  
- **Maturity:** Medium. The codebase is stable enough for prototypes or internal tools, but the integration surface is not fully documented, so expect some engineering effort to understand build scripts and data handling.  
- **Dependencies:** Relies on native Objective‑C++ and third‑party map data packs; ensure you have the correct toolchain and monitor updates for breaking changes.  
- **Maintenance:** Regular commits suggest ongoing support, yet you should lock to a specific tag or commit for production to avoid unexpected regressions.  

**Bottom Line**  
OsmAnd‑iOS offers a powerful, offline‑first mapping stack that can be integrated into iOS apps with moderate effort. It is suitable for internal or prototype deployments, but teams should perform a focused integration test and establish a version‑pinning strategy before committing to production use.

### Русский

OsmAnd‑iOS — это открытая iOS‑версия популярного навигационного клиента OsmAnd, написанная на Objective‑C/Objective‑C++. Она позволяет встраивать офлайн‑карты, маршрутизацию и поиск POI в собственные мобильные приложения или использовать готовый клиент для внутренних тестов и прототипов. Проект имеет средний уровень готовности к production: активные обновления, 300+ звёзд и 100+ форков, но путь интеграции не документирован — перед внедрением рекомендуется проверить зависимости, собрать пример проекта и оценить затраты на настройку.

### 中文

**项目简介**  
OsmAnd‑iOS 是 OsmAnd 在 iOS 平台的官方实现，提供离线地图、导航、轨迹记录等功能，采用 Objective‑C++ 编写，社区活跃（≈340 星、115 叉）。

**价值**  
- **离线可靠**：地图、路网、POI 均可完整离线使用，适合网络不稳定或对隐私有要求的场景。  
- **跨平台一致性**：与 Android 版 OsmAnd 功能基本保持一致，便于在多设备间统一用户体验。  
- **可定制**：源码开放，可根据业务需求裁剪插件、添加自定义图层或集成企业内部的 GIS 数据。

**典型接入方式**  
1. **源码集成**：将项目 clone 到本地，使用 Xcode 打开 `OsmAnd.xcodeproj`，在目标项目中通过 CocoaPods（或手动）引入 `OsmAndCore` 与 UI 模块。  
2. **库化使用**：编译生成的 `.framework`（或 `.a`）文件加入到自己的 iOS 应用中，按需调用 `OsmAndMapViewController`、`OsmAndRoutingEngine` 等公开 API。  
3. **插件扩展**：在 `OsmAnd` 项目中添加自定义 `OsmAndPlugin`，实现业务特定的地图渲染或导航逻辑，然后在主工程中注册插件。

**生产可用性**  
- **成熟度**：项目已持续维护至 2026‑06‑25，社区活跃度中等，代码质量和文档相对完整，适合作为内部原型或面向特定用户的正式产品。  
- **风险**：集成文档较为分散，缺少一键式 SDK 打包方案，首次接入需要手动梳理依赖（Objective‑C++、CMake、Boost 等），并进行编译环境验证。  
- **建议**：在正式上线前完成以下检查：  
  1. **编译兼容性**：确认项目在目标 Xcode 版本和 iOS SDK 上能够成功编译。  
  2. **功能覆盖**：验证离线地图、路径规划、实时定位等核心功能在实际设备上的表现。  
  3. **维护成本**：评估后续升级（如新 iOS 版本、地图数据更新）所需的人力投入。  

总体而言，OsmAnd‑iOS 具备中等生产就绪度，适合作为内部工具或面向对离线导航有强需求的业务的技术基座，只要做好前期的集成验证和后期维护规划，即可投入生产使用。

## 🧭 Practical evaluation

**Value:** osmandapp/OsmAnd-iOS may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 341 GitHub stars
- 115 forks
- updated 2026-06-25
- primary language: Objective-C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 54/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/osmandapp/OsmAnd-iOS) · [← Back to Mobile](./README.md)</sub>
