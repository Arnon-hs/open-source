# infobyte/faraday-cli

[![Stars](https://img.shields.io/github/stars/infobyte/faraday-cli?style=flat-square&color=yellow)](https://github.com/infobyte/faraday-cli/stargazers) [![Forks](https://img.shields.io/github/forks/infobyte/faraday-cli?style=flat-square&color=blue)](https://github.com/infobyte/faraday-cli/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Faraday's Command Line Interface

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 52 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`command-line` `devops` `devsecops` `faraday` `pentest` `security-automation` `security-pipeline` `vulnerability-management` `vulnerability-scanning`

## 🎯 Categories

Automation · DevTools · DevOps/Infra · Security

## 📝 Summary

### English

**Brief Summary**  
Faraday‑CLI is a Python‑based command‑line interface that automates the repetitive tasks surrounding Faraday’s security platform, enabling users to script, schedule, and chain operations that would otherwise require manual interaction. With active maintenance, a modest but growing community (52 ★, 22 forks) and clear API/CLI exposure, it is positioned as a production‑ready OSS component for security‑focused automation pipelines.  

**Value**  
- **Time‑saving automation** – eliminates manual steps in vulnerability triage, scan triggering, and report generation, turning ad‑hoc actions into repeatable scripts.  
- **Workflow orchestration** – the CLI can be chained with other tools (CI/CD, ticketing, SIEM) to build end‑to‑end security flows that run on a schedule or in response to events.  
- **Low entry barrier** – being a pure Python package with a familiar CLI syntax, teams can adopt it without heavy language or infrastructure changes.  

**Practical Adoption Path**  
1. **Pilot the CLI** on a non‑critical environment: install via `pip`, configure the Faraday API token, and run a few basic commands (e.g., list workspaces, trigger a scan).  
2. **Script common tasks** (e.g., nightly scan launches, bulk issue imports) and store them in version‑controlled repositories.  
3. **Integrate** with orchestration tools (Cron, Airflow, GitHub Actions) to schedule or trigger the scripts automatically.  
4. **Extend** by wrapping the CLI in custom Python modules or invoking it from other automation frameworks as needed.  

**Production Readiness**  
- **Active development** – last commit on 2026‑05‑14, regular issue activity, and a responsive maintainer base.  
- **Ecosystem fit** – exposes a stable API/CLI surface, documented usage examples, and is packaged for easy pip installation.  
- **Community signals** – while modest, the star/fork count and nine topical tags indicate a focused user base and growing adoption.  
- **Risks** – final due‑diligence on licensing, security audit of the code, and confirmation of long‑term maintainership are recommended, but no major red flags are evident.  

Overall, Faraday‑CLI offers a practical, low‑friction way to embed Faraday operations into automated security pipelines and is mature enough for a serious production pilot.

### Русский

**infobyte/faraday-cli** — это командный интерфейс для платформы Faraday, позволяющий автоматизировать повторяющиеся операции, интегрировать сторонние инструменты в единые рабочие потоки и планировать периодические задачи. Проект активно поддерживается (обновления — 2026‑05‑14, 52 ★, 22 fork, Python), имеет хорошие сигналы зрелости и готов к использованию в продакшене после окончательной проверки лицензии и безопасности. Типичный сценарий — замена ручных действий (например, импорт уязвимостей, запуск сканеров) на скрипты, вызываемые из CI/CD или планировщика задач.

### 中文

**项目简介**  
infobyte/faraday‑cli 是 Faraday 平台的官方命令行工具，提供一套 Python 实现的 API/SDK/CLI 接口，帮助安全团队把手动的漏洞收集、任务调度、工具链集成等操作自动化，形成可重复、可编排的工作流。

**价值**  
- **削减重复劳动**：通过脚本化调用 Faraday API，省去在 Web UI 上手动创建、更新、关联资产的步骤。  
- **实现工具链编排**：可轻松把扫描器、CI/CD、报告生成等工具通过 CLI 串联，构建端到端的安全自动化流水线。  
- **支持定时任务**：配合 cron 或 CI 平台，定期触发资产同步、漏洞导入等运营任务。

**典型接入方式**  
1. **直接使用 CLI**：在本地或 CI 环境安装 `faraday-cli`（`pip install faraday-cli`），通过 `faraday login` 配置凭证后，调用如 `faraday workspace create`、`faraday vulnerability import` 等子命令。  
2. **在脚本/CI 中调用 API**：CLI 底层使用 Faraday REST API，亦可直接使用其 Python SDK（`faraday-client`），在自定义脚本或自动化平台中嵌入调用。  
3. **与其他工具集成**：结合 Docker、Kubernetes 或 Ansible，将 CLI 作为容器入口或任务步骤，实现跨系统的漏洞信息同步。

**生产可用性**  
- **活跃度**：最近一次提交（2026‑05‑14）且仍在维护，GitHub 统计 52 ⭐、22 🍴，社区活跃。  
- **技术成熟度**：使用主流 Python 语言，提供完整的 OpenAPI 文档和示例，易于审计和二次开发。  
- **风险评估**：暂无重大许可证或安全漏洞报告，但仍建议在正式投产前完成许可证合规和安全审计。  
综合以上因素，faraday‑cli 已具备 **高** 的生产可用性，适合作为安全自动化项目的首选 OSS 组件进行试点并逐步推广。

## 🧭 Practical evaluation

**Value:** infobyte/faraday-cli helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 52 GitHub stars
- 22 forks
- updated 2026-05-14
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 37/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/infobyte/faraday-cli) · [← Back to Automation](./README.md)</sub>
