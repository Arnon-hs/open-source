# frappe/bench

[![Stars](https://img.shields.io/github/stars/frappe/bench?style=flat-square&color=yellow)](https://github.com/frappe/bench/stargazers) [![Forks](https://img.shields.io/github/forks/frappe/bench?style=flat-square&color=blue)](https://github.com/frappe/bench/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> CLI to manage Multi-tenant deployments for Frappe apps

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 1.3k |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `frappe-bench` `frappe-framework` `python` `setup-bench`

## 🎯 Categories

DevTools

## 📝 Summary

### English

Here's a brief summary of the project:

**Summary:** frappe/bench is an open-source command-line interface (CLI) designed to simplify management of multi-tenant deployments for Frappe applications, saving developers time in daily development and review loops. This tool accelerates workflows, automates local engineering tasks, and enhances Continuous Integration (CI) feedback. With its strong adoption and recent activity, frappe/bench is a promising candidate for production use.

**Value:** The primary value proposition of frappe/bench lies in its ability to streamline developer workflows, automate repetitive tasks, and improve the speed of feedback loops. By leveraging this tool, engineers can focus on higher-level tasks while reducing the time spent on mundane activities.

**Practical Adoption Path:** To adopt frappe/bench, follow these steps:

1. **Evaluate the tool**: Assess the tool's features, documentation, and community support to ensure it aligns with your organization's needs.
2. **Install and configure**: Set up the CLI on your local machine and configure it to work with your Frappe applications.
3. **Integrate with CI/CD**: Integrate frappe/bench with your Continuous Integration and Continuous Deployment (CI/CD) pipeline to automate tasks and improve feedback loops.
4. **Monitor and refine

### Русский

**frappe/bench** — это CLI‑утилита на Python для управления многопользовательскими (multi‑tenant) развертываниями приложений Frappe. Она ускоряет ежедневные циклы разработки и ревью, автоматизируя локальные задачи (создание/обновление сайтов, миграции, запуск тестов) и улучшая обратную связь в CI‑pipeline. Проект имеет высокую готовность к production: активные коммиты, более 1700 звёзд, широкое принятие в сообществе и надёжную экосистему, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句话）**  
`frappe/bench` 是一款基于 Python 的命令行工具，专为 Frappe 应用的多租户部署而设计。它提供统一的工作流管理、环境初始化、服务编排和自动化脚本，帮助开发者在本地和生产环境中快速搭建、维护和升级 Frappe 实例。

**价值**  
- **提升开发效率**：一键创建/销毁站点、同步数据库、管理后台进程，显著缩短每日开发与代码审查的循环时间。  
- **自动化本地任务**：通过 CLI 脚本可实现依赖安装、迁移、测试和 CI/CD 流水线的全自动化，降低人为错误。  
- **加速 CI 反馈**：在 CI 环境中可快速启动完整的 Frappe 堆栈，提供真实的集成测试环境，从而提升回归检测的可靠性。

**典型接入方式**  
1. **CLI 调用**：在本地或 CI 容器中直接执行 `bench init`, `bench new-site`, `bench start` 等命令。  
2. **Python SDK**：通过 `bench` 包提供的内部 API（如 `bench.utils`）在自定义脚本或插件中调用，实现更细粒度的自动化。  
3. **Docker/Compose 集成**：官方提供的 Docker 镜像和 `docker-compose.yml` 示例，可在容器化环境中即插即用，适配 Kubernetes 或 GitHub Actions 等 CI 平台。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑29，项目拥有 1.7k+ ★、1.3k+ Fork，最近一次提交在数天前，表明维护活跃。  
- **成熟生态**：已被多个大型 Frappe/ERPNext 部署采用，社区提供丰富的插件和文档。  
- **技术成熟**：核心实现基于 Python，代码结构清晰，支持多租户管理、日志聚合和备份恢复等生产必备特性。  
- **风险**：仍需进一步审查许可证（MIT）兼容性、潜在安全漏洞以及核心维护者的长期可用性，但整体风险较低，适合作为正式生产环境的候选方案。

## 🧭 Practical evaluation

**Value:** frappe/bench helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1705 GitHub stars
- 1346 forks
- updated 2026-06-29
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 69/100 |
| topics | 63/100 |
| outlook | 63/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 71/100 |
| production | 59/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/frappe/bench) · [← Back to DevTools](./README.md)</sub>
