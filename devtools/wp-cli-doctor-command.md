# wp-cli/doctor-command

[![Stars](https://img.shields.io/github/stars/wp-cli/doctor-command?style=flat-square&color=yellow)](https://github.com/wp-cli/doctor-command/stargazers) [![Forks](https://img.shields.io/github/forks/wp-cli/doctor-command?style=flat-square&color=blue)](https://github.com/wp-cli/doctor-command/network) [![Language](https://img.shields.io/badge/lang-Gherkin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Diagnose problems within WordPress by running a series of checks for symptoms

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 165 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | Gherkin |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`check` `cli` `hacktoberfest` `health` `wordpress` `wp-cli` `wp-cli-package`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **wp‑cli/doctor‑command** package adds a “doctor” sub‑command to WP‑CLI that runs a suite of automated checks to surface common WordPress configuration, environment, and plugin issues. By turning ad‑hoc diagnostics into repeatable, scriptable steps, it enables developers to embed health‑checks directly into deployment pipelines or multi‑agent workflows.  

**Value**  
- **Standardised diagnostics** – Encapsulates dozens of best‑practice checks in a single CLI entry point, removing the need for custom scripts or manual troubleshooting.  
- **Agent‑friendly** – The command’s deterministic output and clear exit codes make it easy for autonomous agents or orchestration tools to consume results, trigger remedial actions, or feed a knowledge base.  
- **Reusable workflow building block** – Acts as a plug‑in for larger tool‑chains (e.g., CI/CD, multi‑agent orchestration, or “tool‑use pipelines”), turning isolated prompts into repeatable, auditable processes.  

**Practical Adoption Path**  
1. **Prototype** – Install the package locally (`wp package install wp-cli/doctor-command`) and run `wp doctor` on a staging site to evaluate the relevance of its checks.  
2. **Integrate** – Wrap the command in a shell script or WP‑CLI alias that outputs JSON or machine‑readable status codes; feed this into existing CI pipelines (GitHub Actions, GitLab CI) or orchestration frameworks (Airflow, Temporal).  
3. **Extend** – If additional checks are needed, contribute custom Gherkin scenarios or fork the repo; the codebase is primarily Gherkin‑driven, making it straightforward to add new symptom tests.  
4. **Govern** – Add the command to your organization’s “pre‑deployment health check” stage, and configure alerts for non‑zero exit codes.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑05‑14), has 165 ⭐ and 24 🍴, and provides clear API/CLI signals, but it still depends on the broader WP‑CLI ecosystem and may require periodic updates to stay compatible with newer WordPress versions.  
- **Risk considerations**: No immediate licensing or security red flags, but a final review of the MIT‑style license, vulnerability scan of bundled dependencies, and confirmation of an active maintainer are advisable before wide‑scale rollout.  
- **Suitability**: Ideal for prototypes, internal QA, or as a safety net in CI/CD; with a brief dependency audit and monitoring of upstream changes, it can be hardened for production environments.

### Русский

**wp-cli/doctor-command** — это набор проверок для диагностики проблем WordPress, который позволяет превратить разрозненные запросы и инструменты в повторяемые рабочие процессы агентов (например, координацию многопользовательских сценариев, построение пайплайнов с использованием внешних утилит и стандартизацию памяти агентов). Типичный сценарий — интеграция в CI/CD или внутренняя автоматизация, где команда WP‑CLI запускает команду `wp doctor` как часть пайплайна, получая структурированные сигналы о состоянии сайта и возможность автоматически исправлять типичные симптомы. Проект имеет средний уровень готовности к production: достаточно зрелый (165 ★, 24 fork, активные коммиты) для прототипов и внутренних процессов, но требует окончательной проверки лицензии, безопасности и наличия постоянных мейнтейнеров перед масштабным внедрением.

### 中文

**项目简介**  
`wp-cli/doctor-command` 是一个 WordPress 诊断工具，基于 WP‑CLI 扩展实现。它通过一系列检查（symptom checks）自动发现并报告站点潜在问题，帮助开发者快速定位故障根源。

**价值**  
- **把零散的诊断脚本统一为可重复的工作流**，便于在多代理（multi‑agent）或自动化流水线中调用。  
- **标准化诊断输出**，为后续的记忆（agent memory）或报告生成提供结构化数据。  
- **降低运维成本**：一次部署即可在本地、CI 或生产环境中复用，避免手动排查的重复劳动。

**典型接入方式**  
1. **CLI 直接调用**：在已有的 WP‑CLI 环境中执行 `wp doctor run` 即可触发全部检查。  
2. **SDK/脚本封装**：项目提供了 PHP 类库（`DoctorCommand`）和 Gherkin 定义，可在自定义脚本或 CI 步骤中以函数调用的形式集成。  
3. **多代理工作流**：将 `wp doctor` 作为子任务嵌入 Airflow、GitHub Actions、或 LangChain 等编排平台，实现“诊断 → 修复 → 验证”的闭环。

**生产可用性**  
- **成熟度**：GitHub 165 ★、24 Fork，最近一次提交于 2026‑05‑14，活跃度尚可。  
- **依赖**：仅依赖 WP‑CLI 与标准 PHP 扩展，部署门槛低。  
- **风险**：需进一步确认许可证兼容性、代码安全审计以及维护者响应速度。  
- **建议**：适合作为原型或内部工具投入使用；在面向客户的生产环境前，建议完成安全审计并制定升级/回滚策略。

## 🧭 Practical evaluation

**Value:** wp-cli/doctor-command helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 165 GitHub stars
- 24 forks
- updated 2026-05-14
- primary language: Gherkin
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 47/100 |
| topics | 88/100 |
| outlook | 69/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 44/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/wp-cli/doctor-command) · [← Back to DevTools](./README.md)</sub>
