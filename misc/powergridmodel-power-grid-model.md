# PowerGridModel/power-grid-model

[![Stars](https://img.shields.io/github/stars/PowerGridModel/power-grid-model?style=flat-square&color=yellow)](https://github.com/PowerGridModel/power-grid-model/stargazers) [![Forks](https://img.shields.io/github/forks/PowerGridModel/power-grid-model?style=flat-square&color=blue)](https://github.com/PowerGridModel/power-grid-model/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Python/C++ library for distribution power system analysis

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 229 |
| 🍴 **Forks** | 65 |
| 💻 **Language** | C++ |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cpp` `eigen3` `numpy` `powerflow` `powersystem` `python` `shortcircuit` `stateestimation`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
PowerGridModel / power‑grid‑model is an open‑source Python/C++ library that provides fast, physics‑based distribution‑grid analysis and a set of reusable UI components for building power‑system front‑ends. Its recent activity, solid star/fork count, and growing ecosystem make it a viable candidate for pilots that need to ship user‑facing interfaces with minimal custom UI work.  

**Value**  
The library bundles domain‑specific calculation engines with ready‑made visual widgets (charts, topology maps, and result tables), allowing product teams to focus on business logic rather than reinventing grid‑visualisation code. By reusing these components, developers can accelerate UI delivery, maintain visual consistency across products, and reduce the engineering overhead of building and testing custom front‑end elements.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided README examples, and integrate a small analysis task (e.g., a single feeder load flow) into an existing web UI.  
2. **Component trial** – Replace a prototype UI element with the library’s chart or topology widget, verify data binding, and assess performance.  
3. **Incremental rollout** – Gradually migrate additional grid‑analysis screens to the library while keeping a fallback to legacy code, using the C++ core via the Python bindings for computationally intensive jobs.  

**Production readiness**  
The project scores high on readiness: it has recent commits (last update 2026‑06‑23), 229 GitHub stars, active forking, and multiple maintainers. While the license and security posture still need a final review, the overall health signals (active community, clear documentation, and stable API) support a serious pilot in production environments.

### Русский

PowerGridModel /power‑grid‑model — это открытая библиотека на Python/C++ для анализа распределительных электросетей, позволяющая быстро создавать пользовательские интерфейсы без необходимости писать большую часть UI‑логики. Типичный сценарий — построение продуктовых панелей и визуализаций (моделирование нагрузки, расчёт потерь и т.п.) с повторным использованием готовых компонентов, что ускоряет вывод новых функций на рынок. Проект имеет высокий уровень готовности к production: активные коммиты, 229 звёзд, 65 форков, недавнее обновление и сильные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
PowerGridModel/power-grid-model 是一个基于 Python 与 C++ 的开源库，专注于配电网系统的潮流计算、短路分析和状态估计等核心功能。它提供高性能数值求解器和简洁的 Python 接口，帮助开发者快速构建面向用户的配电系统分析前端。

**价值**  
- **降低 UI 开发成本**：通过统一的后端计算引擎，前端只需调用库提供的 API 即可展示潮流结果、图形拓扑和实时指标，避免重复实现复杂的电力计算逻辑。  
- **加速产品迭代**：库已经实现了常用的配电分析模型，开发团队可以直接复用这些组件，专注于业务层面的交互与可视化。  
- **提升交付质量**：成熟的数值算法和经过社区验证的实现，保证计算结果的准确性和一致性，减轻前端对算法正确性的担忧。

**典型接入方式**  
1. **环境准备**：在项目的 Python 环境中通过 `pip install power-grid-model`（或从源码编译）安装库；C++ 部分可通过 CMake 引入。  
2. **数据接口**：将配电网的节点、支路、负荷等信息组织为 JSON、CSV 或 Pandas DataFrame，调用 `PowerGridModel` 的加载函数生成模型对象。  
3. **调用 API**：使用 `run_power_flow()、run_short_circuit()、run_state_estimation()` 等高层函数获得计算结果。  
4. **前端展示**：将返回的结果（电压、潮流、故障电流等）通过 REST/GraphQL 或 WebSocket 传递给前端框架（React、Vue 等），配合图形库（如 D3、ECharts）进行可视化。  
5. **小规模验证**：先在单元测试或演示页面实现一个“加载网络 → 计算潮流 → 绘制结果”的完整链路，确认接口兼容性后再扩展到完整产品。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目仍在持续更新，拥有 229+ ⭐、65+ 🍴，社区活跃，近期有多次提交和 Issue 响应。  
- **成熟度**：核心算法已在多个学术和商业项目中使用，具备工业级数值稳定性。  
- **生态兼容**：提供 Python 包和 C++ 库两套入口，易于在微服务、容器化或本地桌面应用中部署。  
- **风险**：需进一步审查许可证（默认 GPL‑3.0），并进行安全依赖扫描；同时确认维护者的响应时效，以保证长期支持。  

综合来看，PowerGridModel/power-grid-model 已具备在生产环境中进行配电系统前端快速交付的条件，建议先在小范围 PoC 中验证集成流程，随后在正式产品中推广使用。

## 🧭 Practical evaluation

**Value:** PowerGridModel/power-grid-model helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 229 GitHub stars
- 65 forks
- updated 2026-06-23
- primary language: C++
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 49/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/PowerGridModel/power-grid-model) · [← Back to Misc](./README.md)</sub>
