# mahmoud/glom

[![Stars](https://img.shields.io/github/stars/mahmoud/glom?style=flat-square&color=yellow)](https://github.com/mahmoud/glom/stargazers) [![Forks](https://img.shields.io/github/forks/mahmoud/glom?style=flat-square&color=blue)](https://github.com/mahmoud/glom/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> ☄️ Python's nested data operator (and CLI), for all your declarative restructuring needs. Got data? Glom it! ☄️

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.2k |
| 🍴 **Forks** | 74 |
| 💻 **Language** | Python |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apis` `cli` `data` `data-transformation` `declarative` `dictionaries` `nested-structures` `python` `recursion` `utilities`

## 🎯 Categories

DevTools · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Glom is a Python library and CLI that lets you declaratively reshape nested data structures with a concise, expressive syntax. It’s ideal for teams that need to standardize data‑handling logic across APIs, micro‑services, and ETL pipelines, letting them “glom” data instead of hand‑crafting repetitive extraction and transformation code. With strong community adoption (2 k+ stars) and recent activity, it’s a mature open‑source option for backend and data‑centric projects.  

**Value**  
- **Reusable data‑manipulation primitives** – Define a single Glom spec and apply it everywhere, eliminating duplicated parsing and mapping code across services.  
- **Consistent declarative style** – Improves readability and reduces bugs by moving transformation logic out of imperative code into a clear, data‑driven description.  
- **CLI support** – Enables quick ad‑hoc data reshaping in scripts or CI pipelines without writing Python code.  

**Practical Adoption Path**  
1. **Prototype** – Add the library (`pip install glom`) to a sandbox service and replace a few existing dict/list manipulations with Glom specs to gauge readability and performance.  
2. **Create shared specs** – Store common Glom specifications in a version‑controlled module that all services import, establishing a single source of truth for data contracts.  
3. **Integrate into CI** – Use the CLI in test suites to validate incoming payloads against expected shapes, catching schema drift early.  
4. **Roll out incrementally** – Gradually replace legacy extraction code across micro‑services, monitoring latency and error rates to ensure no regressions.  

**Production Readiness**  
- **Activity & Adoption**: 2,153 GitHub stars, 74 forks, recent commits (as of 2026‑06‑29), and multiple topics indicate an active, healthy community.  
- **Stability**: The library follows semantic versioning, has extensive documentation, and is used in several production‑grade projects.  
- **Ecosystem Fit**: Pure‑Python implementation works with any Python 3.8+ runtime, and the CLI can be invoked from containers or serverless functions.  
- **Risk Considerations**: No major licensing or security red flags yet, but a final review of the license (MIT) and any disclosed vulnerabilities is advisable before full‑scale deployment.  

Overall, Glom is production‑ready for teams looking to streamline nested‑data handling and standardize backend transformation patterns.

### Русский

**mahmoud/glob** — это библиотека‑оператор для вложенных структур данных в Python (с CLI), позволяющая декларативно трансформировать и извлекать информацию из JSON‑похожих объектов. Команда может быстро построить API‑сервисы, стандартизировать общие паттерны доступа к данным и переиспользовать уже проверенную инфраструктуру без написания собственного кода. Проект имеет высокий уровень готовности к production: активные коммиты, более 2000 звёзд, широкая экосистема и поддержка CLI/SDK, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

mahmoud/glom 是一个 Python 的嵌套数据操作库（附带 CLI），能够以声明式方式快速重构、提取和转换复杂的 JSON/YAML 数据，帮助团队复用后端基础设施而非重复造轮子。典型的接入方式是通过 pip 安装后在代码中引用 `glom` 函数或使用其提供的命令行工具进行数据处理，亦可作为服务间数据映射的通用 SDK。得益于持续的活跃维护、较高的星标数和最近的更新，glom 在生产环境中具有较高的可用性，适合作为后端服务或数据管道的原型或正式组件进行试点。

## 🧭 Practical evaluation

**Value:** mahmoud/glom helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2153 GitHub stars
- 74 forks
- updated 2026-06-29
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/mahmoud/glom) · [← Back to DevTools](./README.md)</sub>
