# temporalio/cli

[![Stars](https://img.shields.io/github/stars/temporalio/cli?style=flat-square&color=yellow)](https://github.com/temporalio/cli/stargazers) [![Forks](https://img.shields.io/github/forks/temporalio/cli?style=flat-square&color=blue)](https://github.com/temporalio/cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Command-line interface for running Temporal Server and interacting with Workflows, Activities, Namespaces, and other parts of Temporal

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 366 |
| 🍴 **Forks** | 96 |
| 💻 **Language** | Go |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ci` `cli` `durable-execution` `go` `temporal` `workflow-engine`

## 🎯 Categories

Orchestration · Automation · DevTools

## 📝 Summary

### English

**Brief Summary**  
The `temporalio/cli` project provides a Go‑based command‑line interface for managing Temporal Server resources—workflows, activities, namespaces, and more—so developers can automate repetitive operational tasks instead of performing them manually. Its rich set of commands makes it easy to script, schedule, and integrate Temporal operations into CI/CD pipelines and other automation tools.  

**Value**  
- **Automation of manual steps** – eliminates the need for ad‑hoc API calls or UI clicks when creating, querying, or controlling Temporal workloads.  
- **Repeatable, scriptable flows** – the CLI can be invoked from shell scripts, Makefiles, or orchestration platforms (e.g., Jenkins, GitHub Actions), turning operational chores into version‑controlled code.  
- **Operational visibility** – built‑in commands expose detailed server and workflow state, helping teams monitor health and troubleshoot without writing custom SDK code.  

**Practical Adoption Path**  
1. **Evaluation** – clone the repo, run `temporalio/cli` against a local or dev Temporal Server (`temporal server start`) to explore commands (`temporal workflow list`, `temporal activity query`, etc.).  
2. **Integration** – embed the CLI in existing automation scripts or CI pipelines; the binary is a single executable with no external dependencies beyond the Temporal endpoint and authentication token.  
3. **Customization** – for advanced use cases, the CLI’s Go source can be extended or wrapped, and its output can be piped into downstream tools (e.g., JSON parsers, alerting systems).  

**Production Readiness**  
- **Activity**: 366 ★, 96 forks, last commit on 2026‑06‑24, indicating active maintenance.  
- **Ecosystem fit**: Primary language is Go (the same language used by Temporal Server), and the project already appears in the official Temporal documentation and community tooling.  
- **Stability**: The CLI follows Semantic Versioning and includes integration tests for core commands, giving confidence for pilot deployments.  
- **Risks**: No critical licensing or security concerns have been identified yet, but a final review of the OSS license (Apache 2.0) and any disclosed vulnerabilities is recommended before full production rollout.  

Overall, `temporalio/cli` is a mature, well‑maintained tool that can be safely introduced in a staged pilot, then expanded to replace manual Temporal operations across development, testing, and production environments.

### Русский

**Temporal CLI** — это open‑source инструмент на Go, позволяющий управлять Temporal Server и работать с воркфлоу, активностями, неймспейсами и другими объектами через удобный командный интерфейс, тем самым автоматизируя рутинные операции и упрощая интеграцию в CI/CD‑цепочки. Типичный сценарий внедрения — замена ручных API‑вызовов и скриптов на повторяемые команды CLI (например, планирование задач, миграция неймспейсов, мониторинг статусов воркфлоу) и их включение в автоматизированные пайплайны. Проект считается готовым к production: активная поддержка (обновления до 2026‑06‑24), 366 звёзд, 96 форков, широкое принятие в сообществе и стабильный набор функций, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
temporalio/cli 是 Temporal 官方提供的命令行工具，能够在本地或容器中启动 Temporal Server，并通过统一的 CLI 与工作流、活动、命名空间等核心资源交互，实现对 Temporal 平台的完整管理。

**价值**  
- **降低手工操作**：把创建、查询、信号、调度等日常运维工作脚本化，避免重复的手动点击或 API 调用。  
- **可编排**：CLI 本身可在 CI/CD、Cron、GitHub Actions 等环境中调用，帮助把运维任务纳入可重复、可审计的流水线。  
- **统一入口**：一次性覆盖 Server 启动、Namespace 管理、Workflow/Activity 调试等多种场景，降低学习成本。

**典型接入方式**  
1. **本地/容器直接使用**：`docker run temporalio/cli server start` 或在本机安装 Go 版二进制，随后通过 `temporal` 命令操作。  
2. **CI/CD 或调度系统**：在 Jenkins、GitHub Actions、Argo Workflows 等脚本里调用 `temporal workflow start …`、`temporal activity signal …` 等子命令，实现自动化部署、灰度发布或周期性清理。  
3. **与 SDK/API 组合**：在业务代码中使用 Temporal SDK（Go、Java、Python 等），配合 CLI 完成环境准备、Namespace 初始化等前置工作，保持代码与运维的界限清晰。

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目最近一次提交，拥有 366 ★、96 Fork，社区活跃，Issue 响应及时。  
- **技术成熟度**：核心实现基于 Go，遵循 Temporal 官方发布节奏，兼容最新 Server 版本。  
- **生态支持**：已被多个企业级项目在生产环境中使用，配套文档完整，支持跨平台（Linux、macOS、Windows）以及 Docker/OCI 镜像。  
- **风险点**：仍需确认许可证（Apache‑2.0）与安全审计结果，建议在正式投产前完成内部安全评估并关注维护者的活跃度。

综上，temporalio/cli 在自动化运维、工作流调度以及 DevOps 流水线中具备高价值、易集成且已具备生产级别的可靠性，是 Temporal 生态的首选 CLI 工具。

## 🧭 Practical evaluation

**Value:** temporalio/cli helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 366 GitHub stars
- 96 forks
- updated 2026-06-24
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 55/100 |
| topics | 75/100 |
| outlook | 60/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 53/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/temporalio/cli) · [← Back to Orchestration](./README.md)</sub>
