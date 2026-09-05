# python-pendulum/pendulum

[![Stars](https://img.shields.io/github/stars/python-pendulum/pendulum?style=flat-square&color=yellow)](https://github.com/python-pendulum/pendulum/stargazers) [![Forks](https://img.shields.io/github/forks/python-pendulum/pendulum?style=flat-square&color=blue)](https://github.com/python-pendulum/pendulum/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Python datetimes made easy

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.7k |
| 🍴 **Forks** | 432 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`date` `datetime` `python` `python3` `time` `timezones`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
Pendulum is an open‑source Python library that simplifies working with dates, times and time zones, offering a more intuitive API than the standard `datetime` module. With over 6 600 ★, active maintenance (last update 2026‑06‑30) and a growing user base, it is a mature candidate for projects that need reliable, human‑readable datetime handling.

**Value**  
Pendulum removes much of the boilerplate and ambiguity of the built‑in `datetime` package, providing clear parsing, formatting, time‑zone conversion, and period arithmetic out of the box. Its API aligns closely with natural language concepts (e.g., `pendulum.now().add(days=5)`), which speeds development and reduces bugs in time‑sensitive logic.

**Practical adoption path**  
1. **Proof‑of‑concept** – Replace a few `datetime` usages in a sandbox module with Pendulum to verify API compatibility and check the README for migration guidelines.  
2. **Incremental migration** – Gradually refactor utility functions and services that handle timestamps, leveraging Pendulum’s `parse`, `in_timezone`, and `diff` helpers.  
3. **Full integration** – Once the POC passes tests and performance checks, adopt Pendulum across the codebase, adding it to the dependency lockfile and updating CI pipelines.

**Production readiness**  
Pendulum scores high on production readiness: recent commits, a sizable community, and widespread adoption signal stability. While the license and security posture should be confirmed in a final audit, the library’s activity, fork count, and ecosystem integration (e.g., compatibility with Django, Flask, and data‑processing pipelines) make it suitable for a serious pilot or even full production deployment.

### Русский

Резюме проекта python-pendulum/pendulum:

Проект python-pendulum/pendulum предназначен для упрощения работы с датами и временем в Python. Он может быть полезен для конкретных рабочих процессов, если README и активность проекта соответствуют этим процессам. Проект готов к serious пилоту в production, поскольку он имеет недавнюю активность, широкое распространение и сильные сигналы из экосистемы.

### 中文

**项目简介**  
`python-pendulum/pendulum` 是一个对 Python 标准库 `datetime` 的增强封装，提供更直观、时区安全且人性化的日期时间操作接口，让日期时间的解析、算术、格式化等工作变得轻松可靠。

**价值**  
- **易用性**：链式调用和丰富的自然语言解析，使代码更简洁、可读性更高。  
- **时区安全**：内置完善的时区管理，避免了常见的 “naive vs aware” 混淆。  
- **功能完整**：支持时区转换、相对时间（如 “3 days ago”）、人类可读的差值输出等，覆盖大多数业务场景。  

**典型接入方式**  
1. **依赖安装**：`pip install pendulum`（或在 `requirements.txt` 中声明）。  
2. **代码迁移**：将项目中使用 `datetime` 的地方替换为 `pendulum`，例如：  
   ```python
   import pendulum

   # 解析 ISO8601 字符串
   dt = pendulum.parse("2024-05-01T12:30:00Z")
   # 时区转换
   dt_in_shanghai = dt.in_timezone("Asia/Shanghai")
   # 计算相对时间
   three_days_ago = pendulum.now().subtract(days=3)
   # 人类可读的差值
   print(dt.diff_for_humans())
   ```  
3. **渐进式迁移**：可以先在新模块或新功能中使用 Pendulum，验证无误后再逐步替换旧代码，降低风险。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑30 最近一次提交，星标 6666，Fork 432，社区活跃度高。  
- **成熟度**：已被多个大型项目采用，文档完整，兼容 Python 3.8+，具备稳定的 API。  
- **风险**：暂无重大安全或许可证问题，但在正式上线前建议再做一次许可证合规检查和安全扫描。  

综上，Pendulum 具备高可用性、易集成和强大功能，是在 Python 项目中替代或补充标准 `datetime` 的可靠选择，适合作为生产环境的日期时间处理库进行试点或直接推广。

## 🧭 Practical evaluation

**Value:** python-pendulum/pendulum may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6666 GitHub stars
- 432 forks
- updated 2026-06-30
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 81/100 |
| topics | 75/100 |
| outlook | 73/100 |
| quality | 81/100 |
| recency | 80/100 |
| adoption | 77/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/python-pendulum/pendulum) · [← Back to Misc](./README.md)</sub>
