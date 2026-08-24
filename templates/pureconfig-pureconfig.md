# pureconfig/pureconfig

[![Stars](https://img.shields.io/github/stars/pureconfig/pureconfig?style=flat-square&color=yellow)](https://github.com/pureconfig/pureconfig/stargazers) [![Forks](https://img.shields.io/github/forks/pureconfig/pureconfig?style=flat-square&color=blue)](https://github.com/pureconfig/pureconfig/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> A boilerplate-free library for loading configuration files

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 182 |
| 💻 **Language** | Scala |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`configuration` `hacktoberfest` `pureconfig` `scala` `scala-library` `shapeless`

## 🎯 Categories

Templates

## 📝 Summary

### English

**Summary**  
PureConfig is a Scala library that lets you map configuration files (e.g., HOCON, JSON, YAML) directly onto case‑class hierarchies without writing boiler‑plate code. It is actively maintained (last commit 2026‑07‑12), has a solid community signal (≈1.5 k stars, 182 forks), and aims to simplify configuration handling in Scala applications.

**Value proposition**  
- **Zero‑boilerplate mapping** – By leveraging Scala’s type‑level programming, PureConfig automatically derives readers for most standard types and case classes, eliminating repetitive parsing code.  
- **Broad format support** – Works with Typesafe Config, JSON, and YAML, making it a one‑stop solution for most configuration needs in the Scala ecosystem.  
- **Strong type safety** – Configuration errors are caught at compile time or reported with clear runtime messages, reducing bugs caused by malformed config files.

**Practical adoption path**  
1. **Proof‑of‑concept** – Add the library as a test‑scope dependency and try loading a small config file into a simple case class, following the examples in the README.  
2. **Integration checklist** – Verify that your build tool (sbt, Maven, or Mill) resolves the transitive dependencies without version conflicts, and confirm that the configuration format you use (HOCON, JSON, YAML) is supported out‑of‑the‑box.  
3. **Gradual rollout** – Replace existing manual parsing code module‑by‑module, starting with low‑risk components, and add unit tests that assert the derived config objects match expected values.  

**Production readiness**  
PureConfig sits at a **medium** readiness level: it is mature enough for prototypes, internal services, and even production workloads provided you perform a few due‑diligence steps:  

- **Dependency audit** – Ensure the library’s transitive dependencies (e.g., Typesafe Config) are compatible with your current stack and do not introduce licensing or security concerns.  
- **Maintenance check** – Monitor the repository for issue response times and release cadence; the recent activity suggests active maintenance, but keep an eye on upcoming Scala version upgrades.  
- **Operational testing** – Validate error handling in staging, especially for missing or malformed configuration keys, to confirm that the library’s error messages meet your observability standards.  

If these checks pass, PureConfig can be safely promoted to production for most Scala‑based services, especially where type‑safe configuration is a priority.

### Русский

PureConfig — это библиотека без шаблонного кода, позволяющая легко загружать конфигурационные файлы в Scala‑приложения, автоматически маппя их на case‑классы. Она подходит для быстрых прототипов и внутренних сервисов, где требуется простая интеграция через README‑пример; перед выпуском в продакшн стоит проверить совместимость зависимостей и поддерживаемость проекта. Готовность к production — средняя: библиотека активно поддерживается (обновления 2026 г., 1,5 k звёзд), но путь интеграции не полностью описан в метаданных, поэтому рекомендуется начать с небольшого proof‑of‑concept.

### 中文

**项目简介**  
PureConfig 是一个 **零样板（boilerplate‑free）** 的 Scala 库，帮助开发者以类型安全的方式直接从 HOCON、JSON、Properties 等配置文件加载配置对象，免去手写解析和映射代码。

**价值**  
- **类型安全**：配置会在编译期映射到 case class，出现不匹配时立即报错，降低运行时配置错误。  
- **极简 API**：只需 `ConfigSource.default.load[MyConfig]`，无需手写解析逻辑或大量样板代码。  
- **与主流生态兼容**：原生支持 Typesafe Config、Jackson、circe 等常用格式，且可以通过自定义 `ConfigReader` 扩展任意类型。  

**典型接入方式**  
1. **在 build.sbt 中加入依赖**（以最新 2.x 版本为例）  
   ```scala
   libraryDependencies += "com.github.pureconfig" %% "pureconfig" % "0.17.5"
   ```
2. **定义配置模型**  
   ```scala
   case class HttpConfig(host: String, port: Int)
   case class AppConfig(http: HttpConfig, db: DbConfig)
   ```
3. **加载配置**（默认读取 `application.conf`）  
   ```scala
   import pureconfig._
   import pureconfig.generic.auto._

   val config: AppConfig = ConfigSource.default.loadOrThrow[AppConfig]
   ```
4. **如需自定义读取**，实现 `ConfigReader[T]` 并在 `implicit` 范围内提供即可。  

**生产可用性**  
- **成熟度**：GitHub ★1.5k、Fork 182，活跃维护至 2026‑07‑12，社区成熟度中等。  
- **适用场景**：内部服务、原型、以及对配置安全性要求较高的生产系统均可使用。  
- **风险与注意点**  
  - 依赖于 Typesafe Config；若项目已有其他配置框架，需评估兼容性。  
  - 需要在 CI 中加入配置加载的单元测试，以捕获结构变化导致的编译错误。  
  - 对于极高并发的启动路径，建议在应用启动阶段一次性加载并缓存配置对象，避免重复解析。  

综合来看，PureConfig 在 **类型安全、开发效率** 方面提供了显著价值，接入成本低，适合作为 Scala 项目的首选配置库。只要在上线前进行一次完整的加载测试并确认依赖版本稳定，即可在生产环境放心使用。

## 🧭 Practical evaluation

**Value:** pureconfig/pureconfig may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1538 GitHub stars
- 182 forks
- updated 2026-07-12
- primary language: Scala
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 68/100 |
| topics | 75/100 |
| outlook | 56/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 65/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/pureconfig/pureconfig) · [← Back to Templates](./README.md)</sub>
