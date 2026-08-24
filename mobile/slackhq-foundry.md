# slackhq/foundry

[![Stars](https://img.shields.io/github/stars/slackhq/foundry?style=flat-square&color=yellow)](https://github.com/slackhq/foundry/stargazers) [![Forks](https://img.shields.io/github/forks/slackhq/foundry?style=flat-square&color=blue)](https://github.com/slackhq/foundry/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Gradle and IntelliJ build tooling used in Slack's Android repo

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 474 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `gradle` `intellij` `intellij-plugin` `java` `kotlin`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
slackhq/foundry is an open‑source Gradle and IntelliJ tooling suite that streamlines the build, testing, and packaging of UI components in Slack’s Android codebase. By providing ready‑made build scripts, SDK helpers, and reusable UI primitives, it lets teams ship user‑facing screens faster with far less custom Gradle or IDE configuration. The project is actively maintained (last update 2026‑07‑02) and has gathered a modest community of 474 stars on GitHub.  

**Value Proposition**  
- **Accelerated UI delivery** – Pre‑configured Gradle plugins and IntelliJ extensions remove boilerplate, letting developers focus on design rather than build plumbing.  
- **Component reuse** – A library of shared UI modules and SDK hooks encourages consistent look‑and‑feel across Android products.  
- **Lower entry barrier** – The tooling is language‑agnostic within Kotlin/Java Android projects, making it easy for new teams to adopt without rewriting existing build logic.  

**Practical Adoption Path**  
1. **Pilot Integration** – Clone the repo and add the Foundry Gradle plugin to a sandbox Android module; run the provided sample tasks to verify that builds succeed locally.  
2. **Component Migration** – Gradually replace custom build scripts in an existing feature module with Foundry’s DSL, re‑using its UI component libraries where appropriate.  
3. **CI/CD Hook‑up** – Extend your CI pipeline (e.g., GitHub Actions, CircleCI) to invoke the Foundry tasks, ensuring that linting, unit tests, and UI packaging are automatically enforced.  
4. **Documentation & Training** – Leverage the project’s README and generated API docs to onboard developers; hold a short walkthrough to cover the most common commands and extension points.  

**Production Readiness**  
- **Maturity**: Medium. The tool is stable enough for internal prototypes and workflow automation, but production use should be preceded by a dependency audit and a review of the release cadence.  
- **Community Signals**: 474 stars, 21 forks, and recent activity indicate a healthy interest, though the contributor base is relatively small.  
- **Risks**: No critical licensing or security red flags have been identified, but you should verify the OSS license compatibility with your product and confirm that the maintainers are responsive to security issues.  
- **Maintenance**: Because Foundry is tied to Slack’s internal Android stack, keep an eye on upstream changes (e.g., Gradle or Android Gradle Plugin upgrades) that may require you to pin or upgrade the plugin version.  

Overall, slackhq/foundry offers a pragmatic way to speed up Android UI development, and with a modest due‑diligence effort it can be safely introduced into production pipelines.

### Русский

Резюме проекта slackhq/foundry:

С помощью slackhq/foundry можно ускорить процесс разработки пользовательских интерфейсов для Android-приложений, снижая объем личной работы с UI. Этот проект представляет собой набор инструментов Gradle и IntelliJ для автоматизации процесса разработки. Он особенно полезен для внутренних потоков разработки и прототипирования, но требует тщательного рассмотрения зависимостей и поддержки перед внедрением в производство.

### 中文

**项目简介（2‑3 句话）**  
slackhq/foundry 是 Slack Android 代码库中使用的 Gradle 与 IntelliJ 构建工具套件，提供统一的构建脚本、插件与 IDE 配置，帮助团队快速编译、打包和发布 Android UI。它抽象了大量重复的 UI 编译与资源处理逻辑，使开发者能够专注于业务界面实现。

**价值**  
- **加速 UI 开发**：通过统一的构建插件和预置的任务，减少手动配置和重复工作，让产品 UI 能更快交付。  
- **复用组件**：内置的模块化依赖管理和资源合并机制，使团队可以在多个子项目之间共享 UI 组件和资源。  
- **提升交付质量**：统一的检查、代码生成和 lint 规则在编译阶段即捕获错误，降低 UI 回归风险。

**典型接入方式**  
1. **在根项目的 `build.gradle.kts`（或 `build.gradle`）中引入插件**  
   ```kotlin
   plugins {
       id("com.slack.foundry") version "x.y.z"
   }
   ```
2. **在子模块中使用 Foundry 提供的 DSL**，如 `foundry { uiComponent("myButton") }` 来声明 UI 组件依赖。  
3. **在 IntelliJ/Android Studio 中安装对应的插件**（可通过 IDE Marketplace），插件会自动识别 `foundry` 配置并提供代码补全、模板和调试支持。  
4. **通过 CLI**（`./gradlew foundryPublish`）完成组件打包与内部 Maven/Google Artifact Registry 发布。

**生产可用性**  
- **成熟度**：GitHub 474 ★、活跃更新（截至 2026‑07‑02），代码主要使用 Kotlin，社区活跃度中等。  
- **适用场景**：非常适合内部原型、功能演示或 Slack 内部的 UI 流水线；在对外生产环境使用前，需要对依赖版本、许可证（MIT/Apache）以及安全审计进行一次完整评估。  
- **风险**：目前缺少明确的长期维护者承诺，且未提供完整的安全报告；因此在正式生产环境部署前，建议：  
  1. **锁定插件版本**，防止意外升级。  
  2. **执行内部安全扫描**（如 OWASP Dependency‑Check）。  
  3 **制定回滚方案**，以防构建插件出现不兼容变更。  

总体而言，foundry 在提升 Android UI 开发效率方面表现突出，适合作为内部或半生产环境的构建基础设施；在完成上述审查后即可安全投入生产。

## 🧭 Practical evaluation

**Value:** slackhq/foundry helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 474 GitHub stars
- 21 forks
- updated 2026-07-02
- primary language: Kotlin
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 57/100 |
| topics | 75/100 |
| outlook | 56/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/slackhq/foundry) · [← Back to Mobile](./README.md)</sub>
