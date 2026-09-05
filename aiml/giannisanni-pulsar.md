# giannisanni/pulsar

[![Stars](https://img.shields.io/github/stars/giannisanni/pulsar?style=flat-square&color=yellow)](https://github.com/giannisanni/pulsar/stargazers) [![Forks](https://img.shields.io/github/forks/giannisanni/pulsar?style=flat-square&color=blue)](https://github.com/giannisanni/pulsar/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> SSD-streaming inference engine for giant MoE models (Rust + CUDA). GLM 5.2 743B at 2 tok/s and Hy3 295B at 7 tok/s on two consumer 16GB GPUs. Zero-config multi-GPU: measures PCIe bandwidth, places attention and hot experts where they fit.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 105 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Rust |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cuda` `gguf` `glm` `inference-engine` `llm` `local-llm` `mixture-of-experts` `moe` `multi-gpu` `quantization` `rust` `ssd-streaming`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

Giannisanni/pulsar is an SSD‑streaming inference engine written in Rust + CUDA that enables fast, zero‑config multi‑GPU execution of massive Mixture‑of‑Experts models (e.g., GLM‑5.2 743B at 2 tok/s, Hy3 295B at 7 tok/s on two 16 GB consumer GPUs). Its value lies in accelerating research and prototyping of AI‑driven trading workflows—such as strategy back‑testing and market‑workflow monitoring—by letting users run giant MoE models without manual model‑parallel tuning. Adoption should start with a small proof‑of‑concept to validate the setup cost and README guidance, and while the project shows medium production readiness (useful for prototypes/internal tools), teams should perform dependency and maintenance checks before moving to production.

### Русский

giannisanni/pulsar — это высокопроизводительный движок SSD‑стриминговой инференции на Rust + CUDA, позволяющий запускать гигантские MoE‑модели (например, GLM 5.2 743B и Hy3 295B) на двух потребительских GPU 16 ГБ с нулевой конфигурацией за счёт автоматического измерения PCIe‑полосы и размещения внимания и «горячих» экспертов там, где они помещаются. Типовой сценарий внедрения — исследовательские или внутренние торговые workflows, где требуется быстрое бэктестинг‑ и мониторинг‑поддержка стратегий без сложной настройки. Проект имеет средний уровень готовности к production: полезен для прототипов и пилотных проектов, но перед промышленным использованием рекомендуется

### 中文

**简短介绍**
giannisanni/pulsar 是一个开源项目，用于在巨型混合精度（MoE）模型上实现实时推理引擎，支持 NVIDIA CUDA 和 Rust 编程语言。该项目能够在两个 16GB GPU 上实现高性能的推理，例如：GLM 5.2 743B 在 2 个 token/秒 Hy3 295B 在 7 个 token/秒。

**价值**
giannisanni/pulsar 帮助研究和自动化市场工作流，适用于以下场景：

* 研究交易系统
* 回测策略
* 监控市场工作流

**典型接入方式**
由于该项目的接入路径不明显，建议从小规模的 PoC（原型）开始，检查 README 文档以确保正确的接入方式。

**生产可用性**
该项目的生产可用性为中等（Medium），适合用于原型或内部工作流，需要注意依赖项和维护成本。

## 🧭 Practical evaluation

**Value:** giannisanni/pulsar helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 105 GitHub stars
- 11 forks
- updated 2026-08-02
- primary language: Rust
- 12 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-08-02 · [View on GitHub](https://github.com/giannisanni/pulsar) · [← Back to AI/ML](./README.md)</sub>
