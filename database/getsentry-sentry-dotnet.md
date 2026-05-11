# getsentry/sentry-dotnet

[![Stars](https://img.shields.io/github/stars/getsentry/sentry-dotnet?style=flat-square&color=yellow)](https://github.com/getsentry/sentry-dotnet/stargazers) [![Forks](https://img.shields.io/github/forks/getsentry/sentry-dotnet?style=flat-square&color=blue)](https://github.com/getsentry/sentry-dotnet/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Sentry SDK for .NET

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 753 |
| 🍴 **Forks** | 232 |
| 💻 **Language** | C# |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`crash-reporting` `dotnet` `hacktoberfest` `performance-monitoring` `sdk` `sentry` `tag-production` `team-gdx`

## 🎯 Categories

Database · Observability · Product

## 📝 Summary

### English

**Brief Summary**  
getsentry/sentry‑dotnet is the official Sentry SDK for the .NET ecosystem, enabling applications to capture and report errors, performance traces, and custom events to Sentry’s observability platform. With 750+ stars, frequent releases, and strong community adoption, it is a production‑ready, open‑source component for .NET teams that need reliable monitoring and debugging.  

**Value**  
- Provides turnkey error‑tracking and performance monitoring without writing custom instrumentation or building a separate logging pipeline.  
- Consolidates crash reports, stack traces, and contextual metadata in a single UI, reducing mean‑time‑to‑resolution and improving overall system reliability.  
- Supports ASP.NET Core, Blazor, Xamarin, Unity and other .NET runtimes, making it a versatile choice for a wide range of applications.  

**Practical Adoption Path**  
1. **Evaluate** – Add the `Sentry.AspNetCore` (or appropriate) NuGet package to a sandbox project and configure the DSN in `appsettings.json`.  
2. **Instrument** – Enable automatic exception capture, performance tracing, and add any custom breadcrumbs or tags needed for your domain.  
3. **Test** – Trigger a few test exceptions to verify that events appear in the Sentry dashboard and that sensitive data is scrubbed.  
4. **Roll Out** – Deploy the SDK to staging, monitor payload volume, and tune sampling rates or filters.  
5. **Production** – Promote the configuration to production, optionally integrating with CI/CD to keep the SDK version up‑to‑date.  

**Production Readiness**  
- **Activity & Maintenance**: Recent commits (last update 2026‑05‑11), regular releases, and an active maintainer community.  
- **Adoption**: Hundreds of stars/forks and usage in many high‑traffic .NET services indicate real‑world stability.  
- **Quality**: Clear documentation, extensive unit tests, and built‑in support for .NET 6+ and .NET Framework 4.6+.  
- **Risk**: No critical licensing or security red flags identified, though a final review of the MIT license and any third‑party dependencies is advisable.  

Overall, getsentry/sentry‑dotnet is a mature, well‑supported SDK that can be introduced with minimal friction and trusted for mission‑critical .NET workloads.

### Русский

getsentry/sentry-dotnet — это официальная SDK‑библиотека Sentry для платформы .NET, позволяющая быстро интегрировать мониторинг ошибок и событий в C#‑приложения без собственного инфраструктурного кода. Типичный сценарий — подключение SDK к веб‑сервису или микросервису, после чего все исключения, трассировки и пользовательские метрики автоматически отправляются в Sentry для дальнейшего анализа и оповещения. Проект имеет высокую готовность к production: активные коммиты, более 750 звёзд, регулярные релизы и широкое принятие в сообществе, что делает его надёжным выбором для мониторинга .NET‑приложений.

### 中文

**项目简介**  
getsentry/sentry-dotnet 是 Sentry 为 .NET 平台提供的官方 SDK，帮助开发者在 C#、F#、VB.NET 等语言的应用中捕获异常、性能数据和自定义事件，并将这些信息安全、实时地上报到 Sentry 云端或自托管实例。

**价值**  
- **统一可观测性**：无需自行搭建日志、异常或性能监控体系，SDK 自动收集堆栈、请求上下文、用户信息等，极大降低运维成本。  
- **快速定位问题**：通过聚合的错误视图、事务追踪和采样控制，团队可以在几秒钟内定位根因，提升修复效率。  
- **灵活扩展**：提供丰富的拦截器、过滤器和自定义事件 API，能够与现有的依赖注入、日志框架（Serilog、NLog、log4net）以及 ASP.NET Core 中间件无缝集成。

**典型接入方式**  
1. **NuGet 安装**：`dotnet add package Sentry.AspNetCore`（或 `Sentry`、`Sentry.Extensions.Logging` 等子包）。  
2. **在 `Program.cs`/`Startup.cs` 中注册**：  
   ```csharp
   builder.WebHost.UseSentry(options =>
   {
       options.Dsn = "https://examplePublicKey@o0.ingest.sentry.io/0";
       options.TracesSampleRate = 0.2;   // 性能采样率
       options.Environment = "production";
   });
   ```  
3. **可选的中间件/拦截器**：在 ASP.NET Core 中加入 `app.UseSentryTracing();`，在 WPF/WinForms 中调用 `SentrySdk.Init(...)`。  
4. **自定义事件**：`SentrySdk.CaptureMessage("业务关键点");`、`SentrySdk.CaptureException(ex);`。

**生产可用性**  
- **活跃维护**：截至 2026‑05‑11 最近一次提交，拥有 753 ★、232 Fork，社区活跃，官方每月发布安全补丁。  
- **成熟生态**：支持 .NET 6/7/8、ASP.NET Core、Entity Framework、Xamarin、Blazor 等主流框架，且已在多家大型互联网公司生产环境中使用。  
- **安全与合规**：采用 MIT 许可证，提供完整的 DSN 加密、PII 脱敏和 GDPR/CCPA 配置选项。  
- **风险**：需自行评估内部审计对第三方 SDK 的合规要求，并关注依赖的 Sentry 后端（云端或自托管）的可用性与网络连通性。  

综上所述，getsentry/sentry-dotnet 具备高可用、易集成、功能完整的特性，是 .NET 项目实现异常与性能可观测性的首选方案。

## 🧭 Practical evaluation

**Value:** getsentry/sentry-dotnet helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 753 GitHub stars
- 232 forks
- updated 2026-05-11
- primary language: C#
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 82/100 |
| recency | 100/100 |
| adoption | 61/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/getsentry/sentry-dotnet) · [← Back to Database](./README.md)</sub>
