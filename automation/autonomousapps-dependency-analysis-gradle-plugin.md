# autonomousapps/dependency-analysis-gradle-plugin

[![Stars](https://img.shields.io/github/stars/autonomousapps/dependency-analysis-gradle-plugin?style=flat-square&color=yellow)](https://github.com/autonomousapps/dependency-analysis-gradle-plugin/stargazers) [![Forks](https://img.shields.io/github/forks/autonomousapps/dependency-analysis-gradle-plugin?style=flat-square&color=blue)](https://github.com/autonomousapps/dependency-analysis-gradle-plugin/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Gradle plugin for JVM projects written in Java, Kotlin, Groovy, or Scala; and Android projects written in Java or Kotlin. Provides advice for managing dependencies and other applied plugins

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 147 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `gradle-plugin` `groovy` `java` `jvm` `kotlin` `scala`

## 🎯 Categories

Automation · Mobile

## 📝 Summary

### English

**Summary**  
The autonomousapps/dependency‑analysis‑gradle‑plugin is a Kotlin‑based Gradle plugin that inspects JVM (Java, Kotlin, Groovy, Scala) and Android projects and automatically generates actionable advice for cleaning up unused, duplicate, or mis‑scoped dependencies and for managing applied plugins. With over 2 000 stars, frequent releases, and strong community adoption, it turns a tedious manual dependency‑audit process into a repeatable, automated step in the build pipeline.

**Value**  
- **Time‑saving automation** – eliminates the manual effort of hunting down unused or conflicting libraries, letting developers focus on feature work.  
- **Consistent builds** – by enforcing best‑practice dependency configurations across modules, it reduces runtime crashes and build‑time bloat.  
- **Integrates with CI/CD** – the plugin can be run as part of any Gradle build, making it easy to embed in continuous‑integration pipelines, scheduled scans, or pre‑merge checks.

**Practical adoption path**  
1. **Add the plugin** to the root `build.gradle.kts` (or Groovy DSL) using the standard Gradle plugin DSL.  
2. **Run a baseline analysis** with `./gradlew dependencyAnalysis` to generate a report of recommendations.  
3. **Iteratively apply the suggested fixes** (e.g., removing unused dependencies, consolidating versions) and re‑run the analysis until the report is clean.  
4. **Enforce compliance** by configuring the plugin to fail the build when new violations are introduced, and optionally hook it into pull‑request checks or scheduled nightly jobs.

**Production readiness**  
The project shows high production readiness: recent commits (last update 2026‑05‑12), active maintainers, a sizable user base (2 135 stars, 147 forks), and clear documentation. Its Kotlin implementation aligns with modern Gradle ecosystems, and it exposes standard Gradle APIs, making integration straightforward. While a final review of licensing and security posture is advisable, the plugin is mature enough for a serious pilot in production environments.

### Русский

**autonomousapps/dependency-analysis-gradle-plugin** — это Gradle‑плагин, который автоматически анализирует зависимости в JVM‑ и Android‑проектах (Java, Kotlin, Groovy, Scala) и выдаёт рекомендации по их оптимизации, а также по использованию других подключённых плагинов. Типичный сценарий — включить плагин в CI/CD, чтобы избавиться от ручного аудита зависимостей, обеспечить согласованность версий и сократить размер артефактов. Проект имеет высокую готовность к production: активные коммиты, более 2000 звёзд, широкое принятие в сообществе и стабильный набор API/CLI, однако окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句话）**  
`autonomousapps/dependency-analysis-gradle-plugin` 是一款面向 JVM（Java、Kotlin、Groovy、Scala）以及 Android（Java、Kotlin）项目的 Gradle 插件。它自动分析项目的依赖关系，给出“删除未使用依赖、合并重复依赖、替换低效依赖”等优化建议，帮助团队消除手动依赖检查的繁琐工作。

**价值**  
- **降低运维成本**：自动发现并移除冗余或未使用的依赖，避免因手工审查导致的遗漏或误删。  
- **提升构建质量**：通过建议更合理的依赖版本和插件组合，减少冲突、提升编译速度和运行时体积。  
- **促进 CI/CD 自动化**：可在 CI 流水线中持续运行，形成可重复的依赖治理流程，确保每次提交都符合最佳实践。

**典型接入方式**  
1. **在根项目的 `build.gradle.kts`（或 `build.gradle`）中添加插件**  
   ```kotlin
   plugins {
       id("com.autonomousapps.dependency-analysis") version "1.20.0"
   }
   ```
2. **在 CI 环境（GitHub Actions、GitLab CI、Jenkins 等）执行 Gradle 检查**  
   ```bash
   ./gradlew build dependencyAnalysis
   ```
   生成的报告默认位于 `build/reports/dependency-analysis`，可在构建日志或 PR 检查中直接展示。  
3. **可选配置**：通过 `dependencyAnalysis { ... }` DSL 过滤特定子项目、忽略某些依赖或自定义报告格式，以适配不同团队的需求。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，插件最近一次提交在 2026‑05‑12，拥有 2135+ Stars、147+ Forks，社区活跃，Issue 响应及时。  
- **成熟度**：已在多个大型 Android 与 JVM 项目中实际使用，具备稳定的 API、完整的文档以及示例。  
- **兼容性**：支持 Gradle 7.x/8.x，兼容 Kotlin DSL 与 Groovy DSL，且对 Android Gradle Plugin 7+ 完全兼容。  
- **安全与许可证**：采用 Apache‑2.0 许可证，暂无已知安全漏洞，仍建议在正式上线前进行一次内部安全审计。  

综合来看，`dependency-analysis-gradle-plugin` 已具备 **高生产可用性**，可放心在企业级 CI/CD 流程中推广使用，以实现依赖管理的自动化和质量提升。

## 🧭 Practical evaluation

**Value:** autonomousapps/dependency-analysis-gradle-plugin helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2135 GitHub stars
- 147 forks
- updated 2026-05-12
- primary language: Kotlin
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 71/100 |
| topics | 88/100 |
| outlook | 79/100 |
| quality | 83/100 |
| recency | 100/100 |
| adoption | 66/100 |
| production | 77/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/autonomousapps/dependency-analysis-gradle-plugin) · [← Back to Automation](./README.md)</sub>
