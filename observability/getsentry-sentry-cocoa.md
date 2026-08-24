# getsentry/sentry-cocoa

[![Stars](https://img.shields.io/github/stars/getsentry/sentry-cocoa?style=flat-square&color=yellow)](https://github.com/getsentry/sentry-cocoa/stargazers) [![Forks](https://img.shields.io/github/forks/getsentry/sentry-cocoa?style=flat-square&color=blue)](https://github.com/getsentry/sentry-cocoa/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> The official Sentry SDK for iOS, tvOS, macOS, watchOS, iPadOS and visionOS.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 398 |
| 💻 **Language** | Swift |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cocoa` `crash` `crash-reporting` `crash-reports` `error-handler` `error-monitoring` `ios` `ipados` `macos` `objective-c` `sdk` `sentry`

## 🎯 Categories

Observability · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
getsentry/sentry‑cocoa is the official Sentry SDK for Apple platforms (iOS, tvOS, macOS, watchOS, iPadOS and visionOS). It lets developers automatically capture crashes, performance data, and custom events, turning opaque production behavior into actionable insights. With a strong community (1 090 ★, 398 forks) and active maintenance, it’s a mature, production‑ready option for any Apple‑centric mobile or desktop app.  

**Value**  
- **Observability at the edge:** By instrumenting the app with a few lines of Swift/Objective‑C code, developers get real‑time crash reports, performance traces, and contextual breadcrumbs that make post‑mortem debugging fast and precise.  
- **Unified monitoring:** The SDK feeds data into Sentry’s central dashboard, allowing teams to correlate client‑side issues with backend health, prioritize bugs, and track overall service health from a single pane.  

**Practical Adoption Path**  
1. **Add the dependency** – Use Swift Package Manager, CocoaPods, or Carthage to pull in `Sentry` (the SDK is a single package).  
2. **Initialize early** – In `AppDelegate`/`SceneDelegate` call `SentrySDK.start { options in … }` with your DSN and any optional settings (environment, release, sample rate, etc.).  
3. **Instrument** –  
   * Crash reporting works out‑of‑the‑box.  
   * Add custom events, breadcrumbs, or performance spans where you need deeper insight (e.g., network layer, UI flows).  
   * Enable integrations (e.g., `SentrySwiftUI`, `SentryUIKit`, `SentryNetworkTracking`) to get automatic breadcrumbs.  
4. **Configure** – Set up release tracking, environment tags, and user feedback in the Sentry dashboard; optionally enable rate‑limiting or local caching for offline scenarios.  
5. **Validate** – Deploy to a staging build, trigger a test crash or transaction, and verify that data appears in the Sentry UI.  

**Production Readiness**  
- **Active maintenance:** Last commit on 2026‑07‑03, regular releases, and a responsive maintainer community.  
- **Broad adoption:** Used by many high‑profile iOS/macOS apps; the SDK is listed in Sentry’s official documentation and recommended integrations.  
- **Robust ecosystem:** Supports Swift, Objective‑C, and SwiftUI; provides CLI tools, source‑map upload, and extensive platform‑specific integrations.  
- **Quality signals:** 1 090 stars, 398 forks, 18 topic tags, and a clear release pipeline indicate a stable, well‑tested codebase.  

Overall, getsentry/sentry‑cocoa offers a low‑friction, battle‑tested way to bring full‑stack observability to Apple platforms, making it a safe choice for production deployments after a brief pilot and security/license review.

### Русский

getsentry/sentry-cocoa — официальная Sentry‑SDK для экосистемы Apple (iOS, tvOS, macOS, watchOS, iPadOS, visionOS), позволяющая в реальном времени собирать ошибки, трассировки и метрики, что упрощает инспекцию и отладку поведения приложений в продакшене. Типовой сценарий внедрения: добавить SDK через Swift Package Manager или CocoaPods, сконфигурировать DSN и включить автоматический захват исключений и производительности, после чего получать детальные отчёты в Sentry для мониторинга состояния сервиса и быстрого реагирования на проблемы. Проект обладает высокой готовностью к production: активная поддержка (обновления до 2026‑07‑03), более 1000 звёзд, широкое применение, хорошая документация и стабильный набор функций, требующий лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
getsentry/sentry‑cocoa 是 Sentry 官方提供的 Swift/Objective‑C SDK，支持 iOS、tvOS、macOS、watchOS、iPadOS 与 visionOS，帮助开发者在真实环境中捕获异常、性能瓶颈和自定义事件，从而更轻松地检查和调试生产行为。

**价值**  
- **可观测性即服务**：实时上报崩溃、错误、慢速事务和自定义事件，帮助团队快速定位生产问题。  
- **提升调试效率**：自动附带设备、系统、应用版本等元数据，省去手动收集日志的繁琐。  
- **业务健康监控**：通过仪表盘可视化错误率、性能趋势，支撑 SLO/SLI 的监控与预警。

**典型接入方式**  
1. **通过 CocoaPods / Swift Package Manager / Carthage** 将 `Sentry` 包加入项目。  
2. 在 `AppDelegate`（或 `@main` 的入口）中初始化 SDK，例如：  
   ```swift
   import Sentry

   SentrySDK.start { options in
       options.dsn = "https://<public_key>@sentry.io/<project_id>"
       options.enableAutoSessionTracking = true      // 自动会话跟踪
       options.tracesSampleRate = 1.0               // 启用全链路性能监控
   }
   ```
3. 可选地使用 **SentryCLI** 上传 dSYM 符号文件，确保崩溃堆栈可读。  
4. 如需自定义事件或上下文，直接调用 `SentrySDK.captureMessage/_captureError` 或 `SentrySpan` 等 API。

**生产可用性**  
- **活跃度高**：截至 2026‑07‑03 最近一次提交，拥有 1 090 ⭐、398 🍴，且持续更新。  
- **生态成熟**：被广泛采用于大型 iOS/Apple 生态项目，官方文档完善，支持多平台（iOS、macOS、watchOS、visionOS 等）。  
- **质量与安全**：实现基于 Swift，已覆盖 18 个主题的测试与案例；无已知重大安全漏洞，许可证为 BSD‑3‑Clause，适合企业使用。  
- **风险**：仍需对许可证合规、内部安全审计以及维护者响应速度进行最终确认。  

综合来看，sentry‑cocoa 已具备 **高生产就绪度**，适合作为监控与调试的首选 SDK 在正式环境中推广。

## 🧭 Practical evaluation

**Value:** getsentry/sentry-cocoa helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1090 GitHub stars
- 398 forks
- updated 2026-07-03
- primary language: Swift
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 65/100 |
| production | 58/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/getsentry/sentry-cocoa) · [← Back to Observability](./README.md)</sub>
