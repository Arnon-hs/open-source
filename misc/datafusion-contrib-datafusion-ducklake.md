# datafusion-contrib/datafusion-ducklake

[![Stars](https://img.shields.io/github/stars/datafusion-contrib/datafusion-ducklake?style=flat-square&color=yellow)](https://github.com/datafusion-contrib/datafusion-ducklake/stargazers) [![Forks](https://img.shields.io/github/forks/datafusion-contrib/datafusion-ducklake?style=flat-square&color=blue)](https://github.com/datafusion-contrib/datafusion-ducklake/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> A Rust-native DuckLake engine built on Apache DataFusion

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 140 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | Rust |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
datafusion-contrib/datafusion‑ducklake is a Rust‑native engine that extends Apache DataFusion with DuckLake‑style query capabilities, enabling developers to build user‑facing data interfaces with far less custom UI code. It’s a community‑driven project (≈140 ★, 12 forks) that is actively maintained as of June 2026, but its integration points are not well documented, requiring a manual review before adoption.

**Value**  
By providing ready‑made query execution and result formatting layers, the project lets frontend teams focus on UI composition rather than building data‑access plumbing from scratch. Reusing its components can accelerate product UI development, promote consistency across dashboards, and reduce the engineering effort needed to expose DataFusion‑backed data to end users.

**Practical adoption path**  
1. **Evaluate the repository** – clone the project, run the example binaries, and verify that the DuckLake query semantics match your data model.  
2. **Prototype integration** – wrap the engine in a small service (e.g., a gRPC or REST endpoint) and connect a test UI to confirm end‑to‑end data flow.  
3. **Inspect dependencies** – review Cargo.toml for version compatibility with your existing DataFusion stack and ensure no conflicting native libraries.  
4. **Add integration tests** – codify the expected query results and UI payloads to catch regressions early.  
5. **Gradual rollout** – replace custom UI data‑fetch layers with the DuckLake service in a low‑risk feature or internal tool before scaling to production.

**Production readiness**  
The project sits at a **medium** readiness level: it is functional enough for prototypes and internal workflows, but it lacks comprehensive integration documentation and automated CI/CD pipelines. Before committing to production, teams should perform a thorough dependency audit, add their own health‑check and monitoring wrappers, and consider maintaining a fork or contributing back fixes to mitigate future maintenance risk.

### Русский

**datafusion-contrib/datafusion-ducklake** — это Rust‑native движок DuckLake, построенный поверх Apache DataFusion, который позволяет быстро собрать пользовательские интерфейсы, минимизируя написание собственного UI‑кода. Его типичное применение — ускоренная разработка продуктовых UI и повторное использование готовых компонентов в прототипах или внутренних инструментах, однако перед внедрением требуется ручная проверка интеграции, так как метаданные о связях скудны. Готовность к production — средняя: проект подходит для прототипов и ограниченных внутренних сценариев, но перед запуском в продакшн следует оценить затраты на настройку, зависимости и долгосрочное обслуживание.

### 中文

**介绍**

datafusion-contrib/datafusion-ducklake 是一个基于 Apache DataFusion 的 Rust 原生 DuckLake 引擎。它可以帮助开发者快速构建产品 UI，并且可以重用界面组件，改善前端交付。

**价值**

datafusion-contrib/datafusion-ducklake 的主要价值在于帮助开发者快速构建产品 UI，减少自定义 UI 的工作量。它可以帮助开发者:

* 快速构建产品 UI
* 重用界面组件
* 改善前端交付

**典型接入方式**

由于 datafusion-contrib/datafusion-ducklake 需要手动检查和验证，因此需要进行以下步骤：

1. 检查项目的 GitHub 页面，并了解项目的文档和说明。
2. 验证项目的依赖和维护情况。
3. 手动检查和验证项目的接入方式。

**生产可用性**

datafusion-contrib/datafusion-ducklake 的生产可用性为 Medium。它适合用于原型或内部工作流程的快速开发，但需要进行依赖和维护检查后方可用于生产环境。

## 🧭 Practical evaluation

**Value:** datafusion-contrib/datafusion-ducklake helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 140 GitHub stars
- 12 forks
- updated 2026-06-30
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 46/100 |
| topics | 0/100 |
| outlook | 57/100 |
| quality | 53/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/datafusion-contrib/datafusion-ducklake) · [← Back to Misc](./README.md)</sub>
