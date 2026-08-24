# open-delivery-spec/spec

[![Stars](https://img.shields.io/github/stars/open-delivery-spec/spec?style=flat-square&color=yellow)](https://github.com/open-delivery-spec/spec/stargazers) [![Forks](https://img.shields.io/github/forks/open-delivery-spec/spec?style=flat-square&color=blue)](https://github.com/open-delivery-spec/spec/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-33%2F100-brightgreen?style=flat-square)](#)

> Mentioned in dev.to article (tag github): Your Git History Already Knows Which Code Is AI-Written. Your CI Should Too.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 33/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | devto |

## 🏷️ Topics

`devto` `github` `ai` `devops` `opensource`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The project detects AI‑generated code by mining Git history metadata and exposes the findings to CI pipelines, letting teams enforce AI‑usage policies automatically. It provides ready‑made detection logic so you can prototype AI‑aware CI checks without training your own model stack.  

**Value**  
- **Immediate AI‑awareness**: Leverages existing commit data to flag AI‑written code, saving the effort of building a custom classifier.  
- **Policy enforcement**: Enables automated gating (e.g., fail builds, add review tags) directly in CI, helping compliance and security teams keep track of AI contributions.  
- **Rapid prototyping**: Ideal for experimenting with RAG, agent‑driven workflows, or evaluating new model‑assisted tooling while keeping the detection layer lightweight.  

**Practical Adoption Path**  
1. **Pilot** – Clone the repo, run the provided CLI on a sample branch, and manually review the generated reports to understand detection confidence and false‑positive patterns.  
2. **CI Integration** – Add the tool as a step in your CI (GitHub Actions, GitLab CI, etc.) using the supplied Docker image or npm package; configure thresholds or annotation rules that match your policy.  
3. **Feedback Loop** – Collect developer feedback on flagged commits, tune the confidence cutoff, and optionally augment the metadata (e.g., add commit‑message tags) to improve signal density.  
4. **Scale** – Once the false‑positive rate is acceptable, promote the CI step to all protected branches and integrate alerts (Slack, Jira) for continuous monitoring.  

**Production Readiness**  
- **Maturity**: Rated *Medium* – the core detection works well for prototypes and internal workflows, but the metadata signals are sparse, so manual validation is required before fully trusting the results.  
- **Dependencies & Maintenance**: Verify the project’s license, check the activity of its issue tracker, and ensure the underlying language/runtime versions align with your stack.  
- **Risk Mitigation**: Run a parallel “dry‑run” mode in production to gather metrics without breaking builds, and establish a fallback process (e.g., manual code review) for ambiguous cases.  

Overall, the tool offers a low‑friction way to make CI AI‑aware, suitable for early‑stage adoption and internal tooling, provided you perform the recommended validation and monitoring steps before treating it as a production‑critical gate.

### Русский

**Your Git History Already Knows Which Code Is AI‑Written. Your CI Should Too** — это open‑source‑инструмент, который автоматически извлекает метаданные о том, какой код был сгенерирован ИИ, из истории Git и делает их доступными в CI‑pipeline, позволяя быстро прототипировать AI‑фичи, строить RAG‑ и агентные воркфлоу, а также оценивать инструменты моделей без необходимости обучать собственные модели. Типичный сценарий — подключить плагин к существующему репозиторию, настроить проверку в CI и использовать полученные сигналы для автоматической маркировки, аудита или отката AI‑сгенерированного кода; перед вводом в продакшн рекомендуется вручную проверить метаданные, так как сигналы могут быть редкими. Готовность к production — средняя: решение подходит для прототипов и внутренних процессов, но требует проверки лицензии, поддержки и частоты релизов перед масштабным внедрением.

### 中文

**项目简介**

Your Git History Already Knows Which Code Is AI-Written. Your CI Should Too. 是一个开源项目，旨在帮助开发者在 Git 历史中识别 AI 生成的代码，并将其整合到 CI 流程中。

**价值**

该项目的价值在于，它可以帮助开发者在不从头搭建 AI 模型栈的情况下，添加 AI 能力。它适用于快速 prototyping AI 特性、构建 RAG 或代理工作流、评估模型工具等场景。

**接入方式**

该项目需要手动检查和采纳，因为其整合信号在发现的元数据中较为稀疏。开发者需要根据项目的文档和说明进行适当的配置和集成。

**生产可用性**

该项目的生产可用性为中等（Medium），适合用于快速 prototyping 或内部工作流。然而，开发者需要检查依赖项和维护项，以确保其在生产环境中正常运行。

## 🧭 Practical evaluation

**Value:** Your Git History Already Knows Which Code Is AI-Written. Your CI Should Too. helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-02
- 5 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 63/100 |
| outlook | 36/100 |
| quality | 30/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 39/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 70/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/open-delivery-spec/spec) · [← Back to AI/ML](./README.md)</sub>
