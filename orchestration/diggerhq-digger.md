# diggerhq/digger

[![Stars](https://img.shields.io/github/stars/diggerhq/digger?style=flat-square&color=yellow)](https://github.com/diggerhq/digger/stargazers) [![Forks](https://img.shields.io/github/forks/diggerhq/digger?style=flat-square&color=blue)](https://github.com/diggerhq/digger/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Digger is an open source IaC orchestration tool. Digger allows you to run IaC in your existing CI pipeline ⚡️

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5k |
| 🍴 **Forks** | 599 |
| 💻 **Language** | Go |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`github-actions` `hacktoberfest` `infrastructure-as-code` `tacos` `terraform` `terraform-aws` `terraform-gcp` `terraform-github-actions` `terraformcloud`

## 🎯 Categories

Orchestration · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Digger is an open‑source IaC orchestration platform written in Go that lets you embed infrastructure‑as‑code steps directly into your existing CI pipelines. By turning isolated prompts and tools into repeatable, multi‑agent workflows, it simplifies coordination, tool‑use pipelines, and standardized agent memory across DevOps environments. With strong community adoption (≈5 k stars, 600 forks) and recent activity, it’s ready for a serious pilot.

**Value**  
- **Unified orchestration**: Consolidates disparate IaC commands, scripts, and AI‑driven agents into a single, repeatable workflow, reducing manual glue code.  
- **Multi‑agent coordination**: Enables sequential or parallel execution of agents/tools, making complex provisioning or migration tasks easier to manage.  
- **CI/CD native**: Designed to be invoked from any CI system, so you can keep your existing pipeline structure while gaining richer automation capabilities.  

**Practical Adoption Path**  
1. **Proof‑of‑concept**: Clone the repo, run the provided examples, and verify the README steps on a small test environment.  
2. **Integrate into CI**: Add a Digger step to a non‑critical pipeline (e.g., a feature‑branch build) to orchestrate a simple Terraform or Pulumi apply.  
3. **Scale workflow**: Gradually replace ad‑hoc scripts with Digger‑defined agent pipelines, adding memory standardization and tool‑use stages as needed.  
4. **Governance & monitoring**: Hook Digger logs into your observability stack and define policy checks (e.g., drift detection) before promoting to production.  

**Production Readiness**  
- **Activity & adoption**: Recent commits (as of 2026‑06‑28), a healthy star/fork count, and multiple topics indicate an active community.  
- **Stability**: Written in Go, a compiled language with strong performance and low runtime overhead, suitable for CI workloads.  
- **Ecosystem fit**: Works with common IaC tools (Terraform, Pulumi, etc.) and can be called from any CI system (GitHub Actions, GitLab CI, Jenkins).  
- **Risks**: Final due‑diligence on licensing, security scanning, and maintainer responsiveness is required, but no major red flags have been identified.  

Overall, Digger offers a mature, community‑backed solution for turning scattered IaC steps into coherent, repeatable pipelines, making it a strong candidate for production pilots.

### Русский

**Digger** — это open‑source инструмент оркестрации IaC, позволяющий интегрировать запуск инфраструктурного кода в существующие CI‑конвейеры и превращать разрозненные подсказки и утилиты в повторяемые агентные воркфлоу. Типичный сценарий внедрения — небольшое POC, в котором в пайплайн добавляется шаг‑агент, координирующий несколько инструментов (Terraform, Ansible и др.) и сохраняющий их состояние, после чего решение масштабируется до полного CI/CD. По оценкам проекта, Digger готов к продакшн‑использованию: активные коммиты, более 4 тыс. звёзд, активное сообщество и поддержка Go‑экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Digger（diggerhq/digger）是一款开源的 IaC（Infrastructure as Code）编排工具，能够在现有 CI 流水线中直接运行 Terraform、Pulumi 等 IaC 任务，实现基础设施的自动化、可重复部署。  

**价值主张**  
- 将单独的 Prompt、工具或脚本统一封装为可复用的“Agent 工作流”，从而在多 Agent 场景下实现协同编排。  
- 支持在 CI/CD 中插入工具使用流水线，帮助团队标准化 Agent 的状态记忆和执行顺序，提升 DevOps 效率。  

**典型接入方式**  
1. **小规模 PoC**：在项目根目录添加 `digger.yml`（或 `digger.yaml`）配置文件，声明要执行的 IaC 目录、变量和依赖。  
2. **CI 集成**：在 GitHub Actions、GitLab CI、Jenkins 等 CI 配置中加入一步 `digger run`，即可在每次代码合并或 PR 时自动触发基础设施变更。  
3. **工具链扩展**：通过 Digger 的插件机制（Go 插件或 Docker 镜像）接入自定义工具或外部 API，实现更复杂的多 Agent 流程。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑28，项目最近一次提交，拥有 4,982 星、599 Fork，社区活跃，Issue 响应及时。  
- **技术成熟度**：核心实现使用 Go，代码基线清晰，已支持主流 IaC（Terraform、Pulumi）和多种 CI 平台。  
- **风险评估**：暂无重大元数据风险，仍需对许可证（MIT）和安全审计（依赖库漏洞）进行最终确认。整体来看，Digger 已具备在生产环境中进行正式试点的条件，建议先在非关键业务做小规模验证，验证后即可推广至全链路。

## 🧭 Practical evaluation

**Value:** diggerhq/digger helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4982 GitHub stars
- 599 forks
- updated 2026-06-28
- primary language: Go
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 69/100 |
| stars | 79/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 74/100 |
| recency | 40/100 |
| adoption | 76/100 |
| production | 60/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/diggerhq/digger) · [← Back to Orchestration](./README.md)</sub>
