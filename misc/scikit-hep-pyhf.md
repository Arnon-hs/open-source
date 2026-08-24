# scikit-hep/pyhf

[![Stars](https://img.shields.io/github/stars/scikit-hep/pyhf?style=flat-square&color=yellow)](https://github.com/scikit-hep/pyhf/stargazers) [![Forks](https://img.shields.io/github/forks/scikit-hep/pyhf?style=flat-square&color=blue)](https://github.com/scikit-hep/pyhf/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> pure-Python HistFactory implementation with tensors and autodiff

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 301 |
| 🍴 **Forks** | 100 |
| 💻 **Language** | Python |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asymptotic-formulas` `closember` `cls` `frequentist-statistics` `hep` `hep-ex` `high-energy-physics` `histfactory` `jax` `numpy` `python` `scientific-computations`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary (2‑3 sentences)**  
scikit‑hep/pyhf is a pure‑Python implementation of the HistFactory statistical model, built on tensor operations and automatic differentiation. It lets HEP analysts define, fit, and combine complex likelihoods without writing custom C++ code, while remaining fully compatible with the broader scikit‑hep ecosystem. The library is actively maintained, widely used, and comes with extensive documentation and examples.

**Value proposition**  
- **Unified statistical workflow** – By handling model building, fitting, and hypothesis testing in pure Python, pyhf removes the need for bespoke C++/ROOT pipelines, reducing development overhead and simplifying reproducibility.  
- **Tensor‑backed performance** – Leveraging NumPy, JAX, PyTorch, or TensorFlow back‑ends provides GPU/CPU acceleration and automatic differentiation, speeding up large‑scale fits that would otherwise be bottlenecks.  
- **Interoperability** – The library integrates naturally with other scikit‑hep tools (e.g., uproot, awkward, hist) and standard data‑science stacks, enabling seamless data ingestion, transformation, and downstream analysis.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the tutorial notebooks, and verify that existing HistFactory XML cards can be parsed and reproduced with pyhf.  
2. **Pilot integration** – Replace a single analysis channel in a current workflow with a pyhf model, using the same data formats (ROOT files via uproot) to confirm numerical consistency.  
3. **Full migration** – Gradually refactor the remaining channels, adopt a tensor back‑end that matches your compute environment (e.g., JAX for GPU), and incorporate pyhf into CI pipelines for regression testing.  
4. **Productionization** – Containerize the environment (Docker/Singularity), lock dependencies with a `requirements.txt` or `conda` environment, and use the library’s built‑in logging and profiling tools for monitoring in production runs.

**Production readiness**  
- **Activity & community** – 301 stars, 100 forks, recent commits (as of 2026‑06‑30), and active issue discussions indicate a healthy, responsive maintainer base.  
- **Maturity** – The core API is stable, documented, and covered by unit tests; multiple back‑ends have been vetted in real HEP analyses.  
- **Risk assessment** – No major metadata or licensing concerns identified; a final security audit of dependencies and confirmation of maintainer commitment are advisable, but overall the project is ready for a serious pilot or production deployment.

### Русский

**scikit‑hep/pyhf** — это чисто‑питоновская реализация HistFactory, использующая тензоры и автодифференцирование, что позволяет быстро и точно выполнять статистический анализ данных в HEP без необходимости писать собственный низкоуровневый код. Типичный сценарий внедрения — подключить pyhf к существующей аналитической цепочке (например, в рамках прототипа сервиса, где результаты вычислений сохраняются в базе) и через небольшую proof‑of‑concept‑проект проверить совместимость с вашими данными и пайплайнами. Проект имеет высокий уровень готовности к production: активные коммиты, более 300 звёзд на GitHub, широкое принятие в сообществе и стабильную экосистему, требующая лишь финальной проверки лицензии и безопасности.

### 中文

**简短介绍**

scikit-hep/pyhf 是一个纯 Python 的 HistFactory 实现，使用张量和自动微分功能。它可以帮助团队减少自定义管道，提高数据访问速度和管理持久化。

**价值**

scikit-hep/pyhf 的价值在于：

* 管理持久化：通过使用张量和自动微分功能，scikit-hep/pyhf 提供了一个高效的数据管理方式。
* 加速数据访问：使用张量和自动微分功能，可以显著加速数据访问速度。
* 构建数据库驱动应用：scikit-hep/pyhf 可以帮助团队快速构建数据库驱动的应用。

**典型接入方式**

接入 scikit-hep/pyhf 可以通过以下步骤：

1. 检查 README 文档，了解项目的基本使用和接入方式。
2. 构建一个小型的原型应用，验证 scikit-hep/pyhf 的功能和性能。
3. 根据原型应用的需求，进一步扩展和优化 scikit-hep/pyhf 的功能。

**生产可用性**

scikit-hep/pyhf 的生产可用

## 🧭 Practical evaluation

**Value:** scikit-hep/pyhf helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 301 GitHub stars
- 100 forks
- updated 2026-06-30
- primary language: Python
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/scikit-hep/pyhf) · [← Back to Misc](./README.md)</sub>
