# wikimedia/apps-android-wikipedia

[![Stars](https://img.shields.io/github/stars/wikimedia/apps-android-wikipedia?style=flat-square&color=yellow)](https://github.com/wikimedia/apps-android-wikipedia/stargazers) [![Forks](https://img.shields.io/github/forks/wikimedia/apps-android-wikipedia?style=flat-square&color=blue)](https://github.com/wikimedia/apps-android-wikipedia/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 📱The official Wikipedia app for Android!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 809 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `android-app` `coroutines` `java` `kotlin` `mediawiki` `mediawiki-api` `rest-api` `viewmodel` `wiki` `wikipedia` `wikipedia-android`

## 🎯 Categories

Backend · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *wikimedia/apps-android-wikipedia* repository houses the official Wikipedia Android client, a mature Kotlin‑based mobile app that leverages Wikimedia’s shared service infrastructure. With over 2,900 stars, frequent commits, and a robust ecosystem, it offers teams a ready‑made backend stack for rapid API‑driven feature delivery without reinventing common services.

**Value**  
- **Infrastructure reuse** – The app consumes Wikimedia’s standardized APIs, authentication, caching, and analytics layers, letting teams focus on product‑specific UI/UX instead of building and maintaining backend services.  
- **Speed to market** – By plugging into proven service contracts (REST/GraphQL, SDKs, CLI tools), developers can ship new API‑backed features or experiment with content‑driven experiences in days rather than weeks.  
- **Pattern standardization** – The codebase follows Wikimedia’s service patterns (error handling, rate limiting, telemetry), providing a reference implementation for other Android projects that need the same reliability and scalability.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the Gradle build, and explore the `api` module to understand the exposed endpoints and SDK usage.  
2. **Integration** – Replace the default Wikipedia data source with your own backend by implementing the same `Repository` interfaces or by extending the existing `NetworkService` classes.  
3. **Customization** – Add or override UI components, inject feature flags, and configure the built‑in analytics to align with your product’s metrics.  
4. **Testing & Deployment** – Use the existing CI pipelines as a template, run unit/instrumentation tests, and deploy the APK via your standard release process.

**Production Readiness**  
- **Activity & Community** – The project is actively maintained (last commit 2026‑05‑13), has strong adoption (2926 stars, 809 forks), and is backed by Wikimedia’s engineering team.  
- **Stability** – The codebase follows semantic versioning, includes comprehensive test suites, and runs on modern Android SDKs, indicating a high level of reliability for production use.  
- **Risk Considerations** – While no immediate metadata or licensing issues are evident, a final review of the Apache‑2.0 license compliance, security audit reports, and maintainer responsiveness is recommended before large‑scale rollout.  

Overall, *wikimedia/apps-android-wikipedia* is a production‑grade, well‑documented foundation for Android teams that want to accelerate API‑centric feature development while benefiting from Wikimedia’s proven backend services.

### Русский

**Wikimedia/apps-android-wikipedia** — официальное Android‑приложение Википедии, которое предоставляет готовую инфраструктуру бэкенда (API, SDK, CLI) и набор проверенных сервисных паттернов, позволяя командам быстро запускать собственные API‑сервисы без необходимости «изобретать велосипед». Типичный сценарий — подключение к существующим сервисам Википедии, переиспользование их аутентификации, кеширования и аналитики, что ускоряет вывод продукта на рынок и стандартизирует архитектуру. Проект находится в высокой готовности к production: активные коммиты, более 2900 звёзд на GitHub, широкое принятие в экосистеме и поддержка Kotlin, однако перед внедрением требуется окончательная проверка лицензии, безопасности и наличия активных мейнтейнеров.

### 中文

**项目简介**  
Wikimedia 官方的 Android 版 Wikipedia 应用（`wikimedia/apps-android-wikipedia`），使用 Kotlin 开发，是一款功能完整、界面友好的移动端阅读客户端。

**价值**  
- **复用后端基础设施**：直接使用 Wikimedia 已经搭建好的 API、缓存、认证等服务，避免团队自行实现通用的后端功能。  
- **加速 API 服务交付**：通过现成的 SDK/CLI 调用 Wikipedia API，可快速构建搜索、内容展示、离线阅读等业务。  
- **统一服务模式**：遵循 Wikimedia 的服务治理、监控和安全规范，为内部新项目提供一致的后端实现参考。

**典型接入方式**  
1. **依赖 SDK**：在 Android 项目中通过 Gradle 添加 `org.wikipedia:app`（或相应的 Maven 坐标）即可获得 API 客户端。  
2. **使用公开 API**：直接调用 `https://en.wikipedia.org/api/rest_v1/` 等 REST 接口，配合官方提供的 Kotlin 示例代码。  
3. **CLI/脚本**：利用项目中提供的 `wikimedia-cli`（若有）进行批量数据抓取或离线包生成，适用于后台服务或 CI 流程。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13 最近一次提交，2926 ⭐、809 🍴，社区活跃，Bug 反馈和 PR 处理速度快。  
- **成熟度**：已在全球数亿用户的正式 Wikipedia Android 客户端中运行，具备完整的日志、崩溃上报和 A/B 测试框架。  
- **风险**：暂无重大元数据风险；仍需在正式使用前完成许可证合规审查、第三方库安全扫描以及维护者联系方式确认。  

综上，该项目具备高生产就绪度，适合作为内部移动业务的后端服务基线或直接嵌入到自研 Android 应用中。

## 🧭 Practical evaluation

**Value:** wikimedia/apps-android-wikipedia helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2926 GitHub stars
- 809 forks
- updated 2026-05-13
- primary language: Kotlin
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 74/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 73/100 |
| production | 73/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/wikimedia/apps-android-wikipedia) · [← Back to Backend](./README.md)</sub>
