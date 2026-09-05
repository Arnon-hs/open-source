# maplibre/maplibre-native

[![Stars](https://img.shields.io/github/stars/maplibre/maplibre-native?style=flat-square&color=yellow)](https://github.com/maplibre/maplibre-native/stargazers) [![Forks](https://img.shields.io/github/forks/maplibre/maplibre-native?style=flat-square&color=blue)](https://github.com/maplibre/maplibre-native/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> MapLibre Native - Interactive vector tile maps for iOS, Android and other platforms.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2k |
| 🍴 **Forks** | 547 |
| 💻 **Language** | C++ |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`maplibre` `maps` `vector-tiles`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
MapLibre Native is an open‑source library that renders interactive vector‑tile maps on iOS, Android and other platforms using C++. It provides a high‑performance, fully offline‑capable map engine that can be embedded in native mobile apps and cross‑platform frameworks. The project is actively maintained (last commit 2026‑06‑24) and has a modest community footprint (≈2027 ★, 547 forks).  

**Value proposition**  
MapLibre Native lets teams ship rich, vector‑based maps without tying themselves to proprietary SDKs or costly licensing. Because the library works directly with raw vector tiles, developers can control data pipelines, cache tiles locally, and integrate custom styling or data layers, reducing the amount of custom plumbing needed for map persistence and query.  

**Practical adoption path**  

| Step | What to do | Why it matters |
|------|------------|----------------|
| 1️⃣ Evaluate fit | Clone the repo, build the C++ core for your target (iOS/Android) using the provided CMake scripts, and run the sample apps. | Confirms that the build system works with your toolchain and that the API surface matches your needs. |
| 2️⃣ Integrate | Add the compiled library (or use the pre‑built binaries) to your mobile project, replace any existing map SDK calls with MapLibre Native equivalents, and point the map source to your vector‑tile server or offline MBTiles bundle. | Provides a drop‑in replacement for map rendering while keeping your existing data backend. |
| 3️⃣ Test persistence & styling | Verify tile caching, offline usage, and custom style JSON loading; write unit tests for map‑related data queries. | Guarantees that the library meets performance and reliability expectations before scaling. |
| 4️⃣ Harden & monitor | Set up CI to rebuild the native library on each OS update, monitor the upstream repo for breaking changes, and pin a specific tag/commit in your dependency lockfile. | Reduces risk from the “sparse integration signals” noted in the metadata. |

**Production readiness**  
- **Maturity:** Medium. The codebase is actively maintained and compiles cleanly, but the integration documentation is thin, so you’ll need to perform a manual validation of the build and runtime behavior.  
- **Best suited for:** Prototypes, internal tools, or products where you can allocate time for a modest integration effort and ongoing dependency monitoring.  
- **Risks:** Lack of detailed onboarding guides and limited community‑generated integration examples mean you may encounter platform‑specific quirks (e.g., Gradle vs. CocoaPods packaging). Conduct a small‑scale pilot, verify build stability across iOS/Android versions, and establish a process for tracking upstream changes before committing to a production rollout.

### Русский

MapLibre Native – это кроссплатформенная библиотека на C++ для отображения интерактивных векторных тайлов на iOS, Android и других устройствах, позволяющая быстро интегрировать карты без необходимости разрабатывать собственный рендеринг. Типичный сценарий – команда добавляет карту в мобильное приложение, используя готовый набор API для загрузки, кэширования и отрисовки тайлов, что ускоряет прототипирование и упрощает работу с геоданными. Готовность к production – средняя: проект стабилен и активно поддерживается, но путь интеграции не полностью документирован, поэтому перед выпуском в продакшн требуется проверка настроек и оценка затрат на внедрение.

### 中文

**项目简介**  
MapLibre Native 是一套跨平台的原生 SDK（iOS、Android 以及其他平台），用于在移动端渲染交互式矢量瓦片地图。它基于开源的 MapLibre GL，使用 C++ 实现高性能渲染，兼容常见的矢量瓦片服务（如 Mapbox、TileServer‑GL、自建 MBTiles 等）。

**价值主张**  
- **统一的原生地图能力**：一次编写代码即可在 iOS 与 Android 上获得同等的渲染效果，免去维护两套不同的地图实现。  
- **低耦合、易扩展**：仅提供渲染层，业务方可以自行决定数据来源（本地数据库、网络 API、缓存等），从而在不增加额外 “管道” 的情况下实现地图持久化、查询和更新。  
- **成本可控的原型与内部工具**：对需要快速展示矢量瓦片的原型或内部业务系统，MapLibre Native 能在几行代码内完成集成，显著缩短开发周期。

**典型接入方式**  
1. **依赖引入**  
   - **iOS**：通过 CocoaPods (`pod 'MapLibre'`) 或 Swift Package Manager 添加 `MapLibre` 包。  
   - **Android**：在 `build.gradle` 中加入 `implementation 'org.maplibre.gl:android-sdk:<version>'`。  
   - **其他平台**（如 Qt、React Native）：使用对应的 C++ 库或社区桥接层。  
2. **初始化地图**  
   ```swift
   // iOS 示例
   let mapView = MapView(frame: view.bounds)
   mapView.mapboxMap.styleURI = StyleURI(url: URL(string: "https://example.com/tiles/style.json")!)
   view.addSubview(mapView)
   ```
   ```kotlin
   // Android 示例
   val mapView = MapView(this)
   mapView.getMapboxMap().loadStyleUri("https://example.com/tiles/style.json")
   setContentView(mapView)
   ```
3. **数据接入**  
   - 直接使用公开的矢量瓦片 URL（HTTP/HTTPS）。  
   - 若需离线或自定义数据，可将 MBTiles、SQLite 或自建的矢量瓦片服务挂载为本地资源，然后在 `Style` 中引用。  
4. **功能扩展**  
   - 通过 `AnnotationManager`、`Layer`、`Source` API 添加标记、热力图、路径规划等交互层。  
   - 如需持久化用户绘制的要素，可自行将要素序列化存入本地数据库（Realm、SQLite 等），再通过 SDK 的 `addGeoJSONSource` 进行加载。

**生产可用性**  
- **成熟度**：项目活跃，2026‑06‑24 最近一次提交，拥有约 2027 星、547 fork，社区贡献持续。  
- **适用场景**：非常适合原型、内部工具以及对地图渲染质量要求高但业务逻辑相对简单的移动应用。  
- **风险与注意事项**  
  - **集成路径不够明确**：官方文档对跨平台（如 Qt、React Native）支持较少，需自行评估包装成本。  
  - **依赖维护**：SDK 依赖 C++ 渲染引擎，升级时需检查与项目中已有的原生库冲突。  
  - **离线/自定义数据**：需要自行实现本地瓦片缓存或 MBTiles 读取逻辑，SDK 本身不提供完整的离线解决方案。  
- **结论**：在做好依赖审查和离线数据方案的前提下，MapLibre Native 可在生产环境中稳定运行，尤其适用于对渲染性能有要求且希望保持对地图数据来源完全控制的团队。

## 🧭 Practical evaluation

**Value:** maplibre/maplibre-native helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2027 GitHub stars
- 547 forks
- updated 2026-06-24
- primary language: C++
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 70/100 |
| topics | 38/100 |
| outlook | 68/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 70/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/maplibre/maplibre-native) · [← Back to Mobile](./README.md)</sub>
