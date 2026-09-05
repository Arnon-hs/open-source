# TIGER-AI-Lab/ClawBench

[![Stars](https://img.shields.io/github/stars/TIGER-AI-Lab/ClawBench?style=flat-square&color=yellow)](https://github.com/TIGER-AI-Lab/ClawBench/stargazers) [![Forks](https://img.shields.io/github/forks/TIGER-AI-Lab/ClawBench?style=flat-square&color=blue)](https://github.com/TIGER-AI-Lab/ClawBench/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Open-source benchmark for browser AI agents on daily tasks.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 415 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-evaluation` `agentic-ai` `ai-agent-benchmark` `ai-agents` `benchmark` `browser-agent` `browser-automation` `browser-use` `chrome-agent` `chrome-extension` `computer-use` `dataset`

## 🎯 Categories

Automation · AI/ML

## 📝 Summary

### English

**Summary**  
ClawBench (TIGER‑AI‑Lab) is an open‑source benchmark that evaluates browser‑based AI agents on everyday tasks, helping teams automate repetitive, manual steps in their workflows. With strong community signals (415 ★, recent commits, Python core) it is ready for pilot projects, though a brief proof‑of‑concept and license/security review are advisable before full integration.

**Value**  
ClawBench provides a standardized way to measure how well AI agents can navigate web interfaces, fill forms, click buttons, and orchestrate multi‑tool flows. By quantifying performance on realistic daily tasks, it lets organizations identify the most capable agents, reduce manual labor, and build repeatable, tool‑agnostic automation pipelines.

**Practical adoption path**  
1. **Proof of concept** – Clone the repo, run the supplied README examples, and benchmark a candidate agent on a small set of tasks relevant to your workflow.  
2. **Integration** – Wrap the chosen agent with ClawBench’s driver scripts, connect it to your internal tooling (e.g., CI/CD, ticketing, or data‑ingestion systems), and iterate on task definitions.  
3. **Scale** – Expand the benchmark suite to cover the full spectrum of daily operations, embed the agent in scheduled jobs or orchestration platforms, and monitor success metrics.

**Production readiness**  
The project shows high production readiness for an OSS solution: recent activity (last update 2026‑06‑22), solid adoption (415 stars, 24 forks), a well‑documented Python codebase, and a broad topic coverage. While no major metadata risks are evident, a final check of the license, security posture, and maintainer responsiveness is recommended before committing to a production‑grade deployment.

### Русский

**Краткое резюме:**  
TIGER‑AI‑Lab/ClawBench — это открытый бенчмарк для оценки браузерных AI‑агентов, позволяющий автоматизировать рутинные задачи и собрать инструменты в повторяемые рабочие потоки. Типовой сценарий внедрения — начать с небольшого proof‑of‑concept, проверив README и запустив несколько тестовых задач, после чего масштабировать автоматизацию и планировать операции. Проект обладает высокой готовностью к production: активные коммиты, 415 звёзд, 24 форка и сильные сигналы экосистемы, хотя окончательная проверка лицензии, безопасности и поддержки поддерживающих разработчиков всё‑ещё требуется.

### 中文

**项目简介**  
TIGER‑AI‑Lab/ClawBench 是一个开源基准套件，用于评估浏览器 AI 代理在日常工作任务中的表现，帮助开发者快速验证和对比不同方案的自动化能力。

**价值**  
- **消除重复手工操作**：通过统一的基准，快速定位哪些任务可以交给 AI 代理完成，从而把人力从繁琐的点击、数据录入等环节中解放出来。  
- **构建可复用的工作流**：基准中提供的任务模板和评估脚本，可直接嵌入 CI/CD 或调度系统，实现工具之间的自动化衔接。  
- **降低试验成本**：只需运行几行 Python 脚本，即可得到量化的性能分数，帮助团队在选型和迭代时作出数据驱动的决策。

**典型接入方式**  
1. **阅读 README 与示例**：先确认环境依赖（Python 3.9+、Playwright/Chrome 等），按照文档完成本地运行。  
2. **小范围 PoC**：在单机或容器中选取 1‑2 条代表性任务（如表单填写、网页抓取），使用 `clawbench run` 命令执行基准，观察指标（成功率、时延、资源占用）。  
3. **集成到现有流水线**：把基准脚本包装为 Docker 镜像或 GitHub Action，加入 CI 流程，实现每次模型或代码更新后的自动回归测试。  
4. **扩展任务库**：依据业务需求编写自定义任务 JSON，复用已有评估框架即可快速上线新场景。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑22，拥有 415 Stars、24 Forks，社区讨论活跃，说明项目维护良好。  
- **技术成熟度**：基于 Python 与 Playwright，易于与现有后端服务、调度平台（Airflow、K8s CronJob）对接。  
- **风险**：目前未发现重大元数据或许可证冲突，但仍建议在正式投产前完成安全审计并确认维护者的响应时效。  
- **结论**：在完成上述小规模验证后，ClawBench 完全可以作为生产环境的自动化评估与监控组件，支持持续改进浏览器 AI 代理的业务流程。

## 🧭 Practical evaluation

**Value:** TIGER-AI-Lab/ClawBench helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 415 GitHub stars
- 24 forks
- updated 2026-06-22
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/TIGER-AI-Lab/ClawBench) · [← Back to Automation](./README.md)</sub>
