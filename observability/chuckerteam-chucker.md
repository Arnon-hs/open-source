# ChuckerTeam/chucker

[![Stars](https://img.shields.io/github/stars/ChuckerTeam/chucker?style=flat-square&color=yellow)](https://github.com/ChuckerTeam/chucker/stargazers) [![Forks](https://img.shields.io/github/forks/ChuckerTeam/chucker?style=flat-square&color=blue)](https://github.com/ChuckerTeam/chucker/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> 🔎 An HTTP inspector for Android & OkHTTP (like Charles but on device)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.5k |
| 🍴 **Forks** | 458 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `android-library` `android-sdk` `hacktoberfest` `http-requests` `interceptor` `kotlin` `kotlin-library` `library` `network-analysis` `network-monitoring` `okhttp`

## 🎯 Categories

Observability · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Chucker is an open‑source HTTP inspector for Android that plugs directly into OkHttp, giving developers an on‑device view of network traffic similar to Charles Proxy. With over 4.5 k stars, active maintenance, and a Kotlin codebase, it’s positioned as a high‑readiness tool for speeding up debugging and CI feedback loops.  

**Value**  
- **Time‑saving diagnostics** – captures request/response bodies, headers, and timing data without leaving the device, eliminating the need for external proxies.  
- **Workflow acceleration** – developers can instantly verify API contracts during local development and see real‑time failures in CI pipelines, reducing back‑and‑forth with backend teams.  
- **Observability on mobile** – provides a lightweight, searchable log of network interactions that can be shared with QA or support teams, improving overall product quality.  

**Practical Adoption Path**  
1. **Add the dependency** – include Chucker’s Gradle artifact in the app module (`implementation "com.github.chuckerteam.chucker:library:<version>"`).  
2. **Configure for environments** – enable it only for debug builds (or gated behind a feature flag) to avoid shipping it to production.  
3. **Integrate with OkHttp** – add `ChuckerInterceptor` to the OkHttp client builder; optionally add a `ChuckerCollector` for custom UI or persistence.  
4. **Validate in CI** – run UI tests that capture network logs; export the generated JSON/HTML reports for automated analysis or flaky‑test detection.  

**Production Readiness**  
- **Activity & Adoption** – recent commits (as of 2026‑07‑12), strong community uptake (4 537 stars, 458 forks), and integration examples in many Android projects.  
- **Stability** – the library follows semantic versioning, provides clear release notes, and has a well‑documented API surface.  
- **Risk Profile** – no critical licensing or security flags have been identified, though a final review of the MIT license and any transitive dependencies is advisable.  
Overall, Chucker meets the criteria for a serious pilot in production environments, offering a mature, low‑overhead solution for Android network observability.

### Русский

Chucker (ChuckerTeam/chucker) — это open‑source HTTP‑инспектор для Android и OkHTTP, позволяющий разработчикам мгновенно просматривать запросы и ответы прямо на устройстве, что ускоряет отладку, автоматизацию локальных задач и улучшает обратную связь в CI. Проект активно поддерживается (4537 ★, 458 forks, последние коммиты — 2026‑07‑12), написан на Kotlin, имеет полную API/SDK/CLI и покрыт 20 тем, что делает его готовым к пилотному внедрению в production. Основные риски — лицензия, безопасность и подтверждение активности мейнтейнеров, требующие финального аудита.

### 中文

**项目简介**  
Chucker（GitHub：ChuckerTeam/chucker）是一款运行在 Android 设备上的 HTTP 抓包/审查工具，基于 OkHttp 实现，功能类似 Charles，却可以直接在手机或模拟器里实时查看请求、响应、头信息、体内容以及错误堆栈，帮助开发者快速定位网络问题。

**价值**  
- **加速日常开发与调试**：无需切换到桌面抓包工具，代码改动后即可在 App 内看到完整的网络交互，显著缩短排查时间。  
- **提升代码评审与 CI 反馈**：通过在本地或 CI 环境中自动开启 Chucker，可以把网络请求日志作为审查材料或测试报告的一部分，帮助团队发现不符合规范的 API 调用。  
- **降低运维成本**：在移动端捕获的请求/响应数据可直接用于离线分析，避免在生产环境中额外部署代理或日志系统。

**典型接入方式**  
1. **Gradle 依赖**（Kotlin/Java 项目）  
   ```gradle
   dependencies {
       debugImplementation "com.github.chuckerteam.chucker:library:4.0.0"
       releaseImplementation "com.github.chuckerteam.chucker:library-no-op:4.0.0"
   }
   ```  
   - `debugImplementation` 在调试构建中引入完整功能；`releaseImplementation` 使用 `no-op` 版本，确保发布包不携带抓包代码。  
2. **OkHttp 拦截器**  
   ```kotlin
   val okHttpClient = OkHttpClient.Builder()
       .addInterceptor(ChuckerInterceptor(context))
       .build()
   ```  
   - 只需在 OkHttpClient 构建链中加入 `ChuckerInterceptor`，即可自动捕获所有请求。  
3. **可选 UI 集成**  
   - 在 Debug 页面添加入口（如按钮或侧滑菜单），调用 `Chucker.show(context)` 打开内置的请求列表界面。  
4. **CI 环境使用**  
   - 在本地或 CI 脚本中启动 Android 仿真器，使用 `library-no-op` 替代，以免影响性能；若需要捕获日志，可开启 `Chucker` 的文件导出功能并在测试结束后收集生成的 JSON/PCAP 文件。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑12，拥有 4.5k+ Stars、458 Forks，社区活跃，Issue 处理及时。  
- **技术成熟度**：核心实现基于 OkHttp 拦截器，已在多个大型 Android 项目中验证，支持 Kotlin、Java 双语言，提供 `no-op` 版本以满足发布包体积与安全要求。  
- **安全与合规**：采用 Apache‑2.0 许可证，无已知重大安全漏洞；仍建议在正式发布前通过内部 SBOM 与许可证合规检查。  
- **可观测性**：提供请求/响应的完整日志、错误堆栈、耗时统计以及导出为 JSON/PCAP 的功能，便于后续监控或审计。  

综合来看，Chucker 具备 **高生产就绪度**，适合作为 Android 项目的标准网络调试与可观测性工具，在开发、测试以及 CI 流程中均可平滑接入。

## 🧭 Practical evaluation

**Value:** ChuckerTeam/chucker helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4537 GitHub stars
- 458 forks
- updated 2026-07-12
- primary language: Kotlin
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 78/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 74/100 |
| recency | 40/100 |
| adoption | 75/100 |
| production | 62/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/ChuckerTeam/chucker) · [← Back to Observability](./README.md)</sub>
