# Tinder/bazel-diff

[![Stars](https://img.shields.io/github/stars/Tinder/bazel-diff?style=flat-square&color=yellow)](https://github.com/Tinder/bazel-diff/stargazers) [![Forks](https://img.shields.io/github/forks/Tinder/bazel-diff?style=flat-square&color=blue)](https://github.com/Tinder/bazel-diff/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Performs Bazel Target Diffing between two revisions in Git, allowing for Test Target Selection and Selective Building

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 510 |
| 🍴 **Forks** | 81 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bazel` `target-selection` `test-selection`

## 🎯 Categories

DevTools

## 📝 Summary

### English

Tinder/bazel-diff speeds up frontend delivery by diffing Bazel targets across Git revisions to enable selective test running and building, letting teams reuse UI components and ship interfaces with less custom code. Adoption requires manual inspection and validation of setup costs due to sparse integration signals, making it best suited for prototypes or internal workflows. Before moving to production, check dependencies and maintenance overhead, as the tool is currently rated medium‑readiness.

### Русский

**Tinder/bazel-diff** — это open‑source утилита на Kotlin, которая сравнивает набор Bazel‑таргетов между двумя Git‑ревизиями, позволяя автоматически выбрать тестовые таргеты и выполнять селективную сборку. Она упрощает ускоренную доставку пользовательских интерфейсов, позволяя быстро собрать только изменённые UI‑компоненты и тем самым сократить кастомную работу над фронтендом. Проект находится на среднем уровне готовности: подходит для прототипов и внутренних процессов, но требует ручной проверки интеграции и контроля зависимостей перед выводом в продакшн.

### 中文

Tinder/bazel‑diff 通过在两个 Git 版本之间进行 Bazel 目标差分，帮助团队快速识别需要重新构建或测试的目标，从而实现更精准的构建和测试选择，降低不必要的编译开销。典型的接入方式是在 CI/CD 流程中加入该工具的脚本，基于代码变更自动生成 Bazel 构建或测试目标列表，随后交给 Bazel 执行。虽然该项目拥有 510 颗星且定期更新，但其集成信息较为稀疏，建议在采用前进行手动检查和依赖评估，适用于原型或内部工作流，生产环境使用前需做好维护和兼容性验证。

## 🧭 Practical evaluation

**Value:** Tinder/bazel-diff helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 510 GitHub stars
- 81 forks
- updated 2026-06-29
- primary language: Kotlin
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 58/100 |
| topics | 38/100 |
| outlook | 64/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 64/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/Tinder/bazel-diff) · [← Back to DevTools](./README.md)</sub>
