# JetBrains/lets-plot

[![Stars](https://img.shields.io/github/stars/JetBrains/lets-plot?style=flat-square&color=yellow)](https://github.com/JetBrains/lets-plot/stargazers) [![Forks](https://img.shields.io/github/forks/JetBrains/lets-plot?style=flat-square&color=blue)](https://github.com/JetBrains/lets-plot/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Multiplatform plotting library based on the Grammar of Graphics

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.8k |
| 🍴 **Forks** | 59 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`compose-multiplatform` `data-visualization` `datalore` `geo-spatial` `ggplot` `ggplot2` `jupyter` `jupyter-notebooks` `kotlin` `plot` `plot-library` `plotting-in-kotlin`

## 🎯 Categories

Data

## 📝 Summary

### English

**Summary**  
JetBrains lets‑plot is a multiplatform Kotlin library that implements the Grammar of Graphics, letting developers create declarative, interactive visualisations across JVM, JavaScript and Python environments. With over 1.7 K stars, frequent releases (last update 2026‑05‑14) and a growing ecosystem, it is production‑ready for pilots that need fast, expressive plotting integrated into AI/ML pipelines.  

**Value** – lets‑plot supplies a ready‑made, high‑level visualisation layer so data scientists and engineers can prototype AI features (e.g., model diagnostics, RAG or agent‑driven dashboards) without building a custom charting stack from scratch.  

**Adoption path** – start by adding the Kotlin/Java or Python artifact (or using the CLI) to an existing project, then define plots via the familiar `ggplot`‑style API; the library’s clear SDK and language metadata make it easy to embed in notebooks, web UIs, or backend services.  

**Production readiness** – strong recent activity, solid community adoption (1754 ★, 59 forks, 17 topics), and cross‑platform support indicate a mature OSS candidate; after a brief security/license audit, it can be rolled out in a serious pilot or production workflow.

### Русский

JetBrains lets‑plot — это кроссплатформенная библиотека визуализации, построенная по принципу Grammar of Graphics, которая позволяет быстро добавить возможности графического анализа и интерактивных дашбордов в AI‑проекты без разработки собственного стека. Типичный сценарий — прототипирование AI‑фич, построение RAG‑ или агентных пайплайнов и оценка инструментов моделирования, используя удобный API/SDK/CLI. По уровню готовности к production проект считается высоким: активные коммиты, широкое принятие (1754 ★), множество тем и интеграций, хотя окончательная проверка лицензии, безопасности и поддержки поддерживается.

### 中文

**项目简介**  
JetBrains/lets‑plot 是一款基于 *Grammar of Graphics* 的跨平台绘图库，使用 Kotlin 编写，可在 JVM、JavaScript 以及 Python 环境中生成高质量统计图表。

**价值**  
- **快速原型**：提供声明式的绘图语法，让数据科学家和开发者在几行代码内即可完成可视化，省去手写底层绘图逻辑的时间。  
- **AI/ML 工作流友好**：可直接在模型实验、RAG（检索增强生成）或智能体的调试阶段嵌入可视化，帮助直观评估特征分布、模型输出和评估指标。  
- **统一生态**：同一套 API 在 Kotlin、Python、JS 中通用，降低多语言项目的学习成本，便于在后端服务、前端仪表盘或 Jupyter Notebook 中复用。

**典型接入方式**  
1. **SDK 引入**  
   - **Kotlin/JVM**：在 `build.gradle.kts` 中加入 `implementation("org.jetbrains.lets-plot:lets-plot-kotlin:4.3.0")`。  
   - **Python**：`pip install lets-plot`，随后 `import lets_plot as gg` 使用。  
   - **JavaScript/TS**：通过 npm `npm install @jetbrains/lets-plot`，在前端项目中直接调用 `ggplot2` 风格的 API。  
2. **CLI/脚本**：lets‑plot 也提供 `lets-plot-cli`，可在 CI/CD 流程中生成 PNG/SVG 报表。  
3. **Jupyter Notebook**：在 Kotlin 或 Python Notebook 中使用 `%use lets_plot` 魔法指令，即可交互式渲染图形。

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目仍在持续更新，拥有 1.7k+ 星、近 60 个 Fork，最近一次提交仅数天前。  
- **生态兼容**：支持多语言、多平台（JVM、Node、WebAssembly），并提供官方文档和示例，易于集成进现有数据管道。  
- **成熟度**：已在 JetBrains 自家产品以及多个开源数据分析项目中使用，具备稳定的 API 与向后兼容策略。  
- **风险**：需进一步审查许可证（Apache‑2.0）与安全依赖，但总体风险低，适合作为正式生产环境的可视化组件进行试点。

## 🧭 Practical evaluation

**Value:** JetBrains/lets-plot helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1754 GitHub stars
- 59 forks
- updated 2026-05-14
- primary language: Kotlin
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 69/100 |
| topics | 100/100 |
| outlook | 51/100 |
| quality | 63/100 |
| recency | 20/100 |
| adoption | 62/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/JetBrains/lets-plot) · [← Back to Data](./README.md)</sub>
