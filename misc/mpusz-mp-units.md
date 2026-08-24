# mpusz/mp-units

[![Stars](https://img.shields.io/github/stars/mpusz/mp-units?style=flat-square&color=yellow)](https://github.com/mpusz/mp-units/stargazers) [![Forks](https://img.shields.io/github/forks/mpusz/mp-units?style=flat-square&color=blue)](https://github.com/mpusz/mp-units/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> The Domain-Correct Quantities and Units Library for C++ — full quantity kind safety, ISO 80000 compliant, C++29 standardization candidate.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 119 |
| 💻 **Language** | C++ |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cmake` `conan` `cpp` `cpp20` `cpp23` `dimensional-analysis` `dimensions` `isq` `library` `physical-quantities` `physical-units` `quantity`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary:** mpusz/mp-units is an open-source C++ library that provides a domain-correct quantities and units system, ensuring full quantity kind safety and compliance with the ISO 80000 standard. This library is suitable for research and automation of market workflows, particularly in trading and AI/ML applications. With strong adoption and recent activity, mpusz/mp-units is production-ready for a serious pilot.

**Value:** The library offers a robust and standardized way to handle quantities and units in C++, which is essential for accurate and reliable market workflow automation. By using mpusz/mp-units, developers can ensure that their applications adhere to the ISO 80000 standard and are free from quantity kind-related errors.

**Practical Adoption Path:** To integrate mpusz/mp-units into a project, start with a small proof-of-concept and carefully review the README documentation. This will help evaluate the library's feasibility and identify potential integration challenges. Once familiar with the library, developers can validate the setup cost before committing to a larger-scale implementation.

**Production Readiness:** mpusz/mp-units has demonstrated strong production readiness, with recent activity, adoption, and ecosystem signals indicating its maturity. The library has received 1440 GitHub stars, 119 forks, and regular updates, making it a reliable

### Русский

**mpusz/mp-units** — это библиотека C++ для работы с величинами и единицами измерения, обеспечивающая полную типовую безопасность и соответствие ISO 80000; она уже рассматривается как кандидат для включения в стандарт C++29. Для типичного внедрения в финансовых проектах её используют в качестве ядра расчётов при исследовании торговых стратегий, бэктестинге и мониторинге рыночных процессов, начиная с небольшого proof‑of‑concept, проверяя примеры в README. Показатели активности (1440 звёзд, 119 форков, частые обновления) свидетельствуют о высокой готовности к production‑использованию, однако следует заранее уточнить детали интеграции и оценить затраты на настройку.

### 中文

**项目简介（2‑3 句）**  
mpusz/mp‑units 是一套面向 C++ 的“域正确”量与单位库，提供完整的量种类安全、符合 ISO 80000 标准的单位体系，并已提交为 C++29 的标准化候选。它通过编译期检查防止单位错误，让物理量的运算既安全又高效。

**价值**  
- **量级安全**：在编译期捕获单位不匹配，避免因单位换算错误导致的交易系统漏洞。  
- **标准兼容**：遵循 ISO 80000，便于与行业规范、金融模型和科研代码对接。  
- **高性能**：零运行时开销，适合对延迟敏感的高频交易和实时监控场景。  

**典型接入方式**  
1. **依赖管理**：使用 CMake 的 `FetchContent` 或者 Conan 包管理器将库拉入项目。  
2. **概念引入**：在交易算法或回测框架中，用 `quantity<double, unit::currency::usd>`、`quantity<double, unit::time::second>` 等类型替代裸 `double`。  
3. **小规模验证**：先在一个独立的子模块（如价格转换或风险计算）实现一个 POC，确认编译期检查生效后再逐步推广到整个系统。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑05，项目仍在维护，最近一次提交仅几天前；GitHub 计 1440 ★、119 Fork，社区活跃。  
- **生态兼容**：纯 C++ 实现，无外部运行时依赖，易嵌入现有 C++17/20/23 代码基。  
- **成熟度**：已被多个开源项目引用，具备正式的单元测试和 CI，适合作为正式生产环境的 OSS 组件进行试点。  
- **风险**：文档和集成示例相对有限，建议在正式投入前通过小规模原型验证集成成本与编译时间开销。  

总体来看，mpusz/mp‑units 在保证量级安全的同时保持高性能，是金融研究、策略回测以及实时市场工作流自动化的可靠底层工具，具备直接用于生产环境的条件。

## 🧭 Practical evaluation

**Value:** mpusz/mp-units helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1440 GitHub stars
- 119 forks
- updated 2026-07-05
- primary language: C++
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/mpusz/mp-units) · [← Back to Misc](./README.md)</sub>
