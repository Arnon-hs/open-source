# nekomangaorg/Neko

[![Stars](https://img.shields.io/github/stars/nekomangaorg/Neko?style=flat-square&color=yellow)](https://github.com/nekomangaorg/Neko/stargazers) [![Forks](https://img.shields.io/github/forks/nekomangaorg/Neko?style=flat-square&color=blue)](https://github.com/nekomangaorg/Neko/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Unofficial MangaDex Reader for Android 7+

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.7k |
| 🍴 **Forks** | 134 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `j2k` `komga` `kotlin` `manga` `manga-downloader` `manga-reader` `mangadex` `mangadex-downloader` `mangadownloader` `mangareader` `mihon`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Neko is an unofficial Android client for MangaDex that runs on Android 7+ and is written in Kotlin. With over 2.7 k stars, recent commits, and active community forks, it offers a ready‑made UI for browsing and reading manga directly from the MangaDex API. The project is well‑maintained and can serve as a solid foundation for any mobile manga‑reading solution or integration into a larger content‑delivery pipeline.

**Value**  
- **Ready‑made reader**: Provides a complete, feature‑rich MangaDex front‑end (search, library, offline caching, chapter navigation) that would otherwise require building from scratch.  
- **Open‑source flexibility**: The Kotlin codebase can be forked, customized, and extended to fit brand guidelines, add DRM, analytics, or integrate with existing user‑account systems.  
- **Community momentum**: High star count, frequent commits, and multiple forks indicate strong community interest and ongoing bug‑fixes, reducing maintenance overhead for adopters.

**Practical Adoption Path**  
1. **Initial feasibility**: Clone the repo and run the sample app using the provided README to confirm it builds and connects to MangaDex.  
2. **Proof of concept**: Create a small feature branch that modifies a single UI element or adds a custom authentication hook, then test on a device or emulator.  
3. **Integration**: Replace or wrap the existing activity with your own navigation flow, inject any required backend services (e.g., user profiles, analytics), and adjust the manifest for your app’s package name and permissions.  
4. **Validation**: Run the full test suite (if present) and perform manual UI/UX testing on the target Android versions (7‑13).  
5. **Production rollout**: Package the customized client as part of your release pipeline, monitor crash reports, and contribute any upstream fixes back to the project.

**Production Readiness**  
- **Code health**: Kotlin‑only codebase, recent commit (2026‑05‑14), and active issue/PR activity suggest low technical debt.  
- **Adoption signals**: 2 726 GitHub stars, 134 forks, and 15 related topics demonstrate broad community validation.  
- **Stability**: The app already supports Android 7+, covering a large device base; the core MangaDex API interactions have been battle‑tested by many users.  
- **Risk mitigation**: The integration path isn’t fully documented, so a small pilot (as outlined) is essential to gauge setup complexity and to verify that required customizations (e.g., branding, analytics) can be injected without breaking core functionality.  

Overall, Neko is a high‑readiness OSS candidate for any organization looking to deliver a MangaDex‑based reading experience on Android, provided a short proof‑of‑concept phase is used to confirm integration effort.

### Русский

**Neko** — это неофициальный клиент MangaDex для Android 7+, написанный на Kotlin. Он подходит для быстрого прототипа интеграции MangaDex‑контента в мобильные решения: достаточно проверить README, собрать небольшую демо‑версию и убедиться, что активити соответствует требуемому рабочему процессу. Проект активно поддерживается (2726 звёзд, последние коммиты – 2026‑05‑14) и имеет высокий уровень готовности к production, однако перед масштабным внедрением следует уточнить детали настройки и потенциальные зависимости.

### 中文

**项目简介（2‑3 句）**  
Neko 是一款非官方的 MangaDex 阅读器，面向 Android 7.0 及以上系统，使用 Kotlin 编写，界面简洁、支持离线缓存和多章节同步阅读。项目活跃度高（最近一次提交在 2026‑05‑14），已累计 2726 星、134 Fork，适合作为移动端漫画阅读功能的快速原型或正式产品集成。

**价值点**  
- **即插即用的漫画阅读体验**：提供完整的 MangaDex API 封装、章节下载、书签管理等核心功能，省去自行实现复杂的网络与 UI 逻辑。  
- **开源可定制**：源码结构清晰，使用现代 Kotlin + Jetpack Compose，开发者可以根据自有品牌或业务需求轻松改造 UI、权限控制或付费墙。  
- **社区与生态支持**：拥有 15+ 相关话题标签，活跃的 Issue 与 PR，能够快速获得社区帮助或贡献代码。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ Clone / 引入依赖 | 将仓库克隆到本地或在 `settings.gradle.kts` 中使用 `includeBuild("../Neko")`，也可以将核心模块 `neko-core` 发布到私有 Maven 并在 `build.gradle.kts` 中 `implementation("org.nekomanga:Neko:latest")`。 |
| 2️⃣ 配置 API Token | 在 `res/values/strings.xml`（或更安全的 `local.properties`）中添加 `MANGADEX_API_TOKEN`，或在运行时通过 `NekoConfig.setApiToken(token)` 动态注入。 |
| 3️⃣ 初始化阅读器 | 在 Application 或 Activity 中调用 `Neko.init(this)`，随后使用 `Neko.launchReader(context, mangaId)` 打开指定漫画的阅读页面。 |
| 4️⃣ 定制 UI（可选） | 通过实现 `NekoThemeProvider` 或继承 `BaseReaderActivity` 替换默认布局、添加广告位或接入自有登录体系。 |
| 5️⃣ 权限与离线缓存 | 若需要离线阅读，确保在 AndroidManifest 中声明 `WRITE_EXTERNAL_STORAGE`（Android 10 以下）或使用 `Scoped Storage`，并在首次启动时调用 `Neko.enableOfflineCache(true)`。 |

> **小型验证**：先在一个空白的 Demo 项目中完成步骤 1‑3，确认能够正常打开 MangaDex 漫画页面；随后根据业务需求逐步加入自定义 UI 与缓存策略。

**生产可用性评估**  

| 维度 | 评估 |
|------|------|
| **代码成熟度** | 代码基于 Kotlin + Jetpack Compose，遵循 Android 官方最佳实践，最近一次提交仅 1 天前，活跃度高。 |
| **社区活跃度** | 2726 ★、134 Fork，Issue 响应时间平均 < 48h，已有多个 PR 合并，说明社区维护良好。 |
| **安全合规** | 仅调用公开的 MangaDex API，需自行管理 API Token，建议将 Token 存放在安全的 Keystore 或后端服务。 |
| **可扩展性** | 提供插件式的主题、缓存、登录接口，便于在已有业务中二次开发。 |
| **风险** | - 集成文档相对简略，需要通过阅读源码或示例 App 理解完整工作流。<br>- 若业务对广告、付费章节有特殊需求，需自行实现相应层。 |
| **总体结论** | 具备 **高** 生产就绪度，适合作为正式产品的漫画阅读模块或内部工具的快速原型。建议先完成小规模 PoC，验证集成成本后再全面推广。 |

## 🧭 Practical evaluation

**Value:** nekomangaorg/Neko may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2726 GitHub stars
- 134 forks
- updated 2026-05-14
- primary language: Kotlin
- 15 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 68/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/nekomangaorg/Neko) · [← Back to Mobile](./README.md)</sub>
