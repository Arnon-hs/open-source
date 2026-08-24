# amir20/dtop

[![Stars](https://img.shields.io/github/stars/amir20/dtop?style=flat-square&color=yellow)](https://github.com/amir20/dtop/stargazers) [![Forks](https://img.shields.io/github/forks/amir20/dtop?style=flat-square&color=blue)](https://github.com/amir20/dtop/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Terminal dashboard for Docker monitoring across multiple hosts with Dozzle integration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 28 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Observability · DevOps/Infra

## 📝 Summary

### English

**Summary**  
*am​ir20/dtop* is a Rust‑based terminal dashboard that aggregates Docker metrics from many hosts and embeds Dozzle logs for real‑time inspection. It lets engineers quickly view container health, resource usage, and log streams in a single, keyboard‑driven UI, making production behavior easier to monitor and debug.

**Value**  
- **Unified observability:** Combines container stats and live logs without switching between CLI tools or web UIs.  
- **Low‑overhead, developer‑friendly:** Runs locally in a terminal, so no extra services or browsers are required, which speeds up incident triage.  
- **Extensible for multi‑host setups:** Supports connecting to multiple Docker daemons, fitting teams that manage clusters of hosts or edge nodes.

**Practical adoption path**  
1. **Proof‑of‑concept:** Clone the repo, run the binary on a single test host, and verify that Docker stats and Dozzle logs appear as expected.  
2. **README validation:** Follow the quick‑start instructions to add additional Docker endpoints and configure Dozzle URLs; adjust any environment variables for your environment.  
3. **Pilot rollout:** Deploy the binary on a small set of production nodes (e.g., a staging cluster) and integrate it into existing on‑call runbooks.  
4. **Automation & CI:** Package the tool as a container or a pre‑built binary artifact, add health‑check scripts, and document the upgrade process.

**Production readiness**  
The project shows medium readiness: it has a solid community signal (1 079 stars, 28 forks) and recent activity (updated 2026‑05‑12), but it lacks a formal release schedule, thorough security audit, and guaranteed long‑term maintainers. Before using it in critical production environments, teams should:  

- Review the MIT/Apache license for compatibility.  
- Perform a security scan of the compiled binary and its dependencies.  
- Pin a specific version and set up monitoring for upstream changes.  

With those checks, *amir20/dtop* is suitable for internal tooling, prototypes, or as a supplemental observability layer, while a more hardened solution may be preferred for high‑availability production pipelines.

### Русский

**am​ir20/dtop** — это терминальный дашборд, написанный на Rust, позволяющий в реальном времени наблюдать за контейнерами Docker на нескольких хостах и сразу просматривать логи через интеграцию с Dozzle. Его обычно внедряют как лёгкую панель мониторинга для отладки продакшн‑сервисов и контроля их здоровья, начиная с небольшого proof‑of‑concept и проверки README, а затем масштабируют в более крупные внутренние воркфлоу. Готовность к продакшн — средняя: проект уже имеет 1 079 звёзд, активные коммиты и поддержку Rust, но перед полномасштабным запуском следует уточнить лицензию, состояние безопасности и наличие активных мейнтейнеров.

### 中文

**价值**  
`amir20/dtop` 是一款基于终端的 Docker 仪表盘，能够在同一界面实时监控多台主机上的容器状态，并内置 Dozzle 日志查看功能。它帮助运维和开发人员快速洞察生产环境的行为，定位异常容器、查看日志，从而加速故障排查和服务健康监控。

**典型接入方式**  
1. **环境准备**：在需要监控的机器上安装 Rust（或直接使用发布的二进制），确保 Docker Engine 可通过本机或远程 API 访问。  
2. **部署 dtop**：  
   ```bash
   cargo install dtop   # 或下载对应平台的预编译二进制
   dtop --hosts host1:2375,host2:2375   # 指定要监控的 Docker 主机列表
   ```  
3. **Dozzle 集成**：在启动 dtop 时添加 `--dozzle` 参数，或在配置文件中声明 Dozzle 的 HTTP 接口地址，随后在仪表盘中即可直接打开容器日志页面。  
4. **验证**：运行 `dtop --help` 查看完整选项，确认能够看到容器列表、CPU/内存/网络指标以及日志入口。  

**生产可用性**  
- **成熟度**：GitHub 近 1.1k 星、28 个 Fork，最近一次提交在 2026‑05‑12，活跃度尚可，适合作为内部或原型项目的监控工具。  
- **使用场景**：适合需要轻量级、终端化监控的团队，尤其是对多主机 Docker 集群进行快速状态检查和日志追踪的场景。  
- **限制与风险**：  
  - 仍需对许可证（MIT）和安全依赖进行最终审查。  
  - 作为命令行工具，缺乏细粒度的 RBAC 与审计功能，生产环境建议配合已有的集中式监控平台使用。  
  - 依赖 Rust 运行时和 Docker API，需确保网络连通性和 API 权限配置妥当。  

**结论**  
`amir20/dtop` 在原型开发和内部运维工作流中能够显著提升对 Docker 容器的可观测性，接入成本低。若在生产环境使用，建议先在单机或小规模集群上进行概念验证（PoC），并完成许可证、依赖安全及运维流程的评估后再推广。

## 🧭 Practical evaluation

**Value:** amir20/dtop helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1079 GitHub stars
- 28 forks
- updated 2026-05-12
- primary language: Rust

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 65/100 |
| topics | 0/100 |
| outlook | 49/100 |
| quality | 46/100 |
| recency | 20/100 |
| adoption | 57/100 |
| production | 45/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/amir20/dtop) · [← Back to Observability](./README.md)</sub>
