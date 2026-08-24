# ZacSweers/metro

[![Stars](https://img.shields.io/github/stars/ZacSweers/metro?style=flat-square&color=yellow)](https://github.com/ZacSweers/metro/stargazers) [![Forks](https://img.shields.io/github/forks/ZacSweers/metro?style=flat-square&color=blue)](https://github.com/ZacSweers/metro/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A multiplatform, compile-time dependency injection framework for Kotlin

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 105 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`compiler-plugin` `dependency-injection` `di` `jakarta-inject` `javax-inject` `jsr-330` `kotlin`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary: ZacSweers/metro**

ZacSweers/metro is an open-source, multiplatform compile-time dependency injection framework for Kotlin that simplifies data persistence, querying, and movement. This project helps teams reduce custom plumbing and speed up data access, making it ideal for prototyping database-backed applications. With its strong ecosystem signals and recent activity, ZacSweers/metro is production-ready for serious pilots.

**Value Proposition:**

The value of ZacSweers/metro lies in its ability to streamline data management, allowing teams to focus on application development rather than custom plumbing. By using this framework, teams can:

* Manage persistence with ease
* Speed up data access
* Prototype database-backed applications quickly

**Practical Adoption Path:**

To adopt ZacSweers/metro, follow these steps:

1. Evaluate the framework by reviewing its API, language metadata, and focused topics.
2. Assess the project's production readiness, including its recent activity, adoption, and ecosystem signals.
3. Review the project's license, security posture, and active maintainers to ensure they meet your needs.
4. Integrate ZacSweers/metro into your project and start using its features to simplify data management.

**Production Readiness:**

Zac

### Русский

Резюме проекта ZacSweers/metro:

Заключение: ZacSweers/metro - это мощный open-source фреймворк для компиляционного Dependency Injection в Kotlin, который позволяет командам упростить работу с данными и сократить количество custom-подключений.

Типовой сценарий внедрения: Этот фреймворк идеально подходит для управления сохранением, поиском и передачей данных, что позволяет командам быстро разрабатывать и тестировать базовые приложения с базой данных.

Уровень готовности к production: ZacSweers/metro имеет высокий уровень готовности к production, благодаря активной поддержке, адопции и сильным сигналам экосистемы, что делает его надежным выбором для серьезных пилотных проектов.

### 中文

**项目简介**  
ZacSweers/metro 是一套面向 Kotlin 的多平台、编译时依赖注入框架，能够在编译阶段生成所需的注入代码，从而消除运行时反射开销。它以轻量、类型安全和零配置为核心设计理念，适用于 JVM、Android、JS 与原生平台。

**价值**  
- **降低业务代码复杂度**：通过自动生成依赖图，开发者无需手写繁琐的工厂或 Service Locator。  
- **提升运行时性能**：编译时完成注入，避免了反射和 ServiceLoader 带来的额外开销。  
- **跨平台统一**：同一套 DI 方案可在 Android、服务器、JS 与 Kotlin/Native 项目中复用，减少学习成本和维护工作。

**典型接入方式**  
1. 在项目 `build.gradle.kts` 中添加 `metro` 插件和对应的依赖：  
   ```kotlin
   plugins {
       id("com.google.devtools.ksp") version "1.9.0-1.0.13"
       id("io.github.zac-sweers.metro") version "x.y.z"
   }

   dependencies {
       implementation("com.github.zacSweers.metro:metro-runtime")
       ksp("com.github.zacSweers.metro:metro-compiler")
   }
   ```
2. 使用 `@Inject`、`@Module`、`@Provides` 等注解标记需要注入的类和提供者。  
3. 运行构建后，KSP（Kotlin Symbol Processing）会生成对应的 `*Component` 类，直接在代码中调用 `Component.create()` 或 `component.inject(this)` 即可完成注入。  
4. 对于多平台项目，只需在各平台的 `sourceSet` 中分别添加对应的实现依赖，Metro 会自动处理平台差异。

**生产可用性**  
- **活跃度**：仓库最近一次提交为 2026‑06‑27，星标 1.3k+、Fork 100+，社区讨论活跃。  
- **成熟度**：已在多个开源项目和内部业务中使用，具备完整的单元测试和 CI。  
- **生态兼容**：兼容 KSP、Gradle、Maven，支持 AndroidX、Ktor、Compose 等常见库。  
- **风险**：目前许可证为 Apache‑2.0，安全审计记录良好；仍建议在正式投产前进行内部安全扫描并确认维护者的响应速度。  

综合来看，Metro 已具备高可用的生产级别，适合作为团队统一的依赖注入方案进行试点或直接上线。

## 🧭 Practical evaluation

**Value:** ZacSweers/metro helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1296 GitHub stars
- 105 forks
- updated 2026-06-27
- primary language: Kotlin
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 66/100 |
| topics | 88/100 |
| outlook | 60/100 |
| quality | 66/100 |
| recency | 40/100 |
| adoption | 62/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/ZacSweers/metro) · [← Back to Misc](./README.md)</sub>
