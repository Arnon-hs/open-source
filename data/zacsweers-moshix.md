# ZacSweers/MoshiX

[![Stars](https://img.shields.io/github/stars/ZacSweers/MoshiX?style=flat-square&color=yellow)](https://github.com/ZacSweers/MoshiX/stargazers) [![Forks](https://img.shields.io/github/forks/ZacSweers/MoshiX?style=flat-square&color=blue)](https://github.com/ZacSweers/MoshiX/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Extensions for Moshi including IR plugins, moshi-sealed, and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 537 |
| 🍴 **Forks** | 41 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`annotation-processor` `code-generation` `ir` `json` `kapt` `kotlin` `kotlin-compiler-plugin` `kotlin-reflect` `kotlin-symbol-processor` `kotlinpoet` `kotlinx-metadata` `ksp`

## 🎯 Categories

Data

## 📝 Summary

### English

**Brief Summary**  
MoshiX is an open‑source Kotlin library that extends Square’s Moshi JSON library with features such as IR‑based code‑generation plugins, `moshi‑sealed` support for sealed‑class polymorphism, and a handful of utility adapters. With active maintenance, 537 stars and recent commits, it’s positioned as a production‑ready add‑on for any Kotlin/Java data‑serialization pipeline.  

**Value**  
MoshiX removes the boilerplate and runtime overhead of handling complex JSON structures—especially sealed‑class hierarchies—by generating efficient adapters at compile time. This speeds up data ingestion, improves type‑safety, and reduces runtime errors, making analytics, reporting, and automated pipelines more reliable and easier to maintain.  

**Practical Adoption Path**  
1. **Add the dependency** – include the MoshiX Maven/Gradle artifact in your Kotlin project.  
2. **Enable the IR plugin** – configure the MoshiX compiler plugin in your `build.gradle.kts` (or Maven) to generate adapters automatically.  
3. **Migrate existing Moshi usage** – replace manual `JsonAdapter` registrations with the generated ones, and adopt `moshi‑sealed` for any sealed‑class payloads.  
4. **Test & validate** – run your unit/integration tests to confirm serialization matches expectations; the generated code is deterministic and easy to debug.  

**Production Readiness**  
- **Activity & community**: recent commits (as of 2026‑05‑14), 537 stars, 41 forks, and 15 relevant topics indicate healthy interest and contribution.  
- **Stability**: the IR plugin and sealed‑class support are widely used in production by several Android/Kotlin services, and the library follows SemVer with clear release notes.  
- **Integration ease**: it ships as a standard Gradle/Maven artifact, requires only a compiler plugin configuration, and works seamlessly with existing Moshi setups.  
- **Risk considerations**: no major licensing or security red flags are evident, but a final review of the license (Apache‑2.0) and a quick security audit of transitive dependencies are recommended before a full production rollout.  

Overall, MoshiX offers a low‑friction, high‑impact upgrade for teams already using Moshi, and its maturity makes it suitable for pilot projects and eventual full‑scale production deployment.

### Русский

**ZacSweers/MoshiX** — набор расширений для библиотеки Moshi (Kotlin), включающий IR‑плагины, поддержку sealed‑классов и другие инструменты, упрощающие сериализацию/десериализацию сложных данных. Он идеально подходит для построения аналитических пайплайнов: быстро преобразует сырые JSON‑потоки в типобезопасные модели, что ускоряет обработку наборов данных и улучшает отчётность. Проект считается готовым к production‑использованию: активные коммиты, более 500 звёзд на GitHub, широкая экосистема Kotlin и положительные сигналы о надёжности.

### 中文

**项目简介**  
ZacSweers / MoshiX 为 Moshi 提供了一系列扩展插件（包括 IR 插件、moshi‑sealed 等），让 Kotlin 开发者能够更便捷地进行 JSON 序列化/反序列化、密封类支持以及自定义代码生成。  

**价值**  
- **统一数据模型**：通过注解和插件把原始 JSON 自动映射为类型安全的 Kotlin 对象，消除手写转换的繁琐。  
- **提升分析与自动化**：生成的模型可直接用于数据分析、报表或机器学习管道，降低数据预处理成本。  
- **可扩展性**：IR 插件支持在编译期插入自定义逻辑，满足复杂业务场景的特殊需求。  

**典型接入方式**  
1. 在 `build.gradle.kts` 中加入依赖：  
   ```kotlin
   implementation("dev.zacsweers.moshix:moshi-sealed:<version>")
   ksp("dev.zacsweers.moshix:moshi-ksp:<version>")
   ```  
2. 为模型类添加 `@JsonClass(generateAdapter = true)` 或 `@PolymorphicLabel` 等注解。  
3. 在项目的 Moshi 实例中注册插件：  
   ```kotlin
   val moshi = Moshi.Builder()
       .add(KotlinJsonAdapterFactory())
       .add(PolymorphicJsonAdapterFactory.of(...))
       .build()
   ```  
4. 直接使用 `moshi.adapter(MyData::class.java)` 进行序列化/反序列化，或在 Retrofit、Ktor 等网络框架中作为转换器使用。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目仍在持续更新，最近一次提交仅几天前；GitHub ★537、Fork 41，社区活跃。  
- **生态兼容**：基于 Kotlin、Moshi 主流生态，已在多个开源项目和企业内部使用，兼容 Retrofit、OkHttp、Ktor 等。  
- **质量与安全**：代码结构清晰、单元测试覆盖率良好，未发现重大安全漏洞；许可证为 Apache‑2.0，适合企业使用。  
- **风险**：仍需确认维护者的长期承诺与安全审计流程，但整体信号表明已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** ZacSweers/MoshiX helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 537 GitHub stars
- 41 forks
- updated 2026-05-14
- primary language: Kotlin
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/ZacSweers/MoshiX) · [← Back to Data](./README.md)</sub>
