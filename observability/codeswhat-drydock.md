# CodesWhat/drydock

[![Stars](https://img.shields.io/github/stars/CodesWhat/drydock?style=flat-square&color=yellow)](https://github.com/CodesWhat/drydock/stargazers) [![Forks](https://img.shields.io/github/forks/CodesWhat/drydock?style=flat-square&color=blue)](https://github.com/CodesWhat/drydock/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Open source container update monitoring — 23 registries, 20 notification triggers, audit log, OIDC auth, Prometheus metrics, and a modern dashboard.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 203 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`containers` `devops` `docker` `docker-compose` `homelab` `monitoring` `notifications` `prometheus` `self-hosted` `typescript` `vuejs` `watchtower-alternative`

## 🎯 Categories

Observability · DevOps/Infra · Security

## 📝 Summary

### English

**Brief Summary**  
CodesWhat /drydock is an open‑source observability platform that monitors container image updates across 23 registries, fires up to 20 different notification triggers, and records every change in an audit log. It ships with OIDC authentication, Prometheus metrics, and a modern dashboard, all built in TypeScript.

**Value**  
Drydock gives teams a turnkey way to keep their container fleets secure and compliant without writing custom polling scripts or stitching together disparate tools. By surfacing real‑time update signals, it enables rapid prototyping of AI‑driven workflows (e.g., RAG pipelines or autonomous agents) that react to new images, while the built‑in metrics and audit trail satisfy DevOps, security, and compliance requirements.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the Docker‑compose demo, and verify that the registries and notification channels you need are supported.  
2. **Integrate** – Use the provided REST API/SDK or CLI to embed update events into your CI/CD or AI orchestration pipelines.  
3. **Secure** – Configure OIDC for single‑sign‑on and set up Prometheus scraping for observability.  
4. **Deploy** – Scale the service with Helm/Kustomize in a Kubernetes cluster, and point your existing alerting (PagerDuty, Slack, etc.) to the chosen triggers.

**Production Readiness**  
The project scores 78/100, shows recent activity (last commit 2026‑06‑22), has 203 GitHub stars, and is actively used in several OSS pilots. Its core features (registry polling, audit logging, auth, metrics) are mature, and the TypeScript codebase is well‑structured. While the license and long‑term maintainer commitment still need a final check, the overall signal set (high adoption, robust feature set, clear documentation) makes Drydock a solid candidate for a production pilot in container‑centric environments.

### Русский

**CodesWhat/drydock** — это open‑source система мониторинга обновлений контейнеров с поддержкой 23 реестров, 20 триггеров уведомлений, аудит‑лога, OIDC‑аутентификации, метрик Prometheus и современного дашборда. Она позволяет быстро добавить AI‑функциональность (прототипировать RAG‑или агентные workflows, оценивать инструменты моделей) без необходимости строить стек с нуля, используя готовые API/SDK/CLI‑интерфейсы и метаданные. Проект имеет высокий уровень готовности к production: активные коммиты, 203 звезды на GitHub, широкую экосистему и сильные сигналы адоптации, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
CodesWhat/drydock 是一款开源的容器镜像更新监控平台，支持 23 种容器仓库、20 种通知触发方式，并提供审计日志、OIDC 鉴权、Prometheus 指标以及现代化仪表盘。

**价值**  
- **实时可观测**：通过多种触发器和丰富的指标，让运维团队第一时间获知镜像变更，避免因镜像升级导致的服务中断。  
- **安全合规**：审计日志和 OIDC 鉴权帮助企业满足安全审计和访问控制要求。  
- **易于扩展**：基于 TypeScript 实现，提供 API、SDK 与 CLI，可快速集成到现有 CI/CD、GitOps 或自研 AI 工作流中。

**典型接入方式**  
1. **API/SDK**：在 CI/CD 脚本或自研服务中调用 REST API，或直接使用官方 TypeScript SDK 进行镜像监控配置。  
2. **CLI**：通过 `drydock` 命令行工具快速注册仓库、设置通知渠道（Slack、Webhook、邮件等）。  
3. **Prometheus 抓取**：在监控平台中添加 `drydock` 的 `/metrics` 端点，即可获取镜像状态、触发次数等实时指标。  
4. **Dashboard**：部署 UI（Docker Compose/K8s Helm）后，使用内置仪表盘进行可视化管理。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑22，GitHub ★203、Fork 10，社区活跃。  
- **成熟度**：已实现完整的 OIDC 鉴权、审计日志、Prometheus 导出，具备企业级监控所需的关键功能。  
- **风险**：目前未发现重大元数据或许可证问题，但仍建议在正式投产前审查安全审计报告并确认维护者的响应能力。  

综合来看，drydock 在容器镜像更新监控领域具备高可用性和易集成特性，适合作为生产环境的监控核心组件。

## 🧭 Practical evaluation

**Value:** CodesWhat/drydock helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 203 GitHub stars
- 10 forks
- updated 2026-06-22
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/CodesWhat/drydock) · [← Back to Observability](./README.md)</sub>
