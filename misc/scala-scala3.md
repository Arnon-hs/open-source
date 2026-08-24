# scala/scala3

[![Stars](https://img.shields.io/github/stars/scala/scala3?style=flat-square&color=yellow)](https://github.com/scala/scala3/stargazers) [![Forks](https://img.shields.io/github/forks/scala/scala3?style=flat-square&color=blue)](https://github.com/scala/scala3/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> The Scala 3 compiler, also known as Dotty.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.3k |
| 🍴 **Forks** | 1.2k |
| 💻 **Language** | Scala |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`compiler` `dotty` `epfl` `scala` `scala3`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Scala 3 (the Dotty compiler) is the modern, officially‑supported compiler for the Scala language, offering a cleaner type system, improved metaprogramming, and better tooling than Scala 2. With over 6 000 stars, active maintenance (last update 2026‑06‑23), and a growing ecosystem, it is a solid candidate for projects that need a forward‑looking Scala platform.  

**Value**  
Scala 3 brings language‑level innovations—union/intersection types, implicit‑function types, and a more expressive macro system—that can simplify complex domain models, reduce boilerplate, and improve compile‑time safety. Its compatibility layer (the “-Xsource:3” flag) lets existing Scala 2 codebases migrate incrementally, protecting prior investments while unlocking new language features.  

**Practical adoption path**  
1. **Proof‑of‑concept**: Clone the repo, run the provided sbt build, and compile a small module of your codebase with the `-Xsource:3` flag to verify toolchain compatibility.  
2. **README validation**: Follow the official README instructions for setting up the compiler, checking the Docker/CI examples, and confirming that required plugins (e.g., sbt‑dotty) work in your environment.  
3. **Incremental migration**: Convert one microservice or library at a time, using the `-source:future` mode to surface incompatibilities, then refactor to pure Scala 3 syntax.  

**Production readiness**  
The project scores high on production readiness: recent commits, a vibrant contributor community, and widespread adoption in major Scala‑based products (e.g., Apache Spark, Lightbend). The extensive documentation, stable release cadence, and strong ecosystem (metals, sbt, coursier) make Scala 3 suitable for a serious pilot, provided the initial integration effort is scoped to a limited component and the build pipeline is validated early.

### Русский

Scala 3 (Dotty) — это современный компилятор языка Scala, активно поддерживаемый сообществом (62 % балл, > 6 тыс. звёзд, частые обновления). Он подходит для команд, которые уже используют Scala или планируют мигрировать на новую версию: достаточно проверить README и выполнить небольшой proof‑of‑concept, после чего можно запускать полноценные проекты, поскольку готовность к продакшну уже подтверждена широким принятием и стабильным экосистемным окружением. При внедрении следует уточнить детали интеграции и оценить затраты на настройку, но в целом проект считается готовым к серьёзному пилотному использованию.

### 中文

**项目简介**  
Scala 3 编译器（代号 Dotty）是 Scala 语言的下一代实现，提供更简洁的语法、强大的类型系统以及对多平台（JVM、JS、Native）的统一编译支持。

**价值**  
- **语言进化**：引入了显式的类型推断、隐式函数改写（given/using）和宏系统，显著提升代码可读性和安全性。  
- **生态兼容**：兼容现有 Scala 2 项目，可逐步迁移，降低改造成本。  
- **社区活跃**：超过 6 k 星、1 k Fork，近期仍在频繁更新，生态插件（sbt、Metals、Scala‑CLI）成熟，适合作为企业级微服务、数据处理和 DSL 开发的核心语言。

**典型接入方式**  
1. **阅读官方 README**，确认所需的 Scala 版本和构建工具（sbt、Maven、Mill）。  
2. 在项目的 `build.sbt` 中添加 `scalaVersion := "3.x.x"`，并根据需要引入对应的库依赖。  
3. 使用 **Metals**（VS Code/IntelliJ 插件）或 **Scala‑CLI** 快速创建一个 “Hello World” 示例，验证编译、运行和 IDE 集成是否正常。  
4. 若已有 Scala 2 代码库，可通过 `-source:3.0-migration` 编译选项进行增量迁移，逐步替换旧语法。

**生产可用性**  
- **成熟度高**：项目活跃，最近一次提交仅在 2026‑06‑23，且已在多个大规模生产环境（如 Twitter、LinkedIn、Databricks）中使用。  
- **生态完整**：官方发布的发行版、sbt 插件、Metals IDE 支持以及丰富的第三方库（Cats 3、ZIO 2）均已兼容 Scala 3。  
- **风险评估**：主要风险在于迁移成本和特定库的兼容性，建议先在小型 PoC 中验证编译与运行时行为，再逐步推广。总体而言，Scala 3 已具备在生产环境中安全部署的条件。

## 🧭 Practical evaluation

**Value:** scala/scala3 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6261 GitHub stars
- 1162 forks
- updated 2026-06-23
- primary language: Scala
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 77/100 |
| stars | 81/100 |
| topics | 63/100 |
| outlook | 59/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 80/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/scala/scala3) · [← Back to Misc](./README.md)</sub>
