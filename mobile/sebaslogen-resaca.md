# sebaslogen/resaca

[![Stars](https://img.shields.io/github/stars/sebaslogen/resaca?style=flat-square&color=yellow)](https://github.com/sebaslogen/resaca/stargazers) [![Forks](https://img.shields.io/github/forks/sebaslogen/resaca?style=flat-square&color=blue)](https://github.com/sebaslogen/resaca/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Compose Multiplatform library to scope ViewModels to a Composable, surviving configuration changes and navigation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 636 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `android-architecture` `android-library` `architecture-components` `compose` `compose-multiplatform` `compose-multiplatform-library` `hilt-dependency-injection` `koin-dependency-injection` `kotlin` `viewmodel`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief summary**  
Resaca is a Kotlin‑Multiplatform Compose library that lets you scope a ViewModel to a specific Composable, automatically surviving configuration changes and navigation events. It simplifies state‑sharing across UI layers while keeping the ViewModel lifecycle tightly coupled to the composable that uses it.

**Value proposition**  
- **Reduced boilerplate** – No need to manually hoist ViewModels to navigation graphs or recreate them on rotation; Resaca handles the scoping automatically.  
- **Consistent state** – The same ViewModel instance survives configuration changes and navigation, preventing UI flicker and data loss.  
- **Multiplatform support** – Works on Android and other Compose targets (desktop, web), enabling a single codebase for shared UI logic.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the sample app, and follow the README to add the `resaca` dependency to a small feature module.  
2. **Integrate a test composable** – Replace an existing `viewModel()` call with `resacaViewModel { … }` and observe that the instance persists across device rotation and navigation.  
3. **Gradual rollout** – Once the pattern is validated, refactor other screens incrementally, keeping both the legacy and Resaca‑scoped ViewModels during the transition.  
4. **CI/CD check** – Add a simple unit test that asserts the same ViewModel instance is returned after a simulated configuration change.

**Production readiness**  
- **Maturity**: Medium. The library has 636 stars, recent commits (as of 2026‑05‑12), and a modest number of forks, indicating community interest but limited large‑scale adoption.  
- **Stability**: The core API is stable, but documentation around full integration (e.g., DI, navigation‑component interop) is sparse, so teams should allocate time for exploratory testing.  
- **Risks**: Integration steps are not fully described in the metadata; you’ll need to verify compatibility with your existing DI framework and navigation setup. Dependency management and long‑term maintenance should be reviewed before committing to production use.  

Overall, Resaca is a promising tool for teams looking to streamline Compose ViewModel lifecycles, especially in prototype or internal projects, with a manageable path to production after a small proof‑of‑concept and due‑diligence on integration overhead.

### Русский

**sebaslogen/resaca** — это мультиплатформенная библиотека Compose, позволяющая привязывать ViewModel к конкретному Composable и сохранять её состояние при изменениях конфигурации и навигации. Она упрощает работу с данными в мобильных проектах, ускоряя прототипирование и обеспечивая более надёжный доступ к базе без написания собственного « plumbing». Готовность к production — средняя: библиотека уже имеет 600+ звёзд и активные обновления, но путь интеграции не полностью документирован, поэтому рекомендуется начать с небольшого proof‑of‑concept и тщательно проверить зависимости и процесс настройки перед использованием в продакшене.

### 中文

**项目简介**  
`sebaslogen/resaca` 是一个基于 Jetpack Compose Multiplatform 的库，能够在 Composable 范围内为 ViewModel 提供作用域，并在配置变化（如屏幕旋转）和页面导航时保持实例不被销毁。  

**价值**  
- **持久化与状态管理**：自动把 ViewModel 与 Composable 绑定，避免手动编写跨页面、跨配置的状态保存代码。  
- **提升开发效率**：省去大量自定义 plumbing，让团队可以更专注于业务逻辑和 UI 实现。  
- **跨平台支持**：同一套代码可在 Android、Desktop、Web（via Kotlin/JS）等平台使用，降低多平台维护成本。  

**典型接入方式**  
1. **在项目中添加依赖**（示例 Gradle Kotlin DSL）：  
   ```kotlin
   dependencies {
       implementation("io.github.sebaslogen:resaca:<latest-version>")
   }
   ```  
2. **在根 Composable 中声明作用域**：  
   ```kotlin
   @Composable
   fun MyApp() {
       ResacaScope {
           // 这里的所有子 composable 都可以通过 rememberResacaViewModel() 获取同一个 ViewModel 实例
           HomeScreen()
       }
   }
   ```  
3. **获取 ViewModel**：  
   ```kotlin
   @Composable
   fun HomeScreen(viewModel: MyViewModel = rememberResacaViewModel()) {
       // 使用 viewModel 正常工作，配置变化或导航后仍保持同一实例
   }
   ```  
4. **可选**：在需要持久化的 ViewModel 中使用 `SavedStateHandle` 或自行实现 `ResacaPersistable` 接口，以实现更细粒度的状态保存。  

**生产可用性**  
- **成熟度**：已有 636 ⭐、16 🍴，最近一次提交在 2026‑05‑12，活跃度尚可。  
- **适用场景**：非常适合内部工具、原型以及需要快速交付的多平台项目；在对稳定性要求极高的核心业务系统中使用前，建议进行充分的集成测试。  
- **风险与注意事项**：  
  - 文档主要集中在 README，完整的集成指南相对有限，建议先在小型 PoC 中验证配置流程。  
  - 依赖于 Kotlin Multiplatform 与 Compose 生态，确保项目的 Compose 版本与库兼容。  
  - 关注后续维护频率和社区响应，以防止出现长期未更新的情况。  

**结论**：`resaca` 为 Compose Multiplatform 项目提供了轻量级、开箱即用的 ViewModel 作用域管理，能够显著减少状态持久化的样板代码。对原型或内部业务系统可直接投入使用；若用于生产环境，建议在正式上线前完成完整的兼容性和回归测试。

## 🧭 Practical evaluation

**Value:** sebaslogen/resaca helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 636 GitHub stars
- 16 forks
- updated 2026-05-12
- primary language: Kotlin
- 11 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/sebaslogen/resaca) · [← Back to Mobile](./README.md)</sub>
