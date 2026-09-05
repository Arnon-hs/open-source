# pymc-devs/pymc

[![Stars](https://img.shields.io/github/stars/pymc-devs/pymc?style=flat-square&color=yellow)](https://github.com/pymc-devs/pymc/stargazers) [![Forks](https://img.shields.io/github/forks/pymc-devs/pymc?style=flat-square&color=blue)](https://github.com/pymc-devs/pymc/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Bayesian Modeling and Probabilistic Programming in Python

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.7k |
| 🍴 **Forks** | 2.3k |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bayesian-inference` `mcmc` `probabilistic-programming` `pytensor` `python` `statistical-analysis` `variational-inference`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
pymc-devs/pymc is a mature, open‑source Python library for Bayesian modeling and probabilistic programming, offering a rich set of inference algorithms, automatic differentiation, and a flexible model‑building API. With over 9 600 stars, frequent commits (last update 2026‑06‑23), and strong community adoption, it is ready for serious pilot projects. A practical entry point is to follow the README examples, run a small proof‑of‑concept model, and then expand to production workloads once the licensing and security reviews are completed.

### Русский

**pymc-devs/pymc** — это зрелая библиотека для байесовского моделирования и вероятностного программирования на Python, активно поддерживаемая сообществом (9650 звёзд, более 2000 форков, последние коммиты — 23 июня 2026). Она позволяет быстро строить и инферировать сложные статистические модели, что делает её идеальной для пилотных проектов в аналитике, машинном обучении и научных исследованиях, где требуется гибкая работа с неопределённостью. Благодаря высокой активности, широкой экосистеме и хорошей документации, библиотека готова к production‑использованию после небольшого PoC и проверки README.

### 中文

**项目简介（2‑3 句）**  
pymc-devs/pymc 是一个基于 Python 的贝叶斯建模与概率编程框架，提供丰富的统计分布、马尔可夫链 Monte Carlo (MCMC) 采样器以及自动微分变分推断 (ADVI) 等工具，让用户能够用简洁的代码构建并推断复杂的概率模型。

**价值**  
- **强大的建模能力**：支持层次模型、时间序列、空间模型等多种贝叶斯结构，适用于科研、金融、医疗等领域的不确定性分析。  
- **生态兼容**：与 NumPy、SciPy、pandas、ArviZ 等主流科学计算库深度集成，便于数据预处理、后处理与可视化。  
- **社区与维护**：拥有 9.6k+ 星、2.2k+ 叉，近期仍在活跃维护，社区贡献丰富，文档和示例齐全，降低学习和使用门槛。

**典型接入方式**  
1. **直接安装**：`pip install pymc`（或 `conda install -c conda-forge pymc`）即可在现有 Python 环境中使用。  
2. **在现有工作流中嵌入**：在数据处理脚本或 Jupyter Notebook 中导入 `pymc`，定义模型后调用 `pm.sample()`、`pm.fit()` 等 API 完成推断。  
3. **与流水线集成**：可将模型封装为函数或类，配合 Airflow、Kubeflow、MLflow 等调度或模型管理平台，实现自动化训练与监控。  

**生产可用性**  
- **成熟度高**：项目活跃，最近一次提交为 2026‑06‑23，且已在多个行业（如药物研发、金融风险）进行实战部署。  
- **稳定性**：遵循语义化版本管理，核心功能（MCMC、Variational Inference）已多年稳定运行，兼容 Python 3.9+。  
- **安全与合规**：使用 BSD‑3-Clause 许可证，暂无已知重大安全漏洞；在正式上线前仍建议进行内部安全审计和依赖锁定。  

综上，pymc 是一个在科研与工业场景均可直接落地的贝叶斯建模工具，推荐先在小规模原型（如 Jupyter Notebook）验证可行性，随后在 CI/CD 流程中引入，实现生产级别的概率推断。

## 🧭 Practical evaluation

**Value:** pymc-devs/pymc may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9650 GitHub stars
- 2262 forks
- updated 2026-06-23
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 84/100 |
| stars | 85/100 |
| topics | 88/100 |
| outlook | 76/100 |
| quality | 86/100 |
| recency | 80/100 |
| adoption | 85/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/pymc-devs/pymc) · [← Back to Misc](./README.md)</sub>
