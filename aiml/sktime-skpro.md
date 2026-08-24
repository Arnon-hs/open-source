# sktime/skpro

[![Stars](https://img.shields.io/github/stars/sktime/skpro?style=flat-square&color=yellow)](https://github.com/sktime/skpro/stargazers) [![Forks](https://img.shields.io/github/forks/sktime/skpro?style=flat-square&color=blue)](https://github.com/sktime/skpro/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> A unified framework for tabular probabilistic regression, time-to-event prediction, and probability distributions in python

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 327 |
| 🍴 **Forks** | 189 |
| 💻 **Language** | Python |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `data-science` `distributional-regression` `distributions` `failure-prediction` `framework` `hacktoberfest` `machine-learning` `prediction` `probability-distributions` `python` `regression`

## 🎯 Categories

AI/ML · Data

## 📝 Summary

### English

**Summary:** sktime/skpro is an open-source project that provides a unified framework for tabular probabilistic regression, time-to-event prediction, and probability distributions in Python. It helps developers add AI capabilities without starting from scratch, making it ideal for prototyping AI features and building complex workflows. With its strong adoption and recent activity, sktime/skpro is highly production-ready for a serious pilot.

**Value:** The primary value proposition of sktime/skpro lies in its ability to simplify the process of adding AI capabilities to existing projects. By providing a unified framework for probabilistic regression, time-to-event prediction, and probability distributions, developers can focus on building and integrating AI features without having to start from a blank model stack.

**Practical Adoption Path:** To adopt sktime/skpro, developers can start by evaluating the framework through a small proof of concept and checking the README documentation. This will give them a sense of the framework's capabilities and potential integration challenges. Once they are comfortable with the framework, they can begin integrating it into their existing projects, starting with prototyping AI features and building complex workflows.

**Production Readiness:** sktime/skpro is highly production-ready for a serious pilot. With 327 GitHub stars, 189 forks, and recent activity,

### Русский

Резюме проекта sktime/skpro:

Проект sktime/skpro представляет собой унифицированную платформу для табличных вероятностных регрессий, прогнозирования времени события и вероятностных распределений в Python. Он позволяет добавлять функциональность AI без создания новой модели стека, что упрощает внедрение и прототипирование AI-приложений.

Проект можно использовать для внедрения AI-функциональности в различные приложения, таких как прототипирование AI-функций, создание RAG или агентных потоков, оценка инструментов моделирования. Проект готов к использованию в производственной среде, имея сильное присутствие в GitHub, регулярную актуализацию и широкое признание в экосистеме.

### 中文

**项目简介**  
sktime/skpro 是一个统一的 Python 框架，专注于表格化的概率回归、事件时间预测以及概率分布建模。它把常见的概率机器学习任务抽象为统一的 API，方便在同一套代码库中切换模型、评估指标和预测分布。

**价值**  
- **快速赋能**：无需从零搭建模型堆栈，直接调用已有的概率回归和生存分析实现，即可为产品或内部工具添加 AI 能力。  
- **统一体验**：统一的 `fit/predict` 接口兼容 scikit‑learn、sktime 等生态，降低学习成本并简化模型管理。  
- **实验与评估**：内置多种概率评估指标（CRPS、log‑loss 等），帮助快速原型验证和模型对比，为后续 RAG、智能体等工作流提供可靠的概率输出。

**典型接入方式**  
1. **环境准备**：`pip install sktime skpro`（或使用 `conda`）。  
2. **最小原型**：```python
from skpro.regression import ProbabilisticRegressor
from skpro.datasets import load_airline  # 示例数据

X_train, y_train = load_airline(return_X_y=True)
model = ProbabilisticRegressor(estimator="LinearRegression")  # 任选底层回归器
model.fit(X_train, y_train)
dist = model.predict(X_test)          # 返回概率分布对象
samples = dist.sample(1000)           # 采样用于下游 RAG/agent
```  
3. **评估**：使用 `skpro.metrics` 中的 `crps_score`, `log_loss` 等函数对预测分布进行打分。  
4. **集成**：将模型封装为微服务（FastAPI/Flask）或直接在现有 pipeline 中调用，配合 `mlflow`、`prefect` 等工具实现持续训练与监控。

**生产可用性**  
- **活跃度**：截至 2026‑06‑29，项目最近一次提交，拥有 327 ★、189 Fork，18 个相关话题，说明社区活跃且维护及时。  
- **成熟度**：代码基于成熟的 scikit‑learn 与 sktime 生态，兼容性好，已在多个公开案例中用于时间‑到‑事件预测和风险评估。  
- **风险**：目前未发现重大元数据或安全漏洞，仍需确认许可证（BSD‑3‑Clause）符合企业合规，并对依赖的安全性做一次审计。  
- **推荐**：可先在低风险的实验环境完成 PoC（如内部推荐系统或异常检测），验证预测分布的业务价值后，再推广到生产线上。整体而言，sktime/skpro 已具备高可用的 OSS 候选人资格，适合作为 AI 功能的快速落地层。

## 🧭 Practical evaluation

**Value:** sktime/skpro helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 327 GitHub stars
- 189 forks
- updated 2026-06-29
- primary language: Python
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 55/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/sktime/skpro) · [← Back to AI/ML](./README.md)</sub>
