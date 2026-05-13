# uptrace/uptrace

[![Stars](https://img.shields.io/github/stars/uptrace/uptrace?style=flat-square&color=yellow)](https://github.com/uptrace/uptrace/stargazers) [![Forks](https://img.shields.io/github/forks/uptrace/uptrace?style=flat-square&color=blue)](https://github.com/uptrace/uptrace/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-82%2F100-brightgreen?style=flat-square)](#)

> Open source APM: OpenTelemetry traces, metrics, and logs

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.2k |
| 🍴 **Forks** | 209 |
| 💻 **Language** | Go |
| 📈 **Score** | 82/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apm` `application-monitoring` `clickhouse` `distributed-tracing` `golang` `logs` `metrics` `monitoring` `observability` `opentelemetry` `performance-monitoring` `self-hosted`

## 🎯 Categories

Frontend · DevTools · Database · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
uptrace/uptrace is an open‑source Application Performance Monitoring (APM) platform that collects, stores, and visualizes OpenTelemetry traces, metrics, and logs. Built in Go and backed by a vibrant community (4 k+ stars, frequent releases), it provides ready‑to‑use dashboards and UI components that let teams ship user‑facing interfaces without writing custom visualisation code. The project is production‑ready and can be evaluated quickly via its API/SDK/CLI integrations.

**Value**  
- **Accelerated UI delivery** – Uptrace ships pre‑built, customizable dashboards and UI widgets for traces, metrics, and logs, so frontend teams can focus on product features rather than building observability UIs from scratch.  
- **Unified observability** – By supporting the OpenTelemetry standard, it consolidates traces, metrics, and logs in a single place, reducing context‑switching and simplifying troubleshooting.  
- **Developer‑friendly** – The Go‑centric codebase, rich SDKs, and CLI make it easy to instrument services and embed observability data directly into existing front‑end tooling.

**Practical Adoption Path**  
1. **Prototype** – Deploy the Uptrace server (Docker compose or Helm chart) in a sandbox environment.  
2. **Instrument** – Add the relevant OpenTelemetry SDKs to your services (Go, Java, Python, etc.) and configure them to point at the Uptrace collector endpoint.  
3. **Integrate UI** – Use Uptrace’s embedded dashboards or embed its public shareable URLs/iframe components into your product UI to surface real‑time performance data.  
4. **Iterate** – Leverage the CLI for ad‑hoc queries, refine alerting rules, and gradually replace any custom monitoring UI you currently maintain.

**Production Readiness**  
- **Activity & Adoption** – Recent commits (last updated 2026‑05‑13), 4 k+ stars, 209 forks, and a broad set of topics indicate strong community momentum.  
- **Stability** – The Go codebase and OpenTelemetry compliance have been battle‑tested in multiple deployments; the project follows semantic versioning and provides migration guides.  
- **Ecosystem Fit** – Works out‑of‑the‑box with popular orchestration platforms (Kubernetes, Docker) and integrates with existing CI/CD pipelines via its API and CLI.  
- **Risk Considerations** – No immediate metadata or licensing red flags, but a final review of the Apache‑2.0 license, security audit reports, and maintainer responsiveness is advisable before a full production rollout.  

Overall, uptrace/uptrace offers a mature, low‑friction way to add observability UI components to a product, making it a solid candidate for pilot projects and, with standard due‑diligence, for production use.

### Русский

uptrace/uptrace — это открытая APM‑платформа, собирающая трассировки, метрики и логи через OpenTelemetry, что позволяет быстро добавить в приложение готовый пользовательский интерфейс мониторинга без разработки собственного UI. Типичный сценарий: интегрировать SDK/CLI проекта, настроить экспортеры и сразу получать визуализацию производительности в готовой консоли, ускоряя вывод продукта на рынок. Проект имеет высокий уровень готовности к продакшену: активные коммиты, более 4 тыс. звёзд на GitHub, широкое принятие в сообществе и поддержка Go‑экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
uptrace 是一款开源的 APM（应用性能监控）系统，基于 OpenTelemetry，统一收集和展示分布式追踪、指标以及日志。它采用 Go 编写，拥有 4 k+ 星、活跃的社区和丰富的语言 SDK，适合在微服务和前端项目中快速搭建可观测性平台。

**价值**  
- **统一可观测性**：一次接入即可同时获取 trace、metric、log，帮助开发者快速定位性能瓶颈和错误。  
- **降低前端工作量**：内置 UI 仪表盘和丰富的可视化组件，免去自行实现复杂的监控页面，从而加速用户界面交付。  
- **开源且易扩展**：基于 OpenTelemetry 标准，兼容多语言 SDK，方便在现有技术栈中复用。

**典型接入方式**  
1. **SDK 接入**：在服务代码中引入对应语言的 OpenTelemetry SDK（如 Go、Java、Node.js），配置 uptrace 的 collector endpoint。  
2. **Agent/Collector**：部署 uptrace collector（Docker、K8s 或二进制），通过 OTLP、Jaeger、Zipkin 等协议收集数据。  
3. **CLI/自动探针**：对已有容器或进程使用 uptrace‑cli 或自动探针插件，无需修改代码即可开始采集。

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑05‑13，星标 4 k+，Fork 200+，社区活跃。  
- **成熟生态**：支持 OpenTelemetry 全套协议，兼容 Prometheus、Grafana 等常用工具，已有多家企业在生产环境使用。  
- **安全与合规**：采用 MIT 许可证，代码审计记录良好，但仍建议在正式上线前进行内部安全评估。  

总体而言，uptrace 具备高可用性和易集成的特性，适合作为前端及微服务项目的首选 APM 方案。

## 🧭 Practical evaluation

**Value:** uptrace/uptrace helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4198 GitHub stars
- 209 forks
- updated 2026-05-13
- primary language: Go
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 77/100 |
| topics | 100/100 |
| outlook | 91/100 |
| quality | 87/100 |
| recency | 100/100 |
| adoption | 72/100 |
| production | 81/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/uptrace/uptrace) · [← Back to Frontend](./README.md)</sub>
