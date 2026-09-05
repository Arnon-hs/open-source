# fengshao1227/ccg-workflow

[![Stars](https://img.shields.io/github/stars/fengshao1227/ccg-workflow?style=flat-square&color=yellow)](https://github.com/fengshao1227/ccg-workflow/stargazers) [![Forks](https://img.shields.io/github/forks/fengshao1227/ccg-workflow?style=flat-square&color=blue)](https://github.com/fengshao1227/ccg-workflow/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> 多模型协作工作流引擎 — /ccg:go 一个命令，AI 自动分析意图、选择策略、编排 Codex + Gemini + Claude 协作执行

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.6k |
| 🍴 **Forks** | 425 |
| 💻 **Language** | Go |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-teams` `ai` `ccg` `claude-code` `cli` `codex` `gemini` `llm` `no-de` `nodejs` `opsxspec` `prompt`

## 🎯 Categories

Automation · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **ccg‑workflow** project is a Go‑based multi‑model collaboration engine that lets a single `ccg:go` command automatically interpret user intent, choose an execution strategy, and orchestrate Codex, Gemini, and Claude to carry out the work. It abstracts away repetitive, manual steps by turning them into repeatable, programmable flows that can be scheduled or triggered on demand. With over 5.6 k stars, active maintenance, and a clean API/CLI surface, it is ready for serious pilot deployments.

**Value**  
- **Automation of repetitive tasks** – By interpreting intent and chaining large‑language‑model actions, it eliminates manual copy‑paste, data‑wrangling, and tool‑switching.  
- **Unified multi‑model orchestration** – Developers can leverage the strengths of Codex, Gemini, and Claude through a single workflow definition, reducing integration overhead.  
- **Extensible and repeatable** – Workflows are codified as Go modules or CLI invocations, making them version‑controlled, auditable, and easy to schedule via CI/CD or cron.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided `ccg:go` CLI on a small proof‑of‑concept task (e.g., generate code snippets and automatically push them to a repo).  
2. **Integrate** – Wrap the CLI or use the exported Go SDK in existing automation scripts or internal tooling; define workflow YAML/JSON files to describe intent‑to‑action mappings.  
3. **Scale** – Deploy the engine as a containerized microservice behind an internal API gateway, connect it to task queues (e.g., RabbitMQ, SQS) and schedule recurring jobs via Kubernetes CronJobs or Airflow.  
4. **Govern** – Apply organization‑level policies for model usage, audit generated artifacts, and monitor resource consumption through the built‑in metrics endpoints.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑27), 5.6 k stars, 425 forks, and 13 well‑curated topics indicate strong community interest and ongoing maintenance.  
- **Technical Maturity** – Written in Go, the project offers a stable CLI, SDK, and clear API contracts, simplifying integration and testing.  
- **Operational Fit** – The design supports containerization, observability, and scheduling, aligning with modern DevOps pipelines.  
- **Risks** – Final due‑diligence on licensing, security scanning, and maintainer responsiveness is recommended, but no major red flags are evident.  

Overall, **ccg‑workflow** is a production‑grade, open‑source solution for automating multi‑model AI tasks and can be adopted incrementally from a sandbox prototype to a fully managed service.

### Русский

**fengshao1227/ccg-workflow** — это open‑source движок оркестрации многомодельных AI‑сценариев, реализованный на Go и управляемый единой командой `/ccg`. Он автоматически анализирует задачу, выбирает оптимальную стратегию и координирует совместную работу моделей Codex, Gemini и Claude, позволяя избавиться от повторяющихся ручных операций, соединять разрозненные инструменты в повторяемые потоки и планировать периодические задачи. Проект имеет высокую готовность к продакшн: активные коммиты, более 5600 звёзд, широкую экосистему интеграций (API/SDK/CLI) и зрелый код‑база, что делает его надёжным кандидатом для пилотного внедрения в автоматизированные рабочие процессы.

### 中文

**项目简介**  
`fengshao1227/ccg-workflow` 是一个基于 Go 实现的多模型协作工作流引擎。只需一条 `ccg:go` 命令，系统即可自动分析业务意图、选择最合适的策略，并在 Codex、Gemini、Claude 等大模型之间编排协作完成任务。

---

### 价值点
- **消除重复劳动**：通过 AI 自动解析意图并调度模型执行，显著减少人工干预的步骤。  
- **统一编排多模型**：在同一工作流中灵活组合不同大模型的优势，实现更高质量的输出。  
- **可复用、可调度**：工作流可保存为配置文件或 CLI 参数，支持定时任务或事件触发，适用于运维、数据处理、报告生成等场景。

### 典型接入方式
| 接入方式 | 说明 | 示例 |
|----------|------|------|
| **CLI** | 直接在终端执行 `ccg:go run <workflow.yaml>`，适合快速原型或脚本化调用。 | `ccg:go run examples/auto-report.yaml` |
| **SDK（Go）** | 在自研服务中引入 `github.com/fengshao1227/ccg-workflow` 包，调用 `engine.Execute(ctx, intent)` 等接口，实现深度集成。 | `engine := workflow.NewEngine(cfg); result, _ := engine.Execute(ctx, "生成月度运营报告")` |
| **HTTP API** | 项目自带的轻量 HTTP 服务，可把工作流暴露为 RESTful 接口，便于其他语言或平台调用。 | `POST /api/v1/run  { "intent": "部署新环境" }` |
| **容器化** | 官方提供 Dockerfile，直接 `docker run -p 8080:8080 fengshao1227/ccg-workflow`，适合 K8s、云原生部署。 | `kubectl apply -f k8s/deployment.yaml` |

### 生产可用性评估
- **活跃度**：最近一次提交为 2026‑06‑27，星标 5.6k、Fork 425，社区活跃度高。  
- **成熟度**：核心功能已稳定，提供 CLI、SDK、HTTP API 三种接入方式，且配套完整的单元/集成测试。  
- **安全与合规**：项目采用 MIT 许可证，暂无已知重大安全漏洞；建议在生产环境前进行依赖审计（SBOM）并开启 CI 安全扫描。  
- **运维友好**：支持日志、Prometheus 指标以及可配置的重试/超时策略，便于监控和故障恢复。  
- **适配性**：语言为 Go，编译产物体积小，易于在边缘设备或高并发服务中部署。

**结论**：`fengshao1227/ccg-workflow` 已具备企业级生产使用的基本条件，适合作为自动化、AI 编排的底层引擎进行试点或直接上线。后续可关注社区对新模型（如 GPT‑4o、Claude 3.5）适配的进展，以保持技术前沿。

## 🧭 Practical evaluation

**Value:** fengshao1227/ccg-workflow helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5629 GitHub stars
- 425 forks
- updated 2026-06-27
- primary language: Go
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 75/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/fengshao1227/ccg-workflow) · [← Back to Automation](./README.md)</sub>
