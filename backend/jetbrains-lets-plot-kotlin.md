# JetBrains/lets-plot-kotlin

[![Stars](https://img.shields.io/github/stars/JetBrains/lets-plot-kotlin?style=flat-square&color=yellow)](https://github.com/JetBrains/lets-plot-kotlin/stargazers) [![Forks](https://img.shields.io/github/forks/JetBrains/lets-plot-kotlin?style=flat-square&color=blue)](https://github.com/JetBrains/lets-plot-kotlin/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Grammar of Graphics for Kotlin

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 484 |
| 🍴 **Forks** | 39 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`charts` `geotools` `ggplot` `ggplot2` `graphics` `jupyter` `jupyter-notebooks` `jvm` `kotlin` `kotlin-api` `plot` `plot-library`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Project Summary:**

JetBrains/lets-plot-kotlin is an open-source project that provides a Grammar of Graphics for Kotlin, enabling developers to add AI capabilities to their applications without starting from scratch. This project allows for the rapid prototyping of AI features, building of RAG (Relationship-Action-Goal) or agent workflows, and evaluating model tooling. With its recent activity, strong adoption, and well-established ecosystem, lets-plot-kotlin is a high-production-readiness open-source candidate.

**Value:**

The value proposition of JetBrains/lets-plot-kotlin lies in its ability to simplify the addition of AI capabilities to existing applications. By providing a Grammar of Graphics for Kotlin, developers can leverage this foundation to build and prototype AI features, workflows, and tooling, saving time and effort. This project enables developers to focus on the application logic rather than building a custom AI stack from scratch.

**Practical Adoption Path:**

To adopt JetBrains/lets-plot-kotlin, developers can follow these steps:

1. **Evaluate the project**: Review the project's documentation, code, and community activity to ensure it meets the project's requirements.
2. **Integrate the library**: Include the lets-plot-kotlin library in the project's dependencies and follow the provided guidelines

### Русский

Резюме проекта JetBrains/lets-plot-kotlin:

JetBrains/lets-plot-kotlin - это открытый источник проект, который предоставляет Grammar of Graphics для Kotlin, позволяя добавлять функциональность AI без создания новой базовой стэка моделей. Этот проект идеально подходит для прототипирования AI-особенностей, построения RAG или агентных потоков, а также оценки инструментов моделирования. Проект готов к производству на высоком уровне, с сильными сигналами активности, адоптации и экосистемы, что делает его серьезным кандидатом для пилотного проекта.

### 中文

**项目简介（2‑3 句话）**  
JetBrains/lets‑plot‑kotlin 是基于 Grammar of Graphics 的 Kotlin 可视化库，提供类似 R ggplot2 的声明式绘图 API，帮助开发者在 Kotlin 应用中快速生成高质量统计图表。

**价值**  
- **快速原型**：无需手写底层绘图逻辑，即可用几行代码完成复杂图形，极大缩短数据探索和报告的迭代周期。  
- **统一语言栈**：在 Kotlin 后端或 Android 前端直接使用，无需在 Java/Kotlin 与 Python/R 之间切换，降低跨语言集成成本。  
- **生态兼容**：与 JetBrains 的其它工具（如 Kotlin DSL、IntelliJ 插件）深度集成，便于在现有项目中无缝引入可视化能力。

**典型接入方式**  
1. **Gradle/Maven 依赖**：在 `build.gradle.kts` 中添加 `implementation("org.jetbrains.lets-plot:lets-plot-kotlin:VERSION")`。  
2. **DSL 编码**：使用 Kotlin DSL 描述图层（`geomLine`, `geomBar` 等），如 `letsPlot(data) + geomLine { x = "time"; y = "value" }`。  
3. **输出渠道**：图表可直接渲染为 HTML、SVG、PNG，或通过 `show()` 在浏览器/IDE 中预览，也支持在服务器端生成图片返回给前端。  
4. **CLI/SDK**：提供 `lets-plot-cli` 可在脚本或 CI 中批量生成图表，适用于自动化报告或模型评估。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目仍在持续更新，拥有 484+ Stars、39 Forks，14 个相关主题，表明社区和 JetBrains 官方均保持活跃维护。  
- **成熟度**：库已在多个 JetBrains 产品和开源项目中使用，具备完整的文档、示例和类型安全的 Kotlin API，适合直接用于生产环境。  
- **风险**：目前未发现重大元数据或许可证风险，但仍建议在正式投产前完成安全审计并确认维护者响应速度。  

综上，lets‑plot‑kotlin 是一个高质量、易集成且已具备生产级别稳定性的 Kotlin 可视化解决方案，适合在数据密集型后端服务、Android 应用或 AI 原型平台中快速添加图表功能。

## 🧭 Practical evaluation

**Value:** JetBrains/lets-plot-kotlin helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 484 GitHub stars
- 39 forks
- updated 2026-06-30
- primary language: Kotlin
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/JetBrains/lets-plot-kotlin) · [← Back to Backend](./README.md)</sub>
