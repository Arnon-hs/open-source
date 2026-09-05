# rodrigo-arenas/Sklearn-genetic-opt

[![Stars](https://img.shields.io/github/stars/rodrigo-arenas/Sklearn-genetic-opt?style=flat-square&color=yellow)](https://github.com/rodrigo-arenas/Sklearn-genetic-opt/stargazers) [![Forks](https://img.shields.io/github/forks/rodrigo-arenas/Sklearn-genetic-opt?style=flat-square&color=blue)](https://github.com/rodrigo-arenas/Sklearn-genetic-opt/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> ML hyperparameters tuning and features selection, using evolutionary algorithms.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 362 |
| 🍴 **Forks** | 92 |
| 💻 **Language** | Python |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`artificial-intelligence` `automl` `begginer-friendly` `contributions-welcome` `deap` `evolutionary-algorithms` `feature-selection` `featureselection` `good-first-issue` `goodfirstissue` `help-wanted` `hyperparameter-optimization`

## 🎯 Categories

AI/ML · Education

## 📝 Summary

### English

rodrigo-arenas/Sklearn-genetic-opt automates hyper‑parameter tuning and feature selection for scikit‑learn models using evolutionary algorithms, eliminating repetitive manual experimentation. Adoption is straightforward: start with a small proof‑of‑concept by reviewing the README and integrating the library into a notebook or pipeline before scaling to production workflows. The project shows strong recent activity, solid community adoption (362★, 92 forks), and high production readiness, making it suitable for a serious pilot after a quick license and security check.

### Русский

**Sklearn‑genetic‑opt** — это open‑source библиотека на Python, позволяющая автоматизировать подбор гиперпараметров и отбор признаков в моделях scikit‑learn с помощью эволюционных алгоритмов, избавляя от повторяющихся ручных настроек. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept на одном из существующих пайплайнов, проверка README и интеграция в CI/CD для регулярного переобучения моделей. По оценке готовности проекта к продакшн: высокий уровень (активные коммиты, 362 звёзд, 92 форка, обновления до 2026‑06‑26), что делает его подходящим для серьёзных пилотных запусков после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
`rodrigo-arenas/Sklearn-genetic-opt` 是一个基于进化算法的 Python 库，可对 Scikit‑learn 模型的超参数和特征子集进行自动化搜索与优化，帮助机器学习工程师摆脱繁琐的手工调参过程。

**价值**  
- **自动化**：通过遗传算法在大规模搜索空间中高效找到近最优解，显著减少人工调参和特征筛选的时间成本。  
- **可重复**：所有搜索过程以代码形式保存，便于在不同数据集、不同环境中复现并对比实验结果。  
- **灵活集成**：兼容 Scikit‑learn 的标准 API，可直接嵌入现有的模型训练流水线或 AutoML 框架。

**典型接入方式**  
1. **安装**：`pip install sklearn-genetic-opt`（或从源码 `pip install .`）。  
2. **在代码中使用**：  
   ```python
   from sklearn_genetic import GASearchCV
   from sklearn.ensemble import RandomForestClassifier

   ga_search = GASearchCV(
       estimator=RandomForestClassifier(),
       cv=5,
       scoring='accuracy',
       population_size=50,
       generations=20,
       n_jobs=-1,
       verbose=True
   )
   ga_search.fit(X_train, y_train)
   best_model = ga_search.best_estimator_
   ```  
   只需替换传统的 GridSearchCV/RandomizedSearchCV，即可获得进化搜索的优势。  
3. **流水线集成**：可与 `sklearn.pipeline.Pipeline`、`mlflow`、`kubeflow` 等工具组合，形成端到端的可调度、可监控的机器学习工作流。  

**生产可用性**  
- **成熟度**：项目近期活跃（2026‑06‑26 更新），拥有 362 星、92 Fork，覆盖 20+ 主题，社区活跃度良好。  
- **准备度**：代码基于纯 Python，依赖明确，易于在容器或虚拟环境中部署；已有多个开源项目引用，具备在生产环境中进行试点的基础。  
- **风险**：目前未发现重大元数据或安全隐患，但仍建议在正式上线前完成许可证合规、依赖安全审计以及维护者沟通确认。  

综上，`Sklearn-genetic-opt` 可作为 **自动化超参数调优与特征选择** 的可靠组件，适合在实验阶段快速验证后，直接迁移至生产流水线进行大规模、可重复的模型优化。

## 🧭 Practical evaluation

**Value:** rodrigo-arenas/Sklearn-genetic-opt helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 362 GitHub stars
- 92 forks
- updated 2026-06-26
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/rodrigo-arenas/Sklearn-genetic-opt) · [← Back to AI/ML](./README.md)</sub>
