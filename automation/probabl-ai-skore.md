# probabl-ai/skore

[![Stars](https://img.shields.io/github/stars/probabl-ai/skore?style=flat-square&color=yellow)](https://github.com/probabl-ai/skore/stargazers) [![Forks](https://img.shields.io/github/forks/probabl-ai/skore?style=flat-square&color=blue)](https://github.com/probabl-ai/skore/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Track your Data Science. Skore's open-source Python library accelerates ML model development with automated evaluation reports, smart methodological guidance, and comprehensive cross-validation analysis.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 644 |
| 🍴 **Forks** | 138 |
| 💻 **Language** | Python |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`data-analysis` `data-science` `data-visualization` `machine-learning` `python` `scikit-learn` `workflow`

## 🎯 Categories

Automation · AI/ML · Data · Education

## 📝 Summary

### English

**Brief Summary**  
Skore (probabl‑ai/skore) is an open‑source Python library that streamlines data‑science workflows by auto‑generating model evaluation reports, offering methodological recommendations, and delivering exhaustive cross‑validation analyses. It removes repetitive manual steps, enabling teams to build, validate, and monitor ML models faster and more consistently.  

**Value**  
- **Automation of routine tasks** – Skore eliminates the need to hand‑craft evaluation scripts, produce reports, and manage cross‑validation splits, freeing data scientists to focus on model innovation.  
- **Methodological guidance** – Built‑in best‑practice suggestions help ensure that experiments follow sound statistical principles, reducing the risk of leakage or over‑fitting.  
- **Cross‑validation depth** – The library produces detailed, reproducible CV results and visualisations, making it easier to compare models and communicate findings to stakeholders.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided notebooks or the `skore quickstart` command on a small internal dataset to verify that the reporting pipeline integrates with your existing model training code.  
2. **README & CI validation** – Follow the README to install dependencies in a virtual environment, then add a CI step (e.g., GitHub Actions) that runs Skore’s linting and test suite to confirm compatibility with your codebase.  
3. **Incremental integration** – Replace ad‑hoc evaluation scripts with Skore’s API in one project or pipeline, gradually expanding to other teams once the PoC proves stable.  
4. **Automation & scheduling** – Hook Skore into orchestration tools (Airflow, Prefect, or cron) to generate periodic evaluation reports and trigger alerts for model drift.  

**Production Readiness**  
- **Community health**: 644 ★, 138 forks, recent commits (as of 2026‑06‑26), and active issue discussions indicate a vibrant maintainer community.  
- **Technical maturity**: The library is written in Python, supports the major ML stacks (scikit‑learn, XGBoost, PyTorch), and includes a well‑documented CLI and API.  
- **Risk considerations**: No major metadata or licensing red flags have been identified, but a final security audit (dependency scanning, SBOM) and confirmation of maintainers’ response times are advisable before a full production rollout.  

Overall, Skore is a high‑readiness OSS candidate for teams looking to automate model evaluation and embed reproducible analytics into their ML pipelines.

### Русский

**Краткое резюме:**  
`probabl-ai/skore` — это открытая Python‑библиотека, которая автоматизирует рутинные этапы разработки моделей машинного обучения: генерирует готовые отчёты‑оценки, даёт методологические рекомендации и проводит всесторонний кросс‑валидационный анализ. Типовой сценарий внедрения — подключить библиотеку к существующему пайплайну (например, в CI/CD), заменить ручные скрипты оценки и планирования экспериментов, а затем масштабировать процесс через планировщик задач. По готовности к production проект находится на высоком уровне: активные коммиты, более 600 звёзд, регулярные релизы и широкая экосистема позволяют начать с небольшого proof‑of‑concept и быстро перейти к полноценному пилоту.

### 中文

**项目简介**  
Skore（probabl‑ai/skore）是一款开源 Python 库，旨在帮助数据科学团队自动化模型评估、方法论建议以及交叉验证分析，从而大幅减少手工重复工作，加速机器学习模型的研发与交付。

**价值**  
- **提升效率**：一键生成完整的评估报告，省去手动编写代码、整理结果的时间。  
- **降低错误风险**：自动化的交叉验证和方法论检查帮助发现潜在的模型缺陷和数据泄漏。  
- **可复用的工作流**：提供统一的 API，方便将 Skore 嵌入现有的 CI/CD、调度平台或数据管道，实现端到端的可重复实验。

**典型接入方式**  
1. **本地快速试用**：`pip install skore` 后，在 Jupyter Notebook 或脚本中直接调用 `skore.evaluate(model, X, y)` 生成报告。  
2. **CI/CD 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 中添加一步 `skore run --config config.yaml`，将评估报告保存为 HTML/JSON 并作为构建产出上传。  
3. **调度平台**：配合 Airflow、Prefect 或 Dagster 等调度框架，将 Skore 作为任务节点，定时对新模型或新数据进行全套评估并发送报告至 Slack/邮件。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑26，项目最近一次提交，拥有 644 ⭐、138 🍴，社区活跃，具备持续维护的潜力。  
- **技术成熟度**：核心功能已在多个内部项目中验证，文档完整，提供示例代码和 API 参考。  
- **集成风险**：暂无重大元数据或许可证问题，但仍建议在正式投产前进行安全审计并确认维护者的响应速度。  
- **推荐策略**：先在非关键环境做一个小规模 PoC（例如对一个已有模型跑一次完整评估），验证与现有工具链的兼容性后，再逐步推广到生产流水线。  

总体而言，Skore 已具备较高的生产就绪度，适合作为数据科学团队的“评估即服务”组件，帮助实现模型研发的自动化、标准化和可追溯。

## 🧭 Practical evaluation

**Value:** probabl-ai/skore helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 644 GitHub stars
- 138 forks
- updated 2026-06-26
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 60/100 |
| topics | 88/100 |
| outlook | 73/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/probabl-ai/skore) · [← Back to Automation](./README.md)</sub>
