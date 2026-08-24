# ansys/pyaedt

[![Stars](https://img.shields.io/github/stars/ansys/pyaedt?style=flat-square&color=yellow)](https://github.com/ansys/pyaedt/stargazers) [![Forks](https://img.shields.io/github/forks/ansys/pyaedt?style=flat-square&color=blue)](https://github.com/ansys/pyaedt/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> AEDT Python Client Package

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 333 |
| 🍴 **Forks** | 243 |
| 💻 **Language** | Python |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ansys` `electronics` `pyaedt` `python`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
The **ansys/pyaedt** package is a Python client for ANSYS Electronic Desktop (AEDT) that lets engineers script, automate, and integrate AEDT functionality directly from Python. With 333 ★ and recent commits (last update 2026‑05‑11), it offers a mature, well‑documented API that can accelerate daily development, testing, and CI pipelines for electromagnetic simulation workflows.

**Value** – By exposing AEDT’s core capabilities through a clean Python SDK/CLI, pyaedt eliminates manual GUI steps, shortens iteration cycles, and enables reproducible, automated engineering tasks, which translates into faster design reviews and higher productivity for simulation teams.

**Adoption path** – Teams can start by installing the package from PyPI, importing the SDK in existing Python test suites or CI jobs, and gradually replacing repetitive GUI actions with scripted calls; the library’s clear API and example notebooks make a quick “proof‑of‑concept” integration feasible within a sprint.

**Production readiness** – The project shows high readiness: active maintainers, frequent releases, strong community signals (stars, forks, topics), and a stable Python codebase. While a final check on licensing and security policies is advisable, the current health metrics indicate that pyaedt is suitable for pilot deployments and can be scaled to production‑grade workflows.

### Русский

**ansys/pyaedt** — это клиентская библиотека Python для взаимодействия с Ansys Electronic Desktop (AEDT), позволяющая инженерам автоматизировать рутинные задачи, ускорять локальные разработки и получать быстрый CI‑feedback. Типичный сценарий внедрения — написание скриптов, которые управляют моделированием, проводят пакетный запуск симуляций и собирают результаты, что существенно сокращает время цикла «разработать‑проверить‑оптимизировать». Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 300 звёзд, широкое принятие в сообществе и стабильный Python‑API, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
ansys/pyaedt 是 Ansys 提供的 AEDT（Ansys Electronic Desktop）Python 客户端库，帮助工程师在 Python 环境中直接调用 AEDT 的 API，实现设计自动化、批量仿真和结果后处理。

**价值**  
- **提升效率**：通过脚本化操作，显著缩短每日的开发、验证和审查循环。  
- **工作流自动化**：可将本地仿真任务、参数扫描和报告生成自动化，轻松嵌入 CI/CD 流程，提升反馈速度。  
- **统一语言**：使用熟悉的 Python 生态（NumPy、pandas、pytest 等），降低学习成本并便于与其他工具链集成。

**典型接入方式**  
1. **安装**：`pip install pyaedt`（或通过 conda）。  
2. **初始化客户端**：在脚本中 `from pyaedt import Hfss`（或其他模块），创建项目对象并连接本地或远程的 AEDT 实例。  
3. **API 调用**：使用提供的类方法完成几何建模、材料设置、仿真求解、结果提取等操作。  
4. **CI 集成**：在 Jenkins、GitHub Actions 等 CI 环境中启动无头 AEDT，运行 pyaedt 脚本并将仿真结果作为构建报告或质量门槛。

**生产可用性**  
- **活跃度**：截至 2026‑05‑11 最近一次提交，拥有 333 Stars、243 Forks，社区活跃。  
- **成熟度**：库已在多个内部项目和公开案例中验证，支持主流 Ansys AEDT 版本，具备完整的文档与示例。  
- **风险**：暂无重大版权或安全隐患，但仍建议在正式投产前审查许可证（MIT/Apache 类）和依赖的 Ansys 许可证合规性。  

综上，pyaedt 已具备高生产就绪度，适合作为工程仿真自动化和 CI/CD 流程的核心组件进行试点乃至全面落地。

## 🧭 Practical evaluation

**Value:** ansys/pyaedt helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 333 GitHub stars
- 243 forks
- updated 2026-05-11
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 54/100 |
| topics | 50/100 |
| outlook | 47/100 |
| quality | 52/100 |
| recency | 20/100 |
| adoption | 55/100 |
| production | 50/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/ansys/pyaedt) · [← Back to Misc](./README.md)</sub>
