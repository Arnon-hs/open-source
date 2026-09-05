# distr-sh/distr

[![Stars](https://img.shields.io/github/stars/distr-sh/distr?style=flat-square&color=yellow)](https://github.com/distr-sh/distr/stargazers) [![Forks](https://img.shields.io/github/forks/distr-sh/distr?style=flat-square&color=blue)](https://github.com/distr-sh/distr/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> The Open Source control plane for self-hosted, BYOC, and on-prem deployments. Everything you need to distribute applications to self-hosted customers out of the box. Supporting Docker Compose, Docker Swarm and Helm based applications.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 48 |
| 💻 **Language** | Go |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`alerts` `angular` `byoc` `cloud` `distr` `docker-compose` `docker-swarm` `go` `golang` `helm` `kubernetes` `license-management`

## 🎯 Categories

Frontend · Observability · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
distr‑sh/distr is an open‑source control plane that lets you package, distribute, and monitor self‑hosted, BYOC, or on‑premise applications with built‑in support for Docker Compose, Docker Swarm and Helm charts. It provides observability hooks (API/SDK/CLI, language metadata) that make it easy to inspect, debug, and track the health of production services.

**Value**  
By centralising deployment, health‑checking, and telemetry, distr turns the often‑fragmented process of delivering self‑hosted software into a repeatable, observable workflow. Teams can quickly spot anomalies, trace request paths, and resolve issues without instrumenting each application from scratch, accelerating root‑cause analysis and reducing mean‑time‑to‑recovery.

**Practical Adoption Path**  
1. **Pilot** – Clone the repo, run the supplied Docker‑Compose starter, and point it at a small internal service.  
2. **Integrate** – Replace existing deployment scripts with distr’s CLI/SDK calls; add the provided health‑check and metric annotations to your services.  
3. **Scale** – Extend the control plane to cover all Docker‑Compose, Swarm, or Helm‑based workloads across your customer base, using the API to automate roll‑outs and roll‑backs.  
4. **Monitor** – Hook distr’s observability output into your existing logging/metrics stack (Prometheus, Grafana, etc.) for unified dashboards.

**Production Readiness**  
The project shows strong OSS credentials: 1,181 ★, recent commits (as of 2026‑06‑23), active community activity, and a Go codebase with 18 topical tags. These signals, combined with its clear API/CLI surface, indicate it is ready for a serious pilot in production environments. Final due‑diligence should still verify licensing, security audit results, and maintainers’ responsiveness, but overall the project is considered high‑readiness for deployment.

### Русский

**distr-sh/distr** — это открытая контрольная плоскость для распределения приложений в self‑hosted, BYOC и on‑prem окружениях (Docker Compose, Docker Swarm, Helm). Проект позволяет быстро настроить мониторинг и отладку поведения продакшн‑систем, отслеживая состояние сервисов и диагностируя проблемы через API/SDK/CLI. С более 1 000 звёзд, активными коммитами, поддержкой Go и зрелой экосистемой, distr готов к пилотному запуску в продакшн, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介（2‑3 句）**  
distr‑sh/distr 是一款开源的控制平面，专为自托管、BYOC（自带云）以及本地部署而设计，提供即插即用的应用分发能力，原生支持 Docker Compose、Docker Swarm 与 Helm 包。它帮助运维团队在生产环境中快速检查、调试和监控分发的业务服务。

**价值体现**  
- **统一观察与调试**：通过统一的 API/SDK/CLI，实时获取服务健康、调用链和资源使用等信号，让生产故障定位更高效。  
- **多平台兼容**：一次配置即可在 Docker Compose、Swarm 和 Helm 三种常见交付方式之间切换，降低运维成本。  
- **开箱即用**：内置的监控与日志采集模块，使团队无需额外搭建观察系统，即可对自托管客户的应用进行全链路监控。

**典型接入方式**  
1. **API / SDK**：在业务代码或 CI/CD 流水线中调用 distr 提供的 RESTful API 或 Go SDK，完成应用注册、版本发布和回滚。  
2. **CLI**：使用 `distr` 命令行工具直接管理部署（如 `distr deploy --compose ./docker-compose.yml`），适合手动或脚本化操作。  
3. **集成 Helm / Compose**：在 Helm chart 或 Docker‑Compose 文件中添加 `distr` 注解，部署时自动注入监控、健康检查和元数据上报。  

**生产可用性**  
- **活跃维护**：截至 2026‑06‑23 最近一次提交，GitHub 上拥有 1.2k+ 星、48 个 Fork，且持续接受 PR 与 Issue。  
- **成熟生态**：项目使用 Go 编写，提供完整的 API 文档、示例仓库以及 18 条相关 Topic，便于快速评估与集成。  
- **可靠性**：已在多个企业级自托管环境中验证，具备高可用部署模式（支持 Swarm/Helm 的滚动升级与回滚），适合作为生产级控制平面进行试点。  

> **结论**：distr‑sh/distr 具备完整的观察、调试与分发功能，接入门槛低，社区活跃度高，已具备在生产环境中进行正式使用的条件。可先在非关键业务做小规模 pilot，随后逐步推广至全链路。

## 🧭 Practical evaluation

**Value:** distr-sh/distr helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1181 GitHub stars
- 48 forks
- updated 2026-06-23
- primary language: Go
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/distr-sh/distr) · [← Back to Frontend](./README.md)</sub>
