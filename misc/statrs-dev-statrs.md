# statrs-dev/statrs

[![Stars](https://img.shields.io/github/stars/statrs-dev/statrs?style=flat-square&color=yellow)](https://github.com/statrs-dev/statrs/stargazers) [![Forks](https://img.shields.io/github/forks/statrs-dev/statrs?style=flat-square&color=blue)](https://github.com/statrs-dev/statrs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Statistical computation library for Rust

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 806 |
| 🍴 **Forks** | 110 |
| 💻 **Language** | Rust |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
statrs‑dev/statrs is an open‑source Rust library that provides a broad suite of statistical functions (distributions, hypothesis testing, descriptive statistics, etc.). With over 800 ⭐ on GitHub and recent activity (last commit 2026‑07‑01), it can be a handy tool for prototypes or internal data‑analysis pipelines, provided its API matches your workflow.  

**Value**  
The crate bundles many common statistical algorithms in a single, pure‑Rust dependency, eliminating the need to call out to external C/Fortran libraries or to re‑implement routine calculations. This can speed up development of scientific, analytics, or machine‑learning components that already run in a Rust codebase.  

**Practical adoption path**  

1. **Assess API fit** – Review the README and source to confirm that the needed distributions, tests, or utilities are exposed in a way that aligns with your data‑processing flow.  
2. **Add as a dependency** – Include `statrs = "x.y"` in your `Cargo.toml` and run `cargo check` to see if any version conflicts arise with existing crates.  
3. **Prototype** – Write a small test program that exercises the specific functions you need (e.g., sampling from a normal distribution, performing a chi‑square test). This will surface any missing features or performance concerns early.  
4. **Evaluate maintenance** – Check the issue tracker and recent pull‑request activity to gauge how actively bugs are addressed; consider forking if you anticipate needing custom extensions.  

**Production readiness**  
The project sits at a **medium** readiness level. Its recent updates and sizable star count suggest a healthy community, but the lack of detailed integration documentation means you should perform a manual validation step before committing to production. For internal tools or prototypes, adopting statrs is low‑risk after the short prototype phase. For mission‑critical services, conduct a thorough review of the crate’s test coverage, audit its dependencies for security updates, and establish a maintenance plan (e.g., pinning a specific version and monitoring upstream releases).

### Русский

**statrs-dev/statrs** — это открытая библиотека на Rust для статистических вычислений, предоставляющая широкий набор распределений, функций плотности, генераторов случайных чисел и методов оценки параметров. Она подходит для прототипов и внутренних аналитических сервисов, где требуется быстрый и типобезопасный расчёт статистических метрик, однако из‑за скудной документации по интеграции её следует предварительно протестировать и оценить затраты на настройку перед использованием в продакшене. В текущем состоянии проект имеет средний уровень готовности: активные обновления, 800+ звёзд и 110 форков, но требуется ручная проверка совместимости и поддержки зависимостей.

### 中文

statrs-dev/statrs 是一个专注于统计计算的 Rust 库，提供丰富的分布、随机数生成和统计函数，适合需要高性能数值分析的项目。典型的接入方式是在 Cargo.toml 中添加依赖 `statrs = "0.14"`（或对应版本），然后在代码中直接调用其 API 进行概率分布、假设检验等操作。由于其维护活跃且星标较多，可用于原型开发和内部工作流；但在生产环境前建议手动检查依赖兼容性和集成成本，以确保满足稳定性和安全性要求。

## 🧭 Practical evaluation

**Value:** statrs-dev/statrs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 806 GitHub stars
- 110 forks
- updated 2026-07-01
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 62/100 |
| topics | 0/100 |
| outlook | 61/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/statrs-dev/statrs) · [← Back to Misc](./README.md)</sub>
